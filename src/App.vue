<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<script lang="ts">
  export default {
    data: function(){
      return {
        count : 0,
        nama : "Andy"
      };
    },
    methods: {
      changeText(text) {
        this.nama = text;
      }
    } 
  }
</script>

<template>
  <header>
    <h1 v-on:click="changeText('Terserah')">{{ nama }}</h1>
    <!-- <div class="wrapper">
      <HelloWorld msg="nama" />
    </div> -->
  </header>

  <main>
    <!-- <TheWelcome /> -->
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
