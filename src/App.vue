<template>
  <div id="app">
    <h1>{{ msg }}</h1>
    <WordPrompter v-for="word in words" :key='word' :word='word' />
    <div>
        <WordList />
        <WordList />
        <WordList />
    </div>
  </div>
</template>

<script>
import words from '../words.js';
import WordPrompter from './WordPrompter';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Select Which Applies for The Following Values',
      words,
      positives: [],
      neutrals: [],
      negatives: [],
    }
  },
  components: {
      WordPrompter
  }

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
