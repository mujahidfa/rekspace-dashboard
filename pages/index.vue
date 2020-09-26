<template>
  <div class="container">
    <aside
      class="relative h-screen w-64 hidden sm:block shadow-xl bg-indigo-500"
    >
      <div class="p-6">
        <div class="flex justify-center mb-4">
          <a
            href="#"
            class="text-white text-2xl font-semibold hover:text-gray-300"
          >
            Rakan Muda
          </a>
        </div>

        <div class="relative flex justify-center px-6">
          <div>
            <button
              class="bg-blue-600 realtive z-10 w-12 h-12 rounded-full overflow-hidden border-4 border-gray-400 hover:border-gray-300 focus:border-gray-300 focus:outline-none"
              @click="isOpen = !isOpen"
            >
              <!-- <img src=""> -->
              <i class="fas fa-user-cog"></i>
            </button>
          </div>
          <button
            v-show="isOpen"
            class="h-full w-full fixed inset-0 cursor-default"
            @click="isOpen = false"
          ></button>
          <div
            v-show="isOpen"
            class="absolute w-32 bg-white rounded-lg shadow-lg py-2 mt-16"
          >
            <a href="#" class="block px-4 py-2 account-link hover:text-white">
              Info
            </a>
            <a href="#" class="block px-4 py-2 account-link hover:text-white">
              Profile
            </a>
            <a href="#" class="block px-4 py-2 account-link hover:text-white">
              Sign Out
            </a>
          </div>
        </div>

        <div class="flex justify-center">
          <a href="#">
            <button
              class="bg-white cta-btn font-semibold py-1 px-4 mt-5 rounded-lg shadow-lg hover:shadow-xl hover:bg-gray-300 flex items-center justify-center"
            >
              Supervisor Page
            </button>
          </a>
        </div>
      </div>
      <nav class="text-white text-base font-semibold pt-2">
        <a
          href="#"
          class="flex items-center active-nav-link text-white py-4 pl-6 nav-item hover:fo"
        >
          <i class="fas fa-chart-line mr-3"></i>
          Home
        </a>

        <a
          href="#"
          class="flex items-center active-nav-link text-white py-4 pl-6 nav-item hover:fo"
        >
          <i class="fas fa-archive mr-3"></i>
          Settings
        </a>
      </nav>
      <a
        href="#"
        class="absolute w-full upgrade-btn bottom-0 active-nav-link text-white flex items-center justify-center py-4"
      >
        <i class="fas fa-seedling mr-3"></i>
        Built by DSA.
        <!-- Log Out<i class="fas fa-sign-out-alt ml-2"></i> -->
      </a>
    </aside>
    <div class="w-full h-screen overflow-x-hidden border-t flex flex-col">
      <main class="w-full flex-grow p-6">
        <!-- <h1 class="text-3xl text-black pb-6">TABLES</h1> -->

        <div class="w-full mt-0">
          <div>
            <ul class="flex border-b">
              <li id="tab-year" class="-mb-px mr-1">
                <a
                  id="link-year"
                  class="bg-white inline-block py-2 px-4 font-semibold border-l border-t border-r rounded-t text-blue-700 font-semibold"
                  >Across Years</a
                >
              </li>
              <li id="tab-fi" class="mr-1">
                <a
                  id="link-fi"
                  class="bg-white inline-block py-2 px-4 font-semibold text-blue-500 hover:text-blue-800"
                >
                  Across FIs
                </a>
              </li>
            </ul>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
    }
  },
}
</script>

<style scoped>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
