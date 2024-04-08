<template>
    <div class="fixed z-20 lg:w-[310px] pt-[70px] h-full mx-auto bg-white w-[75px] overflow-auto">
        <div class="lg:w-full w-[55px] mx-auto">
            <div>
                <MenuItem iconString="For You" sizeString="30" colorString="#F02C56" />
                <MenuItem iconString="Following" sizeString="27" colorString="#000000" />
                <MenuItem iconString="LIVE" sizeString="27" colorString="#000000" />
            </div>
            <div class="border-b mt-2 lg:ml-2"></div>
            <div>
                <div class="lg:block hidden text-xs text-gray-600 font-semibold pt-4 pb-2 px-2">
                    Suggested accounts
                </div>
                <div class="lg:hidden block mt-3"></div>
                <div class="cursor-pointer">
                    <MenuItemFollow />
                </div>
                <button class="lg:block hidden text-[#F02C56] pt-1.5 pl-2 text-[13px]">
                    See more
                </button>
            </div>
            <div class="border-b mt-2 lg:ml-2"></div>
            <div>
                <div class="lg:block hidden text-xs text-gray-600 font-semibold pt-4 pb-2 px-2">
                    Following accounts
                </div>
                <div class="lg:hidden block mt-3"></div>
                <div class="cursor-pointer">
                    <MenuItemFollow />
                </div>
                <button class="lg:block hidden text-[#F02C56] pt-1.5 pl-2 text-[13px]">
                    See more
                </button>
            </div>
            <div>
                <div class="lg:block hidden border-b lg:mt-4 mt-2"></div>
                <div class="lg:block hidden text-[11px] text-gray-500">
                    <div class="pt-4 px-2">About Newsroom TikTok Shop Contact Careers ByteDance</div>
                    <div class="pt-4 px-2">TikTok for Good Advertise Developers Transparency TikTok Rewards TikTok Browse TikTok Embeds</div>
                    <div class="pt-4 px-2">Help Safety Terms Privacy Creator Portal Community Guidelines</div>
                    <div class="pt-4 px-2">© 2023 TikTok</div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>

</script>