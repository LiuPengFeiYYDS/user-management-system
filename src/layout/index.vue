<template>
  <div class="app-wrapper">
    <sidebar class="sidebar-container"></sidebar>
    <div class="main-container">
      <div class="fiexed-header">
        <navbar></navbar>
        <tags-view></tags-view>
      </div>
      <app-main></app-main>
    </div>
  </div>
</template>

<script setup>
import Sidebar from './Sidebar'
import Navbar from './Navbar'
import AppMain from './AppMain'
import TagsView from '../components/TagsView'
</script>

<style lang="scss" scoped>
.app-wrapper {
  position: relative;
  width: 100%;
  height: 100%;

  .sidebar-container {
    width: 210px;
    height: 100%;
    background-color: #304156;
    overflow-y: auto;
    position: fixed;
    left: 0;
    top: 0;
    bottom: 0;
    float: left;
    -ms-overflow-style: none;
    scrollbar-width: none;
  }

  .main-container {
    float: left;
    width: calc(100% - 210px);
    height: 100%;
    margin-left: 210px;
    position: relative;

    .fiexed-header {
      position: fixed;
      top: 0;
      right: 0;
      z-index: 9;
      width: calc(100% - 210px);
    }
  }
}
::-webkit-scrollbar {
  display: none;
}
</style>
