<script setup lang="ts">
    import SearchIcon from '../icons/SearchIcon.vue';
</script>

<template>
    <div class="relative  text-white ">
        <input class="bg-gray-700 placeholder-white w-full px-4 py-2 
        rounded-lg opacity-90 focus:opacity-60 outline-none 
        focus:outline-none pr-10" laceholder="Search">
        <!-- componente icone -->
        <SearchIcon class="w-4 h-4 absolute top-2.5 right-2.5"/>
    </div>
</template>