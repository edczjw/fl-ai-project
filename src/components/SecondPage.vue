<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="section second-page">
    <div class="box-item">
      <h2>法律研究</h2>
      <i style="font-size: 14px; color: rgb(242, 84, 84); font-weight: 500">一键生成法律研究成果</i>
      <p>
        对话式输入您的问题，一键生成基于&nbsp;<span
          style="font-weight: 600; color: #000; font-size: 18px"
          >法律法规与案例引证</span
        >&nbsp;的专业法律研究报告，有源引的法律问答引擎，杜绝AI幻觉。
      </p>
    </div>
    <div class="box-item">
      <h2>文书分析</h2>
      <i style="font-size: 14px; color: rgb(97, 60, 207); font-weight: 500">事实梳理小助手</i>
      <p>
        从繁杂的文件中抽取出事件、人物关系，梳理出事件时间线，构建出关系图谱，通过对话式基于文书内容展开问答
      </p>
    </div>
    <div class="box-item">
      <h2>法律翻译</h2>
      <i style="font-size: 14px; color: rgba(21, 94, 239, 1); font-weight: 500">专业场景专用翻译</i>
      <p>聚焦法律场景：清晰的逻辑思维+对法律条款的理解能力，助力从业者高效精准完成翻译</p>
    </div>
    <div class="box-item">
      <h2>文书生成</h2>
      <i style="font-size: 14px; font-weight: 500">文书定制化生成</i>
      <p>根据案情需要自动撰写文书，可以根据您历史撰写过的文书作为模板进行标准化文书生成。</p>
    </div>
  </div>
</template>

<style scoped lang="scss">
.section {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 32px;
  h2 {
    font-size: 26px;
    font-weight: 600;
  }
}
.second-page {
  font-family: 'Lato', sans-serif;
}
.box-item {
  font-family: 'Lato', sans-serif;
  width: 46%;
  padding: 32px;
  margin-bottom: 32px;
  color: #333;
  background-color: #fff;
  border-radius: 24px;
  box-shadow: 0 0.6021873017743928px 0.6021873017743928px -1.25px #00000017,
    0 2.288533303243457px 2.288533303243457px -2.5px #00000013, 0 10px 10px -3.75px #00000008;
  display: flex;
  flex-direction: column;
  &:first-child {
    background-color: #dbeeff;
  }
  &:nth-child(2) {
    background-color: #fae6e6;
  }
  &:nth-child(3) {
    background-color: #dedbff;
  }
  &:nth-child(4) {
    background-color: #fff7db;
  }
  i{
    font-family: 'Lato', sans-serif;
  }
}
</style>
