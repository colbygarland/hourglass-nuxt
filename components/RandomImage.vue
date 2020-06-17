<template>
    <img :src="selectedImage" alt="Leaves" class="max-h-screen w-full object-cover"  />
</template>

<script>
    export default {
        data () {
            return {
                images: [
                    '~/assets/img/login/1.jpg',
                    '~/assets/img/login/2.jpg',
                    '~/assets/img/login/3.jpg',
                    '~/assets/img/login/4.jpg',
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
