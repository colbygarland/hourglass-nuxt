<template>
    <div class="rounded-full bg-white shadow px-6 py-2 text-gray-500 relative">
        <p v-on:click="isHidden = !isHidden" class="flex items-center cursor-pointer select-none"><unicon class="mr-3" name="user-circle" fill="#a0aec0" height="20" width="20"></unicon> Hello, Colby Garland</p>
        <div class="absolute" style="top:50px;" v-if="isHidden">
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
