<template>
  <div>
    <script v-if="!sdkLoaded" defer src="https://blygo.io/sdk.min.js"></script>
    <blygo-button :projectKey="projectKey" :email="email" :phone="phone" :title="title"/>
  </div>
</template>

<script>
export default {
  props: {
    projectKey: String,
    email: String,
    phone: String,
    title: String
  },
  data() {
    return {
      sdkLoaded: false
    };
  },
  beforeMount() {
    if (!this.sdkLoaded) {
      this.loadSdk();
    }
  },
  methods: {
    loadSdk() {
      const script = document.createElement('script');
      script.src = 'https://blygo.io/sdk.min.js';
      script.async = true;
      script.defer = true;
      script.onload = () => {
        this.sdkLoaded = true;
      };
      document.body.appendChild(script);
    }
  }
};
</script>
