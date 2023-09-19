<template>
  <div>
    <ul class="grid grid-cols-4 gap-8 w-full">
      <li class="list-none" v-for="(url, index) in urls" :key="index">
        <QRCodeVue3 :value="url.value" :width="2048" :height="2048" :dotsOptions="{ type: 'square' }"
          :qrOptions="{ typeNumber: 16, mode: 'Byte', errorCorrectionLevel: 'H' }"
          :imageOptions="{ hideBackgroundDots: true, imageSize: 0.4, margin: 0 }"
          :cornersDotOptions="{ type: undefined, color: '#000000' }" :cornersSquareOptions="{ type: 'square' }"
          :download="true" :downloadOptions="{ name: url.title, extension: 'png' }" />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import QRCodeVue3 from "qrcode-vue3";

const urls: { title: string, value: string }[] = [
  { title: "Master Class Abordaje Multidisciplinario de la obesidad", value: 'https://suacademiamedica.novonordisk.com.co/educacion-medica/master-class-dr-martin-vasquez-abordaje-integral-de-la-obesidad.html', },
  { title: "Master Class Abordaje Integral de la obesidad", value: 'https://suacademiamedica.novonordisk.com.co/educacion-medica/master-class-dr-martin-vasquez-abordaje-integral-de-la-obesidad.html', },
  { title: "Master Class Obesidad y Salud Femenina", value: 'https://suacademiamedica.novonordisk.com.co/educacion-medica/master-class-dra-ivonne-diaz-obesidad-y-salud-femenina.html', },
  { title: "Mas que peso", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/mas-que-peso.html', },
  { title: "Master Class Abordaje del niño que sangra", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dr-Jimmy-lagos-abordaje-del-nino-que-sangra.html', },
  { title: "Master Class Abordaje de los desordenes del crecimiento y su tratamiento", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dr-juan-pablo-llano-abordaje-de-los-desordenes-de-crecimiento-y-su-tratamiento.html', },
  { title: "Sangrado ginecologico de origen hematologico", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dra-claudia-agudelo-dra-liliana-correa-abordaje-desde-la-hematologia-de-los-sangrados-ginecologicos.html', },
  { title: "Curso de Artropatía Hemofílica", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/curso-salud-articular-en-hemofilia.html', },
  { title: "Venciendo los primeros obstáculos al trascender al mundo digital", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/Venciendo-los-primeros-obstaculos-al-trascender-al-mundo-digital.html', },
  { title: "Evolución de un líder digital", value: 'https://suacademiamedica.novonordisk.com.co/landing-contenidos/evolucion-de-un-lider-de-opinion-digital-y-de-la-marca-profesional-medica.html', },
  { title: "Tendencias y dinamismo en el contenido digital de mi práctica médica", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/landing-contenidos/tendencias-y-dinamismo-en-el-contenido-digital-de-mi-practica-medica.html', },
  { title: "Master Class Manejo personalizado del paciente con diabetes mellitus tipo 2", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dr-edwin-wandurraga-manejo-personalizado-del-paciente-con-diabetes-mellitus-tipo-2.html', },
  { title: "Master Class Manejo de la diabetes Tipo 2", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dr-miguel-omeara-ideglira-en-el-manejo-de-la-diabetes-tipo-2.html', },
  { title: "Master Class Tratamiento del paciente con diabetes tipo 2", value: 'https://suacademiamedica.novonordisk.com.co/content/hcpexperience/co/es_co/educacion-medica/master-class-dra-ana-maria-gomez-intensificacion-de-la-terapia-en-el-paciente-con-diabetes-tipo-2-insulinizado.html', },
  { title: "Red Talks", value: 'https://suacademiamedica.novonordisk.com.co/educacion-medica/red-talks.html', },
  { title: "Directo al corazón de la diabetes", value: 'https://suacademiamedica.novonordisk.com.co/educacion-medica/directo-al-corazon.html', },
];

</script>

<style scoped></style>