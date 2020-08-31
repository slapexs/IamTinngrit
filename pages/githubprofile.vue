<template>
  <div class="sectionPart">
    <div class="container mt-5">
      <div class="has-text-centered">
        <img
          :src="users.avatar_url"
          draggable="false"
          class="imgProfile"
          alt=""
        />
        <h1 class="title my-3">Tinngrit Singkaew</h1>
        <p><strong>Location</strong> : {{ users.location }}</p>
        <p><strong>Bio</strong> : {{ users.bio }}</p>
        <p><strong>Twitter</strong> : {{ users.twitter_username }}</p>
      </div>

      <hr />

      <div class="my-5">
        <h1 class="title">
          <span class="icon"
            ><img
              src="https://image.flaticon.com/icons/svg/919/919847.svg"
              alt=""
          /></span>
          Github repos
        </h1>

        <div class="columns is-multiline">
          <div class="column is-4" v-for="repo in repos" :key="repo.id">
            <div class="card">
              <div class="card-content">
                <div class="media">
                  <div class="media-content">
                    <p class="subtitle">
                      <a :href="repo.html_url" target="_blank">{{
                        repo.name
                      }}</a>
                    </p>
                    {{ repo.description }}
                  </div>
                </div>
              </div>

              <div class="card-footer">
                <a
                  :href="repo.html_url"
                  class="card-footer-item"
                  target="_blank"
                  >View</a
                >
                <small class="card-footer-item"
                  >Language : {{ repo.language }}</small
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  async asyncData({ $axios }) {
    const baseURL = 'https://api.github.com'
    const users = await $axios.$get(`${baseURL}/users/slapexs`)
    const repos = await $axios.$get(`${baseURL}/users/slapexs/repos`)

    return { users, repos }
  },
}
</script>

<style scoped>
.title {
  color: #acbdaa;
}
.imgProfile {
  border-radius: 50%;
  height: 256px;
  width: 256px;
}
.sectionPart {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
strong {
  color: #f1f0f0;
}
</style>
