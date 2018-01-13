<template>
  <div id="app">
    <Topbar class="topbar" />
    <div class="main">
      <Editor class="editor" />
      <Preview class="preview"/>
    </div>
  </div>
</template>

<script>
import Topbar from './components/Topbar'
import Editor from './components/Editor'
import Preview from './components/Preview'
export default {
  components:{
    Topbar,Editor,Preview
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100vh;
  display: flex;
  flex-direction: column;
}
.icon {
  width: 1em; height: 1em;
  vertical-align: -0.15em;
  fill: currentColor;
  overflow: hidden;
}
.topbar{
  box-shadow: 0 0 3px rgba(0,0,0,.3);
  position: relative;
  z-index: 2;
}
.main{
  background: #efefef;
  display: flex;
  flex: 1;
  > .editor{
    background: #fff;
    width: 40em;
    margin: 16px 8px 16px 16px;
    box-shadow: 0 0 3px rgba(0,0,0,.3);
    border-radius: 3px;
    overflow: hidden;
  }
  > .preview{
    background: #fff;
    flex: 1;
    margin: 16px 16px 16px 8px;
    box-shadow: 0 0 3px rgba(0,0,0,.3);
    border-radius: 3px;
    overflow: hidden;
  }
}
</style>
