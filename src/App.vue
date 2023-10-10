<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <p>@core-monorepo/common에서 가져온 함수 : {{ now }}, {{ lastDate }}</p>
    <p>@core-monorepo/vue에서 가져온 컴포넌트 : <Today /></p>
  </div>
</template>

<script>
import { nowDate, nowYearLastDate } from '@core-monorepo/common';
import { Today } from '@core-monorepo/vue';

export default {
  name: 'App',
  components: { Today },
  data() {
    return {
      now: nowDate(),
      lastDate: nowYearLastDate(),
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
ㄴ