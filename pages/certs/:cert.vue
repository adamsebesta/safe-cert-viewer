<template>
  <div class="page">
    <div class="header">
      <h5 class="header-text">SAFE CERT VIEWER 🤖</h5>
      <nuxt-link id="nextBtn" :to="'/certs/' + (certNumber == '0' ? '1' : '0')"
        >NEXT</nuxt-link
      >
      <span>{{ cert.course }}</span>
    </div>
    <iframe id="ifrm" type="application/pdf" :src="cert.src"></iframe>
  </div>
</template>

<script setup lang="ts">
import { Cert } from "types/cert";

const route = useRoute();
const certNumber: string | string[] = route.params.cert;
const certs: Cert[] = [
  {
    src: "https://drive.google.com/file/d/1j68YvYuzY0lk4py03W8vi9wnchv_QZo-/preview",
    course: "AZ-900",
  },

  {
    src: "https://drive.google.com/file/d/17kbxuHHwYjvIKIq6rHTaswCY8zzTCeZs/preview",
    course: "AZ-204",
  },
];

const cert = computed(() => {
  return certNumber === "0" ? certs[0] : certs[1];
});
</script>

<style lang="scss">
.page {
  height: calc(100% - 50px);
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  flex-direction: column;
  color: white;
  .header {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    width: 100%;
    align-items: center;
    max-width: 900px;
    margin: 1rem 0 1.5rem;
    #nextBtn {
      margin: 0.5rem 0 1rem 0;
      padding: 0.75rem 1.5rem;
      box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
      color: white;
      text-decoration: none;
      font-size: 12px;
      font-weight: 600;
    }
    h5 {
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
    display: flex;
    flex: 1 0;
    border: none;
    width: 70%;
    height: 60%;
    max-height: 600px;
    max-width: 900px;
  }
}
@media screen and (max-width: 500px) {
  .page {
    .header {
      #nextBtn {
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
