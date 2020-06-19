<template>
    <div class="rounded-full bg-white shadow px-6 py-2 text-gray-500 relative">
        <p v-on:click="isHidden = !isHidden" class="flex items-center cursor-pointer select-none">
            Colby Garland
            <svg class="-mr-1 ml-2 h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z" clip-rule="evenodd"/>
            </svg>
        </p>
        <div class="absolute right-0" style="top:50px;" v-if="isHidden">
            <userbarmenu @clicked="onClickChild" />
        </div>
    </div>
</template>

<script>
    import userbarmenu from '~/components/UserBarMenu';

    export default {
        data() {
            return {
                isHidden: false,
            }
        },
        methods: {
            close(e){
                if (! this.$el.contains(e.target)) {
                    this.isHidden = false
                }
            },
            onClickChild(val){
                this.isHidden = false;
            }
        },
        components: {
            'userbarmenu': userbarmenu,
        },
        mounted () {
            document.addEventListener('click', this.close)
        },
        beforeDestroy () {
            document.removeEventListener('click',this.close)
        }
    }
</script>
