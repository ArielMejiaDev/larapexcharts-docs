<script setup>
import VueApexCharts from 'vue3-apexcharts';

const chart = {
    type: "heatmap",
    series: [{"name":"Sales","data":[80,50,30,40,100,20]},{"name":"Income","data":[70,10,80,20,60,40]}],
    options: {"chart":{"height":500,"toolbar":{"show":false},"zoom":{"enabled":true}},"plotOptions":{"bar":{"horizontal":false}},"colors":["#008FFB","#00E396","#feb019","#ff455f","#775dd0","#80effe","#0077B5","#ff6384","#c9cbcf","#0057ff","00a9f4","#2ccdc9","#5e72e4"],"dataLabels":{"enabled":false},"title":{"text":"Basic radar chart"},"subtitle":{"text":"","align":""},"xaxis":{"categories":["January","February","March","April","May","June"],"convertedCatToNumeric":false},"grid":{"show":false},"markers":{"size":7,"colors":["#FFA41B","#4F46E5"],"strokeColors":"#fff","strokeWidth":3.5,"hover":{"size":10}}}
}
</script>

<template>
  <ClientOnly>
    <div class="chart-container">
      <div class="chart-card">
        <VueApexCharts :width="chart.options.chart.width" :type="chart.type" :options="chart.options" :series="chart.series"></VueApexCharts>
      </div>
    </div>
  </ClientOnly>
</template>