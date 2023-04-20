<template>
    <div id="MapView">
        <div id="map"></div>

        <div id="VehicleSelection" class="w-full">
            <div class="w-full h-2 border-t"></div>
            <div class="w-full text-center border-t-2 p-1.5 text-gray-700 text-lg font-semibold">
                <span>Distance - 65</span>
            </div>

            <div class="scrollSection">
                <div class="bg-custom-gray">
                    <div class="flex items-center px-4 py-5">
                        <img src="img/uber/ride.png" alt="ride" width="75">
                        <div class="w-full ml-3">
                            <div class="flex items-center justify-between">
                                <div class="text-2xl mb-1">UberX</div>
                                <div class="text-xl">R$ 55,42</div>
                            </div>
                            <div class="text-gray-500">7 hours</div>
                        </div>
                    </div>
                </div>

                <div class="">
                    <div class="flex items-center px-4 py-5">
                        <img src="img/uber/ride.png" alt="ride" width="75">
                        <div class="w-full ml-3">
                            <div class="flex items-center justify-between">
                                <div class="text-2xl mb-1">UberX</div>
                                <div class="text-xl">R$ 55,42</div>
                            </div>
                            <div class="text-gray-500">7 hours</div>
                        </div>
                    </div>
                </div>

                <div class="">
                    <div class="flex items-center px-4 py-5">
                        <img src="img/uber/ride.png" alt="ride" width="75">
                        <div class="w-full ml-3">
                            <div class="flex items-center justify-between">
                                <div class="text-2xl mb-1">UberX</div>
                                <div class="text-xl">R$ 55,42</div>
                            </div>
                            <div class="text-gray-500">7 hours</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script setup>
import { onMounted } from 'vue'

onMounted(() => {
    setTimeout(() => {
        initMap();
    }, 50)
})

const initMap = () => {
    const map = new window.google.maps.Map(document.getElementById("map"), {
        center: { lat: -8.0822671, lng: -34.8332708 },
        zoom: 8,
        fullscreenControl: false,
        zoomControl: false,
        mapTypeControl: false,
        streetViewControl: false,
    });
    console.log(map)
}

</script>
  
<style lang="scss">
#MapView {

    #map {
        width: 100%;
        height: 45vh;
        top: 0px;
        left: 0px;
    }

    .gm-style-cc {
        display: none;
    }

    .bg-custom-gray {
        background-color: rgb(237, 237, 237);
    }

    #VehicleSelection {
        .scrollSection {
            height: calc(50vh - 120px);
            position: absolute;
            overflow-y: auto;
            width: 100%;
        }
    }

}
</style>




