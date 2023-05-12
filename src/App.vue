<script setup lang="ts">
import { ref } from "vue";

const data = ref([
  {
    category: "Reaction",
    score: 80,
    icon: ("./assets/images/icon-reaction.svg"),
  },
  {
    category: "Memory",
    score: 92,
    icon: "./assets/images/icon-memory.svg",
  },
  {
    category: "Verbal",
    score: 61,
    icon: "./assets/images/icon-verbal.svg",
  },
  {
    category: "Visual",
    score: 72,
    icon: "./assets/images/icon-visual.svg",
  },
]);
</script>

<template>
  <main class="w-full h-screen lg:flex">
    <section class="lg:flex lg:m-auto">
      <article class="relative flex sm:z-50 w-full sm:w-[80%] lg:w-auto lg:px-[40px] max-w-[697.6px] sm:mx-auto border-[#1125d4] border-b-2 bg-gradient-to-b from-[#7857ff] to-[#2e2be9] rounded-b-[30px] lg:rounded-[30px]">
        <div class="mx-auto pt-[20px] pb-[30px] text-center w-[220px] lg:w-[180px]">
          <span class="text-[#c8c7ff] font-bold">Your Result</span>
          <div
            class="mx-auto flex justify-center items-center  my-4 bg-gradient-to-b from-[#4e21ca] to-[#2421ca00] w-[120px] lg:w-[150px] h-[120px] lg:h-[150px] rounded-[100%]"
          >
            <div class="">
              <p class="text-[50px] text-white font-extrabold">76</p>
              <p class="text-[13px] font-bold text-[#c8c7ff]">of 100</p>
            </div>
          </div>
          <p class="text-white font-bold text-[20px]">Great</p>
          <p class="text-[13px] text-[#c8c7ff] font-semibold mt-3 lg:mt-[30px]">
            You scored higher than 65% of the people who have taken these tests.
          </p>
        </div>
      </article>
      <article class="relative sm:z-10  sm:mt-[-20px] lg:mt-0 sm:w-[80%] max-w-[697.6px] lg:w-[320px] sm:shadow-lg sm:rounded-[30px] sm:mx-auto mt-4 px-[20px] sm:px-[40px] lg:px-[30px] lg:pl-[70px] lg:ml-[-50px]">
        <h1 class="font-bold sm:pt-[40px] lg:pt-[20px]">Summary</h1>
        <div>
          <button class="mt-5 relative overflow-hidden w-full p-[10px] rounded-[10px] bg-[#ff5757] bg-opacity-5">
            <div class="arc top-[2px] left-[-4px] rotate-[315deg]"></div>
            <div class="arc top-[2px] right-[-4px] rotate-[45deg]"></div>
            <div class="arc bottom-[2px] left-[-4px] rotate-[225deg]"></div>
            <div class="arc bottom-[2px] right-[-4px] rotate-[135deg]"></div>
            <ul class="flex justify-between">
              <li class="flex text-[#ff5757]"><img src="./assets/images/icon-reaction.svg" alt="">&nbsp;{{data[0].category}}</li>
              <li class="text-[#303b5a] font-bold">{{data[0].score}} <span class="text-[#c8c7ff]">/ 100</span></li>
            </ul>
          </button>        
          <button class="mt-4 relative overflow-hidden w-full p-[10px] rounded-[10px] bg-[#ffb01f] bg-opacity-5">
            <div class="arc top-[2px] left-[-4px] rotate-[315deg]"></div>
            <div class="arc top-[2px] right-[-4px] rotate-[45deg]"></div>
            <div class="arc bottom-[2px] left-[-4px] rotate-[225deg]"></div>
            <div class="arc bottom-[2px] right-[-4px] rotate-[135deg]"></div>
            <ul class="flex justify-between">
              <li class="flex text-[#ffb01f]"><img src="./assets/images/icon-memory.svg" alt="">&nbsp;{{data[1].category}}</li>
              <li class="text-[#303b5a] font-bold">{{data[1].score}} <span class="text-[#c8c7ff]">/ 100</span></li>
            </ul>
          </button>        
          <button class="mt-4 relative overflow-hidden w-full p-[10px] rounded-[10px] bg-[#00bd91] bg-opacity-5">
            <div class="arc top-[2px] left-[-4px] rotate-[315deg]"></div>
            <div class="arc top-[2px] right-[-4px] rotate-[45deg]"></div>
            <div class="arc bottom-[2px] left-[-4px] rotate-[225deg]"></div>
            <div class="arc bottom-[2px] right-[-4px] rotate-[135deg]"></div>
            <ul class="flex justify-between">
              <li class="flex text-[#00bd91]"><img src="./assets/images/icon-verbal.svg" alt="">&nbsp;{{data[2].category}}</li>
              <li class="text-[#303b5a] font-bold">{{data[2].score}} <span class="text-[#c8c7ff]">/ 100</span></li>
            </ul>
          </button>        
          <button class="mt-4 relative overflow-hidden w-full p-[10px] rounded-[10px] bg-[#1125d4] bg-opacity-5">
            <div class="arc top-[2px] left-[-4px] rotate-[315deg]"></div>
            <div class="arc top-[2px] right-[-4px] rotate-[45deg]"></div>
            <div class="arc bottom-[2px] left-[-4px] rotate-[225deg]"></div>
            <div class="arc bottom-[2px] right-[-4px] rotate-[135deg]"></div>
            <ul class="flex justify-between">
              <li class="flex text-[#1125d4]"><img src="./assets/images/icon-visual.svg" alt="">&nbsp;{{data[3].category}}</li>
              <li class="text-[#303b5a] font-bold">{{data[3].score}} <span class="text-[#c8c7ff]">/ 100</span></li>
            </ul>
          </button>        
          <button class="my-4 lg:my-[30px] p-[15px] lg:p-[10px] text-white font-bold md:hover:bg-[#2e2be9] w-full bg-[#303b5a] rounded-full">Continue</button>
        </div>
      </article>
    </section>
  </main>
</template>

<style>
.arc {
  position: absolute;
  width: 20px;
  height: 10px;
  border-top: 1px solid rgba(120, 117, 117, 0.648);
  border-radius: 45% / 60% 60% 0 0;
}

.circle {
  background: #2421ca00, #4e21ca, #7857ff, 
  #2e2be9,
  hsl(0, 0%, 100%),
  #303b5a,
  #ebf1ff,
  hsl(241, 100%, 89%),
  #1125d4,
  #00bd91,
  #ffb01f,
  #ff5757;
}
</style>
