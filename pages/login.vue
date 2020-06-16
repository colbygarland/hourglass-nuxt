<template>
    <div>
        <div class="flex bg-gray-100 min-h-screen min-w-full">
            <div class="m-auto pl-3 pr-3 md:w-1/2 sm:w-auto md:w-1/2 lg:w-1/3 lg:pl-12 lg:pr-12">
                <div class="max-w-sm m-auto block">
                    <h1 class="text-4xl font-bold mb-2">Login to Hourglass</h1>
                    <form @submit.prevent="userLogin">
                        <div class="py-2">
                            <label class="block pb-1 font-bold">Email</label>
                            <input v-model="login.email" type="email" name="email" required autofocus
                                   placeholder="Enter email address" class="border-2 p-1 w-full"/>
                        </div>
                        <div class="py-2">
                            <label class="block pb-1 font-bold">Password</label>
                            <input v-model="login.password" type="password" name="password" required autofocus
                                   class="border-2 p-1 w-full"/>
                        </div>
                        <div class="py-6">
                            <button type="submit" class="px-8 py-2 bg-teal-500 text-white hover:bg-teal-600 font-bold rounded-lg">Login</button>
                        </div>
                    </form>
                </div>
            </div>
            <div class="hidden md:block md:w-1/2 lg:w-2/3">
                <img src="~/assets/img/leaves.jpg" alt="Leaves" class="max-h-screen w-full object-cover"  />
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        data() {
            return {
                login: {
                    email: '',
                    password: '',
                }
            }
        },
        layout: 'default',
        methods: {
            async userLogin() {
                try {
                    let response = await this.$auth.loginWith('local', {data: this.login});
                    console.log(response);
                    this.$router.push('/');
                } catch (err) {
                    console.log(err);
                }
            }
        },
        auth: false,
    }
</script>
