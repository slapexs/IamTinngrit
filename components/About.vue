<template>
  <div>
    <div id="about" class="sectionPart" style="background: #222831;">
      <div class="container">
        <h1 class="title">About me</h1>
        <p class="aboutText">
          เอาล่ะ ขอแนะนำตัวสักหน่อยนะครับชื่อทินกฤต สิงห์แก้ว หรือตะวัน
          ส่วนตัวถนัดการพัฒนา<span class="hilightspan">เว็บไซต์</span
          >เป็นหลักมากกว่าการเขียนโปรแกรม หรือ Application mobile
          อยากที่จะทำอาชีพ
          <i>Front-end developer</i>
          ในบางวันก็มีการ Live stream เขียนโค้ดใน
          <a
            href="https://www.twitch.tv/onzelive"
            class="btntwitch"
            target="_blank"
            >Twitch</a
          >
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.title {
  color: #ff4d00;
  font-size: 62px;
  text-transform: uppercase;
  margin-bottom: 50px;
}

.btntwitch {
  text-decoration: none;
  color: rgb(238, 238, 238);
  border: 1px solid rgba(255, 255, 255, 0);
  padding: 5px 20px;
  background: #6441a5;
  border-radius: 5px;
  transition: all 0.2s ease;
  font-size: 18px;
}

.btntwitch:hover {
  color: white;
  border: 1px solid rgba(255, 255, 255, 0);
  padding: 5px 20px;
  background: #492b83;
  border-radius: 5px;
  transition: all 0.2s ease;
}

.aboutText {
  font-size: 24px;
  line-height: 36px;
}

.hilightspan {
  color: #ff9737;
}
</style>
