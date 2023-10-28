<template>
  <div style="width: 100vw;height: 100vh;overflow: hidden;display: flex">
      <div style="flex: 1;background-color: lightskyblue">
          <el-image style="width: 100%;height: 100%" fit="cover"
                    src="https://img1.baidu.com/it/u=3990644324,2899209883&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500"/>
      </div>
      <div class="welcome-title">
          <div style="font-size: 30px;font-weight: bold">欢迎来到Java学习平台</div>
          <div style="margin-top: 10px">掌握Java，开启未来！轻松掌握，实现技术进阶！</div>
          <div style="margin-top: 5px">Java学习平台，为你的编程之路保驾护航！全方位学习支持，助力技术进阶！</div>
      </div>
      <div class="right-card">
          <router-view/>
      </div>
  </div>
</template>

<script>
export default {
    name: "WelcomeView"
}
</script>

<style scoped>
.welcome-title {
    position: absolute;
    bottom: 30px;
    left: 30px;
    color: white;
    text-shadow: 0 0 10px black;
}

.right-card {
    width: 400px;
    z-index: 1;
    background-color: white;
}
</style>