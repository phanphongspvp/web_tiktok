<template>
    <div class="flex items-center w-full py-1.5 px-2 gap-1.5 rounded-md hover:bg-gray-100">
        <img 
            src="https://img.freepik.com/premium-photo/cute-asian-girl-kawaii-anime-avatar-ai-generative-art_225753-9233.jpg" 
            alt="avatar"
            width="35"
            class="rounded-full lg:mx-0 mx-auto"
        >
        <div class="lg:pl-2.5 lg:flex lg:flex-col hidden">
            <div class="flex items-center">
                <span class="font-bold text-[14px]">User name</span>
                <div class="ml-1 bg-[#58D5EC] h-[14px] rounded-full relative">
                    <Icon 
                        class="relative -top-[7px]"
                        name="teenyicons:tick-small-solid"
                        color="#ffffff"
                        size="15" 
                    />
                </div>
            </div>
            <span class="font-light text-[12px] text-gray-600">
                User name
            </span>
        </div>
    </div>
</template>

<script setup>

</script>