<template>
    <div id="Directions">
        <div class="grid grid-cols-12 mt-4 shadow-md">
            <div class="col-span-2 mx-auto">

                <div>
                    <ArrowIcon :size="35"/>
                </div>

                <div class="h-16 mt-4 w-full">
                    <div :class="[isPickuActive ? 'circle-black' : 'circle-gray']"></div>
                    <div class="line"></div>
                    <div :class="[!isPickuActive ? 'square-black' : 'square-gray']"></div>
                </div>
            </div>
            
            <div class="col-span-10 pr-4">
                <div class="w-full h-5"></div>

                <div class="mb-2 mt-5">
                    autoocmplete
                </div>
            </div>

        </div>
    </div>
</template>
  

<script setup>
    import { ref } from 'vue'
    import ArrowIcon from 'vue-material-design-icons/ArrowLeft.vue'
 
    let isPickuActive = ref(true)

</script>
  
  
  
<style lang="scss" scoped>
  #Directions {
    .bg-custom-color {
      background-color: rgb(237, 237, 237);
    }
    .circle-black {
        margin: 0 auto;
        width: 9px;
        height: 9px;
        background-color: black;
        border-radius: 100%;
    }
    
    .circle-gray {
        margin: 0 auto;
        width: 9px;
        height: 9px;
        background-color: rgb(191, 191, 191);
        border-radius: 100%;
    }
    .square-black {
        margin: 0 auto;
        width: 9px;
        height: 9px;
        background-color: black;
    }
    
    .square-gray {
        margin: 0 auto;
        width: 9px;
        height: 9px;
        background-color: rgb(191, 191, 191);
    }
    
    .line {
        margin: 0 auto;
        width: 2px;
        height: 45px;
        background-color: rgb(191, 191, 191);
    }
  }
</style>