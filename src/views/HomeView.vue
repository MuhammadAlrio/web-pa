<template>
  
  <div class="d-flex flex-row bd-highlight mb-3 justify-content-center align-items-center"
    >
    <div class="d-flex w-50 h-25">
      <Camera :resolution="{ width: 1920, height: 1080 }" autoplay="false"></camera>
    </div>
   
  </div>
  
 
</template>



<script setup>
import { defineComponent } from "vue";
import Camera from "simple-vue-camera";


</script>


