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

    <div id="section-1" class="text-center bg-[url('/footeralign.png')] text-gray-600 pb-60 bg-cover bg-center">
      <h1 class="text-6xl uppercase font-oswald text-center pt-20 md:px-24 px-10">
        Building a comprehensive database together
      </h1>
      <p class="font-roboto font-light  text-center text-lg py-6 md:px-28 px-10">
        Help us improve this database by submitting your reviewed talent profile.
      </p>
      <NuxtLink to="/submit"><button class="font-oswald uppercase bg-green-700 text-white py-3 px-8">
        Submit here
      </button></NuxtLink>
    </div>
    <div id="section-2" class="text-center">
      <h2 class="text-6xl font-oswals text-gray-500 uppercase font-medium pt-20">
        Existing Talents
      </h2>
      <p class="text-gray-500 font-light text-xl my-10 md:px-20 px-10">
        A collection of submitted profiles from various teams.
      </p>
      <div class="grid md:grid-cols-2 md:px-40 gap-5">
        <div id="left-item-column">
          <Item
            name="Adam Clark"
            image="/adamclark.jpg"
            age="55"
            url="https://www.linkedin.com/in/adamclark"
            designation="CEO"
          />
          <Item
            name="Chloe Reid"
            image="/chloereid.jpg"
            age="45"
            url="https://www.linkedin.com/in/chloereid"
            designation="CIO"
          />
        </div>
        <div id="right-item-column">
          <Item
            name="Jane Paige"
            image="/janepaige.jpg"
            age="50"
            url="https://www.linkedin.com/in/janepaige"
            designation="CTO"
          />
          <Item
            name="John Graham"
            image="/johngraham.jpg"
            age="51"
            url="https://www.linkedin.com/in/johngraham"
            designation="CFO"
          />
        </div>
      </div>
      <button class="font-oswald uppercase bg-green-700 text-white mb-10 py-3 px-8 text-center">
        <NuxtLink to="/database">Explore Full Database</NuxtLink>
      </button>
    </div>
  </div>
</template>
