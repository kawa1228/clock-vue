<template>
  <div>
    <Clock class="clock"/>
  </div>
</template>

<script>
import Clock from "./components/Clock.vue"

export default {
  components: {
    Clock,
  }
}
</script>

<style scoped>
.clock {
  width: 80%;
  max-width: 500px;
  margin: 30px auto;
}
</style>
