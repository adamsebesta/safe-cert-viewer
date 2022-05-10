<template>
  <div class="page">
    <div class="header">
      <h5 class="header-text">SAFE CERT VIEWER 🤖</h5>
      <nuxt-link id="nextBtn" :to="'/certs/' + (certNumber == '0' ? '1' : '0')"
        >NEXT</nuxt-link
      >
    </div>
    <iframe id="ifrm" type="application/pdf" :src="src"></iframe>
  </div>
</template>

<script setup lang="ts">
const route = useRoute();
const certNumber: string | string[] = route.params.cert;
const src: string = `https://adamdevstorage.blob.core.windows.net/certs/Microsoft_Certified_Professional_Certificate_${certNumber}.pdf#toolbar=0&fitW=1`;
</script>

<style lang="scss">
.page {
  height: calc(100% - 2rem);
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  color: white;
  .header {
    display: flex;
    justify-content: space-evenly;
    width: 100%;
    align-items: center;
    #nextBtn {
      position: absolute;
      right: 35%;
    }
    h5 {
      font-weight: 600;
    }
    a {
      padding: 1rem 2rem;
      box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
      color: white;
      text-decoration: none;
      font-size: 12px;
      font-weight: 600;
    }
    .header-text {
      margin: 0;

      padding: 1rem 2rem;
      box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    }
  }
  #ifrm {
    margin: 0 auto;
    border: none;
    width: 70%;
    height: 60%;
  }
}
@media screen and (max-width: 500px) {
  .page {
    height: 80%;
    .header {
      flex-direction: column;
      #nextBtn {
        position: static;
        margin-top: 4rem;
      }
    }
    #ifrm {
      height: 40%;
      width: 100%;
    }
  }
}
</style>
