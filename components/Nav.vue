<template>
    <div class="fixed z-30 w-full h-[61px] border-b bg-white flex items-center justify-center">
        <div class="flex items-center justify-between w-full px-6 mx-auto max-w-[1150px]">
            <NuxtLink to="/">
                <img src="/assets/images/tiktok-logo.png" alt="Logo" width="115">
            </NuxtLink>
            <div class="hidden md:flex items-center max-w-[300px] border p-1 w-full bg-[#F1F1F2] rounded-full">
                <input 
                    class="w-full focus:outline-none bg-transparent pl-3 my-2 placeholder-[#838383] text-[15px]" 
                    type="text" 
                    placeholder="Search accounts">
                <div class="px-3 py-1 flex items-center justify-center border-l border-l-gray-300">
                    <Icon name="ri:search-line" size="22" color="#A1A2A7" />
                </div>
            </div>
            <div class="flex items-center gap-3">
                <button class="flex justify-center items-center border rounded-md px-3 py-1.5 hover:bg-gray-100">
                    <Icon name="mdi:plus" size="22" color="#000000" />
                    <span class="font-medium px-2 text-[15px]">Upload</span>
                </button>
                <div v-if="false" class="flex items-center">
                    <button class="flex justify-center items-center border rounded-md px-3 py-1.5 bg-[#F02C56] text-white">
                        <span class="font-medium px-4 text-[15px]">Log in</span>
                    </button>
                    <Icon name="mdi:dots-vertical" size="25" color="#161724" />
                </div>
                <div v-else class="flex items-center gap-5">
                    <Icon name="carbon:send-alt" size="30" color="161724" />
                    <Icon name="bx:message-detail" size="27" color="161724" />
                    <div class="relative">
                        <button class="mt-1" @click="$e => showMenu = !showMenu">
                            <img 
                                src="https://img.freepik.com/premium-photo/cute-asian-girl-kawaii-anime-avatar-ai-generative-art_225753-9233.jpg" 
                                alt="avatar"
                                width="33"
                                class="rounded-full"
                            >
                        </button>

                        <div v-if="showMenu" id="popupMenu"class="absolute bg-white rounded-lg py-1.5 w-[200px] shadow-xl border top-[43px] -right-2">
                            <NuxtLink to="/profile" class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer gap-2">
                                <Icon name="mdi:user" size="20" />
                                <span class="font-semibold text-sm">Profile</span>
                            </NuxtLink>
                            <div to="/profile" class="flex items-center justify-start py-3 px-2 hover:bg-gray-100 cursor-pointer gap-2">
                                <Icon name="ic:outline-login" size="20" />
                                <span class="font-semibold text-sm">Log out</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const showMenu = ref(false);

onMounted(() => {
    document.addEventListener("mouseup", function(e) {
        const popupMenu = document.getElementById("popupMenu");
        if(!popupMenu?.contains(e.target)) {
            showMenu.value = false;
        }
    })
});
</script>