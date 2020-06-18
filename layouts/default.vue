<template>
    <div class="lg:flex">
        <div class="lg:w-64">
            <navbar />
        </div>
        <div class="p-5 bg-gray-100 w-full lg:min-h-screen">
            <searchbar />
            <nuxt/>
        </div>
    </div>
</template>

<script>
    import navbar from '~/components/Navbar';
    import searchbar from '~/components/Searchbar';

    export default {
        components: {
            'navbar': navbar,
            'searchbar': searchbar,
        },
    }
</script>
