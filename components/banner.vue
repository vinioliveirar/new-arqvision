<template>
  <section class="relative w-full h-screen">
    <div
      class="container flex content-center items-center h-full pt-40 w-full m-auto justify-center"
    >
      <div class="card">
        <h1>{{ title }}</h1>
        <p>{{ paragraph }}</p>
        <button>{{ cta }}</button>
      </div>
    </div>
    <div>
      <img
        src="../img/please 29.jpg"
        alt="bg"
        class="absolute w-full h-screen right-0 top-0 rounded-bl-[30%] -z-10"
      />
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "Tudo em um só lugar",
      paragraph:
        "Sabemos que os profissionais de design de interiores têm uma variedade de tarefas manuais e ferramentas dispersas em seu dia a dia. É por isso que criamos o ARQVISION para simplificar sua vida profissional.",
      cta: "Saiba mais",
    };
  },
};
</script>

<style lang="scss">
$background: #e0e0e0;
$card-color: rgba(255, 255, 255, 0.1);
$blur: 20px;
$border: 1px solid rgba(255, 255, 255, 0.2);

img {
  /* position: absolute;
  background-image: cover;
  width: 100%;
  height: 100vh;
  right: 0;
  top: 0;
  border-radius: 0 0 0 30%;
  z-index: -1; */
}
.card {
  width: 50%;
  position: relative;
  background: $card-color;
  backdrop-filter: blur($blur);
  border: $border;
  border-radius: 20px;
  padding: 30px;
  margin: 50px 0 !important;
  box-shadow: 10px 10px 30px rgba(0, 0, 0, 0.1);
  text-align: center;

  h1 {
    color: white;
    font-size: 42px;
    text-transform: uppercase;
    margin-bottom: 10px;
  }

  p {
    color: white;
    font-size: 16px;
    margin-bottom: 20px;
  }

  button {
    width: 150px;
    height: 40px;
    background: $card-color;
    border: $border;
    border-radius: 10px;
    color: white;
    font-size: 18px;
    cursor: pointer;
    transition: transform 0.3s;

    &:hover {
      transform: scale(1.1);
    }
  }
}
</style>
