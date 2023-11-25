<script setup lang="ts">
</script>

<template>
  <div class="endpage">
    <div class="title">使命愿景价值观<span>告别低价值重复劳动力，为专业法律工作者“减负”</span></div>
    <div class="contraner">
      <div class="item-s">
        <img src="../assets/images/great-idea-flatline.png" alt="新工具" />
        <div class="desc">使用新工具</div>
      </div>
      <div class="item-s">
        <img src="../assets/images/information-carousel-monochromatic.png" alt="新生产力" />
        <div class="desc">解放新生产力</div>
      </div>
      <div class="item-s">
        <img src="../assets/images/graphic-chart-flatline.png" alt="新价值" />
        <div class="desc">创造新的价值</div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.endpage {
  padding: 40px;
  padding-bottom: 100px;
  background-color: #fff;
  .title {
    text-align: center;
    margin: 0 auto;
    color: #333;
    font-size: 34px;
    line-height: 1;
    font-weight: 400;
    margin-bottom: 65px;
    span {
      margin-top: 20px;
      display: block;
      font-size: 18px;
      color: #666;
    }
  }
  .contraner {
    display: flex;
    align-items: center;
    .item-s {
      flex: 1;
      display: flex;
      flex-direction: column;
      align-items: center;
      img {
        width: 150px;
      }
      .desc {
        font-size: 20px;
        color: #333;
        line-height: 1;
        margin-top: 16px;
      } 
    }
  }
}
</style>
