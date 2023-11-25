<script setup lang="ts">
</script>

<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-top">
        <div class="footer-item">
          <div class="footer-title">Reach Us</div>
          <p>合作邮箱：contact@slaw-ai.com</p>
          <p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 16 16"
              width="18"
              height="18"
              fill="currentColor"
              class="mx-2"
            >
              <path
                fill-rule="evenodd"
                d="M14.763.075A.5.5 0 0 1 15 .5v15a.5.5 0 0 1-.5.5h-3a.5.5 0 0 1-.5-.5V14h-1v1.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V10a.5.5 0 0 1 .342-.474L6 7.64V4.5a.5.5 0 0 1 .276-.447l8-4a.5.5 0 0 1 .487.022zM6 8.694 1 10.36V15h5V8.694zM7 15h2v-1.5a.5.5 0 0 1 .5-.5h2a.5.5 0 0 1 .5.5V15h2V1.309l-7 3.5V15z"
              ></path>
              <path
                d="M2 11h1v1H2v-1zm2 0h1v1H4v-1zm-2 2h1v1H2v-1zm2 0h1v1H4v-1zm4-4h1v1H8V9zm2 0h1v1h-1V9zm-2 2h1v1H8v-1zm2 0h1v1h-1v-1zm2-2h1v1h-1V9zm0 2h1v1h-1v-1zM8 7h1v1H8V7zm2 0h1v1h-1V7zm2 0h1v1h-1V7zM8 5h1v1H8V5zm2 0h1v1h-1V5zm2 0h1v1h-1V5zm0-2h1v1h-1V3z"
              ></path>
            </svg>
            浙江省杭州市滨江区西兴街道聚工路19号9幢1层113室
          </p>
        </div>
        <div class="footer-item">
          <div class="footer-title">Follow us</div>
          <div class="social-icon mt-2">
            <img src="../assets/images/qcode.jpeg" />
          </div>
        </div>
      </div>
      <div class="footer-bottom text-center my-3">
        <div class="footer-name">SLAW AI</div>
        <div class="py-4">
          本网站由 ©语迟智能信息技术有限公司 运营 2023 <br />
          <a class="footer-link" href="https://beian.miit.gov.cn/"
            ><span></span>浙ICP备2023017904号-1</a
          >
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped lang="scss">
.footer { 
  background-color: #000;
  background-position: 50%;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 10px 0;
}
.footer-container {
  align-items: center;
  display: flex;
  flex-direction: column;
}
.footer-top {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  width: 100%;
}
.footer-item {
  flex: 1;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;
}
.footer-title {
  font-size: 34px;
}
.footer p {
  align-items: end;
  color: #b8b8b8;
  cursor: pointer;
  display: flex;
  font-size: 18px;
  font-weight: 400;
  letter-spacing: 1px;
  margin-top: 20px;
}
.mx-2 {
  margin-left: 0.5rem !important;
  margin-right: 0.5rem !important;
}
.footer-bottom {
  align-items: center;
  display: flex;
  flex-direction: column;
  font-size: 18px;
  justify-content: center;
  position: relative;
  width: 90%;
  margin-top: 10px;
}
.footer-name {
  font-size: 36px;
  line-height: 20px;
}
.mt-2 {
  margin-top: 0.5rem !important;
}
.footer img {
  width: 15%;
}
.social-icon {
  text-align: center;
}
.footer-name:after,
.footer-name:before {
  background: #fff;
  content: '';
  height: 1px;
  position: absolute;
  top: 12%;
  width: 40%;
}
.footer-name:before {
  left: 15px;
}
.footer-name:after {
  right: 15px;
}
.py-4 {
  padding-bottom: 1.5rem !important;
  padding-top: 1.5rem !important;
}
.footer-link {
  margin-top: 8px;
  color: #4979ff;
  display: flex;
  align-items: center;
  justify-content: center;

  span {
    display: block;
    width: 16px;
    height: 16px;
    margin-right: 8px;
    background: url('https://www1.pcauto.com.cn/footer/images/ft-ghs.png') no-repeat center;
    background-size: 100%;
  }
}
</style>
