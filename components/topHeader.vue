<template>
  <header
    class="header-header w-full m-auto z-20 max-w-7xl fixed left-0 right-0"
  >
    <nav
      class="header-nav mt-5 bg-lime-600 bg-opacity-90 rounded-full py-5 px-10 m-20"
    >
      <navbar class="flex flex-row justify-between items-center">
        <div class="basis-1/4">ArqVision APP</div>
        <div>
          <ul class="flex gap-5">
            <li><a href="#">Quem Somos</a></li>
            <li><a href="#">Planos</a></li>
            <li><a href="#">Contatos</a></li>
          </ul>
        </div>
        <div>
          <button
            class="transition duration-150 ease-in-out bg-emerald-800 hover:bg-violet-500 p-3 rounded-full"
          >
            Assinar
          </button>
        </div>
      </navbar>
    </nav>
  </header>
</template>

<style lang="scss">
header {
  @apply text-cyan-50 text-lg;
}
li {
  @apply hover:text-emerald-800 transition duration-150 ease-in-out;
}
</style>
