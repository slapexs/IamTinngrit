<template>
  <div>
    <div id="social" class="sectionPart" style="background: #a0a1bf;">
      <div class="container d-flex">
        <h1 class="title">Social media</h1>

        <div class="columns has-text-centered is-multiline my-4">
          <div class="column link">
            <a href="https://www.facebook.com/tinngrits77" target="_blank">
              <img
                src="https://image.flaticon.com/icons/svg/733/733547.svg"
                alt=""
                class="logo"
              />
              <h2 class="subtitle">tinngritS77</h2>
            </a>
          </div>

          <div class="column link">
            <a href="#" target="_blank">
              <img
                src="https://image.flaticon.com/icons/svg/733/733590.svg"
                alt=""
                class="logo"
              />
              <h2 class="subtitle">ONZEDX</h2>
            </a>
          </div>

          <div class="column link">
            <a
              href="https://www.instagram.com/tawan.bamba/?hl=th"
              target="_blank"
            >
              <img
                src="https://image.flaticon.com/icons/svg/733/733558.svg"
                alt=""
                class="logo"
              />
              <h2 class="subtitle">tawan.bamba</h2>
            </a>
          </div>

          <div class="column link">
            <a href="https://www.twitch.tv/onzelive" target="_blank">
              <img
                src="https://image.flaticon.com/icons/svg/733/733577.svg"
                alt=""
                class="logo"
              />
              <h2 class="subtitle">onzelive</h2>
            </a>
          </div>

          <div class="column link">
            <a href="https://github.com/slapexs" target="_blank">
              <img
                src="https://image.flaticon.com/icons/svg/1051/1051326.svg"
                alt=""
                class="logo"
              />
              <h2 class="subtitle">slapexs</h2>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.title {
  color: #000;
  font-size: 62px;
  text-transform: uppercase;
  margin-bottom: 50px;
}

.subtitle {
  color: white;
}

.logo {
  height: 96px;
}

.link {
  transition: all 0.2s ease;
}

.link:hover {
  transition: all 0.2s ease;
  transform: scale(1.1);
  color: aquamarine;
  cursor: pointer;
}
</style>
