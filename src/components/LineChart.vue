<template>
<div>
  <apexchart width="500" type="bar" :options="options" :series="series"></apexchart>
</div>
</template>

<script>
export default {
 name: 'VueChart',
 data: function () {
  return {
  options: {
        title: {
          text: 'Top 5 Apps by Traffic',
          align: 'left',
          style: {
            fontSize: "16px",
            color: '#fff',
            fontFamily: 'poppins',
          }
        },
        colors: ["#20E647"],
        subtitle: {
         text: 'Sorted By Traffic ● Last 30 Days',
         style: {
            fontSize: "14px",
            color: '#fff',
            fontFamily: 'poppins',
          }
        },
         grid: {
            xaxis: {
                lines: {
                show: false
                }
            },
            yaxis:{
                lines:{
                show: false
                }
            }
        },
        chart: {
          type: 'bar',
          height: 350
        },
        plotOptions: {
          bar: {
            borderRadius: 4,
            horizontal: true,
            barHeight: '30%'
          },
          color: '#000'
        },
         fill: {
            type: "gradient",
            gradient: {
            colors: ["#20E647"],
            type: "vertical",
            gradientToColors: ["#87D4F9"],
            stops: [0, 100]
            }
         },
        dataLabels: {
          enabled: false,
           style: {
            color: '#000000'
        },
        },
        xaxis: {
          categories: ['Elastic', 'Launcher', 'Fedora', 'DataLake', 'Nginx'],
          color: '#fff'
        }
  },
    series: [{
          data: [166, 102 , 92,  88, 63]
        }],
  
 }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div{
    background: #1d1f1f;
}
a {
  color: #42b983;
}
</style>
