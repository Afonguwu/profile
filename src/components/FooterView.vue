<script setup>
import { ref } from 'vue'
const personalLink = [
  {
    href: 'https://github.com/Afonguwu',
    name: 'GitHub',
    img: ['cactus01.png', 'cactus01-1.png'],
  },
  {
    href: 'https://www.cake.me/t225310917',
    name: 'Cake',
    img: ['cactus02.png', 'cactus02-1.png'],
  },
  {
    href: 'mailto:t225310917@gmail.com',
    name: 'Gmail',
    img: ['cactus03.png', 'cactus03-1.png'],
  },
]
let hoverImg = ref([0, 0, 0])

const showImg = (val) => {
  hoverImg.value[val] = 1
}

const hideImg = (val) => {
  hoverImg.value[val] = 0
  setTimeout(() => {
    hoverImg.value[val] = 0
  }, 300)
}
</script>
<style scoped>
a:hover p {
  color: #a98f78;
}
</style>
<template>
  <section class="bg-light footer" role="footer">
    <a
      v-for="(item, i) in personalLink"
      rel="noopener noreferrer"
      :key="i"
      :href="item.href"
      target="_blank"
      @touchstart="showImg(i)"
      @touchend="hideImg(i)"
      @mouseover="showImg(i)"
      @mouseleave="hideImg(i)"
    >
      <img :src="hoverImg[i] ? item.img[0] : item.img[1]" :alt="item.name" />
      <p class="text-blue-300 fw-b">{{ item.name }}</p>
    </a>
  </section>
</template>
