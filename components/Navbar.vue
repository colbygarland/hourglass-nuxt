<template>
    <div class="p-3 shadow lg:min-h-screen relative z-10">
        <div class="flex lg:block lg:px-3">
            <div>
                <img src="~/assets/img/logo-horizontal.png" alt="hourglass" class="w-40 lg:w-40" />
            </div>
            <div class="ml-auto lg:mt-20 lg:ml-0">
                <div class="mt-2 cursor-pointer lg:hidden">
                    <unicon v-on:click="isHidden = !isHidden" name="layer-group" fill="#00d8b1" icon-style="monochrome" width="40" height="40"></unicon>
                </div>
                <div class="hidden lg:block">
                    <menuItems />
                </div>
            </div>
        </div>
        <div class="p-3 lg:hidden" v-if="isHidden">
            <menuItems />
        </div>
    </div>
</template>

<script>
    import menuItems from '~/components/Menu';

    export default {
        data(){
            return {
                isHidden: false
            }
        },
        methods: {
            showMenu(){
                this.$swal('hello');
            },
        },
        components: {
            'menuItems': menuItems,
        }
    }
</script>
