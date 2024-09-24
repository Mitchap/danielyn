<!-- <template>
    <main>
        <div class="flex items-center justify-center h-screen flex-col gap-10">
            <!-- bind img src -->
<img id="cat_image" :src="imageSource" alt="" class="w-40 h-40 md:w-64 md:h-64">
<h1 class="text-lg font-medium md:text-2xl">Will you still be my girlfriend, <span class="font-bold">Danielyn</span>?
</h1>
<div class="flex flex-col md:flex-row items-center gap-5">
    <button @click="yes_button" type="button"
        class="transition duration-400 p-4 bg-pink-400 hover:bg-pink-600 hover:text-neutral-100 rounded-lg ">
        Absolutely!
    </button>
    <button type="button"
        class="transition duration-400 p-4 bg-gray-400 hover:bg-red-600 hover:text-neutral-100 rounded-lg ">
        Nooo!
    </button>
</div>
</div>
</main>

</template>

<script>
import { createApp, ref } from 'vue'

createApp({
    setup() {
        return {
            imageSource: 'images/cat_heart1.gif', // Initial image
            image1: 'images/cat_heart2.gif',      // First image source
            // image2: 'https://via.placeholder.com/300x200?text=Image+2',      // Second image source
        };
    },
    methods: {
        // Method to switch between images
        yes_button() {
            this.imageSource = this.imageSource === this.image1;
        }
    }
}).mount('#app')
</script> -->