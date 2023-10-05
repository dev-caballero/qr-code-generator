<template>
  <div>
    <ul class="grid grid-cols-4 gap-8 w-full">
      <li class="list-none" v-for="(url, index) in urls" :key="index">
        <QRCodeVue3
          :value="url.value"
          :width="2048"
          :height="2048"
          :dotsOptions="{ type: 'square' }"
          :qrOptions="{
            typeNumber: 4,
            mode: 'Byte',
            errorCorrectionLevel: 'H',
          }"
          :imageOptions="{
            hideBackgroundDots: true,
            imageSize: 0.4,
            margin: 8,
          }"
          :cornersDotOptions="{ type: undefined, color: '#000000' }"
          :cornersSquareOptions="{ type: 'square' }"
          :download="true"
          :downloadOptions="{ name: url.title, extension: 'png' }"
        />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import QRCodeVue3 from "qrcode-vue3";
const urls: { title: string; value: string }[] = [
  {
    title: "Example",
    value: "https://www.example.com",
  },
];
</script>

<style scoped></style>
