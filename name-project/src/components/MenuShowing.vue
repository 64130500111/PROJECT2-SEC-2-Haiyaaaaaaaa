<script setup>
const props = defineProps({
    menu:{
        type: Object,
        require: true
    }
})
const emits = defineEmits(['selectedFood'])
</script>
 
<template>
<div class= "flex justify-center">
    <img :src="menu.picURL" class="w-[120px] h-[120px] rounded-[30px]"/>
</div>
<div class="font-['Baloo'] text-[0.9em] text-center mt-3" >
    {{ menu.name }}
</div>
<div class="flex flex-row">
    <div class="w-full flex justify-center mt-7">
        <p class="font-['Baloo'] text-lg">{{ menu.price }}฿</p>
    </div>
    <div class="w-full">
         <input type="checkbox" :id="menu.id" :value="menu" 
         class="checkbox checkbox-success checkbox-md ml-8 mt-7" 
        @change="$emit('selectedFood',menu)"/>
    </div>
</div>
</template>
 
<style scoped>
</style>
