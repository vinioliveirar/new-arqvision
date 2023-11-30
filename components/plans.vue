<template>
  <header
    class="w-full text-center m-auto z-20 max-w-7xl absolute left-0 right-0"
  >
    <h2 class="text-lime-600 font-bold text-4xl py-4">
      Confira nossos planos:
    </h2>
  </header>
  <div class="flex justify-center items-center mt-20 py-10">
    <div
      v-for="(plan, index) in plans"
      :key="index"
      :class="{
        'max-w-xs rounded-xl  mx-4': true,
        'bg-blue-100 ': plan.name === 'Plano Premium',
        'bg-white': plan.name !== 'Plano Premium',
      }"
    >
      <div class="rounded-xl flex flex-col justify-between shadow-lg p-6">
        <h3 class="text-3xl text-center font-semibold mb-2 py-2">
          {{ plan.name }}
        </h3>
        <p class="text-gray-600 mb-4 text-center">R${{ plan.price }}</p>
        <ul class="text-sm mb-4">
          <li
            v-for="(benefit, idx) in plan.benefits"
            :key="idx"
            class="flex items-center"
          >
            <component
              :is="benefit.icon"
              :key="idx"
              v-bind="benefit.iconProps"
            ></component>
            {{ benefit.text }}
          </li>
        </ul>
        <button
          @click="contratar(plan)"
          class="block w-full bg-blue-500 hover:bg-blue-600 text-white font-semibold py-2 px-4 rounded focus:outline-none focus:ring focus:border-blue-300"
        >
          Contratar
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import { reactive } from "vue";

const features = reactive([
  {
    icon: "Icon",
    iconProps: { name: "material-symbols:check", size: "40", color: "black" },
  },
  {
    icon: "Icon",
    iconProps: { name: "ph:x", size: "40", color: "black" },
  },
  // Adicione mais objetos de recursos conforme necessário
]);

export default {
  data() {
    return {
      plans: [
        {
          name: "Plano Beta",
          price: " 99,99/mês",
          benefits: [
            {
              text: "Visualização em 3D",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Integração com softwares de design",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Compartilhamento de projetos",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Suporte técnico básico",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Personalização avançada de ambientes",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },

            // Adicione outros benefícios e ícones conforme necessário para o Plano Beta
          ],
        },
        {
          name: "Plano Premium",
          price: " 199,99/mês",
          benefits: [
            {
              text: "Todos os benefícios do Plano Beta +",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Personalização avançada de ambientes",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Renderização de alta qualidade",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Suporte prioritário ao cliente",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            {
              text: "Integração com ferramentas de gestão",
              icon: features[0].icon,
              iconProps: features[0].iconProps,
            },
            // Adicione outros benefícios e ícones conforme necessário para o Plano Premium
          ],
        },
      ],
    };
  },
  methods: {
    contratar(plan) {
      // Lógica para contratar o plano selecionado
      console.log(`Contratando ${plan.name}...`);
      // Aqui você pode adicionar a lógica para contratar o plano selecionado
    },
  },
};
</script>

<style>
/* Estilo de fundo do Plano Premium */
.bg-blue-100 {
  background-color: #ebf8ff; /* Cor de fundo do Plano Premium */
}
</style>
