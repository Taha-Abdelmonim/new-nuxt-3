<template>
  <section>
    <!-- <img src="~/assets" alt="" /> -->
    <!-- <img src="~/public" alt="" /> -->
    <p>This page will be displayed at the /about route.</p>
    Counter: {{ counter }}
    <button @click="counter++">+</button>
    <button @click="counter--">-</button>
    <p>Current color: {{ color }}</p>
  </section>
</template>
<script setup>
const color = useColor();
const counter = useState("counter", () => Math.round(Math.random() * 1000));
</script>
