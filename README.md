# Flappy Bird Parte 2: Agregando Efectos con CSS


## Introducción
En el lab anterior creaste la estructura del juego Flappy Bird utilizando HTML y comenzaste a agregar estilos utilizando CSS. En éste lab agregarás efectos al juego utilizando CSS, más adelante manipularás estos efectos utilizando JavaScript. 

### Instrucciones
Agrega los siguientes efectos CSS al juego de flappy bird:
- bird aletea
- bird cae al suelo
- El suelo se mueve
- El mensaje "Game Over" se muestra en la pantalla
- El obstaculo se ve de color rojo

```
#game-over {
  background-image: url("img/gameover.png");
  height: 42px;
  width: 192px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: +1;
  position: absolute;
}

#colision {
  background-image: url("img/pipe-red.png");
  width: 52px;
}

#fly {
  animation: fly 0.5s infinite;
}

#fall {
  animation: fall 0.8s forwards;
}

#moving {
  background-image: url("img/base.png");
  width: 100%;
  height: 112px;
  position: absolute;
  top: 578px;
  background-repeat: repeat-x;
  z-index: +1;
  animation: slideright 50s infinite linear;
  -webkit-animation: slideright 50s infinite linear;
}

@keyframes fly {
  0%,
  100% {
    background-image: url("img/yellowbird-upflap.png");
  }
  33% {
    background-image: url("img/yellowbird-midflap.png");
  }
  66% {
    background-image: url("img/yellowbird-downflap.png");
  }
}

@keyframes fall {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(50deg);
    bottom: 0;
  }
}

@keyframes slideright {
  from {
    background-position: 1000%;
  }
  to {
    background-position: 0%;
  }
}

@-webkit-keyframes slideright {
  from {
    background-position: 1000%;
  }
  to {
    background-position: 0%;
  }
}

```