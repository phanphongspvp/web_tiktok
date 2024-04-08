<template>
    <div class="flex border-b py-6">
        <div class="cursor-pointer">
            <img 
                src="https://img.freepik.com/premium-photo/cute-asian-girl-kawaii-anime-avatar-ai-generative-art_225753-9233.jpg" 
                alt="avatar"
                width="60"
                class="rounded-full max-h-[60px]"
            >
        </div>
        <div class="pl-3 w-full px-4">
            <div class="flex items-center justify-between pb-0.5">
                <button>
                    <span class="font-bold hover:underline cursor-pointer">User name</span>
                    <span class="text-[13px] text-light text-gray-500 pl-1 cursor-pointer">User name</span>
                </button>
                <button class="border text-[15px] px-[21px] py-0.5 border-[#F02C56] text-[#F02C56] rounded-md font-semibold hover:bg-[#ffeef2]">
                    Follow
                </button>
            </div>
            <div class="text-[15px] break-words md:max-w-[400px] max-w-[300px]">
                This is post text
            </div>
            <div class="text-[14px] text-gray-500 pb-0.5">
                #fun #cool #SupperAwesome
            </div>
            <div class="text-[14px] pb-0.5 flex items-center font-semibold">
                <Icon name="mdi:music" size="17" />
                <span class="px-1">original sound - AWESOME</span>
                <Icon name="mdi:heart" size="20" />
            </div>

            <div class="mt-2 flex">
                <div class="relative min-h-[480px] max-h-[580px] max-w-[260px] flex items-center bg-black rounded-xl cursor-pointer">
                    <video 
                        class="rounded-xl object-cover mx-auto h-full"
                        muted
                        loop
                        ref="video"
                        src="/video.mp4"
                    />
                    <img 
                        class="absolute right-2 bottom-14"
                        src="~/assets/images/tiktok-logo-white.png" 
                        width="90"
                    />
                </div>
                <div class="relative mr-[75px]">
                    <div class="absolute bottom-0 pl-2">
                        <div class="pb-4 text-center">
                            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
                                <Icon name="mdi:heart" size="25" />
                            </button>
                            <span class="text-xs text-gray-800 font-semibold">1.2M</span>
                        </div>
                        <div class="pb-4 text-center">
                            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
                                <Icon name="bx:bxs-message-rounded-dots" size="25" />
                            </button>
                            <span class="text-xs text-gray-800 font-semibold">50K</span>
                        </div>
                        <div class="pb-4 text-center">
                            <button class="rounded-full bg-gray-200 p-2 cursor-pointer">
                                <Icon name="ri:share-forward-fill" size="25" />
                            </button>
                            <span class="text-xs text-gray-800 font-semibold">12k</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
const video = ref(null);

onMounted(() => video.value.play());
</script>