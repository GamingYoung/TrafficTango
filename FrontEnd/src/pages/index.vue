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

<style scoped>
.container {
  display: flex;
  max-width: 100%;
  height: 100%;
  margin: 0;
}

.left-side {
  flex: 3;
  display: flex;
  margin: 0;
  flex-direction: column;
}

.right-side {
  flex: 1;
  background-color: green;
  margin: 0;
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
