<template>
  <div style="text-align: center">
      <el-button @click="userLogout" style="margin-top: 270px" type="danger" plain>退出登录</el-button>
  </div>
</template>

<script setup>
import {logout} from "@/net";
import router from "@/router";

function userLogout() {
    logout(() => router.push('/'))
}
</script>

<style scoped>

</style>