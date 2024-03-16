<script setup>
// Fetch All Posts
const { data, error, pending } = useLazyFetch(
  "https://dummyjson.com/posts?limit=10"
);
const { data: products } = useFetch("/api/products");
//console.log("response of api ", JSON.stringify(products));
useHead({
  title: "My Blog",
});
</script>

<template>
  <div>
    <div v-if="error" class="text-2xl text-white">
      An error has occurred...{{ error }}
    </div>
    <div v-else-if="data">
      <div v-for="{ id, title, body } in data.posts" :key="id">
        <PostCard :id="id" :title="title" :body="body" />
      </div>
    </div>
    <div v-else class="text-2xl text-white">Loading Posts</div>
  </div>
</template>

<style lang="css" scoped></style>
