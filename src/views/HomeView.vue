<template>
  <div id="Home" class="flex flex-col h-screen">
    <div class="m-3 mb-auto">
      <div class="grid grid-cols-2 gap-3 my-3">
        <ServiceSelectLarge text="Ride" imageWidth="70" image="Ride"/>
        <ServiceSelectLarge text="Food" imageWidth="70" image="Food" :promo="true"/>
      </div>
      <div class="grid grid-cols-4 gap-3 my-3">
        <ServiceSelectSmall text="2 Wheels" image="2Wheels"/>
        <ServiceSelectSmall text="Transit" image="transit"/>
        <ServiceSelectSmall text="Reserve" image="Reserve"/>
        <ServiceSelectSmall text="Travel" image="travel"/>
      </div>
    </div>
  </div>
</template>

<script setup>

import ServiceSelectLarge from '@/components/ServiceSelectLarge.vue';
import ServiceSelectSmall from '@/components/ServiceSelectSmall.vue';


</script>
