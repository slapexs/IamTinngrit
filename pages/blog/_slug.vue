<template>
  <div>
    <div class="container-fluid has-text-centered mt-5">
      <h1 class="title is-1">{{ blog.title }}</h1>
      <img :src="blog.tumbnail" class="img-blog" alt="" />
    </div>

    <section class="hero">
      <div class="hero-body">
        <div class="container line-hight">
          <nuxt-content :document="blog" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blog = await $content('blog', params.slug).fetch()
    return { blog }
  },
}
</script>

<style scoped>
.title {
  color: white;
}
.line-hight {
  line-height: 36px;
  font-size: 18px;
}
</style>
