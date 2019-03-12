<template>
  <section class="container">
    <PostCard 
      v-for="post in posts" 
      :key="post.id" 
      :thumbnailImage="post.thumbnailUrl"
      :title="post.title"
      :excerpt="post.previewText"
      :id="post.id"
    />
  </section>
</template>

<script>
import PostCard from '@/components/PostCard'

export default {
  components: {
    PostCard
  },
  data: () => ({
    posts: [
      { 
        title: 'A New Beginning' ,
        previewText: 'this will be awesome don\'t miss it!',
        thumbnailUrl: 'https://foodrevolution.org/wp-content/uploads/2018/04/blog-featured-diabetes-20180406-1330.jpg',
        id: 'a-new-beginning'
      },
      { 
        title: 'A Second Beginning' ,
        previewText: 'this will be awesome don\'t miss it!',
        thumbnailUrl: 'https://foodrevolution.org/wp-content/uploads/2018/04/blog-featured-diabetes-20180406-1330.jpg',
        id: 'a-second-beginning'
      }
    ]
  })
}
</script>

<style>

</style>
