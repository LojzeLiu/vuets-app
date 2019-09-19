<template>
  <div class="login">
    <LoginHeader>
      <el-form :model="ruleForm" label-position="left" label-width="0px" slot="container">
        <div class="title">
          <h3>帐号</h3>
        </div>
      </el-form>
    </LoginHeader>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Provide } from "vue-property-decorator";
import LoginHeader from "./LoginHeader.vue";
@Component({
  components: { LoginHeader }
})
export default class Login extends Vue {
  @Provide() ruleForm: {
    username: String;
    pwd: String;
    autoLogin: boolean;
  } = {
    username: "",
    pwd: "",
    autoLogin: true //是否自动登录
  };
}
</script>

<style lang="scss" scoped>
.title {
  margin: 0px auto 40px auto;
  text-align: center;
  color: #505458;
}

i {
  font-size: 14px;
  margin-left: 8px;
}
.forget {
  float: right;
}
</style>