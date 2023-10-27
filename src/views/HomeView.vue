<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
  <div class="wrapper bg-cover bg-center bg-no-repeat overflow-hidden z-10"
    style="background-image: url('https://images.unsplash.com/photo-1516541196182-6bdb0516ed27?auto=format&fit=crop&q=80&w=3087&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');">
    <div class="flex items-center justify-center h-screen">
      <div class="item-hover">
        <div class="line-top--right flex items-center gap-2 absolute top-[40px] right-[40px]">
          <div class="line-sm bg-yellow-500 h-[10px]"></div>
          <div class="line-lg bg-yellow-500 h-[10px]"></div>
        </div>

        <div class="relative">
          <div class="absolute -top-[107px] -left-[77px] z-10">
            <h1 class="title font-semibold text-[140px] text-yellow-500">We Create</h1>
          </div>

          <div class="overflow-hidden">
            <img
              src="https://images.unsplash.com/photo-1482164565953-04b62dcac1cd?auto=format&fit=crop&q=80&w=2940&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
              class="max-w-[680px] " />
          </div>

          <RouterLink to="" class="link absolute -bottom-[52px] -left-[77px] z-10">
            <div class="link-hover--color flex items-center">
              <h1 class="item-link font-semibold uppercase text-[70px] text-yellow-500">
                Awesome Things
              </h1>

              <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                class="text-yellow-500 ml-3 w-[70px] h-[70px]">
                <path fill-rule="evenodd"
                  d="M3.75 12a.75.75 0 01.75-.75h13.19l-5.47-5.47a.75.75 0 011.06-1.06l6.75 6.75a.75.75 0 010 1.06l-6.75 6.75a.75.75 0 11-1.06-1.06l5.47-5.47H4.5a.75.75 0 01-.75-.75z"
                  clip-rule="evenodd" />
              </svg>
            </div>
          </RouterLink>
        </div>

        <div class="line-bottom--left flex items-center gap-2 absolute bottom-[40px] left-[40px]">
          <div class="line-lg bg-yellow-500 h-[10px]"></div>
          <div class="line-sm bg-yellow-500 h-[10px]"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.item-hover {
  & .title {
    transition: transform .3s ease-in-out;
  }

  & img {
    transition: transform .3s ease-in-out;
    transition: all .3s;
    filter: grayscale(100);
  }

  & .link-hover--color::after {
    transform: translate(-1200px, 0);
    position: absolute;
    content: '';
    width: 0;
  }

  & .link-hover--color:hover::after {
    transition: transform .3s ease-in-out;
    transform: translate(0, 0);
    background-color: rgb(245, 158, 11);
    border-radius: 10px;
    width: 105%;
    height: 70px;
    left: -23px;
  }

  & .link-hover--color:hover {
    & .item-link,
    & svg {
      color: #fff;
      z-index: 10;
    }

    & svg {
      font-size: 70px;
    }
  }

  & .item-link {
    transition: transform .3s ease-in-out;
    transform: translate(-1200px, 0);
    transition: all .3s;
  }

  & svg {
    transition: transform .3s ease-in-out;
    transform: translate(700px, 0);
    transition: all .3s;
  }

  & .line-lg {
    width: 0;
    transition: width .3s;
  }

  & .line-sm {
    width: 0;
    transition: width .4s;
  }

  &:hover {
    & .title {
      transform: translate(10px, 10px);
    }

    & .item-link {
      transform: translate(0, 0);
    }

    & svg {
      transform: translate(0, 0);
    }

    & img {
      filter: grayscale(0);
      transform: scale(1.1, 1.1);
    }

    & .line-lg {
      width: 100px;
    }

    & .line-sm {
      width: 60px;
    }
  }
}
</style>