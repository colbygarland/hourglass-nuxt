<template>
    <img :src="selectedImage" alt="Leaves" class="min-h-screen max-h-screen w-full object-cover"  />
</template>

<script>
    export default {
        data () {
            return {
                images: [
                    require('~/assets/img/login/1.jpg'),
                    require('~/assets/img/login/2.jpg'),
                    require('~/assets/img/login/3.jpg'),
                    require('~/assets/img/login/4.jpg'),
                ],
                selectedImage: ''
            }
        },
        created () {
            const idx = Math.floor(Math.random() * this.images.length);
            this.selectedImage = this.images[idx]
        }
    }
</script>
