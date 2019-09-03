<template>
  <div class="widget-price-range">
    <h3 class="widget-title">Refine a price</h3>
    <div class="app-content">
      <vue-range-slider
        :bg-style="bgStyle"
        :tooltip-style="tooltipStyle"
        :process-style="processStyle"
        :dot-color="dot"
        v-model="value" :min="min" :max="max" :height="height"
      ></vue-range-slider>
    </div>
    <!-- <div
      id="slider-range"
      class="ui-slider ui-slider-horizontal ui-widget ui-widget-content ui-corner-all"
    >
      <div
        class="ui-slider-range ui-widget-header ui-corner-all"
        style="left: 25.102%; width: 52.2449%;"
      ></div>
      <span
        class="ui-slider-handle ui-state-default ui-corner-all"
        tabindex="0"
        style="left: 25.102%;"
      ></span>
      <span
        class="ui-slider-handle ui-state-default ui-corner-all"
        tabindex="0"
        style="left: 77.3469%;"
      ></span>
    </div>-->
    <!-- <div class="block">
      <div
        role="slider"
        aria-valuemin="0"
        aria-valuemax="10"
        aria-orientation="horizontal"
        class="el-slider"
        aria-valuetext="4-8"
        aria-label="slider between 0 and 10"
      >
        <div class="el-slider__runway">
          <div class="el-slider__bar" style="width: 10%; left: 40%;"></div>
          <div tabindex="0" class="el-slider__button-wrapper" style="left: 40%;">
            <div
              class="el-tooltip el-slider__button"
              aria-describedby="el-tooltip-797"
              tabindex="0"
            ></div>
          </div>
          <div tabindex="0" class="el-slider__button-wrapper" style="left: 50%;">
            <div
              class="el-tooltip el-slider__button"
              aria-describedby="el-tooltip-7762"
              tabindex="0"
            ></div>
          </div>
        </div>
      </div>
    </div>-->
    <!-- <input type="range" :dual="true" />
    <div class="block">
      <el-slider v-model="data[0].range" range :max="data[0].max" :min="data[0].min"></el-slider>
    </div>-->

    <!-- <div class="values">
      <input type="text" class="minamount" v-model="data[0].range[0]" />
      <span class="filter-gap">-</span>
      <input type="text" class="maxamount" v-model="data[0].range[1]" />
      <input type="submit" class="btn btn-default" value="search" name="search" />
    </div>-->
  </div>
</template>

<script>
import NoSSR from 'vue-no-ssr'
// import 'vue-range-component/dist/vue-range-slider.css'
// import VueRangeSlider from 'vue-range-component'
export default {
  data() {
    return {
      // data: [{ min: 10, max: 500, slider: 1, range: [30, 150] }],
      value: [80, 225]
    }
  },
  methods: {},
  created() {
    this.dot = {backgroundColor: 'black'}
    this.height = 12
    this.min = 10
    this.max = 500
    this.bgStyle = {
    //  backgroundColor: '#fff',
    //  boxShadow: 'inset 0.5px 0.5px 3px 1px rgba(0,0,0,.36)'
    }
    this.tooltipStyle = {
      backgroundColor: '#666',
      borderColor: '#666'
    }
    this.processStyle = {
      backgroundColor: '#fda341'
    }
  }
}
</script>

<style scoped>
h3.widget-title {
  font-family: 'Montserrat', sans-serif;
  text-transform: uppercase;
  font-size: 13px;
  letter-spacing: 1px;
}
.widget-title {
  margin-bottom: 32px;
  border-bottom: 2px solid #d3d3d3;
  color: #292929;
  padding-bottom: 10px;
}
.values input.minamount,
input.maxamount {
  padding: 8px 12px;
  margin-right: 13px;
  width: 60px;
}
.values input {
  border: 1px solid #a8a8a8;
  display: inline;
  color: #404040;
  margin-bottom: 15px;
}
.minamount,
.maxamount {
  font-weight: 300;
  font-family: 'Montserrat', sans-serif;
  font-size: 13px;
}
.btn {
  font-family: 'Montserrat Light';
  background-color: white;
  border: 1px solid #a8a8a8;
  display: inline-block;
  font-size: 10px;
  text-transform: uppercase;
  font-weight: lighter;
  border-radius: 0px;
}
.values input.btn.btn-default {
  margin-left: 8px;
  padding: 6px 15px;
  -webkit-transition: ease 0.15s;
  transition: ease 0.15s;
}
.values input.btn.btn-default:hover {
  color: #ffffff;
  background-color: #fda341;
  border: 1px solid #fda341;
}
.values .filter-gap {
  color: #404040;
  font-size: 20px;
  margin-right: 11px;
}

.widget-price-range .ui-widget-content {
  background: #f0f0f0 none repeat scroll 0 0;
  border: 1px solid #f0f0f0;
  margin-bottom: 25px;
}
.widget-price-range .ui-widget-content .ui-widget-header {
  background: #fda341;
  border: 0px solid;
}
.widget-price-range .ui-widget-content .ui-state-default {
  background: #202020;
  border: 0px solid;
  border-radius: 50%;
}
.ui-slider .ui-slider-handle {
  position: absolute;
  z-index: 2;
  width: 1.2em;
  height: 1.2em;
  cursor: pointer;
  -ms-touch-action: none;
  touch-action: none;
}
.ui-slider-horizontal .ui-slider-handle {
  top: -0.3em;
  margin-left: -0.6em;
}
.ui-slider-horizontal .ui-slider-range {
  top: 0;
  height: 100%;
}
.ui-slider .ui-slider-range {
  position: absolute;
  z-index: 1;
  font-size: 0.7em;
  display: block;
  border: 0;
  background-position: 0 0;
}
.ui-slider-horizontal {
  height: 0.8em;
}
.ui-slider {
  position: relative;
  text-align: left;
}
.ui-widget-header {
  border: 1px solid #dddddd;
  background: #e9e9e9;
  color: #333333;
  font-weight: bold;
}
.ui-corner-all {
  border-bottom-right-radius: 3px;
  border-bottom-left-radius: 3px;
  border-top-right-radius: 3px;
  border-top-left-radius: 3px;
}
.el-slider__bar {
  height: 6px;
  background-color: #fda341;
  border-top-left-radius: 3px;
  border-bottom-left-radius: 3px;
  position: absolute;
}
</style>