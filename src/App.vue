<template>
  <h2>Node Version Details</h2>
  Data origin source:
  <a href="https://nodejs.org/download/release/index.json"
    >https://nodejs.org/download/release/index.json</a
  >
  <VersionList />
  Data origin source:
  <a href="https://raw.githubusercontent.com/nodejs/Release/main/schedule.json"
    >https://raw.githubusercontent.com/nodejs/Release/main/schedule.json</a
  >
  <br />
  <img
    src="https://raw.githubusercontent.com/nodejs/Release/main/schedule.svg"
  />
</template>

<script>
import VersionList from "./components/VersionList.vue";
export default {
  name: "App",
  components: {
    VersionList,
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
  padding: 20px;
}
</style>
