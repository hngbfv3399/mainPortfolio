<template>
    <canvas ref="chartCanvas" />
  </template>
  
  <script>
  import { onMounted, ref, watch } from 'vue';
  import {
    Chart,
    BarController,
    BarElement,
    CategoryScale,
    LinearScale,
    Tooltip,
    Legend,
  } from 'chart.js';
  
  Chart.register(BarController, BarElement, CategoryScale, LinearScale, Tooltip, Legend);
  
  export default {
    name: 'SkillChart',
    props: {
      skills: {
        type: Array,
        required: true,
      },
    },
    setup(props) {
      const chartCanvas = ref(null);
      let chartInstance = null;
  
      const createChart = () => {
        if (chartInstance) {
          chartInstance.destroy();
        }
        chartInstance = new Chart(chartCanvas.value, {
          type: 'bar',
          data: {
            labels: props.skills.map((s) => s.name),
            datasets: [
              {
                label: '숙련도 %',
                data: props.skills.map((s) => s.level),
                backgroundColor: '#4caf50',
                borderRadius: 5,
                barPercentage: 0.6,
                categoryPercentage: 0.7,
              },
            ],
          },
          options: {
            indexAxis: 'x', // 가로 바 차트
            responsive: true,
            maintainAspectRatio: false, // 부모 컨테이너 크기에 맞게
            scales: {
              x: {
                beginAtZero: true,
                max: 100,
                ticks: {
                  stepSize: 20,
                },
              },
              y: {
                grid: {
                  display: false,
                },
              },
            },
            plugins: {
              legend: {
                display: false,
              },
              tooltip: {
                enabled: true,
              },
            },
          },
        });
      };
  
      onMounted(() => {
        createChart();
      });
  
      watch(
        () => props.skills,
        () => {
          createChart();
        }
      );
  
      return {
        chartCanvas,
      };
    },
  };
  </script>
  
  <style scoped>
  canvas {
    width: 100% !important;
    height: 100% !important;
    display: block;
  }
  </style>
  