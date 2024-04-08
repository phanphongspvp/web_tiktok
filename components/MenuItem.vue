<template>
    <div class="w-full flex items-center p-2.5 rounded-md hover:bg-gray-100">
        <div class="flex items-center lg:mx-0 mx-auto">
            <Icon :name="icon" :color="colorString" :size="sizeString" />
            <span class="hidden lg:block pl-2.5 font-semibold text-[17px]">{{ iconString }}</span>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(["iconString", "colorString", "sizeString"]);
const { iconString, colorString, sizeString } = toRefs(props);

const icon = ref("");

if(iconString?.value === "For You") icon.value = "mdi:home";
if(iconString?.value === "Following") icon.value = "ci:group";
if(iconString?.value === "LIVE") icon.value = "ri:live-line";
</script>