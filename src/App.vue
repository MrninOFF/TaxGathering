<template>
  <div id="app">
    <img width="25%" src="./assets/table.png">
    <HelloWorld msg="Conflict Gathering Tax"/>
    <div class="p-1">
      <button
        type="button"
        v-bind:class="[button_4_2_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit4_2"
        v-on:click="show4_2"
      >4.2</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_4_3_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit4_3"
        v-on:click="show4_3"
      >4.3</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_5_2_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit5_2"
        v-on:click="show5_2"
      >5.2</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_5_3_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit5_3"
        v-on:click="show5_3"
      >5.3</button> &nbsp;
    </div>
    <div class="p-1">
      <button
        type="button"
        v-bind:class="[button_6_0_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit6_0"
        v-on:click="show6_0"
      >6.0</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_6_1_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit6_1"
        v-on:click="show6_1"
      >6.1</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_6_2_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit6_2"
        v-on:click="show6_2"
      >6.2</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_6_3_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit6_3"
        v-on:click="show6_3"
      >6.3</button> &nbsp;
    </div>
    <div class="p-1">
      <button
        type="button"
        v-bind:class="[button_7_0_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit7_0"
        v-on:click="show7_0"
      >7.0</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_7_1_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit7_1"
        v-on:click="show7_1"
      >7.1</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_7_2_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit7_2"
        v-on:click="show7_2"
      >7.2</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_7_3_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit7_3"
        v-on:click="show7_3"
      >7.3</button> &nbsp;
    </div>
    <div class="p-1">
      <button
        type="button"
        v-bind:class="[button_8_0_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit8_0"
        v-on:click="show8_0"
      >8.0</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_8_1_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit8_1"
        v-on:click="show8_1"
      >8.1</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_8_2_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit8_2"
        v-on:click="show8_2"
      >8.2</button> &nbsp;
      <button
        type="button"
        v-bind:class="[button_8_3_class ? 'btn btn-primary' : 'btn btn-success']"
        @click="submit8_3"
        v-on:click="show8_3"
      >8.3</button> &nbsp;
    </div>
    <div class="form-row justify-content-center">
      <div class="form-group col-md-4">
        <input
          type="text"
          class="form-control"
          @input="debounceSearch"
          placeholder="How much do you need to pay ?"
        >
      </div>
      <div class="form-group col-md-4">
        <input type="text" class="form-control" v-model="totalValue" placeholder="You pay total">
      </div>
    </div>
    <div id="T4_2_div" v-if="T4_2_show" class="p-1">
      <h2>T4.2</h2>
      <vue-slider
        v-model="T4_2"
        :min="T4_2_min"
        :max="T4_2_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T4_3_div" v-if="T4_3_show" class="p-1">
      <h2>T4.3</h2>
      <vue-slider
        v-model="T4_3"
        :min="T4_3_min"
        :max="T4_3_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T5_2_div" v-if="T5_2_show" class="p-1">
      <h2>T5.2</h2>
      <vue-slider
        v-model="T5_2"
        :min="T5_2_min"
        :max="T5_2_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T5_3_div" v-if="T5_3_show" class="p-1">
      <h2>T5.3</h2>
      <vue-slider
        v-model="T5_3"
        :min="T5_3_min"
        :max="T5_3_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T6_0_div" v-if="T6_0_show" class="p-1">
      <h2>T6.0</h2>
      <vue-slider
        v-model="T6_0"
        :min="T6_0_min"
        :max="T6_0_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T6_1_div" v-if="T6_1_show" class="p-1">
      <h2>T6.1</h2>
      <vue-slider
        v-model="T6_1"
        :min="T6_1_min"
        :max="T6_1_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T6_2_div" v-if="T6_2_show" class="p-1">
      <h2>T6.2</h2>
      <vue-slider
        v-model="T6_2"
        :min="T6_2_min"
        :max="T6_2_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T6_3_div" v-if="T6_3_show" class="p-1">
      <h2>T6.3</h2>
      <vue-slider
        v-model="T6_3"
        :min="T6_3_min"
        :max="T6_3_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T7_0_div" v-if="T7_0_show" class="p-1">
      <h2>T7.0</h2>
      <vue-slider
        v-model="T7_0"
        :min="T7_0_min"
        :max="T7_0_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T7_1_div" v-if="T7_1_show" class="p-1">
      <h2>T7.1</h2>
      <vue-slider
        v-model="T7_1"
        :min="T7_1_min"
        :max="T7_1_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T7_2_div" v-if="T7_2_show" class="p-1">
      <h2>T7.2</h2>
      <vue-slider
        v-model="T7_2"
        :min="T7_2_min"
        :max="T7_2_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T7_3_div" v-if="T7_3_show" class="p-1">
      <h2>T7.3</h2>
      <vue-slider
        v-model="T7_3"
        :min="T7_3_min"
        :max="T7_3_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T8_0_div" v-if="T8_0_show" class="p-1">
      <h2>T8.0</h2>
      <vue-slider
        v-model="T8_0"
        :min="T8_0_min"
        :max="T8_0_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T8_1_div" v-if="T8_1_show" class="p-1">
      <h2>T8.1</h2>
      <vue-slider
        v-model="T8_1"
        :min="T8_1_min"
        :max="T8_1_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T8_2_div" v-if="T8_2_show" class="p-1">
      <h2>T8.2</h2>
      <vue-slider
        v-model="T8_2"
        :min="T8_2_min"
        :max="T8_2_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
    <div id="T8_3_div" v-if="T8_3_show" class="p-1">
      <h2>T8.3</h2>
      <vue-slider
        v-model="T8_3"
        :min="T8_3_min"
        :max="T8_3_max"
        :min-range="5"
        :height="5"
        :process-dragable="true"
        tooltip-dir="top"
        @input="getTotalValue"
      ></vue-slider>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import VueSlider from "vue-slider-component";

export default {
  name: "App",
  components: {
    HelloWorld,
    VueSlider
  },
  data: () => ({
    debounce: null,
    needPay: 1,
    totalValue: null,
    T4_2_show: false,
    T4_3_show: false,
    T5_2_show: false,
    T5_3_show: false,
    T6_0_show: false,
    T6_1_show: false,
    T6_2_show: false,
    T6_3_show: false,
    T7_0_show: false,
    T7_1_show: false,
    T7_2_show: false,
    T7_3_show: false,
    T8_0_show: false,
    T8_1_show: false,
    T8_2_show: false,
    T8_3_show: false,
    button_4_2_class: true,
    button_4_3_class: true,
    button_5_2_class: true,
    button_5_3_class: true,
    button_6_0_class: true,
    button_6_1_class: true,
    button_6_2_class: true,
    button_6_3_class: true,
    button_7_0_class: true,
    button_7_1_class: true,
    button_7_2_class: true,
    button_7_3_class: true,
    button_8_0_class: true,
    button_8_1_class: true,
    button_8_2_class: true,
    button_8_3_class: true,
    T4_2: 0,
    T4_2_min: 0,
    T4_2_max: 1,
    T4_3: 0,
    T4_3_min: 0,
    T4_3_max: 1,
    T5_2: 0,
    T5_2_min: 0,
    T5_2_max: 1,
    T5_3: 0,
    T5_3_min: 0,
    T5_3_max: 1,
    T6_0: 0,
    T6_0_min: 0,
    T6_0_max: 1,
    T6_1: 0,
    T6_1_min: 0,
    T6_1_max: 1,
    T6_2: 0,
    T6_2_min: 0,
    T6_2_max: 1,
    T6_3: 0,
    T6_3_min: 0,
    T6_3_max: 1,
    T7_0: 0,
    T7_0_min: 0,
    T7_0_max: 1,
    T7_1: 0,
    T7_1_min: 0,
    T7_1_max: 1,
    T7_2: 0,
    T7_2_min: 0,
    T7_2_max: 1,
    T7_3: 0,
    T7_3_min: 0,
    T7_3_max: 1,
    T8_0: 0,
    T8_0_min: 0,
    T8_0_max: 1,
    T8_1: 0,
    T8_1_min: 0,
    T8_1_max: 1,
    T8_2: 0,
    T8_2_min: 0,
    T8_2_max: 1,
    T8_3: 0,
    T8_3_min: 0,
    T8_3_max: 1
  }),
  methods: {
    debounceSearch(event) {
      clearTimeout(this.debounce);

      this.needPay = Number(event.target.value);

      if (!isNaN(this.needPay)) {
        this.T4_2_max = 272 * this.needPay;
        this.T4_3_max = 109 * this.needPay;
        this.T5_2_max = 90 * this.needPay;
        this.T5_3_max = 36 * this.needPay;
        this.T6_0_max = 360 * this.needPay;
        this.T6_1_max = 180 * this.needPay;
        this.T6_2_max = 90 * this.needPay;
        this.T6_3_max = 36 * this.needPay;
        this.T7_0_max = 108 * this.needPay;
        this.T7_1_max = 54 * this.needPay;
        this.T7_2_max = 27 * this.needPay;
        this.T7_3_max = 11 * this.needPay;
        this.T8_0_max = 42 * this.needPay;
        this.T8_1_max = 21 * this.needPay;
        this.T8_2_max = 11 * this.needPay;
        this.T8_3_max = 4 * this.needPay;
      }
    },
    getTotalValue(event) {
      this.totalValue = 0;
      if (this.T4_2_show) this.totalValue = this.totalValue + this.T4_2 / 272;
      if (this.T4_3_show) this.totalValue = this.totalValue + this.T4_3 / 109;
      if (this.T5_2_show) this.totalValue = this.totalValue + this.T5_2 / 90;
      if (this.T5_3_show) this.totalValue = this.totalValue + this.T5_3 / 36;
      if (this.T6_0_show) this.totalValue = this.totalValue + this.T6_0 / 360;
      if (this.T6_1_show) this.totalValue = this.totalValue + this.T6_1 / 180;
      if (this.T6_2_show) this.totalValue = this.totalValue + this.T6_2 / 90;
      if (this.T6_3_show) this.totalValue = this.totalValue + this.T6_3 / 36;
      if (this.T7_0_show) this.totalValue = this.totalValue + this.T7_0 / 108;
      if (this.T7_1_show) this.totalValue = this.totalValue + this.T7_1 / 54;
      if (this.T7_2_show) this.totalValue = this.totalValue + this.T7_2 / 27;
      if (this.T7_3_show) this.totalValue = this.totalValue + this.T7_3 / 11;
      if (this.T8_0_show) this.totalValue = this.totalValue + this.T8_0 / 42;
      if (this.T8_1_show) this.totalValue = this.totalValue + this.T8_1 / 21;
      if (this.T8_2_show) this.totalValue = this.totalValue + this.T8_2 / 11;
      if (this.T8_3_show) this.totalValue = this.totalValue + this.T8_3 / 4;

      this.totalValue = Number(this.totalValue.toFixed(3));
    },
    submit4_2() {
      this.T4_2_show = !this.T4_2_show;
      this.button_4_2_class = !this.T4_2_show;
    },
    show4_2: function() {},
    submit4_3() {
      this.T4_3_show = !this.T4_3_show;
      this.button_4_3_class = !this.T4_3_show;
    },
    show4_3: function() {},
    submit5_2() {
      this.T5_2_show = !this.T5_2_show;
      this.button_5_2_class = !this.T5_2_show;
    },
    show5_2: function() {},
    submit5_3() {
      this.T5_3_show = !this.T5_3_show;
      this.button_5_3_class = !this.T5_3_show;
    },
    show5_3: function() {},
    submit6_0() {
      this.T6_0_show = !this.T6_0_show;
      this.button_6_0_class = !this.T6_0_show;
    },
    show6_0: function() {},
    submit6_1() {
      this.T6_1_show = !this.T6_1_show;
      this.button_6_1_class = !this.T6_1_show;
    },
    show6_1: function() {},
    submit6_2() {
      this.T6_2_show = !this.T6_2_show;
      this.button_6_2_class = !this.T6_2_show;
    },
    show6_2: function() {},
    submit6_3() {
      this.T6_3_show = !this.T6_3_show;
      this.button_6_3_class = !this.T6_3_show;
    },
    show6_3: function() {},
    submit7_0() {
      this.T7_0_show = !this.T7_0_show;
      this.button_7_0_class = !this.T7_0_show;
    },
    show7_0: function() {},
    submit7_1() {
      this.T7_1_show = !this.T7_1_show;
      this.button_7_1_class = !this.T7_1_show;
    },
    show7_1: function() {},
    submit7_2() {
      this.T7_2_show = !this.T7_2_show;
      this.button_7_2_class = !this.T7_2_show;
    },
    show7_2: function() {},
    submit7_3() {
      this.T7_3_show = !this.T7_3_show;
      this.button_7_3_class = !this.T7_3_show;
    },
    show7_3: function() {},
    submit8_0() {
      this.T8_0_show = !this.T8_0_show;
      this.button_8_0_class = !this.T8_0_show;
    },
    show8_0: function() {},
    submit8_1() {
      this.T8_1_show = !this.T8_1_show;
      this.button_8_1_class = !this.T8_1_show;
    },
    show8_1: function() {},
    submit8_2() {
      this.T8_2_show = !this.T8_2_show;
      this.button_8_2_class = !this.T8_2_show;
    },
    show8_2: function() {},
    submit8_3() {
      this.T8_3_show = !this.T8_3_show;
      this.button_8_3_class = !this.T8_3_show;
    },
    show8_3: function() {}
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
