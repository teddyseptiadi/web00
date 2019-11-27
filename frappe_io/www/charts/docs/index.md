<!-- base_template: frappe_io/www/charts/charts_base.html -->
## Installation
* Install via [npm](https://www.npmjs.com/get-npm):

  ```console
  $ npm install frappe-charts
  ```

  and include in your project:
  ```js
  import { Chart } from "frappe-charts/dist/frappe-charts.min.esm"
  ```

* ...or include within your HTML

  ```html
    <script src="https://cdn.jsdelivr.net/npm/frappe-charts@1.1.0/dist/frappe-charts.min.iife.js"></script>
    <!-- or -->
    <script src="https://unpkg.com/frappe-charts@1.1.0/dist/frappe-charts.min.iife.js"></script>
  ```

## Usage
```js
const data = {
    labels: ["12am-3am", "3am-6pm", "6am-9am", "9am-12am",
        "12pm-3pm", "3pm-6pm", "6pm-9pm", "9am-12am"
    ],
    datasets: [
        {
            name: "Some Data", type: "bar",
            values: [25, 40, 30, 35, 8, 52, 17, -4]
        },
        {
            name: "Another Set", type: "line",
            values: [25, 50, -10, 15, 18, 32, 27, 14]
        }
    ]
}

const chart = new Chart("#chart", {  // or a DOM element,
                                            // new Chart() in case of ES6 module with above usage
    title: "My Awesome Chart",
    data: data,
    type: 'axis-mixed', // or 'bar', 'line', 'scatter', 'pie', 'percentage'
    height: 250,
    colors: ['#7cd6fd', '#743ee2']
})
```

## Demo
Here's a demo to try out yourself:
<p data-height="299" data-theme-id="light" data-slug-hash="wjKBoq" data-default-tab="js,result"
    data-user="pratu16x7" data-embed-version="2" data-pen-title="Frappe Charts Demo" class="codepen">
    See the Pen <a href="https://codepen.io/pratu16x7/pen/wjKBoq/">Frappe Charts Demo</a>
    by Prateeksha Singh (<a href="https://codepen.io/pratu16x7">@pratu16x7</a>) on
    <a href="https://codepen.io">CodePen</a>.
</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>
