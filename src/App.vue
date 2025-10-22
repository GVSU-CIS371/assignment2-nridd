<template>
  <div>
    <Beverage :isIced="temp === 'Cold'" />
    <ul>
      <li>
        <input type="radio" value="Hot" v-model="temp" />Hot
        <input type="radio" value="Cold" v-model="temp" />Cold
      </li>
      <li>
        <input type="radio" value="Black Tea" v-model="base" />Black Tea
        <input type="radio" value="Green Tea" v-model="base" />Green Tea
        <input type="radio" value="Coffee" v-model="base" />Coffee
      </li>
      <li>
        <input type="radio" value="No Cream" v-model="creamer" />No Cream
        <input type="radio" value="Milk" v-model="creamer" />Milk
        <input type="radio" value="Cream" v-model="creamer" />Cream
        <input type="radio" value="Half & Half" v-model="creamer" />Half & Half
      </li>
      <li>
        <input type="radio" value="No Syrup" v-model="syrup" />No Syrup
        <input type="radio" value="Vanilla" v-model="syrup" />Vanilla
        <input type="radio" value="Caramel" v-model="syrup" />Caramel
        <input type="radio" value="Hazelnut" v-model="syrup" />Hazelnut
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import Beverage from "./components/Beverage.vue"
import { ref } from "vue"
const temp = ref("Hot")
const base = ref("Coffee")
const creamer = ref("No Cream")
const syrup = ref("No Syrup")
</script>

<style>
body,html{position:relative;display:flex;align-items:center;justify-content:center;height:100%;background:linear-gradient(to bottom,#6e4228 0%,#956f5a 100%);}
ul{list-style:none;padding:0;margin-top:1rem;}
li{margin-bottom:0.5rem;}
input{margin:0 0.25rem;}
</style>
