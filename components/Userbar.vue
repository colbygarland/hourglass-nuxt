<template>
    <div class="rounded-full bg-white shadow px-6 py-2 text-gray-500 relative">
        <p v-on:click="isHidden = !isHidden" class="flex items-center cursor-pointer"><unicon class="mr-3" name="user-circle" fill="#a0aec0" height="20" width="20"></unicon> Hello, Colby Garland!</p>
        <div class="absolute" style="top:50px;" v-if="isHidden">
            <userbarmenu />
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
        },
        components: {
            'userbarmenu': userbarmenu,
        }
    }
</script>
