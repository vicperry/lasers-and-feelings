<template>
    <v-container>
      <h1 v-text="titulo" id="main-title"> </h1>
      <p v-html="textoIntroducao" id="intro-text"></p>
      <v-btn @click="iniciarJogo" id="start-btn">{{ botaoIniciarTexto }}</v-btn>
    </v-container>
  </template>
  
  <script>
  export default {
    name: 'HomeScreen',
    data() {
      return {
        titulo: "LASERS & FEELINGS",
        textoIntroducao: `<b>VOCÊ É DA TRIPULAÇÃO DO NAVIO ESCUTADOR INTERESTELAR <i>RAPTOR</i>.</b> Sua missão é explorar
        regiões desconhecidas do espaço, lidar com alienígenas amigáveis e mortais e defender os mundos do Consórcio
        contra os perigos espaciais. <strong>CAPITÃO DARCY</strong> foi derrotado pela estranha entidade psíquica
        conhecida como <em>Outra Coisa</em>, deixando vocês se defenderem sozinhos enquanto ele se recupera em uma cápsula médica.`,
        botaoIniciarTexto: "Iniciar"
      }
    },
    methods: {
      iniciarJogo() {
        console.log('Jogo iniciado.')
      }
    }
  }
  </script>
  <style scoped>
 v-container {
  display: flex;
  flex-direction: column; 
  align-items: center; 
  justify-content: center; 
  height: 100%; 
  text-align: center; 
  margin: 0; 
}

#main-title {
  font-family: 'Press Start 2P', cursive;
  color: yellow;
  text-align: center; 
  margin: 0; 
}

#intro-text {
  text-align: justify; 
  margin: 20px 40px; 
}

#start-btn {
  margin-top: 20px; 
  background-color: #000000;
  color: #FFFF00;
  font-family: 'Press Start 2P', cursive;
  box-shadow: 0 4px 20px rgba(255, 215, 0, 0.7); 
  transition: box-shadow 0.3s ease;
  display: block; 
  margin-left: auto; 
  margin-right: auto; 
}

#start-btn:hover {
  box-shadow: 0 8px 40px rgba(255, 215, 0, 1); 
}
</style>