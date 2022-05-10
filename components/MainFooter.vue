<template>
  <footer>
    <span>
      ©2022 Adam Sebesta Development | Built with Nuxt 3 Hosted on Azure Static
      Apps</span
    >
  </footer>
</template>

<script setup lang="ts"></script>
<style lang="scss">
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  height: 50px;
  width: calc(100% - 20px);
  padding: 0px 10px;
  background-image: linear-gradient(315deg, #485461 0%, #28313b 74%);
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  font-size: 12px;
  display: flex;
  align-items: center;
}
</style>
