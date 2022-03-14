<script setup>
import { Icon } from "@iconify/vue";
</script>

<template>
  <div
    class="text-gray-700 w-screen h-screen border justify-center items-center"
  >
    <header>
      <div class="text-6xl">Fookie JS</div>
      <div class="text-2xl">Model based reactive javascript framework.</div>
      <div>
        <a href="https://github.com/fookiejs/core">
          <button class="flex justify-center items-center">
            <Icon icon="akar-icons:github-fill" height="32"> </Icon>
            <div class="w-1"></div>
            <span>Github</span>
          </button>
        </a>
        <a href="https://github.com/fookiejs/core">
          <button class="flex justify-center items-center">
            <Icon icon="cib:postman" height="32"> </Icon>
            <div class="w-1"></div>
            <span>Postman</span>
          </button>
        </a>
        <a href="https://github.com/fookiejs/core">
          <button class="flex justify-center items-center">
            <Icon icon="simple-icons:githubpages" height="32"> </Icon>
            <div class="w-1"></div>
            <span>Github Pages</span>
          </button>
        </a>
      </div>
    </header>
    <main>
      <div class="text-4xl">Utils</div>
      <div class="">
        <a class="text-2xl" href="https://ui.fookiejs.com">
          <div>UI</div>
        </a>
        <a class="text-2xl" href="https://doc.fookiejs.com">
          <div>DOC</div>
        </a>
      </div>
    </main>
  </div>
</template>

<style>
</style>
