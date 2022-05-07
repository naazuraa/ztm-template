<template>
  <div class="text-center">
    <div>
      <img :src="'/' + item.image" alt="" class="border border-gray p-5" />
    </div>
    <h4 class="font-oswald uppercase text-2xl mt-5">{{ item.name }}</h4>
    <p class="font-light text-gray-500 my-2">
      {{ item.age }}
    </p>
    <p class="font-medium text-gray-500 ml-5">
      {{ item.designation }}
    </p>
    <p class="font-light text-gray-500 ml-5">
      {{ item.url }}
    </p>
  </div>
</template>

<script>
export default {
  props: ['item'],
};
</script>
