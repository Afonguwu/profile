<script setup>
import TimelineBtns from '@/components/TimelineBtns.vue'
</script>

<template>
  <div class="banner">
    <div>
      <h1 class="h1 heading-brown-200">PORTFOLIO</h1>
      <p class="h3 text-light">Dora Xie</p>
      <p class="h3 text-light">Front-end Engineer</p>
    </div>
  </div>
  <main>
    <section class="bg-light" role="introduction">
      <div class="introduction">
        <div class="img-block"><img src="https://fakeimg.pl/200x200/" alt="" /></div>
        <div>
          <h2 class="heading-dark h2-chinese mb-1">About</h2>
          <p class="text-blue-400 text lh-lg">
            我是 Dora，一個熱愛學習與探索新知的人，喜歡專注於細節並追求完美呈現。
            近期，我的目標是做到精雕細琢但不鑽牛角尖。平時我喜歡玩 RPG
            遊戲、做刺繡或畫插圖，這些興趣幫助我在閒暇時放鬆心情、激發靈感。未來，我希望能保持熱情與毅力，持續提升自己的能力與價值。
          </p>
        </div>
      </div>
    </section>
    <section class="bg-dark work">
      <h2 class="heading-brown-200 h2-chinese mb-1">Works</h2>
      <div>
        <TimelineBtns />
      </div>
      <div>
        <div class="bg-orange w-fit p-1 mb-1">
          <h2 class="heading-dark h3">專案名稱</h2>
          <p class="text-blue-300 fw-b">2024/01~2024/06</p>
        </div>
        <div>
          <div class="img-block">
            <figure>
              <img src="https://fakeimg.pl/100x80/" alt="" />
              <figcaption class="text-center">Desktop</figcaption>
            </figure>
            <figure>
              <img src="https://fakeimg.pl/100x80/" alt="" />
              <figcaption class="text-center">Pad</figcaption>
            </figure>
            <figure>
              <img src="https://fakeimg.pl/100x80/" alt="" />
              <figcaption class="text-center">Mobile</figcaption>
            </figure>
          </div>
          <div>
            <div class="mb-1">
              <h3 class="text-blue-400 fw-b">展示頁面</h3>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem facere alias cumque
                maiores aperiam. Dignissimos corrupti sit illum repellat nesciunt? Quod quae non,
                libero unde possimus accusamus. Doloribus, quia necessitatibus.
              </p>
            </div>
            <div class="mb-1">
              <h3 class="text-blue-400 fw-b">使用技術</h3>
              <p>
                Lorem ipsum dolor, sit amet consectetur adipisicing elit. Illo non necessitatibus
                dolorum, eveniet ratione beatae iure asperiores nemo et voluptates facere
                repellendus ducimus cupiditate laborum, ea architecto? Ullam, modi porro.
              </p>
            </div>
            <div class="mb-1">
              <h3 class="text-blue-400 fw-b">專案技術</h3>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Error corrupti
                exercitationem maiores labore molestiae quasi. Nisi, ad! Et delectus voluptatem
                omnis, recusandae dolores, quod deleniti dolorum in, nemo repellat consequatur!
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
  <section class="bg-light footer" role="footer">
    <div>
      <img src="https://fakeimg.pl/50x50/" alt="GitHub" />
      <p class="text-blue-200 fw-b">GitHub</p>
    </div>
    <div>
      <img src="https://fakeimg.pl/50x50/" alt="Cake" />
      <p class="text-blue-300 fw-b">Cake</p>
    </div>
    <div>
      <img src="https://fakeimg.pl/50x50/" alt="Gmail" />
      <p class="text-blue-400 fw-b">Gmail</p>
    </div>
  </section>
</template>
