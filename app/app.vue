<script setup lang="ts">
// const style = "https://api.maptiler.com/maps/streets/style.json?key=cQX2iET1gmOW38bedbUh"
const style = "https://demotiles.maplibre.org/style.json"
</script>

<template>
  <div class="flex h-svh w-screen">
    <div id="actual-page">
      <MglMap
        :map-style="style"
        :center="[-13, 9]"
        :zoom="3"
      >
        <MglFullscreenControl />
        <MglNavigationControl />
        <MglGeolocateControl />
        <MglScaleControl />

        <MglMarker :coordinates="[-13.6, 9.6004923]" color="#cc0000" draggable>
          <mgl-popup>
            <h1 class="text-black">
              Hello
            </h1>
          </mgl-popup>
        </MglMarker>
      </MglMap>
    </div>
  </div>
</template>

<style>
#actual-page {
  width: 100%;
}

#actual-page > div {
  height: 100%;
}
</style>
