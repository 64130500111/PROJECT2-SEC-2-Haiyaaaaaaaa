<script setup>
const props = defineProps({
    menu: {
        type: Object,
        require: true
    }
})
</script>
 
<template>
    <div class="flex justify-center">
        <img :src="menu.picURL" class="w-[120px] h-[120px] rounded-[30px]" />
    </div>

    <div class="flex flex-row justify-center">
        <p class="font-['Baloo'] text-[0.9em] text-center mt-3">
            {{ menu.name }}
        </p>
    </div>

    <div class="flex flex-row">
              <div class="w-full flex justify-center mt-7">
     <p class="font-['Baloo'] text-lg" >{{ menu.price }}฿</p>
    </div>

    </div>

    

</template>
 
<style scoped></style>