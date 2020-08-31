<template>
  <div>
    <section class="hero is-light mb-3">
      <div class="hero-body has-text-centered">
        <h1 class="title">{{ work.title }}</h1>
        <!-- <figure class="image"> -->
        <img :src="work.tumbnail" class="img-work" draggable="false" alt="" />
        <!-- </figure> -->
      </div>
    </section>

    <section class="hero is-medium">
      <div class="hero-body">
        <div class="container">
          <nuxt-content :document="work" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const work = await $content('work', params.slug).fetch()
    return { work }
  },
}
</script>

<style scoped>
.img-work {
  width: 960px;
}
</style>
