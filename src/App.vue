<template>
  <div id="app">
    <div class = "container">
      <br/>
      <div class = "row">
        <div class = "col-md-6">
          <div class = "card" style="background-color: #1d1f1f;">
                <AreaChart/>
          </div>
        </div>
        <div class = "col-md-6">
           <div class = "card" style="background-color: #1d1f1f;">
                <VisitorChart/>         
          </div>
        </div>
      </div>
      <br/>
      <div class = "row">
        <div class = "col-md-6">
          <div class = "card" style="background-color: #1d1f1f;">
                <BarChart/>
          </div>
        </div>
        <div class = "col-md-6">
           <div class = "card" style="background-color: #1d1f1f;">
                <VueChart/>             
          </div>
        </div>
      </div>
      <br/>
      <div class = "card" style="background-color: #1d1f1f; border-right: 1px solid #1d1f1f;">
        <div class = "row">
              <h2 class = "mt-3" style = "font-size: 16px;color: white; text-align: left; font-weight: 600; margin-left: 5px;">&nbsp;Resource Utilization</h2>
              <p style = "font-size: 14px;color: white; text-align: left; margin-left: 5px;">All Apps ● Last 24 hours <p>
              <div class = "col-sm-4">
                    <GaugeChart/>   
              </div>
               <div class = "col-sm-4">
                    <GaugeChart/>
              </div>
              <div class = "col-sm-4">
                   <GaugeChart/>
              </div>  
        </div>
        <br/>
        </div>
    </div>
    
  </div>
</template>

<script>
import VueChart from './components/LineChart.vue'
import AreaChart from './components/AreaChart.vue'
import VisitorChart from './components/VisitorChart.vue'
import BarChart from './components/BarChart.vue'
import GaugeChart from './components/GaugeChart.vue'
export default {
  name: 'App',
  components: {
    VueChart,
    AreaChart,
    VisitorChart,
    BarChart,
    GaugeChart
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');
#app {
  font-family: poppins;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #fdfdfd; */
  width: 100%;
  height: 100%;
  background-color: #111111;
  margin: 0;
  padding: 0;
}
.card{
  background-color: #181717;
}
</style>
