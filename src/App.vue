<template>
  <main class="relative overflow-hidden">
    <div class="flex items-center justify-center h-screen flex-col gap-10">

      <img :src="catImage" alt="Cat" class="max-w-40 max-h-40 md:max-w-64 md:max-h-64">
      <h1 v-if="!buttonClicked" class="text-lg font-medium md:text-2xl">Will you still be my girlfriend, <a
          href="https://www.facebook.com/danielyn.pantonial.5" class="font-bold hover:text-pink-600">Danielyn</a>?</h1>
      <h1 v-else class="text-lg font-medium md:text-2xl ">Yipeeeee
        <br><br>
        <span class="fa-regular"> I <i class="fa-regular fa-solid fa-heart fa-bounce"></i> YOU</span>
      </h1>


      <div v-if="!buttonClicked" class="flex flex-col md:flex-row items-center gap-10">

        <button id="approve_btn" @click="approve" type="button"
          class="transition duration-400 p-2 md:p-4 bg-pink-400 hover:bg-pink-600 hover:text-neutral-100 rounded-lg">
          Absolutely!
        </button>
        <button @mouseenter="moveNoButton" type="button" :style="noButtonStyle"
          class="transition duration-400 p-2 md:p-4 bg-gray-400 hover:bg-red-600 hover:text-neutral-100 rounded-lg absolute">
          No!
        </button>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      catImage: '/images/cat_heart1.gif',
      buttonClicked: false,
      noButtonStyle: {
        left: '50%',
        top: '10%',
      }
    };
  },
  methods: {
    approve() {
      this.catImage = '/images/cat_heart2.gif';
      this.buttonClicked = true;
    },
    moveNoButton() {
      const randomX = Math.floor(Math.random() * (window.innerWidth - 200)); // Random X within the viewport
      const randomY = Math.floor(Math.random() * (window.innerHeight - 200)); // Random Y within the viewport
      this.noButtonStyle = {
        left: `${randomX}px`,
        top: `${randomY}px`,
        position: 'absolute',

      };
    }
  },
};


</script>
