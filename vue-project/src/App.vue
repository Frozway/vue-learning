<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { ref } from "vue";

const user = ref({
  name: "Thibaut LEFRANCOIS",
  age: 19,
});

const display = () => {
  console.log(user.name, user.age); // Pas besoin de user.value.name car user est un objet
};

display();
</script>

<template>
  <!-- on utilise : pour passer des props -->
  <HelloWorld :user="user" />

  <!-- v-model pour lier la valeur de l'input à une variable -->
  <input type="text" v-model="user.name" />
  <input type="text" v-model="user.age" />
</template>

<style scoped></style>
