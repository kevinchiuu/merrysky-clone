<script>
    import { onMount } from "svelte";
    import Chart from 'chart.js/auto'

    function chart() {
        const ctx = document.getElementById('myChart');
  
        new Chart(ctx, {
            type: 'bar',
            data: {
            labels: ['Monday'],
            datasets: [{
                label: '# of Votes',
                data: [3],
                borderWidth: 1
            },{
                label: '# of Votes',
                data: [8],
                borderWidth: 1
            },{
                label: '# of Votes',
                data: [19],
                borderWidth: 1
            }]
            },
            options: {
                indexAxis: 'y',
                scales: {
                    x:{
                        stacked: true
                    },
                    y: {
                        beginAtZero: true,
                        stacked: true
                    }
                }
            }
        });
    }
    onMount(chart);
</script>

<div>
    <h1 class="text-xl"> This is the chart component </h1>
    <canvas id="myChart"></canvas>
</div>
