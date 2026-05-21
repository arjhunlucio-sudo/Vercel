<script>
</script>

<template>
    <div class="h-25 bg-blue-200 dark:bg-white">

        <div class=" flex justify-around gap-30 items-center ">
            <div class="flex mt-2 px-20">
                <img class=" rounded-full w-16 h-16 p-2" src="https://eastwatch.com/Content/images/Logo.png" alt=""
                    srcset="">
                <img class="h-7 mt-4" src="https://eastwatch.com/Content/images/LogoText.png" alt="">
            </div>
            <div class="flex align-center  text-md p-6 pl-9 text-blue-700 cursor-pointer text-gray-500">
                <h1 @click="navigate('Home')"
                    class="border- cursor-pointer text-center rounded-md  dark:text-rose-600  hover:bg-blue-800 hover:text-white px-5 py-2"
                    :class="activePage === 'Home' ? 'bg-sky-400' : 'bg-none'">Home
                </h1>
                <h1 @click="navigate('About')"
                    class="border- cursor-pointer dark:text-rose-600  rounded-md  hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'About' ? 'bg-sky-400' : 'bg-none'">About</h1>
                <h1 @click="navigate('Services')"
                    class="border- cursor-pointer rounded-md  dark:text-rose-600  hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'Services' ? 'bg-sky-400' : 'bg-none'">
                    Services</h1>


                <h1 @click="navigate('Contact')"
                    class="border- cursor-pointer dark:text-rose-600 text-blue-600  rounded-md  hover:bg-blue-800 hover:text-white text-center px-5 py-2"
                    :class="activePage === 'Contact' ? 'bg-sky-400' : 'bg-none'">
                    Contact </h1>
            </div>
            <div>
                <p class="w-100">Photos used with permission from <span class="text-blue-600">Unsplash</span></p>
            </div>


            <Modal v-if="showLogin" @closeModal="closeLogin" />
        </div>
    </div>
</template>
