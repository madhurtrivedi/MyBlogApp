<script setup>
definePageMeta({
  layout: "custom",
});

const route = useRoute();

//Fetch Single Post
const {
  data: post,
  error,
  pending,
} = useLazyFetch(`https://dummyjson.com/posts/${route.params.id}`);
setTimeout(() => {
  console.log("post ", JSON.stringify(post));
}, 2000);

useHead({
  title: `Post Detail`,
});
</script>

<template>
  <div>
    <div v-if="error" class="text-2xl text-white">
      An error has occurred...{{ error }}
    </div>
    <div v-else-if="post">
      <PostDetail :id="post?.id" :title="post?.title" :body="post?.body" />
    </div>
    <div v-else class="text-2xl text-white">Loading post</div>
  </div>
</template>

<style lang="css" scoped></style>
