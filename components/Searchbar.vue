<template>
    <div class="rounded-full bg-white flex shadow flex-grow mr-16 ">
        <div class="py-2 pl-4 inline-block max-w-2xl flex items-center">
            <unicon name="search" fill="#a0aec0"  width="20" height="20"></unicon>
        </div>
        <input
            ref="search"
            type="text"
            class="py-2 active:border-none active:outline-none focus:border-none focus:outline-none w-full pl-3 text-gray-500"
            placeholder='Search anything (Press "/" to focus)'
            v-on:keyup.esc="blur"
        />
        <div class="inline-block w-10"></div>
    </div>
</template>

<script>
    export default {
        created() {
            window.addEventListener('keyup', (e) => {
                if (e.key === '/') {
                    this.$refs.search.focus();
                }
            });
        },
        methods: {
            blur(){
                this.$refs.search.blur()
            }
        }
    }
</script>
