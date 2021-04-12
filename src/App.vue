<template>
  <div class="app">
    <div class="vertical-centered">
      <div v-for="(oneBox, index) in boxes" :key="index">
        <Box :box="oneBox"/>
    </div>
      <div class="button" @click="addBox">
        Add a box
      </div>
    </div>
  </div>
</template>

<script>
import Box from './components/Box'
export default {
  name: 'App',
  components: {
    Box
  },
  data(){ 
    return {
      boxes: [{ name: 'marketplace' }],
    }
  },
  methods: {
    addBox() {
      let name = 'crowdfunding';
      if (this.boxes.length %2 === 0){
        name = 'marketplace'
      }
      this.boxes.push({name: name});
    }
  }
}
</script>

<style>

@import url(https://fonts.googleapis.com/css?family=Roboto:300,400,500,700);

body {
  min-height: 100vh;
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f0f3f7;
  font-family: Roboto;
  color: #424242;
  font-size: 16px;
}

.app {
  display: flex;
  align-items: center;
  justify-content: center;
}

.vertical-centered {
  max-width: 80%;
}

.button {
  max-width: 20%;
  margin: 0 auto;
  margin-top: 3em;
  background-color: #ea7b57;
  color: #FFFFFF;
  border: none;
  color: white;
  padding: 1.5em 2em;
  text-align: center;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-decoration: none;
  border-radius: 0.2em;
  font-size: 16px;
  text-transform: uppercase;
  cursor: pointer;
}

.button:hover {
  background-image: linear-gradient(
    to right,
    red,
    orange,
    yellow,
    green,
    blue,
    indigo,
    violet,
    red
  );
  animation: slidebg 2s linear infinite;
}
@keyframes slidebg {
  to {
    background-position: 20vw;
  }
}

</style>
