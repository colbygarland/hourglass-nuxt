<template>
    <div class="rounded-full bg-white flex shadow max-w-2xl mb-5">
        <div class="py-2 pl-4 inline-block w-12">
            <unicon name="search" fill="#E2E8F0"  width="20" height="20"></unicon>
        </div>
        <input
            ref="search"
            type="text"
            class="py-2 active:border-none active:outline-none focus:border-none focus:outline-none w-64"
            placeholder='Search anything (Press "/" to focus)'
        />
    </div>
</template>

<script>
    export default {
        created() {
            window.addEventListener('keydown', (e) => {
                if (e.key === '/') {
                    this.$refs.search.focus();
                }
            });
        },
    }
</script>
