<template>
 <div class="small">
    <Chart :chart-data="datacollection"></Chart>
    
  </div>
</template>

<script>
  import Chart from '@/components/chart.js'

  export default {
    components: {
      Chart
    },
    data () {
      return {
        datacollection: null
      }
    },
    mounted () {
      this.fillData()
    },
    methods: {
      fillData () {
        this.datacollection = {
          title: 'Data Pengabdian Internal Per Jurusan',
          labels: [0, 2017, 2018,2019,2020,2021],
          datasets: [
            {
              label: 'Teknik Informatika dan Komputer',
              backgroundColor: 'rgba(27,64,215,30%)',
              pointBackgroundColor: '#1B4091',
              data: [0,6,6,5]
            }, 
            {
              label: 'Teknik Mesin',
              backgroundColor: 'rgba(52,157,204,30%)',
              pointBackgroundColor: 'rgba(52,157,204,100%)',
              data: [0,5,6,11]
            },
            {
              label: 'Teknik Sipil',
              backgroundColor: pattern.draw('diamond', '#97622C'),
              pointBackgroundColor: '#97622C',
              data: [0,5,6,7]
            },
          ]
        }
      },
      getRandomInt () {
        return Math.floor(2,4,6,8,10,12,14,16,18)
      }
    }
  }
</script>

<style>
  .small {
    max-width: 300px;
    margin:  150px auto;
  }
</style>