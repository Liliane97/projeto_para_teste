<script setup lang="ts">
    import Avatar from './Avatar.vue';
</script>

<template>
<!-- cards do conteudo most watched -->
    <div class="bg-black bg-opacity-20 rounded-3xl overflow-hidden ">
       <div class="header">
            <div class="h-32 w-full flex">
                <img src="http://via.placeholder.com/800x600" alt="" class="w-full h-full object-cover">
            </div>
       </div>

        <div class=" relative p-5">
            <!-- componente avatar -->
            <Avatar class="w-12 h-12 absolute right-2 -top-5 rounded-full overflow-hidden"/>
            <h5 class="text-xs mb-2 opacity-50">
                Andy William
                <!-- status de ativo -->
                <div class="w-2 h-2 inline-block ml-2 rounded-full bg-green-400"></div>
            </h5>
            <p>Basic how to ride your Skateboard comfortly</p>
            <div class="text-xs flex items-center space-x-2 opacity-50 mt-3">
                <span>53k views</span>
                <div class="w-1 h-1 rounded-full bg-gray-300"></div>
                <span>2 week ago</span>
             </div>
        </div>
    </div>
</template>