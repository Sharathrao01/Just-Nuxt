<script setup>
const route = useRoute();
const { cars } = useCars()
useHead({
    title:route.params.name
})

const car = computed( () =>{
  return cars.find((c) => {
    return c.id === parseInt(route.params.id);
  });
});


definePageMeta({
  layout:"custom"
})
</script>

<template>
    <div>
      {{ car }}
  <div>
    <!-- CAR HERO -->
    <CarDetailHero :car="car"/>
    <!-- CAR HERO -->
  </div>
  
  <!-- CAR ATTRIBUTES -->
 <CarDetailAttributes :features ="car.features"/>
  <!-- CAR ATTRIBUTES -->
  <!-- CAR DESCRISPTION -->
 <CarDetailDescription :description ="car.description"/>
  <!-- CAR DESCRISPTION -->
  <!-- CAR CONTACT -->
 <CarDetailContact :contact ="car.contact"/>
  <!-- CAR CONTACT -->
</div>
<!-- CAR DETAIL PAGE   -->

</template>