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

const printHello = () => {
  console.log("Hello");
};

display();
</script>

<template>
  <!-- on utilise : pour passer des props -->
  <HelloWorld :user="user" />

  <div v-if="user.age > 15">Mon âge</div>
  <div v-else>J'ai moins de 15 ans</div>
  <br />

  <!-- v-model pour lier la valeur de l'input à une variable -->
  <input type="text" v-model="user.name" v-on:input="printHello" />
  <input type="text" v-model="user.age" @input="printHello" />
</template>

<style scoped></style>
