<template>
  <div class="jishu-wrap">
    <div class="title">技术优势</div>
    <div class="container">
      <div class="box1">
        <img src="../assets/images/1.png" alt="" />
        <p>业界顶尖的大语言模型基座 / 全领域的法律实务知识体系</p>
      </div>
      <div class="box1">
        <img src="../assets/images/2.png" alt="" />
        <p>向量数据库高效优化 / 精准快速响应用户请求</p>
      </div>
      <div class="box1">
        <img src="../assets/images/3.png" alt="" />
        <p>深度引导的自研算法 / 全面自研的深度引导思维链路</p>
      </div>
      <div class="box1">
        <img src="../assets/images/4.png" alt="" />
        <p>深刻理解法律行业痛点和专业用户需求</p>
      </div>
      <div class="box1">
        <img src="../assets/images/5.png" alt="" />
        <p>仅使用可供援引的法律渊源作为训练数据</p>
      </div>
      <div class="box1">
        <img src="../assets/images/6.png" alt="" />
        <p>仅依赖可供援引的法律法规 / 裁判文书 / 指导意见等优质法律数据</p>
      </div>
      <div class="box1">
        <img src="../assets/images/7.png" alt="" />
        <p>基于专家团队的分析 / 标注 / 筛选以及与专业用户的反馈，形成高质量私域数据</p>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { nextTick, onMounted, ref } from 'vue'
const dd = ref(null) as any
onMounted(() => {
  nextTick(() => {
    const elements = document.querySelectorAll('.box1')

    const observer = new IntersectionObserver(callback)
    elements.forEach((ele) => {
      ele.classList.add('opaque')
      observer.observe(ele)
    })

    function callback(entries: any[], instance: { unobserve: (arg0: any) => void }) {
      entries.forEach((entry: { isIntersecting: any; target: any }) => {
        if (entry.isIntersecting) {
          const element = entry.target
          element.classList.remove('opaque')
          element.classList.add('come-in')
          instance.unobserve(element)
        }
      })
    }
  })
})
</script>
<style lang="scss" scoped>
.jishu-wrap {
  padding: 40px 40px 0;
  padding-bottom: 100px;
  background-color: #fff;
  .title {
    text-align: center;
    margin: 0 auto;
    color: #333;
    font-size: 34px;
    line-height: 1;
    font-weight: 400; 
  }
  .container {
    padding: 0 32px;
    position: relative;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    .box1 {
      width: 30%;
      min-height: 220px;
      border-radius: 8px;
      font-size: 18px; 
      box-sizing: border-box;
      margin-right: 24px;
      margin-bottom: 24px;
      text-align: center;
      padding: 10px;
      &:last-child {
        margin-bottom: 0;
      }
      img{
        width: 240px;
        height: 240px;
        object-fit: contain; 
      }
      p{ 
        padding: 0 16px;
        text-align: center;
        line-height: 26px;
        color: #333;
      }
    }
  }
  .come-in {
    opacity: 1;
    transform: translateY(150px);
    animation: come-in 1s ease forwards;
  }
  .come-in:nth-child(odd) {
    animation-duration: 1s;
  }

  @keyframes come-in {
    100% {
      transform: translateY(0);
    }
  }
}
</style>
