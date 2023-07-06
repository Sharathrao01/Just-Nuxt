<script setup>
//import { CarSearchBar } from '~~/.nuxt/components';

const props = defineProps({
  car:Object,
});
</script>

<template>
    <div>
        <div
        class="shadow border w-full overflow-hidden mb-5 cursor-pointer h-[200px]" 
        @click="navigateTo(`/car/${car.name}-${car.id}}`)"
      >
        <div class="flex h-full">
          <img
            :src="car.url"
            alt=""
            class="w-[180px] h-100"
          />
          <div class="p-4 flex flex-col">
            <div>
              <h1 class="text-2xl text-blue-700">{{ car.name }}</h1>
              <p class="text-gray-700 text-xs">
                {{ car.description }}
              </p>
            </div>
            <h1 class="mt-auto text-xl">${{ car.price }}</h1>
          </div>
        </div>
      </div>
    </div>
</template>