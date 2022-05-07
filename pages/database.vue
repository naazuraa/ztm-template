<template>
  <div id="header" class="bg-gray-100 px-20">
    <!-- <p>This is a hero section.</p> </!-->
    <div id="menu" class="grid grid-cols-2 py-5">
      <div id="menu-left">
        <NuxtLink to="/"><img src="greensearchlogo.png" class="w-[100px]" alt="" /></NuxtLink>
      </div>

      <div id="menu-right">
        <!-- ul is unordered list, to create menu item. li is list items</p> </!-->
        <ul class="grid grid-cols-4 font-oswald text-lg text-gray-500 uppercase pt-5">
          <li>About</li>
          <NuxtLink to="/database">Database</NuxtLink>
          <li>Contact Us</li>
        </ul>
      </div>
    </div>

    <div id="hero" class="grid grid-cols-2">
      <div class="pb-10">
          <h1 class="pt-5 text-8xl text-green-700 text-center font-lilita font-light uppercase">
            Talent
          </h1>
          <h2 class="text-6xl text-green-700 text-center font-lilita font-light uppercase my-5">
            Database
          </h2>
      </div>
      <img src="talent.jpg" class="bg-cover bg-center w-[500px] h-[250px] pr-5" alt="" />
    </div>
    <div>
      <h2 class="text-6xl font-oswals text-gray-500 uppercase text-center font-medium pt-20">
        Existing Talents
      </h2>
      <p class="text-gray-500 font-light text-center text-xl my-10 md:px-20 px-10">
        A collection of submitted profiles from various teams.
      </p>
    </div>
    <div id="items" class="grid grid-cols-3">
      <ProfileItem v-for="b in items" :key="b.name" :item="b" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [],
    };
  },
  mounted() {
    this.$axios.get('profiles.json').then((response) => {
      this.items = response.data.profiles;
    });
  },
};
</script>
