<template>
  <div>
      <div>{{word}}</div>
      <div>
          <button>Positive</button>
          <button>Neutral</button>
          <button>Negative</button>
      </div>
  </div>
</template>

<script>
export default {
  name: 'WordPrompter',
  props: {
      word: String,
  },
  data () {
    return {
    }
  }
}
</script>

<style>

</style>
