<template>
  <div>
    <common-card
      title="累计用户数"
      value="¥ 1,087,503"
    >
      <template>
        <v-chart :options="getOptions()" />
      </template>

      <template v-slot:footer>
        <div class="total-users-footer">
          <span>日同比</span>
          <span class="num">8.73%</span>
          <div class="increase"></div>
          <span class="ml-4">月同比</span>
          <span class="num">35.91%</span>
          <div class="decrease"></div>
        </div>
      </template>
    </common-card>
  </div>
</template>

<script>
import commonCardMixin from '@/mixins/commonCardMixin.js'
export default {
  mixins: [commonCardMixin],
  methods: {
    getOptions () {
      return {
        xAxis: {
          type: 'value',
          show: false
        },
        yAxis: {
          type: 'category',
          show: false
        },
        series: [{
          type: 'bar',
          stack: '总量',
          data: [200],
          barWidth: 10,
          itemStyle: {
            color: '#45C946'
          }
        }, {
          type: 'bar',
          stack: '总量',
          data: [250],
          itemStyle: {
            color: '#eee'
          }
        }, {
          type: 'custom',
          stack: '总量',
          data: [200],
          renderItem: (params, api) => {
            const value = api.value(0)
            const endPoint = api.coord([value, 0])
            return {
              type: 'path',
              position: endPoint,
              shape: {
                d: 'M1,21H23L12,2',
                x: -6,
                y: 5,
                width: 12,
                height: 12
              },
              style: {
                fill: '#45C946'
              }
            }
          }
        }],
        grid: {
          top: 0,
          bottom: 0,
          left: 0,
          right: 0
        }
      }
    }
  }
}
</script>

<style scoped>
.total-users-footer {
  display: flex;
  align-items: center;
}
</style>
