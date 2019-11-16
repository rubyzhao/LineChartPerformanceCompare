# Line Chart Performance Comparison

## The selected chart packages

Name|SVG/Canvas|Version|Publish Date|Web
---|---|---|---|---|
Canvas lineTo|Canvas|||https://www.w3schools.com/graphics/canvas_coordinates.asp|
CanvasJS|Canvas|2.3.2|11-Jul-19|https://canvasjs.com/|
Chartist|SVG|0.11.4|11-Apr-17|https://gionkunz.github.io/chartist-js/|
Chartjs|Canvas|2.8.0|14-Mar-19|https://www.chartjs.org/|
D3|SVG|5.12.0|6-Sep-19|https://d3js.org/|
D3|Canvas|5.12.0|6-Sep-19|https://d3js.org/|
Dygraphs|Canvas|2.1.0|9-Dec-17|https://github.com/danvk/dygraphs|
Echarts|Canvas|4.4.0|29-Sep-19|https://www.echartsjs.com/en/index.html|
Echarts|SVG|4.4.0|29-Sep-19|https://www.echartsjs.com/en/index.html|
Flot|Canvas|4.1.0|6-Nov-19|http://www.flotcharts.org/|
Highcharts|Canvas|7.2.1|31-Oct-19|https://www.highcharts.com/|
jqChart|Canvas|5.0.0|18-Jun-18|http://www.jqchart.com/|
SVG line|SVG|||https://www.w3schools.com/graphics/svg_line.asp|
SVG polyline|SVG|||https://www.w3schools.com/graphics/svg_polyline.asp|
uPlot|Canvas|0.1.0|20-Oct-19|https://github.com/leeoniya/uPlot|
ZRender|Canvas|4.1.1|28-Sep-19|https://ecomfe.github.io/zrender-doc/public/|
ZRender|SVG|4.1.1|28-Sep-19|https://ecomfe.github.io/zrender-doc/public/|

## Environment
  1. Windows: 10x86 1803
  2. Processor: Intel(R) Core(TM) i7-4930MX CPU @3.00 GHz
  3. RAM: 32.0GB
  4. Chrome: 78.0.3904.97 (Official Build) (64-bit)
  5. pwmetrics: 4.2.2
  6. Live Server: 5.6.1
  7. VS Code: 1.40.1
  8. Node: 12.11.1
  
## Workflow  
  1. Copy all chart libraries to the local disk
  2. Draw sin wave as examples below:
  
    https://github.com/rubyzhao/Sin-Wave-with-Basic-Canvas
    https://github.com/rubyzhao/Sine-Wave-with-Basic-SVG 
    
   ![Sin wave example](https://github.com/rubyzhao/LineChartPerformanceCompare/blob/master/SinWave.png)
   
  3. Use Live Server to setup local server
  4. Run pwmetrics with runs=5
  5. Change loop in step 2 from loop=2e2, to 2e3, 2e4, 2e5, 2e6 and 2e7 and repeat step 3 and 4

## Performance result for loop=2e3

Source.Name|Average of firstContentfulPaint|Average of firstMeaningfulPaint|Average of interactive|Average of firstCPUIdle
---|---|---|---|---|
Canvas_lineTo.xlsx|731.40|731.40|733.00|731.40|
SVG_polyline.xlsx|744.40|744.40|744.40|744.40|
SVG_line.xlsx|873.60|873.60|873.60|873.60|
uPlot.xlsx|1395.00|1395.00|1488.60|1401.80|
ZRender_SVG.xlsx|1719.80|1719.80|1719.80|1719.80|
ZRender_Canvas.xlsx|1723.00|1723.00|1723.00|1723.00|
Dygraphs.xlsx|1736.60|1736.60|1736.60|1736.60|
Chartjs.xlsx|2190.40|2190.40|2190.40|2190.40|
D3_SVG.xlsx|2202.40|2202.40|2202.40|2202.40|
Chartist.xlsx|2406.00|2406.00|2406.00|2406.00|
D3_Canvas.xlsx|2457.60|2457.60|2457.60|2457.60|
Highcharts.xlsx|2532.40|2532.40|2532.40|2532.40|
jqChart.xlsx|2946.80|2946.80|2946.80|2946.80|
CanvasJS.xlsx|3572.20|3572.20|3672.00|3572.20|
Flot.xlsx|4015.20|4015.20|4015.20|4015.20|
Echarts_Canvas.xlsx|5418.00|5418.00|9604.20|9604.20|
Echarts_SVG.xlsx|6340.80|6340.80|8361.00|8329.00|

   ![Sin wave example](https://github.com/rubyzhao/LineChartPerformanceCompare/blob/master/SinWave2e3.png)

## Performance result for loop=2e5

Source.Name|Average of firstContentfulPaint|Average of firstMeaningfulPaint|Average of interactive|Average of firstCPUIdle
---|---|---|---|---|
Canvas_lineTo.xlsx|1056.40|1056.40|1056.40|1056.40|
uPlot.xlsx|1447.40|1447.40|1729.20|1594.40|
SVG_polyline.xlsx|1704.60|1704.60|1704.60|1704.60|
ZRender_SVG.xlsx|2262.40|2262.40|2275.00|2262.40|
D3_Canvas.xlsx|2896.20|2896.20|2896.20|2896.20|
D3_SVG.xlsx|3035.80|3035.80|3035.80|3035.80|
Highcharts.xlsx|4131.00|4137.40|8337.20|8317.00|
ZRender_Canvas.xlsx|5072.00|5072.00|5072.00|5072.00|
CanvasJS.xlsx|5155.60|5155.60|5158.00|5155.60|
Chartjs.xlsx|8460.80|8460.80|8460.80|8460.80|
Dygraphs.xlsx|11505.80|11505.80|11506.80|11506.80|
jqChart.xlsx|12408.60|12408.60|12408.60|12408.60|
SVG_line.xlsx|13729.20|13729.20|15257.80|15242.00|
Echarts_Canvas.xlsx|14725.00|14725.00|14756.40|14725.00|

![Sin wave example](https://github.com/rubyzhao/LineChartPerformanceCompare/blob/master/SinWave2e5.png)

## Performance result for loop=2e6

Source.Name|Average of firstContentfulPaint|Average of firstMeaningfulPaint|Average of interactive|Average of firstCPUIdle
---|---|---|---|---|
uPlot.xlsx|1666.60|1666.60|2590.40|2380.40|
Canvas_lineTo.xlsx|3472.40|3472.40|3473.40|3472.40|
ZRender_SVG.xlsx|8764.00|8764.00|8764.00|8764.00|
D3_Canvas.xlsx|9220.20|9220.20|9220.20|9220.20|
SVG_polyline.xlsx|10803.80|10803.80|10910.20|10902.60|
Chartjs.xlsx|11894.20|11894.20|11894.20|11894.20|
D3_SVG.xlsx|12160.00|12160.00|12730.00|12730.00|
CanvasJS.xlsx|13156.00|13156.00|13156.00|13156.00|
Highcharts.xlsx|15487.75|18863.50|31234.00|30953.50|

   ![Sin wave example](https://github.com/rubyzhao/LineChartPerformanceCompare/blob/master/SinWave2e6.png)
