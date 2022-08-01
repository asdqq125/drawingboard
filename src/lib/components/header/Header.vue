<script setup lang="ts">
import { ref } from "vue";

defineProps<{ msg: string }>();
</script>


<template>
  <div id="header">
    <div class="left-group">left</div>
    <div class="mid-group">
      <span class="mid-group-title-style el-dropdown-link">{{ msg }}</span>
      <el-dropdown>
        <span class="el-dropdown-link">
          <el-icon style=" margin-top: 5px;margin-left:6px" color="#FFFFFF"><ArrowDown /></el-icon>
        </span>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>保存</el-dropdown-item>
            <el-dropdown-item divided>重命名</el-dropdown-item>
            <el-dropdown-item>查看版本信息</el-dropdown-item>
            <el-dropdown-item divided>页面回收</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
    <div class="right-group">right</div>
  </div>
</template>

<style lang="scss" scoped>
$bg-color: rgb(37, 38, 38) !default;
#header {
  width: 100%;
  min-height: 48px;
  background: $bg-color;
  text-align: center;
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;

  .left-group,
  .right-group {
    min-width: 100px;
    text-align: center;
  }
  .mid-group {
    flex: 1;
    text-align: center;
    .example-showcase .el-dropdown-link {
      cursor: pointer;
      color: var(--el-color-primary);
      display: flex;
      align-items: center;
    }

    .mid-group-title-style {
      font-size: 14px;
      color: #fff;
    }
  }
}
</style>