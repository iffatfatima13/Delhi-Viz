<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>My D3 Chart</title>
  <style>
    body { font-family: sans-serif; margin: 2rem; }
    .observablehq-chart {
      max-width: 960px;
      margin: 0 auto;
    }
  </style>
</head>
<body>

<h1>My Interactive D3 Chart</h1>
<div id="chart" class="observablehq-chart"></div>

<!-- Load Observable Runtime -->
<script type="module">
  import define from "https://api.observablehq.com/d/2b350a58d17c8f13.js?v=3";
  import {Runtime, Inspector} from "https://cdn.jsdelivr.net/npm/@observablehq/runtime@4/dist/runtime.js";

  new Runtime().module(define, name => {
    if (name === "chart") return new Inspector(document.getElementById("chart"));
  });
</script>

</body>
</html>
