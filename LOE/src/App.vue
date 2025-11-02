<script setup lang="ts">
import HeaderView from './components/HeaderView.vue'
</script>

<template>
  <HeaderView />
  <div id="space">
    <div class="stars"></div>
    <div class="stars2"></div>
    <div class="stars3"></div>
    <div id="black-hole"></div>
  </div>
</template>

<style scoped>
/* ---------------------------------- */
/* 1. Configuration Générale */
/* ---------------------------------- */
body {
  background: #000;
  margin: 0;
  overflow: hidden; /* Cache les étoiles qui sortent de l'écran */
}

#space {
  position: absolute;
  width: 100%;
  height: 100%;
  background: #000;
}

/* ---------------------------------- */
/* Étoiles */
/* ---------------------------------- */

.stars, .stars2, .stars3 {
  width: 1px;
  height: 1px;
  background: transparent;
  position: absolute;
  top: 50%; /* Positionnement initial */
  left: 50%;
  /* Utilise box-shadow pour créer des centaines de "points" étoiles */
  box-shadow:
      500px 100px #FFF,
      800px 300px #FFF,
      100px 700px #FFF,
      -200px 450px #FF4444,
      -600px 200px #FFF,
      900px 500px #FFF,
      1300px 200px #FF4444,
      -700px 100px #BBB,
      400px -800px #BBB,
      -1100px -300px #BBB,
      1000px 10px #EEE,
      -100px -100px #DDD;
}

/* Étoiles plus éloignées (petites et moins lumineuses) */
.stars {
  transform: scale(0.6);

  box-shadow:
      1200px 800px #D0E0FF,
      -500px 900px #D0E0FF,
      -900px 700px #DDD,
      1400px 400px #FF4444,
      200px -900px #FF4444,
      1000px -100px #AAA,
      -500px -650px #FFF,
      1100px 100px #EEE,
      -150px 750px #DDD,
      1450px 950px #FFF,
      -1150px -100px #CCC,
      300px 1400px #EEE,
      -800px 1050px #D0E0FF,
      1350px 350px #DDD,
      -100px -1500px #D0E0FF,
      700px 50px #CCC,
      -1400px 1450px #FFF,
      50px -400px #9BBFEF,
      950px -1050px #9BBFEF,
      -550px 150px #FFF,
      1250px -750px #CCC,
      -300px -850px #D0E0FF,
      800px 1300px #FFFFE0,
      -900px 50px #DDD,
      150px 1150px #FFFFE0,
      -1200px -1350px #D0E0FF,
      1400px 650px #FFF,
      -750px -1200px #EEE,
      250px -300px #DDD,
      -1050px 1100px #D0E0FF,
      600px 1500px #CCC,
      1150px -200px #9BBFEF,
      -200px 900px #D0E0FF,
      -1300px 700px #DDD,
      500px 1000px #FFF,
      -950px -900px #FFFFE0;
}

/* Étoiles intermédiaires */
.stars2 {
  transform: scale(0.8);
  box-shadow:
      100px 500px #CCC,
      700px -200px #CCC,
      -400px 600px #FFFFE0,
      -100px -600px #9BBFEF,
      900px 100px #FFF,
      -1200px 500px #FFF,
      -150px 1050px #FFF,
      1300px -250px #D0E0FF,
      -700px -100px #DDD,
      450px 1100px #FFFFE0,
      -1000px 300px #D0E0FF,
      140px -900px #EEE,
      -1200px 650px #FFF,
      850px 1450px #DDD,
      -300px -1400px #FFF,
      550px 100px #D0E0FF,
      100px 1300px #9BBFEF,
      -1450px 50px #FFFFE0,
      1150px 1250px #D0E0FF,
      -950px -350px #FFF,
      200px 980px #CCC,
      -50px -1200px #FFF,
      700px -70px #EEE,
      -800px 1350px #D0E0FF,
      1500px 550px #FFF,
      -1000px -1000px #D0E0FF,
      -10px 880px #FFFFE0,
      1400px -1100px #EEE,
      -650px -900px #DDD,
      350px 1500px #FFF,
      -120px 250px #D0E0FF,
      1050px 450px #FFF,
      -1350px 850px #9BBFEF,
      250px -550px #FFFFE0,
      -400px 100px #FFF,
      1200px -600px #CCC;
}

/* Étoiles proches (plus grandes et lumineuses) */
.stars3 {
  transform: scale(1.0);
  box-shadow:
      200px 200px #FF8866,
      -800px -50px #FFF,
      500px 900px #D0E0FF,
      150px -1100px #FFF,
      890px -60px #EEE,
      -450px 1200px #DDD,
      1150px 150px #FF8866,
      30px 950px #FF8866,
      -980px 800px #e1e1e1,
      1400px -400px #FFF,
      750px -900px #DDD,
      -1300px -200px #FFF,
      -600px 350px #CCC,
      210px 1450px #FFF,
      -1500px 100px #EEE,
      550px 550px #FFF,
      90px -1300px #DDD,
      1050px 1050px #CCC,
      -70px -70px #FF8866,
      1250px 700px #D0E0FF,
      -880px -500px #FFF,
      400px -1200px #DDD,
      -250px 450px #FF8866,
      1500px 300px #FFF,
      -1400px -100px #D0E0FF,
      900px -150px #FF8866,
      -200px 1400px #FFF,
      -1100px 1050px #CCC,
      50px -1450px #FF8866,
      1350px 750px #D0E0FF,
      -350px -950px #DDD,
      600px 1150px #FFF,
      -1250px 450px #9BBFEF,
      -50px -50px #FFF,
      1000px 1300px #D0E0FF,
      -750px 250px #DDD,
      -1500px 650px #FFF,
      250px -850px #CCC,
      100px 1200px #FF4444,
      -400px -1300px #D0E0FF,
      1100px 800px #DDD,
      -900px 900px #FFF,
      1450px -50px #D0E0FF,
      350px 500px #FFF,
      -100px -300px #FF4444,
      800px -1150px #DDD,
      -1350px -700px #D0E0FF,
      450px 1400px #CCC,
      1200px 200px #9BBFEF,
      -550px -100px #EEE,
      200px 700px #DDD,
      -140px 130px #D0E0FF,
      1000px -750px #CCC;
}


/* ---------------------------------- */
/* 3. Animation du Mouvement Lent */
/* ---------------------------------- */

/* Définition du mouvement de dérive (léger déplacement vers le bas/droite) */
@keyframes move-stars {
  from {
    transform: translate(0, 0);
  }
  to {
    /* Déplacement très lent sur la durée de l'animation (300s) */
    transform: translate(100px, 100px);
  }
}
@keyframes move-stars2 {
  from {
    transform: translate(0, 0);
  }
  to {
    /* Mouvement un peu plus rapide (pour l'effet de profondeur) */
    transform: translate(150px, 150px);
  }
}
@keyframes move-stars3 {
  from {
    transform: translate(0, 0);
  }
  to {
    /* Mouvement le plus rapide (pour l'effet de profondeur) */
    transform: translate(200px, 200px);
  }
}

/* Application des animations aux couches d'étoiles */
.stars {
  animation: move-stars 300s linear infinite alternate; /* 300s = 5 minutes ! Très lent. */
}
.stars2 {
  animation: move-stars2 200s linear infinite alternate; /* Moins lent */
}
.stars3 {
  animation: move-stars3 100s linear infinite alternate; /* Le moins lent */
}

#black-hole {
  /* Positionnement au centre de l'écran */
  position: absolute;
  top: 18%;
  left: 82%;
  transform: translate(-50%, -50%);
  width: 100px;
  height: 100px;
  border-radius: 80%;
  background: #040303;
  z-index: 10;
  box-shadow: 0 0 50px rgba(236, 101, 5, 0.72);
  filter: blur(1.1px);
  rotate: 9deg;
}
/* ---------------------------------------------------- */
/*  Disque d'Accrétion
/* ---------------------------------------------------- */

#black-hole::before {
  content: '';
  position: absolute;
  width: 400px; /* Plus large */
  height: 40px; /* Plus plat */

  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);

  border-radius: 30%; /* ellipse */
  z-index: 5;

  /* simuler l'incandescence */
  background: radial-gradient(
      ellipse at center,
      rgba(236, 101, 5, 0.72) 0%, /* Centre lumineux (jaune/orange) */
      rgba(255, 140, 0, 0.2) 20%, /* Moins intense */
      rgba(255, 3, 3, 0.1) 60%,  /* Devient plus rouge/sombre */
      rgba(0, 0, 0, 0) 100%      /* S'estompe vers le noir */
  );

  /* Appliquer un flou pour lisser le dégradé et simuler le mouvement/la chaleur */
  filter: blur(10px);

  /* animation de pulsation ou de rotation pour le disque */
  animation: accrete-pulse 5s ease-in-out infinite alternate;
}

/* ---------------------------------- */
/* Animation pour le Disque d'Accrétion */
/* ---------------------------------- */
@keyframes accrete-pulse {
  0% { transform: translate(-50%, -50%) scale(1); opacity: 0.8; }
  50% { transform: translate(-50%, -50%) scale(1.05); opacity: 1; }
  100% { transform: translate(-50%, -50%) scale(1); opacity: 0.8; }
}

/* ---------------------------------------------------- */
/* Intensification de l'Animation de Dérive */
/* ---------------------------------------------------- */
@keyframes slow-spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

.stars {
  animation: move-stars 300s linear infinite alternate,
  slow-spin 800s linear infinite; /* 800s = très lent */
}
</style>
