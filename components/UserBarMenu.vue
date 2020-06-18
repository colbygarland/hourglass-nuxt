<template>
    <ul class="px-3 py-3 shadow bg-white rounded w-32">
        <li class="mb-2" @click="onClick">
            <nuxt-link exact to="/profile">
                My Profile
            </nuxt-link>
        </li>
        <li>
            Logout
        </li>
    </ul>
</template>

<script>
    export default {
        data() {
            return {
                state: false,
            }
        },
        methods: {
            onClick(event){
                this.$emit('clicked', this.state);
            }
        }
    }
</script>
