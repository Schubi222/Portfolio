<template>
  <div class="Menu-bar-mobile noSelect">
    <div class="Menu-bar-mobile__hover-box " @click="toggle_mobile_menu">
      <div class="Menu-bar-mobile__hamburger" ref="hamburger_div"></div>
    </div>
    <div class="Menu-bar-mobile__side-panel" ref="side_panel">
      <nav class="Menu-bar-mobile__side-panel__link-container">
        <RouterLink class="Menu-bar-mobile__side-panel__link-container__link Menu-bar__link" :to="{name:'home'}" @click="toggle_mobile_menu">
         <span class="mobile-text">Home</span> <span class="mobile-arrow">&rsaquo;</span>
        </RouterLink>
        <RouterLink class="Menu-bar-mobile__side-panel__link-container__link Menu-bar__link" :to="{name:'projects'}" @click="toggle_mobile_menu">
          <span class="mobile-text">Projects</span> <span class="mobile-arrow">&rsaquo;</span>
        </RouterLink>
        <RouterLink class="Menu-bar-mobile__side-panel__link-container__link Menu-bar__link" :to="{name:'about'}" @click="toggle_mobile_menu">
          <span class="mobile-text">About</span> <span class="mobile-arrow">&rsaquo;</span>
        </RouterLink>
      </nav>
    </div>
  </div>

</template>

<script setup>
import { RouterLink } from 'vue-router'
import {ref} from "vue";

const hamburger_div = ref()
const side_panel = ref()

const toggle_mobile_menu = () =>{
  hamburger_div.value.classList.toggle('is_open')
  side_panel.value.classList.toggle('menu_is_open')
}



</script>

<style scoped>
  @import "@/assets/MenuBar.css";
</style>