<script>
export default {
    data() {

    },
    methods: {
        closeLogin() {
            this.$emit('closeModal')
        }
    }
}
</script>
<template>
        <div @click="closeLogin" class="w-full h-screen fixed top-0 bg-black/5"></div>
        <div class="fixed right-5 top-20 border border-blue-900  border border-3 h-50  bg-white p-5 w-fit shadow-xl flex flex-col space-y-5">
            <input class="rounded-full" type="text" placeholder="Username">
            <input class="rounded-full" type="text" placeholder="Password">
            <button class="border-1 border-blue-800 rounded-full  ">Login</button>
            <button class="border-1 border-blue-800 rounded-full  ">Cancel</button>
        </div>
</template>