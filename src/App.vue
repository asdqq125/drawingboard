<script setup lang="ts">
import { ref } from "vue";
import Header from "./lib/components/header/Header.vue";
import Left from "./lib/components/left/Left.vue";

const msg = ref("未命名原型");
</script>

<template>
  <div>
    <el-row>
      <el-col :span="24" class="header-area">
        <Header :msg="msg"></Header>
      </el-col>
    </el-row>
    <el-row>
      <el-col :span="3" class="left-area">
        <Left color="rgb(37, 38, 38)"></Left>
      </el-col>
      <el-col :span="17">
        <div>中</div>
      </el-col>
      <el-col :span="4">
        <div>右</div>
      </el-col>
    </el-row>
  </div>
</template>

<style lang="scss" scoped>
#app {
  width: 100%;
  height: 100%;

  .header-area {
    position: relative;
  }

  .left-area {
    height: 100%;
  }
}
</style>
