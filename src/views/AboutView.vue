<script>
export default {
  methods: {
    moveNoButton() {
      const b = document.querySelector('button.button--nao')
      b.addEventListener("mouseover", moveHover)

      function moveHover() {
        const i = Math.floor(Math.random() * 500) + 1;
        const j = Math.floor(Math.random() * 500) + 1;

        b.style.left = i + "px"
        b.style.top = j + "px"
      }
    }
  }
}
</script>
<template>
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Caveat:wght@500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="Love.css">
    <title>Ester</title>
  </head>

  <body>
    <div class="app">
      <h1>Quer namorar comigo?</h1>

      <div class="buttonGroup">
        <button onclick="alert('Linda, delicia, maravilhosa')">Sim </button>
        <button class="button--nao" @mouseover="moveNoButton" onclick="alert('Muito esforço');">Não</button>
      </div>
    </div>
  </body>
</template>

<style>
body{
  background-color: #E9B0F5;
}
.app{
  font-family: 'Caveat', cursive;
}

h1 {
  color: #FA2C6F;
  font-size: 50px;
  display: block;
  position: absolute;
}

.app {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  font-family: 'Caveat', cursive;
}

.buttonGroup {
  margin-top: 150px;
}

button {
  position: absolute;
  display: flex;
  cursor: pointer;
  margin: 0 10px;
  padding: 10px 30px;
  background-color: white;
  border: none;
  border-radius: 10px;
  color: black;
}

.button--nao {
  left: calc(50% - 100px);
}
</style>
