<script setup>
import TimelineBtns from '@/components/TimelineBtns.vue'
import FooterView from '@/components/FooterView.vue'
import { ref } from 'vue'
const projectData = ref([
  /*example*/
  /* {
    num: ,
    workName: '',
    time: '',
    thoughts: '',
    pages: [],
    skills: [],
    githubUrl: '',
    pagesUrl: '',
  },  */
  {
    num: 0,
    workName: 'ThinkUpTogether小說網站',
    time: '2023 / 07 - 2023 / 10',
    thoughts:
      '這是一個團體協作專案，因喜愛讀小說，我們萌生了創建一個小說網站的想法，讓用戶既能瀏覽小說，又能在論壇中交流和創作。專案過程中，我們使用便利貼法篩選核心功能，但遇到技術瓶頸和組員興趣減少的挑戰。這段經歷教會了我有效溝通和資源協調，並提升了我的靈活性和適應力。',
    pages: [
      '首頁：最新消息、熱門書籍展示、熱門留言展示',
      '搜尋頁面：類別搜尋、文字搜尋',
      '登入按鈕：登入功能切換、討論區',
      '討論區：討論文章展示、發文按鈕、查看文章留言',
    ],
    skills: [
      '專案的初期階段，使用便利貼法來發想和篩選網站的核心功能',
      'Miro 繪製網站地圖、線框圖',
      'Vite、Scss、Bootstrap 5 開發前端網頁',
      '多人協作專案，使用 Git Merge 管控版本',
      '匯入 CKEditor 5 文字編輯器',
    ],
    githubUrl: 'https://github.com/Afonguwu/frontend',
    pagesUrl: 'https://afonguwu.github.io/frontend/',
    showUrl: [{ url: '/TUT-pc.gif', name: 'Desktop' }],
  },
  {
    num: 1,
    workName: '律師事務所網站',
    time: ' 2024 / 04 - 2024 / 06',
    thoughts:
      '從身邊的事物中獲得靈感，自小受到長輩的關愛，我希望在自己能力所及的範圍內回報他們。由於長輩的公司自成立以來一直沒有網站或其他對外宣傳管道，因此我希望通過製作一個網站，為公司的曝光率和形象提升做出貢獻。',
    pages: [
      '首頁：服務總攬、團隊總攬、品牌簡介、辦公室招租簡介',
      '服務項目：服務詳細說明',
      '律師團隊：律師圖卡展示',
      '律師個人頁面：律師個人詳細資訊',
      '聯絡我們：品牌聯絡資訊',
      '合署資訊：辦公室招租資訊',
    ],
    skills: [
      'Figma 繪製線框圖',
      'Vue.js、Scss、Bootstrap 5 開發前端網頁',
      'Vue Router 管理路由',
      'AOS、Swiper、C3.js 增加網頁視覺效果',
      'GitHub Actions 部屬 GitHub Pages',
    ],
    githubUrl: 'https://github.com/Afonguwu/wisdom-win-vite',
    pagesUrl: 'https://afonguwu.github.io/wisdom-win-vite/#/',
    showUrl: [
      { url: '/winsdom-pc.gif', name: 'Desktop' },
      { url: '/winsdom-pad.gif', name: 'Pad' },
      { url: '/winsdom-mobile.gif', name: 'Mobile' },
    ],
  },
  {
    num: 3,
    workName: '高雄捷運輕軌地圖',
    time: ' 2024 / 09 - 2024 / 10',
    thoughts: '實作 SVG 元素結合資料串接',
    pages: ['高雄捷運輕軌地圖：顯示票價、顯示乘車時間、票種切換'],
    skills: [
      'Whimsical 繪製邏輯流程圖',
      'Vue.js、Scss、Bootstrap 5 開發前端網頁',
      'SVG 製作路線圖',
      'Vue Router 管理路由',
      'Pinia 管理資料狀態及串接資料模塊',
      'GitHub Actions 部屬 GitHub Pages',
    ],
    githubUrl: 'https://github.com/Afonguwu/tool-box',
    pagesUrl: 'https://afonguwu.github.io/tool-box/#/',
    showUrl: [
      { url: '/trainmap-pc.gif', name: 'Desktop' },
      { url: '/trainmap-mobile.gif', name: 'Mobile' },
    ],
  },
])
let targetValue = ref(2)
const changeTarget = (val) => {
  targetValue.value = val
}

const isOpen = ref(false)
const currentImage = ref('')

const openImage = (event) => {
  currentImage.value = event.target.src
  isOpen.value = true
}

const closeImage = () => {
  isOpen.value = false
}
</script>
<style scoped>
.thumbnail {
  width: 200px;
  cursor: pointer;
  transition: transform 0.2s;
}

.thumbnail:hover {
  transform: scale(1.1);
}

.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  padding: 2rem;
}

.full-size {
  max-width: 100vw;
  max-height: 100vh;
  border-radius: 10px;
}
</style>
<template>
  <div class="banner">
    <div>
      <h1 class="h1 text-brown-200">PORTFOLIO</h1>
      <p class="h2 text-light">Tsan-Ju Xie</p>
      <p class="h2-chinese text-light">謝璨如</p>
    </div>
  </div>
  <main>
    <section class="bg-light" role="introduction">
      <h2 class="heading-dark h2-chinese">About</h2>
      <div class="introduction">
        <div class="img-block"><img src="/headshot.png" alt="headshot" /></div>
        <div class="text-block">
          <p class="text-blue-400 text lh-lg">
            我是璨如，疫情期間透過線上體驗課程接觸到前端工程師這個領域，並深深喜愛上參與網頁從無到有的創造過程。
            我是一個熱愛學習與探索新知的人，喜歡專注於細節，追求完美呈現。近期，我的目標是做到精雕細琢但不鑽牛角尖。
            <br />平時，我喜歡玩 RPG
            遊戲、做刺繡或畫插圖，這些興趣不僅讓我放鬆心情，也時常激發靈感。未來，我希望能保持熱情與毅力，持續提升自己的能力與價值。
          </p>
        </div>
      </div>
    </section>
    <section class="bg-dark work">
      <h2 class="text-brown-200 h2-chinese mb-1">Works</h2>
      <div>
        <TimelineBtns @change-event="changeTarget" :dotValue="targetValue" />
      </div>
      <div>
        <div class="bg-orange w-fit p-1 mb-1">
          <h2 class="heading-dark h3 text-nowrap">{{ projectData[targetValue].workName }}</h2>
          <p class="text-blue-300 fw-b">{{ projectData[targetValue].time }}</p>
        </div>
        <div>
          <div class="workInfo">
            <div>
              <h3 class="text-blue-400 fw-b mb-1">頁面效果展示</h3>
              <div class="img-block">
                <figure v-for="(item, i) in projectData[targetValue].showUrl" :key="i">
                  <img :src="item.url" :alt="item.name" class="mb-1 thumbnail" @click="openImage" />
                  <figcaption class="text-center mb-1 text-blue-200">{{ item.name }}</figcaption>
                  <div v-if="isOpen" class="overlay" @click="closeImage">
                    <img :src="currentImage" class="full-size" />
                  </div>
                </figure>
              </div>
            </div>
            <div class="mb-2">
              <div class="mb-1">
                <h3 class="text-blue-400 fw-b mb-1">專案發想</h3>
                <p>
                  {{ projectData[targetValue].thoughts }}
                </p>
              </div>
              <div class="mb-1">
                <h3 class="text-blue-400 fw-b mb-1">網站頁面</h3>
                <p
                  class="mb-s"
                  v-for="(page, index) in projectData[targetValue].pages"
                  :key="index"
                >
                  {{ page }}
                </p>
              </div>
              <div class="mb-1">
                <h3 class="text-blue-400 fw-b mb-1">使用技術</h3>
                <p
                  class="mb-s"
                  v-for="(skill, index) in projectData[targetValue].skills"
                  :key="index"
                >
                  {{ skill }}
                </p>
              </div>
            </div>
          </div>
          <div class="btn-group">
            <a
              type="button"
              class="btn-light fw-b mr-1"
              :href="projectData[targetValue].githubUrl"
              target="_blank"
              >GitHub</a
            >
            <a
              type="button"
              class="btn-dark fw-b"
              :href="projectData[targetValue].pagesUrl"
              target="_blank"
              >Pages</a
            >
          </div>
        </div>
      </div>
    </section>
  </main>
  <FooterView />
</template>
