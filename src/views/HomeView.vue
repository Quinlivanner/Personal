<template>
<div class="mainwindow">
  <div class="terminal">
    <div class="terminal-header">
      <div class="buttons">
        <span class="close"></span>
        <span class="minimize"></span>
        <span class="maximize"></span>
      </div>
      <div class="title">Status</div>
    </div>
    <div class="terminal-body">
      <div class="terminal-loader">
        <span class="loader-text">Loading</span>
        <span id="dot1" class="dot">.</span>
        <span id="dot2" class="dot">.</span>
        <span id="dot3" class="dot">.</span>
      </div>
    </div>
  </div>
</div>

</template>

<style scoped>
.mainwindow{
  height: 100vh;
  width: 100vw;
  display: flex;
}
/* Terminal Window */
.terminal {
  margin: auto;
  width: 1000px;
  background-color: #000;
  color: #0f0;
  font-family: "Courier New", Courier, monospace;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
}

/* Terminal Header */
.terminal-header {
  background-color: #333;
  padding: 5px;
  display: flex;
  align-items: center;
  color: #fff;
}

.buttons {
  display: flex;
  margin-right: 15px;
}

.buttons span {
  height: 15px;
  width: 15px;
  border-radius: 50%;
  display: inline-block;
  margin-right: 5px;
}

.close {
  background-color: #ff605c;
}
.minimize {
  background-color: #ffbd44;
}
.maximize {
  background-color: #00ca4e;
}

.title {
  flex-grow: 1;
  text-align: center;
}

/* Terminal Body */
.terminal-body {
  padding: 10px;
}

.terminal-loader {
  display: inline-flex;
  align-items: center;
}

.loader-text {
  margin-right: 5px;
}

.dot {
  opacity: 0;
  animation: dotFadeInOut 1.5s infinite;
}

@keyframes dotFadeInOut {
  0%,
  100% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}

#dot1 {
  animation-delay: 0.5s;
}

#dot2 {
  animation-delay: 0.6s;
}

#dot3 {
  animation-delay: 0.7s;
}

</style>