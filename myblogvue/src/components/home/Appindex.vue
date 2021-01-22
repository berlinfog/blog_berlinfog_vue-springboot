<template>
  <div class="main markdown-body">
  <div v-html="htms"></div>
  </div>
</template>

<script>
import showdown from "showdown"
import readme from "../../1.md"
let converter = new showdown.Converter();
converter.setOption('tables', true);  // 将表格显示出来
  export default {
    name: 'AppIndex',
    data() {
    return {
      htms: ""
    }
  },
  created() {
    this.setMakedown()
  },
  methods: {
    setMakedown() {
     this.htms = converter.makeHtml(readme)
    }
  }
  }
</script>

<style scoped>

  .markdown-body {
    box-sizing: border-box;
    min-width: 200px;
    max-width: 980px;
    margin: 0 auto;
    padding: 45px;
    text-align:left;
}

@media (max-width: 767px) {
    .markdown-body {
        padding: 15px;
    }
}
</style>

