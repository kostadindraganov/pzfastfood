<template>
  <div>{{data}}</div>
</template>
<script setup>
const route = useRoute()

const {
  data: post,
  pending,
  refresh,
  error,
} = await useAsyncData('post', () =>
  queryContent('/blog')
    .findOne()
)



// const storedPost = useState(`blog-${route.params.slug}`);
// if (error) showError({ message: "Blog post not found", cause: error });
</script>
