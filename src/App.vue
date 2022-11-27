<template>
  <div id="app">
    <main>
      <div class="navigation">
      <header>
        <h1>Xudoyberdi</h1>
      </header>
      <nav>
          <a href="#">About us</a>
          <a href="#">Contact</a>
          <a href="#">Portfolio</a>
        </nav>
      </div>
      <ProgressBar :progress="progress"/>
      <Post @progresUpdate="setProgress" />
    </main>
    
  </div>
</template>

<script>
import Post from '@/components/Post.vue'
import ProgressBar from '@/components/ProgressBar.vue'
export default {
  name: 'App',
  components: {
    Post,
    ProgressBar
  },
  data(){
    return {
      progress: 0
    }
  },
  methods:{
    setProgress(progress){
      this.progress=progress
    }
  }
}
</script>

<style >
*{
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  font-family: 'monospace', sans-serif;
  overflow: hidden;
}
main {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  overflow: hidden;
}
.navigation{
  width: 100%;
  height: 10vh;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: rgb(12, 42, 216);
  padding: 30px;
  
}
header h1{
  color: #fff;
  font-size: 32px;
}
nav a{
  margin: 0 20px;
  text-transform: uppercase;
  text-decoration: none;
  color: #fff;
}
</style>
