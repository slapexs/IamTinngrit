<template>
  <div class="">
    <section class="sectionPart">
      <div class="container">
        <div class="columns is-multiline is-vcentered">
          <div class="column is-half">
            <div class="has-text-left">
              <h1 class="title">Tinngrit Singkaew</h1>
              <h2 class="subtitle">ทินกฤต สิงห์แก้ว (ตะวัน)</h2>
            </div>
          </div>
          <div class="column is-half">
            <img
              src="https://scontent.fbkk5-3.fna.fbcdn.net/v/t1.0-9/73515787_107249104062009_7211701035780276224_n.jpg?_nc_cat=105&_nc_sid=09cbfe&_nc_ohc=ndOjSeYLf0EAX-oxugQ&_nc_ht=scontent.fbkk5-3.fna&oh=28a3dc748b06876bb1165699c4002dba&oe=5F6CBF6D"
              alt="Profile image"
              class="imgrounded"
            />
          </div>
        </div>
      </div>
    </section>

    <About />

    <Skill />
    <Social />
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.sectionPart {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}
.title {
  color: #ff4d00;
  font-size: 62px;
  text-transform: uppercase;
}

.subtitle {
  color: #e5e5e5;
}

.imgrounded {
  border-radius: 5px;
  transition: all 0.3s ease;
}
.imgrounded:hover {
  transform: scale(1.02);
}
</style>
