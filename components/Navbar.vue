<template>
    <div class="p-3 shadow lg:min-h-screen relative z-10">
        <div class="flex lg:block lg:px-3">
            <div>
                <nuxt-link to="/">
                    <img src="~/assets/img/logo-horizontal.png" alt="hourglass" class="w-40 lg:w-40" />
                </nuxt-link>
            </div>
            <div class="ml-auto lg:mt-20 lg:ml-0">
                <div class="mt-2 cursor-pointer lg:hidden relative">
                    <unicon v-on:click="menuHidden = !menuHidden" name="user-circle" fill="#777" height="30" width="30"></unicon>
                    <unicon v-on:click="isHidden = !isHidden" name="layer-group" fill="#777" icon-style="monochrome" width="30" height="30"></unicon>
                    <div class="absolute" style="top:50px; right:0;" v-if="menuHidden">
                        <userbarmenu @clicked="onClickChild" />
                    </div>
                </div>
                <div class="hidden lg:block">
                    <menuItems />
                </div>
            </div>
        </div>
        <div class="p-3 lg:hidden" v-if="isHidden">
            <menuItems @clicked="onClickChild" />
        </div>
    </div>
</template>

<script>
    import menuItems from '~/components/Menu';
    import userbarmenu from '~/components/UserBarMenu';

    export default {
        data(){
            return {
                isHidden: false,
                menuHidden: false,
            }
        },
        methods: {
            onClickChild(){
                this.isHidden = false;
                this.menuHidden = false;
            }
        },
        components: {
            'menuItems': menuItems,
            'userbarmenu': userbarmenu,
        }
    }
</script>
