<template>
    <div>
        <div class="flex bg-gray-100 min-h-screen min-w-full">
            <div class="m-auto pl-3 pr-3 md:w-1/2 sm:w-auto md:w-1/2 lg:w-1/3 lg:pl-12 lg:pr-12">
                <div class="max-w-sm m-auto block">
                    <div class="max-w-xs">
                        <img src="~/assets/img/logo.png" alt="Hourglass" class="" />
                    </div>
                    <div v-model="login.error.email" v-if="login.error.email" class="p-3 bg-red-500 text-white rounded">{{ login.error.email}}</div>
                    <form @submit.prevent="userLogin">
                        <div class="py-2">
                            <label class="block text-gray-700 text-sm font-bold mb-2">Email</label>
                            <input v-model="login.email" type="email" name="email" required autofocus
                                   class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"/>
                        </div>
                        <div class="py-2">
                            <label class="block text-gray-700 text-sm font-bold mb-2">Password</label>
                            <input v-model="login.password" type="password" name="password" required autofocus
                                   class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"/>
                        </div>
                        <div class="py-6">
                            <button :loading="login.loading" type="submit" class="px-8 py-2 bg-teal-400 text-white hover:bg-teal-500 font-bold rounded-lg ease-in-out duration-500 focus:outline-none">Login</button>
                        </div>
                    </form>
                </div>
            </div>
            <div class="hidden md:block md:w-1/2 lg:w-2/3">
                <randomImage />
            </div>
        </div>

    </div>
</template>

<script>
    import randomImage from '~/components/RandomImage';

    export default {
        data() {
            return {
                login: {
                    email: 'colbygarland@gmail.com',
                    password: '',
                    error: {
                        email: '',
                    },
                    hasError: false,
                    loading: 'Loading..',
                },
            }
        },
        components: {
            'randomImage': randomImage,
        },
        layout: 'unauth',
        methods: {
            async userLogin() {
                try {
                    let response = await this.$auth.loginWith('local', {data: this.login});
                    this.$router.push('/');
                } catch (err) {
                    console.log(err.response.data);
                    this.login.hasError = true;
                    this.login.error.email = err.response.data.errors.email[0];
                }
            }
        },
        auth: false,
    }
</script>
