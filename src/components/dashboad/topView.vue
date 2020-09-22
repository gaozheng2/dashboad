<template>
  <v-container fluid>
    <v-row>
      <v-col>
        <total-sales />
      </v-col>

      <v-col>
        <total-orders />
      </v-col>

      <v-col>
        <today-users />
      </v-col>

      <v-col>
        <total-users />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TotalSales from './topView/totalSales'
import TotalOrders from './topView/totalOrders'
import TodayUsers from './topView/todayUsers'
import TotalUsers from './topView/totalUsers'
export default {
  name: 'TopView',
  components: {
    TotalSales,
    TotalOrders,
    TodayUsers,
    TotalUsers
  }
}
</script>
