<script setup lang="ts">
import renderTest from './components/renderTest.vue'
import { render, h,ref } from 'vue'


const renderBtn = () => {
  const test = document.querySelector('.test')
  test != null && test.remove()
  render(h(renderTest), document.body)
  count.value+=1
}
const info=ref<string>('激活')
const count=ref<number>(0)

</script>

<template>
  <button @click="renderBtn">{{ info}}</button>
  <div>第{{ count}}次render</div>
</template>

<style scoped>
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
