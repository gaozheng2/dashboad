<template>
  <div>
    <common-card
      title="累计销售额"
      value="¥ 32,039,165"
    >
      <template>
        <div class="compare">
          <span>日同比</span>
          <span class="num">7.33%</span>
          <div class="increase"></div>
        </div>
        <div class="compare">
          <span>月同比</span>
          <span class="num">7.33%</span>
          <div class="decrease"></div>
        </div>
      </template>
      <template v-slot:footer>
        <span>昨日销售额 </span>
        <span class="num">¥ 30,000,000</span>
      </template>
    </common-card>
  </div>
</template>

<script>
import commonCardMixin from '@/mixins/commonCardMixin.js'
export default {
  mixins: [commonCardMixin]

}
</script>

<style lang="scss" scoped>
.compare {
  display: flex;
  align-items: center;
  font-size: 12px;
  margin-top: 3px;
}
</style>
