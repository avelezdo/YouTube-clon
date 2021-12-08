<template>
    <header class="flex justify-between items-center p-2 shadow">
        <!-- !<IconYoutube :width="100" :height="100" /> en este caso da igual pasarle Number (:width="100") o String (width="100")-->
        <IconYoutube width="100" height="20" />
        <div class="flex">
            <IconSearch width="24" height="24" />
            <img
                class="w-8 h-8 rounded-full ml-6"
                alt="youtube user image profile"
                src="https://yt3.ggpht.com/yti/APfAmoFweTgj_KFpU6SuOWrp8Z13tYJDDVyEhdWKfaCpXQ=s88-c-k-c0x00ffffff-no-rj"
            />
        </div>
    </header>
</template>

<script setup>
import IconYoutube from './icons/iconYoutube.vue'
import IconSearch from './icons/iconSearch.vue'
</script>
