<template>
  <div class="w-full m-auto max-w-7xl grid grid-cols-2 gap-4 pt-20">
    <div>
      <img
        src="../img/img-about.jpeg"
        alt="Design de interiores"
        class="img-fluid rounded-2xl"
      />
    </div>
    <div>
      <h2 class="text-4xl py-5 text-center text-gray-600">Sobre a Arqvision</h2>
      <p>
        A Arqvision é uma empresa especializada em soluções de realidade
        aumentada para profissionais de design de interiores. Com o nosso APP,
        você pode criar e apresentar seus projetos de forma interativa e
        realista, usando a câmera do seu smartphone ou tablet. Você também pode
        acessar uma biblioteca completa de objetos e materiais para compor seus
        projetos, além de recursos exclusivos como a personalização de cores,
        texturas e iluminação.
      </p>
      <p>
        Se você quer levar o seu trabalho para o próximo nível, conheça os
        nossos planos e assine já o nosso APP. Você vai se surpreender com os
        resultados que pode alcançar com a nossa tecnologia.
      </p>
      <a href="^2^" class="btn btn-primary">Saiba mais</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
/* .container {
  width: 600px;
  margin: 0 auto;
  border: 1px solid #ccc;
} */

.row {
  display: flex;
  flex-wrap: wrap;
}

.col-md-6 {
  flex: 0 0 50%;
  max-width: 50%;
}

.img-fluid {
  width: 100%;
  height: auto;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  color: white;
  background-color: blue;
  border: none;
  text-decoration: none;
}

.btn:hover {
  background-color: darkblue;
}
</style>
