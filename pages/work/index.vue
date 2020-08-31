<template>
  <div>
    <section class="hero is-light is-medium">
      <div class="hero-body">
        <div class="container">
          <h1 class="title has-text-centered">Works / ผลงาน</h1>
        </div>
      </div>
    </section>
    <div class="">
      <div class="container mt-4">
        <div class="columns is-multiline my-4">
          <div class="column is-4" v-for="work in works" :key="work.slug">
            <nuxt-link :to="`/work/${work.slug}`">
              <div class="card">
                <div class="card-image">
                  <img :src="work.tumbnail" alt="" />
                </div>
                <div class="card-content">
                  <h1 class="title is-4">{{ work.title }}</h1>
                </div>
                <div class="card-footer">
                  <span class="card-footer-item">{{
                    $moment(work.createdAt)
                  }}</span>
                  <small class="card-footer-item has-text-info">{{
                    work.tools
                  }}</small>
                </div>
              </div>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dateTime: this.$moment(),
    }
  },
  async asyncData({ $content }) {
    const works = await $content('work').sortBy('createdAt', 'desc').fetch()
    return { works }
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
  cursor: pointer;
}

.sectionPart {
  /* display: flex; */
  height: 100vh;
  justify-content: center;
  align-items: center;
}

.titleText {
  color: #ff4d00;
  font-size: 62px;
  text-transform: uppercase;
}
</style>
