<template>
  <div style="text-align: center;margin: 0 20px">
      <div style="margin-top: 150px">
          <div style="font-size: 25px;font-weight: bold">登录</div>
          <div style="font-size: 14px;color: grey">在进入系统之前，请输入用户名和密码进行登录</div>
      </div>
      <div style="margin-top: 50px">
          <el-form>
              <el-form-item>
                  <el-input v-model="form.username" maxlength="10" type="text" placeholder="用户名/邮箱">
                      <template #prefix>
                          <el-icon><User/></el-icon>
                      </template>
                  </el-input>
              </el-form-item>
              <el-form-item>
                  <el-input v-model="form.password" maxlength="20" type="password" placeholder="密码">
                      <template #prefix>
                          <el-icon><Lock/></el-icon>
                      </template>
                  </el-input>
              </el-form-item>
              <el-row>
                  <el-col :span="12" style="text-align: left">
                      <el-form-item>
                          <el-checkbox v-model="form.remember" label="记住我"/>
                      </el-form-item>
                  </el-col>
                  <el-col :span="12" style="text-align: right">
                      <el-link>忘记密码？</el-link>
                  </el-col>
              </el-row>
          </el-form>
      </div>
      <div style="margin-top: 40px">
          <el-button style="width: 270px" type="success" plain>立即登录</el-button>
      </div>
      <el-divider>
          <span style="font-size: 13px;color: grey">没有账号</span>
      </el-divider>
      <div>
          <el-button style="width: 270px" type="warning" plain>立即注册</el-button>
      </div>
  </div>
</template>

<script setup>
import  { User, Lock } from '@element-plus/icons-vue'
import {reactive} from "vue";

const form = reactive({
    username: '',
    password: '',
    remember: false
})
</script>

<style scoped>

</style>