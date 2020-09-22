<template>
  <div class="home">
    <top-view />
    <list-view />
    <pie-view />
  </div>
</template>

<script>
import TopView from '@/components/dashboad/topView.vue'
import ListView from '@/components/dashboad/listView.vue'
import PieView from '@/components/dashboad/pieView.vue'

export default {
  name: 'Home',
  components: {
    TopView,
    ListView,
    PieView
  }
}
</script>

<style scoped>
.home {
  height: 100%;
  background: #eee;
  padding: 0 20px;
}
</style>

<style>
.echarts {
  width: 100% !important;
  height: 100% !important;
}
.num {
  margin-left: 5px;
  color: #333;
  font-weight: 700;
}
.increase {
  width: 0;
  height: 0;
  border-width: 5px;
  border-color: transparent transparent red transparent;
  border-style: solid;
  margin: 0 0 4px 5px;
}
.decrease {
  width: 0;
  height: 0;
  border-width: 5px;
  border-color: green transparent transparent transparent;
  border-style: solid;
  margin: 4px 0 0 5px;
}
</style>
