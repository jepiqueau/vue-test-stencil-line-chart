<template>
  <div class="ion-page">
    <ion-header>
      <ion-toolbar color="primary">
        <ion-buttons slot="start">
          <ion-back-button defaultHref="/"></ion-back-button>
        </ion-buttons>
        <ion-title>Linechart</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content>
      <template v-if="this.type === 'basic'">
        <jeep-linechart
          ctitle="Basic Line Chart"
          subtitle="test sub-title"
          xtitle="test for x axis"
          ytitle="test for y axis"
          data='{
                    "color": "#425cef",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 450 },
                        { "x": "2012-01-02", "y": 414 },
                        { "x": "2012-01-03", "y": 520 },
                        { "x": "2012-01-04", "y": 460 },
                        { "x": "2012-01-05", "y": 450 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 480 },
                        { "x": "2012-01-08", "y": 480 },
                        { "x": "2012-01-09", "y": 410 },
                        { "x": "2012-01-10", "y": 500 },
                        { "x": "2012-01-11", "y": 480 },
                        { "x": "2012-01-12", "y": 510 }]}'
          animation
          cborder
        >
        </jeep-linechart>
      </template>
      <template v-if="this.type === 'markers'">
        <jeep-linechart
          ctitle="Basic Line Chart"
          subtitle="With Markers"
          xtitle="test for x axis"
          ytitle="test for y axis"
          data='{
                    "color": "#425cef",
                    "name": "Line 1",
                    "markerType": "plus",
                    "markerSize": 10,
                    "markerColor": "#d543ef",
                "dataPoints":[
                { "x": 14, "y": 450 },
                { "x": 20, "y": 414 },
                { "x": 30, "y": 520 },
                { "x": 40, "y": 460 },
                { "x": 50, "y": 450 },
                { "x": 60, "y": 500 },
                { "x": 70, "y": 480 },
                { "x": 80, "y": 480 },
                { "x": 90, "y": 410 },
                { "x": 100, "y": 500 },
                { "x": 110, "y": 480 },
                { "x": 120, "y": 510 }]}'
        >
        </jeep-linechart>
      </template>
      <template v-if="this.type === 'multiplelines'">
        <jeep-linechart
          ctitle="Multiple Lines Chart"
          subtitle="With Markers"
          xtitle="test for x axis"
          ytitle="test for y axis"
          data='[{
                    "color": "#425cef",
                    "name": "Line 1",
                    "markerType": "plus",
                    "markerSize": 10,
                    "markerColor": "#d543ef",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 450 },
                        { "x": "2012-01-02", "y": 414 },
                        { "x": "2012-01-03", "y": 520 },
                        { "x": "2012-01-04", "y": 460 },
                        { "x": "2012-01-05", "y": 450 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 480 },
                        { "x": "2012-01-08", "y": 480 },
                        { "x": "2012-01-09", "y": 410 },
                        { "x": "2012-01-10", "y": 500 },
                        { "x": "2012-01-11", "y": 480 },
                        { "x": "2012-01-12", "y": 510 }]},
                    {
                    "color": "#efd543",
                    "name": "Line 2",
                    "markerType": "square",
                    "markerSize": 6,
                    "markerColor": "#5def43",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 430 },
                        { "x": "2012-01-02", "y": 510 },
                        { "x": "2012-01-03", "y": 450 },
                        { "x": "2012-01-04", "y": 470 },
                        { "x": "2012-01-05", "y": 430 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 420 },
                        { "x": "2012-01-08", "y": 450 },
                        { "x": "2012-01-09", "y": 380 },
                        { "x": "2012-01-10", "y": 390 },
                        { "x": "2012-01-11", "y": 495 },
                        { "x": "2012-01-12", "y": 505 }]},
                    {
                    "color": "#ff0000",
                    "name": "Line 3",
                    "lineThickness": 2,
                    "markerType": "circle",
                    "markerSize": 10,
                    "markerColor": "#ff0000",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 530 },
                        { "x": "2012-01-02", "y": 410 },
                        { "x": "2012-01-03", "y": 550 },
                        { "x": "2012-01-04", "y": 440 },
                        { "x": "2012-01-05", "y": 330 },
                        { "x": "2012-01-06", "y": 400 },
                        { "x": "2012-01-07", "y": 520 },
                        { "x": "2012-01-08", "y": 550 },
                        { "x": "2012-01-09", "y": 280 },
                        { "x": "2012-01-10", "y": 590 },
                        { "x": "2012-01-11", "y": 395 },
                        { "x": "2012-01-12", "y": 455 }]}]'
          animation
          cborder
        >
        </jeep-linechart>
      </template>
      <template v-if="this.type === 'multipleplots'">
        <div>
          <jeep-linechart
            id="basic"
            ctitle="Basic Line Chart"
            subtitle="test sub-title"
            xtitle="test for x axis"
            ytitle="test for y axis"
            data='{
                    "color": "#425cef",
                        "dataPoints":[
                        { "x": "2012-01-01", "y": 450 },
                        { "x": "2012-01-02", "y": 414 },
                        { "x": "2012-01-03", "y": 520 },
                        { "x": "2012-01-04", "y": 460 },
                        { "x": "2012-01-05", "y": 450 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 480 },
                        { "x": "2012-01-08", "y": 480 },
                        { "x": "2012-01-09", "y": 410 },
                        { "x": "2012-01-10", "y": 500 },
                        { "x": "2012-01-11", "y": 480 },
                        { "x": "2012-01-12", "y": 510 }]}'
            animation
            cborder
            cstyle="--height:250px;--width:70%;--top:20px;--left:10%;--backgroundcolor: rgb(248, 243, 222);"
          >
          </jeep-linechart>
          <jeep-linechart
            id="multiple"
            ctitle="Multiple Lines Chart"
            subtitle="With Markers"
            xtitle="test for x axis"
            ytitle="test for y axis"
            data='[{
                    "color": "#425cef",
                    "name": "Line 1",
                    "markerType": "plus",
                    "markerSize": 10,
                    "markerColor": "#d543ef",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 450 },
                        { "x": "2012-01-02", "y": 414 },
                        { "x": "2012-01-03", "y": 520 },
                        { "x": "2012-01-04", "y": 460 },
                        { "x": "2012-01-05", "y": 450 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 480 },
                        { "x": "2012-01-08", "y": 480 },
                        { "x": "2012-01-09", "y": 410 },
                        { "x": "2012-01-10", "y": 500 },
                        { "x": "2012-01-11", "y": 480 },
                        { "x": "2012-01-12", "y": 510 }]},
                    {
                    "color": "#efd543",
                    "name": "Line 2",
                    "markerType": "square",
                    "markerSize": 6,
                    "markerColor": "#5def43",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 430 },
                        { "x": "2012-01-02", "y": 510 },
                        { "x": "2012-01-03", "y": 450 },
                        { "x": "2012-01-04", "y": 470 },
                        { "x": "2012-01-05", "y": 430 },
                        { "x": "2012-01-06", "y": 500 },
                        { "x": "2012-01-07", "y": 420 },
                        { "x": "2012-01-08", "y": 450 },
                        { "x": "2012-01-09", "y": 380 },
                        { "x": "2012-01-10", "y": 390 },
                        { "x": "2012-01-11", "y": 495 },
                        { "x": "2012-01-12", "y": 505 }]},
                    {
                    "color": "#ff0000",
                    "name": "Line 3",
                    "lineThickness": 2,
                    "markerType": "circle",
                    "markerSize": 10,
                    "markerColor": "#ff0000",
                    "dataPoints":[
                        { "x": "2012-01-01", "y": 530 },
                        { "x": "2012-01-02", "y": 410 },
                        { "x": "2012-01-03", "y": 550 },
                        { "x": "2012-01-04", "y": 440 },
                        { "x": "2012-01-05", "y": 330 },
                        { "x": "2012-01-06", "y": 400 },
                        { "x": "2012-01-07", "y": 520 },
                        { "x": "2012-01-08", "y": 550 },
                        { "x": "2012-01-09", "y": 280 },
                        { "x": "2012-01-10", "y": 590 },
                        { "x": "2012-01-11", "y": 395 },
                        { "x": "2012-01-12", "y": 455 }]}]'
            animation
            cborder
            cstyle="--height:350px;width:90%;--top:30px;--left:15px;"
          >
          </jeep-linechart>
        </div>
      </template>
    </ion-content>
  </div>
</template>

<script>
export default {
  name: "linechart",
  data() {
    return {
      type: this.$route.params.type
    };
  },
  created() {
    const root = document.documentElement;
    switch (this.type) {
      case "basic": {
        root.style.setProperty("--chart-axis-x-interval", "1");
        break;
      }
      case "markers": {
        root.style.setProperty("--chart-axis-x-interval", "20");
        break;
      }
      case "multiplelines": {
        root.style.setProperty("--chart-axis-x-interval", "2");
        break;
      }
      case "multipleplots": {
        root.style.setProperty("--chart-axis-x-interval", "1");
        break;
      }
    }
  }
};
</script>
