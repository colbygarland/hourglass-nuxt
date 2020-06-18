<template>
    <div class="lg:flex">
        <div class="lg:w-64">
            <navbar />
        </div>
        <div class="p-5 bg-gray-100 w-full lg:min-h-screen">
            <div class="hidden lg:flex mb-5">
                <searchbar />
                <userbar />
            </div>
            <nuxt/>
        </div>
    </div>
</template>

<script>
    import navbar from '~/components/Navbar';
    import searchbar from '~/components/Searchbar';
    import userbar from '~/components/Userbar';

    export default {
        components: {
            'navbar': navbar,
            'searchbar': searchbar,
            'userbar': userbar,
        },
    }
</script>
