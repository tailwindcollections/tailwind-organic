<template>
  <div
    class="w-full min-h-screen font-sans text-gray-900 bg-gradient-to-br from-transparent to-green-100"
  >
    <nav class="flex items-center justify-between px-24 py-8 max-w-screen-xl mx-auto">
      <a href="#" class="text-4xl font-bold tracking-wide">
        Organ<span class="text-green">o</span>
      </a>
      <div class="flex items-center space-x-14">
        <ul class="flex items-center space-x-8">
          <li
            class="texl font-medium group"
            :class="{ 'text-green': activeMenu === menu }"
            v-for="menu in menus"
          >
            <a href="#">{{ menu }}</a>
            <div
              class="h-0.5 bg-green scale-x-0 group-hover:scale-100 transition-transform origin-left rounded-full duration-300 ease-out"
            />
          </li>
        </ul>
        <button
          class="flex justify-center items-center h-13 px-7 font-medium text-white bg-green rounded-xl hover:shadow-primary transition-shadow duration-300"
        >
          Get Started
        </button>
      </div>
    </nav>
    <div class="flex justify-between px-24 py-8 max-w-screen-xl mx-auto">
      <div class="max-w-md relative">
        <img class="absolute -top-4 -right-8 w-24 h-auto" src="/img/leaf.png" alt="" />
        <span class="flex items-center px-1 text-xl text-green">
          <span class="font-medium">100% Organic food</span>
          <img class="w-auto h-8" src="/img/vegetable.png" alt="" />
        </span>
        <h1 class="pt-4 text-6xl font-bold tracking-tighter leading-tight">
          Healthy Lifestyle is your only
          <span class="whitespace-nowrap text-green">unfair advantage</span>
        </h1>
        <p class="pt-8 text-lg font-normal text-gray-600 leading-relaxed">
          Choose healthy habits with Organo daily meal prepared by our expert nutritionist
          and chef
        </p>
        <div class="flex pt-8 space-x-6">
          <button
            class="flex justify-center items-center h-13 px-8 font-medium bg-green text-white rounded-xl hover:shadow-primary transition-shadow duration-300"
          >
            Get Started
          </button>
          <button
            class="flex justify-center items-center h-13 px-8 font-medium text-gray-900 border border-gray-900 rounded-xl hover:shadow-xl transition-shadow duration-300"
          >
            Explore menu
          </button>
        </div>
        <div class="flex pt-20">
          <img class="w-24 h-auto" src="/img/chef.png" alt="" />
          <div class="pt-5 pl-3">
            <div class="text-xl font-bold leading-relaxed">Chef of the month</div>
            <div class="inline-flex text-gray-600 leading-relaxed">
              People loved his 🍳
            </div>
            <div class="font-bold text-green leading-relaxed">80+ famous dishes</div>
          </div>
        </div>
      </div>
      <div class="flex-1 flex flex-col relative">
        <img class="max-w-xl drop-shadow-2xl self-end" src="/img/dish.png" alt="" />
        <div
          class="absolute -right-6 top-32 flex flex-col py-5 px-7 rounded-2xl shadow-xl bg-white/80 backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
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
          class="absolute left-0 bottom-16 flex rounded-2xl shadow-xl bg-white/80 backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <img class="w-auto h-20 self-end" src="/img/driver.png" alt="" />
          <div class="pr-7 pl-2 py-5">
            <div class="font-bold">Fast Delivery</div>
            <div class="text-gray-600 leading-relaxed">30 mins delivery 🚀</div>
          </div>
        </div>
        <div class="flex justify-end space-x-1 font-bold">
          <span>Powered by</span>
          <FuelerIcon class="w-6 h-6 text-gray-900 fill-current" />
          <span>Fueler</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import StarIcon from "./icons/star.svg";
import FuelerIcon from "./icons/fueler.svg";
const activeMenu = "Home";
const menus = ["Home", "Delivery", "Pricing", "FAQs", "Contact"];
</script>
