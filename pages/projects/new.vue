<template>
    <div>
        <form>
            <heading>Add New Project</heading>
            <div class="block lg:flex mb-3 mt-3">
                <div class="lg:w-1/2 mr-5">
                    <card class="mb-5">
                        <heading2>Client</heading2>
                        <p class="text-gray-600 mb-3 text-sm">Select a client from the list, or create a new client.</p>

                        <formfield>
                            <Label>Client</Label>
                            <Select2 class="w-full" v-model="values.client" :options="options.client" :settings="{width: '100%'}" />
                        </formfield>
                    </card>
                    <card>
                        <heading2>Project</heading2>
                        <formfield>
                            <Label>Name</Label>
                            <input type="text" name="name" required class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"/>
                        </formfield>
                        <formfield>
                            <Label>Work Order #</Label>
                            <input type="text" name="name" required class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"/>
                        </formfield>
                        <div class="mb-3 flex relative">
                            <Label>Description</Label>
                            <textarea class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"></textarea>
                        </div>
                        <formfield>
                            <Label>Timesheet Category</Label>
                            <select required class="block appearance-none w-full bg-white border border-gray-400 hover:border-gray-500 px-4 py-2 pr-8 rounded shadow leading-tight focus:outline-none focus:shadow-outline">
                                <option value="-1">Select category</option>
                                <option>Admin</option>
                            </select>
                            <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                                <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/></svg>
                            </div>
                        </formfield>
                        <formfield>
                            <Label>Status</Label>
                            <select required class="block appearance-none w-full bg-white border border-gray-400 hover:border-gray-500 px-4 py-2 pr-8 rounded shadow leading-tight focus:outline-none focus:shadow-outline">
                                <option value="-1">Select status</option>
                                <option>Active</option>
                            </select>
                            <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
                                <svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"/></svg>
                            </div>
                        </formfield>
                    </card>
                </div>
                <div class="lg:w-1/2">
                    <card>
                        <heading2>Tasks</heading2>
                    </card>
                </div>
            </div>
        </form>
    </div>
</template>

<script>
    import heading from '~/components/heading';
    import card from '~/components/Card';
    import formfield from '~/components/FormField';
    import Label from '~/components/Label';
    import helper from '~/components/HelperText';
    import heading2 from '~/components/heading2';
    import Select2 from 'v-select2-component';

    export default {
        layout: 'default',
        components: {
            'heading': heading,
            'card': card,
            'formfield': formfield,
            'Label': Label,
            'helper': helper,
            'heading2': heading2,
            'Select2': Select2,
        },
        data(){
            return {
                values: {
                    client: '',
                },
                options: {
                    clients: ['opt1', 'opt2'],
                }
            }
        }
    }
</script>
