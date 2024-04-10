<template>
    <UploadLayout>
        <div class="w-full mt-[80px] mb-[40px] bg-white shadow-lg rounded-md py-6 md:px-10 px-4">
            <div>
                <div class="text-[23px] font-semibold">Upload video</div>
                <div class="text-gray-400 mt-1">Post a video to your account</div>
            </div>

            <div class="mt-8 md:flex gap-6">
                <label 
                    v-if="false"
                    for="fileInput"
                    class="
                        md:mx-0
                        mx-auto
                        mt-4
                        mb-6
                        flex
                        flex-col
                        items-center
                        justify-center
                        w-full
                        max-w-[260px]
                        h-[470px]
                        text-center
                        p-3
                        border-2
                        border-dashed
                        border-gray-300
                        rounded-lg
                        hover:bg-gray-100
                        cursor-pointer
                    "
                >
                    <Icon name="majesticons:cloud-upload" size="40" color="#b3b3b1" />
                    <div class="mt-4 text-[17px]">Select video to upload</div>
                    <div class="mt-1.5 text-gray-500 text-[13px]">Or drag and drop a file</div>
                    <div class="mt-12 text-gray-500 text-sm">MP4</div>
                    <div class="mt-2 text-gray-500 text-[13px]">Up to 30 minutes</div>
                    <div class="mt-2 text-gray-500 text-[13px]">Less than 2 GB</div>
                    <div class="px-2 py-1.5 mt-8 text-white bg-[#F02C56] text-[15px] rounded-sm w-[80%]">
                        Select
                    </div>
                    <input 
                        type="file" 
                        id="fileInput" 
                        hidden
                        accept=".mp4"
                    >
                </label>

                <div 
                    v-else
                    class="
                        md:mx-0
                        mx-auto
                        mt-4
                        md:mb-12
                        mb-16
                        flex
                        items-center
                        justify-center
                        w-full
                        max-w-[260px]
                        h-[540px]
                        p-3
                        rounded-2xl
                        cursor-pointer
                        relative
                    "    
                >
                    <div class="bg-black w-full h-full"></div>
                    <img 
                        src="~/assets/images/mobile-case.png" 
                        class="absolute z-20 pointer-events-none" 
                    />
                    <img 
                        src="~/assets/images/tiktok-logo-white.png" 
                        class="absolute z-20 right-4 bottom-6" 
                        width="90"
                    />
                    <video
                        autoplay
                        loop
                        muted
                        class="object-cover absolute w-full h-full z-10 p-[13px]" 
                        src="/video.mp4"
                    ></video>

                    <div class="absolute -bottom-12 flex items-center justify-between z-50 rounded-xl border w-full p-1.5 border-gray-300">
                        <div class="flex items-center truncate">
                            <Icon name="clarity:success-standard-line" size="16" class="min-w-[16px]" />
                            <div class="text-[14px] pl-1 truncate text-ellipsis">video.mp4</div>
                        </div>
                        <button class="text-[11px] ml-2 font-semibold">Change</button>
                    </div>
                </div>

                <div class="mt-4 mb-6">
                    <div class="flex bg-[#F8F8F8] py-4 px-6">
                        <div>
                            <Icon name="mdi:box-cutter-off" size="20" class="mr-4" />
                        </div>
                        <div>
                            <div class="font-semibold text-[15px] mb-1.5">Divide videos and edit</div>
                            <div class="font-semibold text-[13px] text-gray-400">
                                You can quickly divide videos into multiple parts, remove redundant parts and turn landscape videos into portrait videos
                            </div>
                        </div>
                        <div class="flex justify-end max-w-[130px] w-full h-full text-center my-auto">
                            <button class="px-8 py-1.5 bg-[#F02C56] text-white text-[15px] rounded-sm">Edit</button>
                        </div>
                    </div>

                    <div class="mt-5">
                        <div class="flex items-center justify-between">
                            <div class="mb-1 text-[15px]">Caption</div>
                            <div class="text-gray-400 text-[12px]">0/150</div>
                        </div>
                        <input 
                            v-model="caption"
                            type="text"
                            maxlength="150"
                            class="w-full border p-2.5 rounded-md focus:outline-none"
                        >
                    </div>

                    <div class="flex gap-3">
                        <button class="px-10 py-2.5 mt-8 border text-[16px] hover:bg-gray-100 rounded-sm">Discard</button>
                        <button class="px-10 py-2.5 bg-[#F02C56] text-white mt-8 border text-[16px] rounded-sm">Post</button>
                    </div>

                    <div>
                        <div class="text-red-600">

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </UploadLayout>
</template>

<script setup>
import UploadLayout from '~/layouts/UploadLayout.vue';

const caption = ref("");

</script>