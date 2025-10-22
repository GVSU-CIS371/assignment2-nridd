<template>
  <div>
    <Beverage
      :isIced="temp === 'cold'"
      :base="base"
      :creamer="creamer"
      :syrup="syrup"
    />
    <ul>
      <li>
        <input type="radio" value="hot" v-model="temp" />Hot
        <input type="radio" value="cold" v-model="temp" />Cold
      </li>
      <li>
        <input type="radio" value="coffee" v-model="base" />Coffee
        <input type="radio" value="green-tea" v-model="base" />Green Tea
        <input type="radio" value="black-tea" v-model="base" />Black Tea
      </li>
      <li>
        <input type="radio" value="none" v-model="creamer" />No Cream
        <input type="radio" value="milk" v-model="creamer" />Milk
        <input type="radio" value="cream" v-model="creamer" />Cream
        <input type="radio" value="half-half" v-model="creamer" />Half & Half
      </li>
      <li>
        <input type="radio" value="none" v-model="syrup" />No Syrup
        <input type="radio" value="vanilla" v-model="syrup" />Vanilla
        <input type="radio" value="caramel" v-model="syrup" />Caramel
        <input type="radio" value="hazelnut" v-model="syrup" />Hazelnut
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import Beverage from "./components/Beverage.vue"
import { ref } from "vue"

const temp = ref("hot")
const base = ref("coffee")
const creamer = ref("none")
const syrup = ref("none")
</script>

<style>
body,html{position:relative;display:flex;align-items:center;justify-content:center;height:100%;background:linear-gradient(to bottom,#6e4228 0%,#956f5a 100%);}
ul{list-style:none;padding:0;margin-top:1rem;}
li{margin-bottom:0.5rem;}
input{margin:0 0.25rem;}
</style>
