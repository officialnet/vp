---
layout: default
title: "مثال رسم بياني"
---

<div id="chart" style="height:360px;"></div>

<script src="https://cdn.jsdelivr.net/npm/echarts@5/dist/echarts.min.js"></script>
<script>
  const chart = echarts.init(document.getElementById('chart'));
  chart.setOption({
    title: { text: 'مثال: خط بياني' },
    tooltip: { trigger: 'axis' },
    xAxis: { type: 'category', data: ['2019','2020','2021','2022','2023'] },
    yAxis: { type: 'value' },
    series: [{ type: 'line', data: [80,82,79,85,86], smooth: true }]
  });
  window.addEventListener('resize', () => chart.resize());
</script>
