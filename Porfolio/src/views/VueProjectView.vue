<template>
<div class="Vue-Project-View-Wrapper">
  <div class="Vue-Project-View-Wrapper__back-btn animated-link" @click="$router.back()">&#11013; Back</div>
  <div class="Vue-Project-View-Wrapper__logo"> <img class="main_Menu_Item main_Menu_Img" src="@/assets/logo.svg" alt="logo" /></div>
  <PerfectTextField :text="text" class="Vue-Project-View-Wrapper__description"/>
  <div class="Vue-Project-View-Wrapper__applications">
    <router-link :to="{name:'vue-projects_Age'}" class="Vue-Project-View-Wrapper__applications-btn">Age Calculator</router-link>
    <router-link :to="{name:'vue-projects_BMI'}"  class="Vue-Project-View-Wrapper__applications-btn">BMI Calculator</router-link>
    <router-link :to="{name:'vue-projects_math-quiz'}"  class="Vue-Project-View-Wrapper__applications-btn">Math-Quiz</router-link>
    <router-link :to="{name:'vue-projects_calculator'}"  class="Vue-Project-View-Wrapper__applications-btn">Calculator</router-link>

  </div>
  <router-view class="Vue-Project-View-Wrapper__router-view"/>
</div>
</template>

<script setup>
import {RouterView} from "vue-router";
import PerfectTextField from "@/components/PerfectTextField.vue";
import {onMounted, ref} from "vue";
const text = ref("These are some small Vue.js projects I have built to improve my knowledge!")

onMounted(()=>{
  window.scrollTo({
    top: 0,
    left: 0,
    behavior: "smooth",
  });
})
</script>


<style scoped>
  @import "@/assets/VueProjectCss/VueProjectView.css";

</style>