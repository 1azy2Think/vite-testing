<script setup>
import { ref } from 'vue'

const num = ref(2)
console.log(num.value)

setInterval(() => {
  num.value++
}, 10000)

function Clicking() {
  num.value++
}
</script>

<template>
  <div>
    {{ num }}

    <button type="button" v-on:click="Clicking">Click</button>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
