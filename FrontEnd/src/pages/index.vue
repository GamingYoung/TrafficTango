<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: 'IndexPage',
})

const name = ref('')

const router = useRouter()
function go() {
  if (name.value)
    router.push(`/hi/${encodeURIComponent(name.value)}`)
}

</script>

<template>
<!--  <div>-->
<!--    <div i-carbon-campsite inline-block text-4xl />-->
<!--    <p>-->
<!--      <a rel="noreferrer" href="https://github.com/antfu/vitesse-lite" target="_blank">-->
<!--        Vitesse Lite-->
<!--      </a>-->
<!--    </p>-->
<!--    <p>-->
<!--      <em text-sm op75>Opinionated Vite Starter Template</em>-->
<!--    </p>-->

<!--    <div py-4 />-->

<!--    <TheInput-->
<!--      v-model="name"-->
<!--      placeholder="What's your name?"-->
<!--      autocomplete="false"-->
<!--      @keydown.enter="go"-->
<!--    />-->

<!--    <div>-->
<!--      <button-->
<!--        class="m-3 text-sm btn"-->
<!--        :disabled="!name"-->
<!--        @click="go"-->
<!--      >-->
<!--        Go-->
<!--      </button>-->
<!--    </div>-->
<!--  </div>-->
  <div class="container">
    <div class="left-side">
      <div class="top-section">
        <!-- 上方内容 -->
        1
      </div>
      <div class="bottom-section">
        <!-- 下方内容 -->
        1
      </div>
    </div>
    <div class="right-side">
      <!-- 右侧内容 -->
      1
    </div>
  </div>
</template>

<style>
.container {
  display: flex;
  height: 100%;
  width: 100%;
}

.left-side {
  flex: 3;
  display: flex;
  flex-direction: column;
}

.right-side {
  flex: 1;
  background-color: green;
}

.top-section {
  flex: 3;
  background-color: white;
}

.bottom-section {
  flex: 1;
  background-color: bisque;
}
</style>
