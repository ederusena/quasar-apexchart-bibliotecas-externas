<template>
  <q-page>
    <div class="row q-ma-sm q-col-gutter-sm">
      <div class="col-6">
        <q-card>
          <q-card-section>
            <apexchart
              height="350"
              type="bar"
              :options="options"
              :series="series"
            />
          </q-card-section>
        </q-card>
      </div>

      <div class="col-6">
        <q-card>
          <q-card-section>
            <apexchart
              height="350"
              type="bar"
              :options="options"
              :series="series"
            />
          </q-card-section>
        </q-card>
      </div>
  </div>

  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageIndex',
  data () {
    return {
      options: {
        chart: {
          id: 'vuechart-example'
        },
        xaxis: {
          categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998]
        }
      },
      series: [{
        name: 'series-1',
        data: [30, 40, 45, 50, 49, 60, 70, 91]
      }]
    }
  }
})
</script>
