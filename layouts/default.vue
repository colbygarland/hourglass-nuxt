<template>
    <div>
        <navbar />
        <div class="p-5">
            <nuxt/>
        </div>
    </div>
</template>

<script>
    import navbar from '~/components/Navbar';

    export default {
        components: {
            'navbar': navbar,
        },
    }
</script>
