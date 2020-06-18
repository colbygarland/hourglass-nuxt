<template>
    <div class="">
        <nuxt-link exact to="/" :class="classes">
            <unicon name="apps" fill="#d6d6d6" icon-style="monochrome" width="25" height="25" class="mr-5"></unicon>
            Dashboard
        </nuxt-link>
        <nuxt-link exact to="/timesheets" :class="classes">
            <unicon name="clock" fill="#d6d6d6" icon-style="monochrome" width="25" height="25" class="mr-5"></unicon>
            Timesheets
        </nuxt-link>
        <nuxt-link exact to="/projects" :class="classes">
            <unicon name="grid" fill="#d6d6d6" icon-style="monochrome" width="25" height="25" class="mr-5"></unicon>
            Projects
        </nuxt-link>
        <nuxt-link exact to="/calendar" :class="classes">
            <unicon name="calender" fill="#d6d6d6" icon-style="monochrome" width="25" height="25" class="mr-5"></unicon>
            Calendar
        </nuxt-link>
        <nuxt-link exact to="/reports" :class="classes">
            <unicon name="chart" fill="#d6d6d6" icon-style="monochrome" width="25" height="25" class="mr-5"></unicon>
            Reports
        </nuxt-link>
    </div>
</template>

<script>
    export default {
        data(){
            return {
                classes: 'text-md font-bold text-gray-500 block mb-4 ease-in-out duration-500 hover:text-teal-500 lg:mb-10 flex align-center',
            }
        }
    }
</script>
