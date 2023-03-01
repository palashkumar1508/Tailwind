<template>

  

  <div :class="{bcDark:darkM}" class="md:bg-green-300  flex sm:bg-white h-[900px]">

      <div :class="{bcDark:darkM}" class="bg-green-500  sm:full md:w-1/2 my-auto rounded-lg mx-auto h-[600px]">
        
        <div  class="mx-96 ">
      <button :class="{btnDark:darkM}" class="p-5 bg-black text-white rounded-2xl" @click="onOff(dec)">{{ dec }}</button>

    </div>
        
        <div class="text-white text-3xl font-bold flex  justify-center mt-9">
          <h1>USER LOGIN <hr></h1>
          <!-- <div class="bg-white w-9 h-1"></div> -->
        </div>

        <div class="mt-16 mx-auto ">
          <div class="mt-[40px] flex justify-center">
            <i class="fa-solid text-white fa-2xl my-auto mx-10 fa-user"></i>
            <input type="text" placeholder="Username" class="h-[60px] sm:px-1 md:px-6 sm:text-center md:text-left font-semibold  rounded-full" >
          </div>
          
          <div class="mt-[40px] flex justify-center">
            <i class="fa-solid fa-2xl text-white my-auto mx-10 fa-lock"></i>
            <input type="text" placeholder="Password" class="h-[60px] sm:px-1 md:px-6 sm:text-center md:text-left font-semibold  rounded-full" >
          </div>
          
          <div class="mt-[40px] flex justify-center">
            <i class="fa-solid fa-2xl text-white my-auto mx-10 fa-right-to-bracket"></i>
            <input type="button" value="LOGIN" class="h-[60px] bg-white sm:px-12 md:px-32 sm:text-center md:text-left text-green-500 hover:cursor-pointer font-semibold rounded-full" >
          </div>
          <div :class="{fontD:darkM}" class="mt-[45px] flex justify-center font-bold hover:cursor-pointer text-xl text-slate-600 ">
            <h3>Forgot password? </h3>
          </div>
        </div>


      </div>
    
    
  </div>
</template>

<script setup>
import { ref } from 'vue';

let darkM = ref(false);
let dec = ref("Dark");
function onOff(val){
  if(val == "Light"){
    darkM = false;
  dec.value = "Dark"
  }else{
    darkM = true;
    dec.value = "Light"
  }
}

</script>


<style scoped>

.bcDark {
    @apply bg-black border border-white 
  }
  .fontD{
    @apply text-[#0AE823]
  }

  .btnDark {
    @apply bg-green-500 text-white 
  }

</style>
