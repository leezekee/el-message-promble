<template>
  <el-button type="primary" @click="clickHandler">Primary</el-button>
</template>

<script setup>
import { ElMessage } from 'element-plus';
const clickHandler = () => {
  ElMessage.closeAll()
  ElMessage({
    message: '这是第一条提醒',
    type: 'success',
    duration: 3 * 1000
  })
  // ElMessage.closeAll()
  // ElMessage({
  //   message: '这是第二条提醒',
  //   type: 'success',
  //   duration: 3 * 1000
  // })
  setTimeout(() => {
    ElMessage.closeAll()
    ElMessage({
      message: '这是第二条提醒',
      type: 'success',
      duration: 3 * 1000
    })
  }, 3000);
}
</script>
