<script>
import Counter from './components/Counter.vue' // あなたのCounterコンポーネントがあるパスに適宜変更してください

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
