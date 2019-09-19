<template>
  <div class="login">
    <LoginHeader></LoginHeader>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import LoginHeader from "./LoginHeader.vue";
@Component({
  components: {}
})
export default class Login extends Vue {}
</script>

<style lang="sass">

</style>