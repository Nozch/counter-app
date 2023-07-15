<script>
import Counter from './components/Clock.vue'
export default {
  components: {
    Counter // Counterコンポーネントをローカルコンポーネントとして登録
  }
}
</script>
<template>
  <div id="app">
    <Counter /> <!-- ここでCounterコンポーネントを使用 -->
  </div>
</template>
