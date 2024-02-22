<template>
  <main>
    nav
    <div class="container mx-auto">
      <div class="font-sans text-5xl font-semibold p-3 block text-center">
        A utility-first CSS framework for
        <span class="text-teal-500">rapidly building custom designs.
        </span>
      </div>
      <div>
        <p class="text-slate-600 text-xl text-center">
          Tailwind CSS is a highly customizable, low-level CSS framework that gives you all of the building blocks you
          need to build bespoke designs without any annoying opinionated styles you have to fight to override.
        </p>
      </div>
      <div class="p-2 flex justify-center">
        <button class="bg-teal-500 hover:bg-teal-600 text-white font-bold py-3 px-4 rounded shadow-md mx-2">
          Get Started
        </button>
        <button class="bg-white hover:bg-gray-100 text-black font-semibold py-3 px-4 rounded shadow-md mx-2">
          Why Tailwind?
        </button>
      </div>
    </div>
  </main>
</template>

<script setup>
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
