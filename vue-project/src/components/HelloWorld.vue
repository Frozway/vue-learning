<template>
  <h1>Hello World</h1>
  <p>{{ props.user.name }} | {{ props.user.age }}</p>
</template>

<script setup>
const props = defineProps(["user"]);
</script>
