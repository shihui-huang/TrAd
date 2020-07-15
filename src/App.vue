<template>
  <div id="app">
    <!-- 加载过依稀的内容会放在内存 不会每次刷新都重新加载 -->
    <keep-alive>
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>
