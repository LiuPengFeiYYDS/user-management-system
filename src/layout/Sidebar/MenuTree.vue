<template>
  <div>
    <el-menu
      active-text-color="#ffd04b"
      background-color="#304156"
      class="el-menu-vertical-demo"
      default-active="2"
      text-color="#fff"
      router
    >
      <Item v-for="item in props.menu" :data="item" :key="item"></Item>
    </el-menu>
  </div>
</template>
<script setup>
import { defineProps } from 'vue'
import Item from './Item.vue'

const props = defineProps({
  menu: {
    type: Array,
    default: () => []
  }
})
</script>
<style scoped lang="scss"></style>
