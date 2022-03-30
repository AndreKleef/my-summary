<template>
  <div class="experiense">
    <h2 class="experiense__content-title subtitle">{{ title }}</h2>
    <div class="experiense__block">
      <div class="experiense__container container">
        <div class="experiense__tabs">
          <span @click="currentTab = row.id"
            v-for="row in content" :key="row"
            :class="{ 'active' : currentTab == row.id }"
            class="experiense__tabs-item">{{ row.title }}
          </span>
        </div>
        <div v-for="row in content" :key="row">
          <div v-if="currentTab == row.id" class="experiense__description">
            <p class="experiense__description-text text" v-html="row.content"></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      title: String,
      content: Array
    },
    data() {
      return {
        currentTab: 1
      }
    }

  }
</script>

<style scoped lang="scss">

  .experiense {
    margin: 60px 0 0 0;

    @media (max-width: 1200px) {
      margin: 30px 0 0 0;
    }

    &__block {
      background: url('../../assets/img/experiense.jpeg') no-repeat center/cover;
      width: 100%;
      height: 600px;
      position: relative;

      @media (max-width: 1200px) {
        height: 360px;
      }

      &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.45);
        z-index: 1;
      }

      &::after {
        content: '';
        position: absolute;
        top: 0;
        right: 0;
        width: 50%;
        height: 100%;
        background: rgba(238, 238, 238, 0.65);
        z-index: 1;

        @media (max-width: 768px) {
          width: 100%;
        }
      }
    }

    &__container {
      position: relative;
      height: 100%;
    }

    &__tabs {
      position: absolute;
      top: 0;
      right: 55%;
      width: 40%;
      display: flex;
      flex-direction: column;
      align-items: flex-end;
      padding: 90px 0 90px 15px;
      z-index: 2;

      @media (max-width: 1200px) {
        top: 50%;
        transform: translate(0, -50%);
        padding: 0;
      }

      @media (max-width: 768px) {
        position: relative;
        top: initial;
        right: initial;
        transform: initial;
        width: 100%;
        align-items: center;
        justify-content: center;
        padding: 10px 0;
      }


      &-item {
        background: rgba(0, 0, 0, 0.8);
        color: #ffffff;
        text-transform: uppercase;
        font-size: 36px;
        font-weight: 900;
        padding: 8px 0 8px 16px;
        letter-spacing: 20px;
        margin: 10px 0 30px 0;
        text-align: right;
        max-width: 360px;
        transition: 0.2s;
        cursor: pointer;

        @media (max-width: 1200px) {
          font-size: 24px;
          padding: 4px 0 4px 16px;
          margin: 12px 0;
        }

        @media (max-width: 768px) {
          font-size: 16px;
          padding: 4px 0 4px 16px;
          letter-spacing: 12px;
          margin: 8px 0;
        }

        &.active {
          background: rgba(196, 196, 196, 0.8);
          color: #000000;
        }
      }
    }

    &__description {
      position: absolute;
      top: 0;
      left: 55%;
      width: 40%;
      z-index: 2;
      padding: 90px 15px 90px 0;
      max-height: 420px;
      overflow-y: auto;

      @media (max-width: 1200px) {
        padding: 0;
        margin: 20px 15px 20px 0;
        max-height: 320px;
        overflow: hidden;
        overflow-y: auto;
      }

      @media (max-width: 768px) {
        position: relative;
        top: initial;
        left: initial;
        width: 100%;
        padding: 0;
        margin: 0 15px 0 0;
        max-height: 170px;
        padding: 0;
        overflow: hidden;
        overflow-y: auto
      }

      ;

      &::-webkit-scrollbar {
        width: 5px;
        background-color: rgba(26, 24, 47, 0.15);
        border-radius: 5px;
      }

      &::-webkit-scrollbar-thumb {
          background: #cccccc;
          border-radius: 5px;
      }

      &-text {
        padding: 8px 0;
        letter-spacing: 1px;

        @media (max-width: 768px) {
          padding: 4px 0;
        }
      }
    }
  }
</style>
