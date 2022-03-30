<template>
  <header class="header">
    <div class="header__container container">
      <router-link class="header__logo" to="/">
        <img class="header__logo-pic" alt="logo" v-bind:src="logoBlack">
      </router-link>
      <nav class="header__nav" :class="{ header__nav_active: active }">
        <router-link class="header__nav-link" to="/">Главная</router-link>
        <router-link class="header__nav-link" to="/map">Геопозиция</router-link>
      </nav>
      <div class="header__burger" :class="{ header__burger_active: active }" @click="active = !active" :aria-pressed="active ? 'true' : 'false'">
        <span class="header__burger-global header__burger-global_top"></span>
        <span class="header__burger-global header__burger-global_middle"></span>
        <span class="header__burger-global header__burger-global_bottom"></span>
      </div>
    </div>
  </header>
</template>

<script>
  import logoBlack from '../assets/img/logo_black.png';

  export default {
    name: 'myHeader',
    data() {
      return {
        active: false,
        logoBlack: logoBlack
      }
    },
  }
</script>

<style scoped lang="scss">
  .header {
    padding: 10px 0;
    width: 100%;
    position: sticky;
    top: 0;
    left: 0;
    background: #ffffff;
    z-index: 5;

    &__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &__logo {
      width: 300px;
      height: auto;

      @media (max-width: 575px) {
        width: 240px;
      }

      &-pic {
        width: 100%;
        height: 100%;
      }
    }

    &__nav {
      @media (max-width: 768px) {
        opacity: 0;
        visibility: hidden;
        background: #fff;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        padding: 20px 0px;
        display: flex;
        flex-direction: column;
        box-shadow: 0 2px 8px 0 rgb(0 0 0 / 20%);
        transition: 0.2s;
        &_active {
          opacity: 1;
          visibility: visible;

          & .header__nav-link {
            padding: 8px;
          }
        }
      }
      &-link {
        margin-left: 20px;
        color: #676767;
        letter-spacing: 1.1px;
        text-transform: uppercase;
        transition: 0.2s;
        font-size: 14px;

        &:hover {
          color: rgba(0,0,0,1);
        }
      }
    }

    &__burger {
      display: none;

      @media (max-width: 768px) {
        cursor: pointer;
        display: inline-block;
        width: 26px;
        height: 22px;
        position: absolute;
        top: 50%;
        right: 15px;
        transform: translate(0, -50%);

        &-global {
          backface-visibility: hidden;
          position: absolute;
          border-top: 3px solid #777;
          border-radius: 10px;
          width: 100%;
          transition: 0.4s ease-out;

          &_top {
            top: 0px;
            left: 0;
          }

          &_middle {
            top: 7px;
            left: 0;
          }

          &_bottom {
            top: 14px;
            left: 0;
          }
        }

        &_active {
          z-index: 1000;

          & .header__burger-global {
            &_top,
            &_bottom {
              top: 6px;
              border-top: 3px solid #777;
            }

            &_middle {
              opacity: 0;
            }

            &_top {
              transform: rotate(-225deg);
            }

            &_bottom {
              transform: rotate(225deg);
            }
          }
        }
      }
    }
  }


</style>
