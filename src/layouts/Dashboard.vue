<script setup lang="ts">
   
    import HomeIcon from '../components/icons/HomeIcon.vue';
    import TrendingUpIcon from '../components/icons/TrendingUpIcon.vue';
    import ChevronDownIcon from '../components/icons/ChevronDownIcon.vue';
    import BellIcon from '../components/icons/BellIcon.vue';
    import MenuItem from './navs/MenuItem.vue';
    import InputSearch from '../components/inputs/InputSearch.vue';
    import Avatar from '../components/Avatar.vue';
    import CardItem from '../components/CardItem.vue';

</script>

<template>
    <!-- menu de navegação -->
    <div class=" bg-gray-800 flex text-white max-h-screen h-screen">
       <!-- definindo tamanho fixo para o menu -->
       <div class=" w-64" >
            <span class="font-semibold p-6 block opacity-90">Skateboard</span>
            <!-- Menu principal-->
            <nav class="p-6">
               <h3 class="opacity-50 uppercase font-semibold tracking-wider text-xs mb-6">Menu</h3> 
               <div class="space-y-6">
                <!-- passando os componentes icones na variavel icon de forma dinâmica -->
                    <MenuItem :icon="HomeIcon">Discorver</MenuItem>
                    <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
                    <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
                    <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
                    <MenuItem :icon="TrendingUpIcon">Trending</MenuItem>
               </div>
            </nav>
        </div>
        
        <!-- conteudo principal, hearder e cards -->
        <div class="flex-1 h-screen relative overflow-y-auto">
            <!-- hearder -->
            <header class="flex p-5 bg-gray-800 z-20 sticky top-0 items-center justify-between">
                <!-- componente input search -->
                <InputSearch class="w-96"/>
                <div class="flex items-center ">
                    <div class="flex items-center space-x-3">
                        <!-- componente avatar -->
                        <Avatar class=" w-10 h-10 rounded-full overflow-hidden" />
                        <span>Thomas</span>
                        <!-- componente chrevon down -->
                        <ChevronDownIcon class="w-4 h-4"/>
                    </div>
                    <!-- componente de notificação -->
                        <BellIcon class="w-5 h-5 ml-8 opacity-50 hover:opacity-100 cursor-pointer transition duration-100"/>
                </div>
            </header>
             <!-- conteudo principal e cards -->
           <div class="px-5 pb-5 ">
                 <h1 class="font-bold text-4xl mt-6 mb-4">Discorver</h1>
           <!-- criando cards principal -->
            <div class="grid gap-4  grid-cols-12">
               <div class="rounded-3xl col-span-8 h-80 overflow-hidden relative">
                    <div class=" flex  w-full h-full">
                        <img src="http://via.placeholder.com/2000x1400" alt="" class="w-full object-cover"/>                
                    </div>
                    <div class="z-10 absolute top-0 p-6 w-full bottom-0 ">
                        <h3 class="text-2xl max-w-xs">How to do Basic Jumping and how to landing safely</h3>
                        <div class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 bg-opacity-50 text-white">7 minuts  
                        </div>  
                  </div>
               </div>
                <!--  criando cards principal -->
               <div class="rounded-3xl col-span-4 h-80 overflow-hidden relative">
                    <div class=" flex   w-full h-full">
                        <img src="http://via.placeholder.com/2000x1400" alt="" class="w-full object-cover"/>
                    </div>
                    <div class="z-10 absolute top-0 p-6 w-full bottom-0 ">
                        <h3 class="text-2xl max-w-xs ">How to do Basic Jumping and how to landing safely</h3>
                    <div class="absolute right-6 bottom-6 px-2 py-1 rounded-lg bg-gray-800 bg-opacity-50 text-white">7 minuts</div>  
                  </div>
               </div>
            </div>

            <h1 class=" text-2xl mt-6 mb-4">Most Watched</h1>
            <!-- criando cards  -->
            <div class="grid grid-cols-4 gap-4" >
                <!-- componente cardItem  -->
                <CardItem v-for="n of 10"/>
            </div>
           </div>
        </div>

    </div>
</template>
