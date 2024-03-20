<template>
  <h1>Hello World</h1>
  <p>{{ props.subTitle }}</p>
</template>

<script setup>
const props = defineProps(["subTitle"]);
</script>
