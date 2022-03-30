<template>
  <myHeader/>
  <router-view/>
  <my-footer/>
</template>

<script>
  import myHeader from '@/components/header.vue'
  import myFooter from '@/components/footer.vue'

  export default {
    name: 'app',
    components: {
      myHeader,
      myFooter
    }
  }
</script>

<style lang="scss">
  * {
    font-family: 'Roboto', sans-serif;
    margin: 0;
    padding: 0;
    text-decoration: none;
    -webkit-tap-highlight-color:transparent;
    color: rgba(0,0,0,0.8);
  }

  ul,ol,li {
    list-style-type: none;
  }

  body {
    background: #f0f1f2;
  }

  .title {
    font-size: 36px;
    padding-bottom: 16px;
    letter-spacing: 1.5px;
    color: rgba(0,0,0,0.8);

    @media (max-width: 768px) {
      font-size: 28px;
    }
  }

  .subtitle {
    font-size: 30px;
    padding: 0 15px 20px;
    letter-spacing: 1.5px;
    color: rgba(0,0,0,0.8);
    text-align: center;

    @media (max-width: 768px) {
      font-size: 24px;
    }
  }

  .text {
    font-size: 18px;
    line-height: 1.6;

    @media (max-width: 768px) {
      font-size: 14px;
    }
  }

  #app {
    .container {
      max-width: 1170px;
      padding: 0 15px;
      margin: 0 auto;
    }
  }

</style>
