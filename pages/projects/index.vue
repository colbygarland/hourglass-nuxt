<template>
    <section class="section">
        <div class="mb-5">
            <div class="flex items-center">
                <heading>Projects</heading>
                <div class="ml-auto">
                    <nuxt-link to="/projects/new" class="bg-blue-500 text-white px-6 py-2 font-bold text-sm rounded-full flex items-center hover:bg-teal-600">
                        <unicon name="plus" fill="#fff" height="15" width="15" class="mr-3"></unicon>
                        New Project
                    </nuxt-link>
                </div>
            </div>

        </div>
        <div class="shadow">
            <table class="w-full">
                <thead>
                <tr class="border-b-2">
                    <th class="rounded-l rounded-bl text-gray-500 text-xs bg-gray-200 text-left pl-2 py-3">Work Order</th>
                    <th class="text-gray-500 text-xs bg-gray-200 text-left pl-2 py-3">Client</th>
                    <th class="text-gray-500 text-xs bg-gray-200 text-left pl-2 py-3">Project</th>
                    <th class="text-gray-500 text-xs bg-gray-200 text-left pl-2 py-3">Deadline</th>
                    <th class="text-gray-500 text-xs bg-gray-200 text-left pl-2 py-3">Updated At</th>
                    <th class="rounded-r rounded-br text-xs text-gray-500 bg-gray-200 py-3"></th>
                </tr>
                </thead>
                <tbody>
                <tr class="bg-white">
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <nuxt-link to="/projects/123" class="hover:text-teal-400 ease-in-out duration-500">05009</nuxt-link>
                    </td>
                    <td class="pl-2 text-sm py-3 font-semibold">imageDESIGN</td>
                    <td class="pl-2 text-sm py-3 font-semibold">ID Website Updates</td>
                    <td class="pl-2 text-sm py-3 font-semibold">-</td>
                    <td class="pl-2 text-sm py-3 font-semibold">June 18, 2020   2:27pm</td>
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <div class="cursor-pointer">
                            <unicon name="ellipsis-v" fill="#888" height="15" width="15"></unicon>
                        </div>
                    </td>
                </tr>
                <tr class="bg-gray-100">
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <nuxt-link to="/projects/123">05009</nuxt-link>
                    </td>
                    <td class="pl-2 text-sm py-3 font-semibold">imageDESIGN</td>
                    <td class="pl-2 text-sm py-3 font-semibold">ID Website Updates</td>
                    <td class="pl-2 text-sm py-3 font-semibold">-</td>
                    <td class="pl-2 text-sm py-3 font-semibold">June 18, 2020   2:27pm</td>
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <div class="cursor-pointer">
                            <unicon name="ellipsis-v" fill="#888" height="15" width="15"></unicon>
                        </div>
                    </td>
                </tr>
                <tr class="bg-white">
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <nuxt-link to="/projects/123">05009</nuxt-link>
                    </td>
                    <td class="pl-2 text-sm py-3 font-semibold">imageDESIGN</td>
                    <td class="pl-2 text-sm py-3 font-semibold">ID Website Updates</td>
                    <td class="pl-2 text-sm py-3 font-semibold">-</td>
                    <td class="pl-2 text-sm py-3 font-semibold">June 18, 2020   2:27pm</td>
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <div class="cursor-pointer">
                            <unicon name="ellipsis-v" fill="#888" height="15" width="15"></unicon>
                        </div>
                    </td>
                </tr>
                <tr class="bg-gray-100">
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <nuxt-link to="/projects/123">05009</nuxt-link>
                    </td>
                    <td class="pl-2 text-sm py-3 font-semibold">imageDESIGN</td>
                    <td class="pl-2 text-sm py-3 font-semibold">ID Website Updates</td>
                    <td class="pl-2 text-sm py-3 font-semibold">-</td>
                    <td class="pl-2 text-sm py-3 font-semibold">June 18, 2020   2:27pm</td>
                    <td class="pl-2 text-sm py-3 font-semibold">
                        <div class="cursor-pointer">
                            <unicon name="ellipsis-v" fill="#888" height="15" width="15"></unicon>
                        </div>
                    </td>
                </tr>
                </tbody>
            </table>
            <div class="bg-white px-4 py-1 flex items-center justify-between border-t border-gray-200 sm:px-6">
                <div class="sm:flex-1 sm:flex sm:items-center sm:justify-between">
                    <div>
                        <p class="text-sm leading-5 text-gray-700">
                            Showing
                            <span class="font-medium">1</span>
                            to
                            <span class="font-medium">10</span>
                            of
                            <span class="font-medium">97</span>
                            results
                        </p>
                    </div>
                    <div>
                        <nav class="relative z-0 inline-flex shadow-sm">
                            <button type="button" class="relative inline-flex items-center px-2 py-2 rounded-l-md border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-500 hover:text-gray-400 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-500 transition ease-in-out duration-150" aria-label="Previous">
                                <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                                    <path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </button>
                            <button type="button" class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                1
                            </button>
                            <button type="button" class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                2
                            </button>
                            <button type="button" class="hidden md:inline-flex -ml-px relative items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                3
                            </button>
                            <span class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700">
          ...
        </span>
                            <button type="button" class="hidden md:inline-flex -ml-px relative items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                8
                            </button>
                            <button type="button" class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                9
                            </button>
                            <button type="button" class="-ml-px relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-700 hover:text-gray-500 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-700 transition ease-in-out duration-150">
                                10
                            </button>
                            <button type="button" class="-ml-px relative inline-flex items-center px-2 py-2 rounded-r-md border border-gray-300 bg-white text-sm leading-5 font-medium text-gray-500 hover:text-gray-400 focus:z-10 focus:outline-none focus:border-blue-300 focus:shadow-outline-blue active:bg-gray-100 active:text-gray-500 transition ease-in-out duration-150" aria-label="Next">
                                <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                                    <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </button>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import card from '~/components/Card';
    import heading from '~/components/heading';

    export default {
        layout: 'default',
        components: {
            'card': card,
            'heading': heading,
        }
    }
</script>
