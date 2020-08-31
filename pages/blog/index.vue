<template>
  <div>
    <section class="hero is-light is-medium">
      <div class="hero-body">
        <div class="container">
          <h1 class="title has-text-centered">Blog / บทความ</h1>
        </div>
      </div>
    </section>

    <div class="container my-5">
      <div class="columns is-multiline">
        <div class="column is-4" v-for="blog in blogs" :key="blog.slug">
          <nuxt-link :to="`/blog/${blog.slug}`">
            <div class="card">
              <div class="card-image">
                <img :src="blog.tumbnail" alt="" />
              </div>
              <div class="card-content">
                <h1 class="title">{{ blog.title }}</h1>
                <p>{{ blog.description }}</p>
              </div>
              <div class="card-footer">
                <span class="card-footer-item">{{
                  $moment(blog.createdAt)
                }}</span>
                <small class="card-footer-item has-text-info">{{
                  blog.tools
                }}</small>
              </div>
            </div>
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const blogs = await $content('blog').sortBy('createdAt', 'desc').fetch()
    return { blogs }
  },
}
</script>

<style scoped>
.card {
  transition: all 0.2s ease;
}
.card:hover {
  transform: scale(1.02);
  transition: all 0.2s ease;
}
</style>
