<template>
  <div id="app" class="p-40 text-center flex items-center flex-col gap-10">
    <h3>Dúvidas frequentes</h3>
    <div class="accordion">
      <div class="accordion-item" v-for="item in faq" :key="item.id">
        <div class="accordion-header" @click="toggle(item.id)">
          {{ item.question }}
        </div>
        <div class="accordion-body" v-show="item.open">
          {{ item.answer }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      faq: [
        {
          id: 1,
          question:
            "O que é o APP de Realidade Aumentada para profissionais de design de interiores?",
          answer:
            "O APP de Realidade Aumentada para profissionais de design de interiores é uma ferramenta inovadora que permite aos profissionais criar e apresentar seus projetos de forma interativa e realista. Com o APP, você pode inserir seus projetos em qualquer ambiente, usando a câmera do seu smartphone ou tablet, e mostrar aos seus clientes como ficaria o resultado final.",
          open: false,
        },
        {
          id: 2,
          question:
            "Quais são os benefícios de usar o APP de Realidade Aumentada para profissionais de design de interiores?",
          answer:
            "O APP de Realidade Aumentada para profissionais de design de interiores oferece diversos benefícios, tais como:\n\n- Aumentar a satisfação e a confiança dos seus clientes, ao permitir que eles visualizem e experimentem seus projetos em tempo real.\n- Reduzir o tempo e o custo de produção e revisão dos seus projetos, ao facilitar as alterações e os ajustes necessários.\n- Diferenciar-se da concorrência, ao oferecer um serviço de alta qualidade e tecnologia de ponta.",
          open: false,
        },
        {
          id: 3,
          question:
            "Quais são os planos disponíveis para o APP de Realidade Aumentada para profissionais de design de interiores?",
          answer:
            "O APP de Realidade Aumentada para profissionais de design de interiores possui dois planos: o plano **beta** e o plano **premium**.\n\nO plano beta é gratuito e permite que você crie e apresente até 10 projetos por mês, com até 5 objetos por projeto. Você também pode acessar uma biblioteca limitada de objetos e materiais para compor seus projetos.\n\nO plano premium é pago e permite que você crie e apresente projetos ilimitados, com até 20 objetos por projeto. Você também pode acessar uma biblioteca completa de objetos e materiais para compor seus projetos, além de recursos exclusivos como a personalização de cores, texturas e iluminação.",
          open: false,
        },
        {
          id: 4,
          question:
            "Como faço para adquirir o plano premium do APP de Realidade Aumentada para profissionais de design de interiores?",
          answer:
            "Para adquirir o plano premium do APP de Realidade Aumentada para profissionais de design de interiores, você precisa acessar o site do APP e clicar em [Assinar agora]. Você será redirecionado para uma página de pagamento, onde poderá escolher a forma de pagamento e o período de assinatura (mensal ou anual). Após confirmar o pagamento, você receberá um e-mail com as instruções para ativar o seu plano premium no APP.",
          open: false,
        },
        {
          id: 5,
          question:
            "Como faço para cancelar o plano premium do APP de Realidade Aumentada para profissionais de design de interiores?",
          answer:
            "Você pode cancelar o plano premium do APP de Realidade Aumentada para profissionais de design de interiores a qualquer momento, sem multas ou taxas. Para isso, você precisa acessar o site do APP e clicar em [Minha conta]. Você verá uma opção para cancelar o seu plano premium. Após confirmar o cancelamento, você receberá um e-mail com a confirmação e o prazo para o encerramento do seu plano premium. Você poderá continuar usando o APP no plano beta até o final do período pago.",
          open: false,
        },
      ],
    };
  },
  methods: {
    toggle(id) {
      this.faq.forEach((item) => {
        if (item.id === id) {
          item.open = !item.open;
        } else {
          item.open = false;
        }
      });
    },
  },
};
</script>

<style>
.accordion {
  width: 600px;
  margin: 0 auto;
  border: 1px solid #ccc;
}

.accordion-item {
  border-bottom: 1px solid #ccc;
}

.accordion-header {
  padding: 10px;
  cursor: pointer;
  font-weight: bold;
}

.accordion-body {
  padding: 10px;
}
</style>
