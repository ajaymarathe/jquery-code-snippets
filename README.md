# jquery-code-snippets
hi there, this is jquery code snippets repo, thanks.

### add chart on button click
```
// button
<div class="row">
    <div class="col-md-3">
      <div id="chartId"  height="200"></div>
    </div>

    <div class="col-md-12">
      <Button class="btn btn-primary" id="AddChart">Add Chart</Button>
    </div>
 </div>

// add chart on button click
$(function () {
  var count = 0;
  $('#AddChart').click(function () {
    count += 1;
	var ChartCount = count;
	$("#chartId").append("<canvas id="+ChartCount+"  height="+200+"></canvas>");

	var ctx = document.getElementById(ChartCount).getContext('2d');
	var ChartCount = new Chart(ctx, {
		type: 'bar',
		data: {
			labels: ['New', 'Qualified', 'SVP', 'SVC', 'Lost', 'HOP','HOD', 'All Leads'],
			datasets: [{
				data: [
				12,34,54,55,23,23,78,23			
				],
				backgroundColor: [
					'#337ab7',
					'#36c6d3',
					'#ed6b75',
					'#F1C40F',
					'#3D80D7',
					'#183475',
					'#ffad33',
					'#4caf50'
				],
				borderColor: [
					'#337ab7',
					'#36c6d3',
					'#ed6b75',
					'#F1C40F',
					'#3D80D7',
					'#183475',
					'#ffad33',
					'#4caf50'
				],
				borderWidth: 1,
			}]
		},
		options: {
			legend: {
				display: false
			},
			scales: {
				yAxes: [{
					ticks: {
						beginAtZero:true,
					}
				}],
				xAxes: [{
					gridLines : {
						display : false
					},
					ticks: {
						
					}
				}]
			}
		}
	});
  });
});

```
