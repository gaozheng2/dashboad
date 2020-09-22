<template>
  <v-card
    height="180"
    outlined
    hover
  >
    <v-card-text>
      <div class="card-title">{{title}}</div>
      <div class="value">{{value}}</div>
      <div class="chart">
        <slot></slot>
      </div>
      <div class="line"></div>
      <div class="total">
        <slot name="footer"></slot>
      </div>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: 'common-card',
  props: {
    title: String,
    value: String
  }
}
</script>

<style scoped>
  .card-title {
    font-size: 14px;
    color: #333;
  }
  .value {
    font-size: 25px;
    color: #000;
    margin-top: 10px;
    letter-spacing: 1px;
  }
  .chart {
    height: 50px;
    margin-top: 10px;
  }
  .line {
    margin: 10px 0;
    border-top: 1px solid #eee;
  }
  .total {
    font-size: 12px;
    color: #666;
  }
</style>
