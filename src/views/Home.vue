<template>
  <div id="home" class="font">
    <div class="background">
      <Header />
      <div class="container mx-auto mt-20">
        <div class="h-screen flex justify-around items-center mt-4">
          <div>
            <h1 class="text-9xl hero-text">Hallo :)</h1>
            <p class="mb-6 font-thin">
              For you, for the producers, for the planet.
            </p>
            <a
              title="Click to explore menu"
              class="px-6 py-4 bg-yellow-400 text-white rounded-3xl"
              href="#menu-listing"
              >Explore Foods</a
            >
          </div>
          <div class="hero-image">
            <img
              src="../assets/fooddelivery.png"
              alt="Online shopping illustration"
            />
          </div>
        </div>
      </div>
    </div>
    <!-- menu listing -->
    <div id="menu-listing" class="container mx-auto h-screen">
      <h2 class="text-center my-16 text-4xl font-semibold">
        Top <span class="text-green-600"> Rated </span>Meals
      </h2>
      <!-- A list of meals -->
      <div class="w-full h-50 flex-menu">
        <div class="menu-category border-2">
          <p class="ml-8 mt-6 uppercase text-sm flex items-center gap-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="h-4 w-4"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"
              />
            </svg>
            <span class="font-bold">Categories</span>
          </p>
          <ul class="p-2">
            <li class="ml-6 py-4 cursor-pointer">
              <p @click="!show" class="text-green-600 flex items-center gap-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"
                  />
                </svg>
                <span>Meals</span>
              </p>
            </li>
          </ul>
        </div>
        <Products class="menu-list" />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "../components/Header.vue";
import Products from "../components/Products.vue";
export default {
  name: "Home",
  components: {
    Header,
    Products,
  },
  data: () => ({
    show: false,
  }),
};
</script>

<style scoped>
.hero-text {
  font-family: "Luckiest Guy", cursive;
}

.hero-image > img {
  width: 500px;
  height: auto;
}

.flex-menu {
  display: flex;
  justify-content: space-evenly;
  gap: 0.2rem;
  margin: 0 auto;
}

.menu-category {
  flex: 2;
  /* border: 1px solid #111; */
}

.menu-list {
  flex: 10;
}

.font {
  font-family: "Ubuntu", sans-serif;
}
</style>
