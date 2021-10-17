<template>
  <div
    class="w-full min-h-screen font-sans text-gray-900 bg-gradient-to-br from-transparent to-green-100"
    :class="sidebarOpen ? 'overflow-hidden h-screen' : ''"
  >
    <!-- <div
      class="fixed px-3 py-2 text-sm font-bold text-white bg-gray-900 rounded bottom-4 left-4 z-50"
    >
      <span class="sm:hidden">DEFAULT</span>
      <span class="hidden sm:inline-block md:hidden">SM</span>
      <span class="hidden md:inline-block lg:hidden">MD</span>
      <span class="hidden lg:inline-block xl:hidden">LG</span>
      <span class="hidden xl:inline-block">XL</span>
    </div> -->
    <nav
      class="flex justify-between items-center py-8 px-6 mx-auto max-w-screen-xl md:px-12 lg:px-16 xl:px-24"
    >
      <a href="#" class="text-3xl md:text-4xl font-bold tracking-wide">
        Organ<span class="text-green">o</span>
      </a>
      <div
        class="inset-0 transition-all bg-white/70 backdrop-blur-xl z-20 md:static md:bg-transparent md:flex items-center justify-center space-y-8 md:space-y-0 md:space-x-8 flex-col md:flex-row lg:space-x-14"
        :class="sidebarOpen ? 'fixed flex' : 'hidden'"
      >
        <ul
          class="flex flex-col md:flex-row items-center space-y-6 md:space-y-0 md:space-x-6 lg:md:-x-8"
        >
          <li
            v-for="menu in menus"
            class="text-lg md:text-base lg:text-lg font-medium group"
            :class="{ 'text-green': activeMenu === menu }"
          >
            <a href="#"> {{ menu }} </a>
            <div
              class="h-0.5 bg-green scale-x-0 group-hover:scale-100 transition-transform origin-left rounded-full duration-300 ease-out"
            />
          </li>
        </ul>
        <button
          class="flex justify-center items-center h-13 px-7 font-medium text-white bg-green rounded-xl hover:shadow-primary transition-shadow duration-300 whitespace-nowrap"
        >
          Get started
        </button>
      </div>
      <button @click="sidebarOpen = !sidebarOpen" class="block md:hidden relative z-30">
        <HamburgerIcon class="w-8 h-8 fill-current text-gray-900" />
      </button>
    </nav>

    <div
      class="flex flex-wrap-reverse gap-y-24 justify-between py-12 px-6 mx-auto max-w-screen-xl sm:px-8 md:px-12 lg:px-16 xl:px-24"
    >
      <div class="relative z-10 md:w-1/2 w-full">
        <img
          class="absolute top-0 right-0 md:-top-4 md:-right-8 w-24 h-auto"
          src="/img/leaf.png"
          alt=""
        />
        <span class="flex items-center px-1 text-xl text-green">
          <span class="font-medium">100% Organic food</span>
          <img class="w-auto h-8" src="/img/vegetable.png" alt="" />
        </span>
        <h1
          class="pt-4 text-4xl sm:text-5xl lg:text-6xl font-bold tracking-tighter leading-tight whitespace-nowrap"
        >
          Healthy Lifestyle <br />
          is your only <br />
          <span class="whitespace-nowrap text-green"> unfair advantage </span>
        </h1>
        <p class="pt-8 sm:text-lg max-w-md font-normal text-gray-600 leading-relaxed">
          Choose healthy habits with Organo daily meal prepared by our expert nutritionist
          and chef
        </p>
        <div class="flex pt-8 space-x-4 sm:space-x-6">
          <button
            class="flex justify-center items-center w-full sm:w-auto h-13 px-8 bg-green font-medium text-white rounded-xl whitespace-nowrap hover:shadow-primary transition-shadow duration-300"
          >
            Get started
          </button>
          <button
            class="flex justify-center items-center w-full sm:w-auto h-13 px-8 font-medium text-gray-900 border border-gray-900 rounded-xl whitespace-nowrap hover:shadow-xl transition-shadow duration-300"
          >
            Explore menu
          </button>
        </div>
        <div class="flex pt-20">
          <img class="w-24" src="/img/chef.png" alt="" />
          <div class="pt-5 pl-3">
            <div class="text-xl font-bold leading-relaxed">Chef of the month</div>
            <div class="inline-flex text-gray-600 leading-relaxed">
              People loved his 🍳
            </div>
            <div class="font-bold text-green leading-relaxed">80+ famous dishes</div>
          </div>
        </div>
        <div>
          <div class="flex md:hidden pt-8 justify-end space-x-1 font-bold">
            <span>Powered by</span>
            <FuelerIcon class="w-6 h-6 text-gray-900 fill-current" />
            <span>Fueler</span>
          </div>
        </div>
      </div>

      <div class="relative md:w-1/2 w-full flex flex-col justify-between">
        <img
          class="w-96 lg:w-full drop-shadow-2xl self-center lg:self-end"
          src="/img/dish.png"
          alt=""
        />
        <div
          class="absolute right-0 lg:-right-6 top-0 lg:top-28 flex flex-col py-5 px-7 rounded-2xl shadow-xl bg-white/80 backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <div class="flex -space-x-3">
            <div
              v-for="i in 3"
              class="w-13 h-13 rounded-full border-4 border-white object-cover overflow-hidden"
            >
              <img :src="`/img/avatar-${i}.jpeg`" alt="" />
            </div>
          </div>
          <div class="pt-3 font-bold">Happy customers</div>
          <div class="flex items-center text-gray-600 leading-relaxed">
            <StarIcon class="w-5 h-5" />
            <span class="pl-1">4.9 (+2.5k Ratings)</span>
          </div>
        </div>
        <div
          class="absolute left-0 bottom-0 md:bottom-32 lg:bottom-16 flex bg-white/80 rounded-2xl shadow-xl backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <img class="w-auto h-20 self-end" src="/img/driver.png" alt="" />
          <div class="pr-7 pl-2 py-5">
            <div class="font-bold">Fast delivery</div>
            <div class="text-gray-600 leading-relaxed">30 mins delivery 🚀</div>
          </div>
        </div>
        <div class="hidden md:flex justify-end space-x-1 font-bold">
          <span>Powered by</span>
          <FuelerIcon class="w-6 h-6 text-gray-900 fill-current" />
          <span>Fueler</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import HamburgerIcon from "./icons/hamburger.svg";
import StarIcon from "./icons/star.svg";
import FuelerIcon from "./icons/fueler.svg";
const activeMenu = "Home";
const menus = ["Home", "Delivery", "Pricing", "FAQs", "Contact"];
const sidebarOpen = ref(false);
</script>
