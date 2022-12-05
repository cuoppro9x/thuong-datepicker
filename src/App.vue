<template>
  <div id="app">
    <div class="single-test">
      <h3>Single</h3>
      <div style="margin-bottom: 8px">Value: {{ datetime }}</div>
      <ThuongDatepicker
        v-model="datetime"
        placeholder="Single date pick"
        locale="default"
        refs="inputDate"
        mode="single"
        @onFocus="onFocus"
        @onBlur="onBlur"
        @onSelect="onSelect"
        @onClear="onClear"
      />
    </div>
    <div class="multiple-test">
      <h3>Multiple</h3>
      <div style="margin-bottom: 8px">Value: {{ datetime2 }}</div>
      <ThuongDatepicker
        v-model="datetime2"
        placeholder="Multiple date pick"
        locale="default"
        refs="inputDate"
        mode="multiple"
        @onFocus="onFocus"
        @onBlur="onBlur"
        @onSelect="onSelect"
        @onClear="onClear"
      />
    </div>
    <div class="range-test">
      <h3>Range</h3>
      <div style="margin-bottom: 8px">Value: {{ datetime3 }}</div>
      <ThuongDatepicker
        v-model="datetime3"
        placeholder="Range date pick"
        locale="default"
        refs="inputDate"
        mode="range"
        @onFocus="onFocus"
        @onBlur="onBlur"
        @onSelect="onSelect"
        @onClear="onClear"
      />
    </div>
  </div>
</template>

<script>
import ThuongDatepicker from "./components/ThuongDatepicler.vue";

export default {
  name: "App",
  components: {
    ThuongDatepicker,
  },
  data() {
    return {
      datetime: null,
      datetime2: null,
      datetime3: null,
    };
  },
  methods: {
    onFocus() {
      console.log("focus");
    },
    onBlur() {
      console.log("blur");
    },
    onSelect(val) {
      console.log(val);
    },
    onClear() {
      console.log("clear");
    },
  },
};
</script>
