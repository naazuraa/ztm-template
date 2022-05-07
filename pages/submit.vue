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
    <tr>
      <td colspan="3">
        <input
          id="name"
          type="name"
          placeholder="Please enter the name"
          class="w-full border border-gray-300 text-xl mt-5 py-3 px-2"
        />
      </td>
      <td colspan="2">
        <input
          id="age"
          type="age"
          placeholder="Please enter age"
          class="w-full border border-gray-300 text-xl mt-5 py-3 px-2"
        />
      </td>
      <td colspan="2">
        <input
          id="image"
          type="url"
          placeholder="Please enter image URL"
          class="w-full border border-gray-300 text-xl mt-5 py-3 px-2"
        />
      </td>
      <td colspan="2">
        <input
          id="url"
          type="url"
          placeholder="Please enter LinkedIn URL"
          class="w-full border border-gray-300 text-xl mt-5 py-3 px-2"
        />
      </td>
      <td colspan="2">
        <input
          id="designation"
          type="designation"
          placeholder="Please enter current designation"
          class="w-full border border-gray-300 text-xl mt-5 py-3 px-2"
        />
      </td>
    </tr>
    <div>
      <td colspan="2" class="text-right">
        <button
          class="font-oswald uppercase bg-green-700 text-white text-xl py-3 px-2 ml-5 mt-5"
          @click="submitProfile"
        >
          Submit Profile
        </button>
      </td>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    submitProfile() {
      this.$axios.post('/.netlify/functions/email', {
        email: document.getElementById('email').value,
        orders: this.$store.state.orders,
      });

      this.$axios.post('/.netlify/functions/db', {
        email: document.getElementById('email').value,
        orders: this.$store.state.orders,
      })
    },
  },
};
</script>
