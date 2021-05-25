<template>
<div>
  <apexchart width="500" type="line" :options="options" :series="series"></apexchart>
</div>
</template>

<script>
export default {
 name: 'AreaChart',
 data: function () {
  return {
  options: {
      chart: {
          height: 350,
          type: 'line',
        },
        stroke: {
          width: 7,
          curve: 'smooth'
        },
        xaxis: {
          type: 'datetime',
          categories: ['1/11/2000', '2/11/2000', '3/11/2000', '4/11/2000', '5/11/2000', '6/11/2000', '7/11/2000', '8/11/2000', '9/11/2000', '10/11/2000', '11/11/2000', '12/11/2000', '1/11/2001', '2/11/2001', '3/11/2001','4/11/2001' ,'5/11/2001' ,'6/11/2001'],
          tickAmount: 10,
          labels: {
            formatter: function(value, timestamp, opts) {
              return opts.dateFormatter(new Date(timestamp), 'dd MMM')
            }
          }
        },
        title: {
          text: 'Daily Visitor Trend',
          align: 'left',
          style: {
            fontSize: "16px",
            color: '#fff',
            fontFamily: 'poppins',
          }
        },
        subtitle: {
         text: 'All active users ● Last 24 Hours',
         style: {
            fontSize: "14px",
            color: '#fff',
            fontFamily: 'poppins',
          }
        },
        fill: {
          type: 'gradient',
          gradient: {
            shade: 'dark',
            gradientToColors: [ '#FDD835'],
            shadeIntensity: 1,
            type: 'horizontal',
            opacityFrom: 1,
            opacityTo: 1,
            stops: [0, 100, 100, 100]
          },
        },
        markers: {
          size: 4,
          colors: ["#FFA41B"],
          strokeColors: "#fff",
          strokeWidth: 2,
          hover: {
            size: 7,
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
        yaxis: {
          min: -10,
          max: 40,
          title: {
            text: '',
          },
        }
  },
    series: [{
          name: 'Visitor',
          data: [4, 3, 10, 9, 29, 19, 22, 9, 12, 7, 19, 5, 13, 9, 17, 2, 7, 5]
    }]
  
 }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div{
    background: #1d1f1f;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
