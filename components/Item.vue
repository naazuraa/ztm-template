<template>
  <div class="border rounded-md border-gray-200 text-left pb-5 mb-5">
    <img :src="image" alt="" class="h-[200px]" />
    <h3 class="font-oswald font-medium text-2xl uppercase text-gray-500 mt-5 mb-2 ml-5">
      {{ name }}
    </h3>
    <p class="font-medium text-xl text-gray-500 ml-5">
      {{ age }}
    </p>
        <p class="font-medium text-gray-500 ml-5">
      {{ designation }}
    </p>
        <p class="font-light text-gray-500 ml-5">
      {{ url }}
    </p>
  </div>
</template>

<script>
export default {
  props: ['image', 'name', 'age', 'designation', 'url'],
};
</script>
