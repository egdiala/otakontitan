<template>
    <h1>COMING SOON!!</h1>
</template>

<style scoped>
h1 {
    animation: flow 8s ease-in-out infinite;
    background: linear-gradient(-60deg, #904e95, #904e95, #e73c7e, #ee7752);
    background-size: 300%;

    -webkit-background-clip: text;
            background-clip: text;
      -webkit-text-fill-color: transparent;
}

@keyframes flow {
  0% {
    background-position: 0 50%;
  }

  50% {
    background-position: 100% 50%;
  }

  100% {
    background-position: 0 50%;
  }
}
</style>
