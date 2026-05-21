<script>
import Modal from '../Modal/Login.vue'
export default {
    components: {
        Modal
    },
    data() {
        return {
            showLogin: false,
            activePage: 'Home'
        }
    },
    methods: {
        showLoginbtn() {
            this.showLogin = true;
        },
        closeLogin() {
            this.showLogin = false;
        },
        navigate(page) {
            this.$emit('goToPage', page)
            this.activePage = page
        }
    }
}
</script>


<template>
    <div class="bg-blue-100 dark:bg-white flex items-center fixed w-full">

        <div class=" flex justify-around gap-30 items-center ">
            <div class="flex mt-2 px-20">
                <img class=" rounded-full w-16 h-16 p-2" src="https://eastwatch.com/Content/images/Logo.png" alt=""
                    srcset="">
                <img class="h-7 mt-4" src="https://eastwatch.com/Content/images/LogoText.png" alt="">
            </div>
            <div class="flex align-center  text-md  text-blue-700 cursor-pointer">
                <h1 @click="navigate('Home')"
                    class="border- cursor-pointer text-center rounded-md  dark:text-rose-600 dark:hover:bg-rose-800 hover:bg-blue-800 hover:text-white px-5 py-2"
                    :class="activePage === 'Home' ? 'bg-sky-400' : 'bg-none'">Home
                </h1>
                <h1 @click="navigate('About')"
                    class="border- cursor-pointer dark:hover:bg-rose-800 dark:text-rose-600 rounded-md hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'About' ? 'bg-sky-400' : 'bg-none'">About
                    Us</h1>
                <h1 @click="navigate('Services')"
                    class="border- cursor-pointer dark:hover:bg-rose-800 rounded-md dark:text-rose-600 hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'Services' ? 'bg-sky-400' : 'bg-none'">
                    Services</h1>


                <h1 @click="navigate('Contact')"
                    class="border- cursor-pointer dark:hover:bg-rose-800 dark:text-rose-600 rounded-md hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'Contact' ? 'bg-sky-400' : 'bg-none'">
                    Contact Us</h1>
            </div>
            <button @click="showLoginbtn"
                class="rounded-full h-10 w-30 text-md text-gray-500 cursor-pointer border border-4xl dark:hover:bg-rose-800 hover:bg-blue-800 hover:text-white dark:border-rose-800 dark:text-rose-600  border-blue-800">Login</button>
        </div>
        <Modal v-if="showLogin" @closeModal="closeLogin" />
    </div>

</template>