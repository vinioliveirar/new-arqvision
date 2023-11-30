<template>
  <section
    class="relative max-w-7xl w-full flex justify-center items-center m-auto"
  >
    <div class="features flex flex-col lg:flex-row gap-4">
      <div
        class="rounded-xl gap-4 p-5 my-40 border flex flex-col justify-between text-center"
        v-for="(feature, index) in features"
        :key="index"
      >
        <span><component :is="feature.icon" v-bind="feature.iconProps" /></span>
        <h3 class="text-2xl text-purple-500">{{ feature.title }}</h3>
        <p>{{ feature.description }}</p>
      </div>
    </div>
  </section>

  <section class="bg-slate-500 flex justify-center">
    <blockquote
      class="py-20 text-2xl font-semibold italic text-center text-slate-900"
    >
      Com o APP
      <span
        class="before:block before:absolute before:-inset-1 before:-skew-y-3 before:bg-lime-600 relative inline-block"
      >
        <span class="relative text-white">ARQVISION</span>
      </span>
      você terá maior facilidade na hora de realizar a reunião com seu cliente.
    </blockquote>
  </section>
</template>

<script setup lang="ts">
const features = reactive([
  {
    icon: shallowRef("Icon"),
    iconProps: { name: "mingcute:cube-3d-line", size: "40", color: "black" },
    title: "Visualização em 3D Imersiva",
    description:
      "Explore designs detalhados em 3D com uma experiência imersiva e realista.",
  },
  {
    icon: shallowRef("Icon"),
    iconProps: {
      name: "mdi:file-cad-box",
      size: "40",
      color: "black",
    },
    title: "Compatibilidade com Principais Softwares de Design",
    description:
      "Integração perfeita com softwares como Promob, AutoCAD e outros.",
  },
  {
    icon: shallowRef("Icon"),
    iconProps: { name: "teenyicons:share-solid", size: "40", color: "black" },
    title: "Facilidade de Compartilhamento e Colaboração",
    description:
      "Compartilhe projetos com clientes e colegas de equipe de forma rápida e eficaz.",
  },
  {
    icon: shallowRef("Icon"),
    iconProps: { name: "mdi:design", size: "40", color: "black" },
    title: "Personalização de Ambientes e Móveis",
    description:
      "Customize ambientes e experimente diferentes opções de mobiliário.",
  },
]);
</script>

<style></style>
