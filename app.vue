<template>
  <NuxtLayout>
    <NuxtPage />
    <MainFooter />
  </NuxtLayout>
</template>
<style lang="scss">
html,
body,
#__nuxt {
  height: calc(100%);
  width: 100%;
  overflow: hidden;
  background-color: #485461;
  background-image: linear-gradient(315deg, #485461 0%, #28313b 74%);
  color: white;
  font-family: Montserrat, Trebuchet MS, Helvetica, sans-serif;
}

@font-face {
  font-family: "Neuzeit Grotesk";
  src: url("~/assets/fonts/NeuzeitGro-Bla.ttf"); /* IE9 Compat Mode */
  // src: url("~/assets/fonts/NeuzeitGro-Bol.ttf"); /* IE9 Compat Mode */
  src: url("~/assets/fonts/NeuzeitGro-Reg.ttf"); /* IE9 Compat Mode */
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: "Neuzeit Grotesk";
  src: url("~/assets/fonts/NeuzeitGro-Bol.ttf"); /* IE9 Compat Mode */
  font-weight: 700;
  font-style: normal;
}

@font-face {
  font-family: "Montserrat";
  src: url("~/assets/fonts/Montserrat-Regular.ttf"); /* IE9 Compat Mode */
  font-weight: normal;
  font-style: normal;
}

@font-face {
  font-family: "Montserrat";
  src: url("~/assets/fonts/Montserrat-Medium.ttf"); /* IE9 Compat Mode */
  font-weight: 500;
  font-style: normal;
}

@font-face {
  font-family: "Montserrat";
  src: url("~/assets/fonts/Montserrat-SemiBold.ttf"); /* IE9 Compat Mode */
  font-weight: 600;
  font-style: normal;
}

@font-face {
  font-family: "Montserrat";
  src: url("~/assets/fonts/Montserrat-Bold.ttf"); /* IE9 Compat Mode */
  font-weight: 700;
  font-style: normal;
}
</style>
