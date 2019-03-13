<template>
  <nuxt-link :to="id">
    <article class="post-preview">
      <div class="post-thumbnail" :style="{backgroundImage: `url(${thumbnailImage})`}"></div>
      <div class="post-content">
        <h1>{{ title }}</h1>
        <p>{{ excerpt }}</p>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: { type: String, required: true },
    excerpt: { type: String, required: true },
    thumbnailImage: { type: String, required: true },
    id: { type: String, required: true },
  }
}
</script>

<style scoped>
  a {
    text-decoration: none;
  }

  .post-preview {
    border-radius: 3px;
    box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.5);
    width: 90%;
    margin: auto;
    height: 20rem;
  }

  .post-thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 10rem;
  }

  .post-content {
    text-align: center;
    padding: 1rem;
  }

  @media screen and (min-width: 35rem) {
    .post-preview {
      width: 25rem;
      margin: 1rem;
    }
  }
</style>


