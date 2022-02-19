<template>
<div class="w-full min-h-screen font-sans text-gray-900 bg-gradient-to-br from-transparent to-green-100">

  <nav class="flex items-center justify-between px-24 py-8 max-w-screen-xl mx-auto">
    <a href="" class="text-4xl font-bold tracking-wide">Organ<span class="text-green">o</span></a>
    <ul class="flex items-center space-x-8">
      <li v-for="menu in menus" :key="menu" class="texl font-medium group" :class="{'text-green' : activeMenu == menu }" >
        <a href="">{{menu}}</a>
        <div class="h-0.5 bg-green scale-x-0 group-hover:scale-100 transition-transform origin-left rounded-full duration-300 ease-out "></div>
      </li>
    </ul>
     <button
          class="flex justify-center items-center h-13 px-7 font-medium text-white bg-green rounded-xl hover:shadow-primary transition-shadow duration-300 whitespace-nowrap">
          Get started
        </button>
  </nav>

  <div class="flex justify-between px-24 py-8 max-w-screen-xl mx-auto">
    <div class="max-w-md">
      <span class="flex items-center px-1 text-xl text-green">
        <span>100% Organic food</span>
        <img class="h-10 w-auto" src="/img/vegetable.png" alt="">
      </span>
      
      <h1 class="pt-4 text-6xl font-bold tracking-tighter leading-tight">Healthy Lifestyle is your 
        <span class="whitespace-nowrap text-green">unfair advantage</span></h1>
      <p class="pt-8 text-lg font-normal text-gray-600 leading-relaxed">Choose healthy habits with Organo 
        daily meal prepared by our expert nutritionist</p>
      <div class="flex pt-8 space-x-4 sm:space-x-6">
        <button
          class="flex justify-center items-center w-full sm:w-auto h-13 px-8 bg-green font-medium text-white rounded-xl whitespace-nowrap hover:shadow-primary transition-shadow duration-300"
        >
          Get started
        </button>
        <button
          class="flex justify-center items-center w-full sm:w-auto h-13 px-8 font-medium text-gray-900 border border-gray-800 rounded-xl whitespace-nowrap hover:shadow-xl transition-shadow duration-300"
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
    </div>

    <div class="flex-1 flex flex-col relative">
      <img class="max-w-xl drop-shadow-2xl self-end" src="/img/dish.png" alt="">
       <div class="absolute right-0 lg:-right-6 top-0 lg:top-28 flex flex-col py-5 px-7 rounded-2xl shadow-xl bg-white backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300">
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
            <!-- <StarIcon class="w-5 h-5" /> -->
            <span class="pl-1">4.9 (+2.5k Ratings)</span>
          </div>
        </div>

        <div
          class="absolute left-0 bottom-0 md:bottom-32 lg:bottom-16 flex bg-white rounded-2xl shadow-xl backdrop-blur-xl hover:-translate-y-2 hover:shadow-2xl transition-all duration-300"
        >
          <img class="w-auto h-20 self-end" src="/img/driver.png" alt="" />
          <div class="pr-7 pl-2 py-5">
            <div class="font-bold">Fast delivery</div>
            <div class="text-gray-600 leading-relaxed">30 mins delivery 🚀</div>
          </div>
        </div>
        
    </div>



  </div>


</div>
  
</template>

<script>


export default {
  name: 'Home',
  components: {
  
  },
  data(){
    return{
      menus: ["Home", "Delivery","Pricing","FAQs","Contact"],
      activeMenu : 'Home'
    }
  }
}
</script>
