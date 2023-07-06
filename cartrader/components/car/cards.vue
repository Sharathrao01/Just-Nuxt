<script setup>
const {cars} = useCars()
</script>

<template>
    <div>
        <div class="w-full">
      <!-- CAR CARD -->
      <CarCard v-for="car in cars" :key="car.id" :car="car"/>
      <!-- CAR CARD -->
    </div>
    </div>
</template>