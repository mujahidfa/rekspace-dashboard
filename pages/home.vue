<template>
  <div>
    <!-- breadcrumb -->
    <nav class="text-sm font-semibold mb-6" aria-label="Breadcrumb">
      <ol class="list-none p-0 inline-flex">
        <li class="flex items-center text-blue-500">
          <a href="#" class="text-gray-400">Home</a>
          <svg
            class="fill-current w-3 h-3 mx-3"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 320 512"
          >
            <path
              d="M285.476 272.971L91.132 467.314c-9.373 9.373-24.569 9.373-33.941 0l-22.667-22.667c-9.357-9.357-9.375-24.522-.04-33.901L188.505 256 34.484 101.255c-9.335-9.379-9.317-24.544.04-33.901l22.667-22.667c9.373-9.373 24.569-9.373 33.941 0L285.475 239.03c9.373 9.372 9.373 24.568.001 33.941z"
            />
          </svg>
        </li>
        <li class="flex items-center">
          <a href="#" class="text-gray-100">Control panel</a>
        </li>
      </ol>
    </nav>
    <!-- breadcrumb end -->

    <div class="lg:flex justify-between items-center mb-6">
      <p class="text-2xl font-bold mb-2 lg:mb-0 text-white">
        The HLX - Floor 11
      </p>
      <button
        class="bg-blue-700 hover:bg-blue-500 text-white focus:outline-none rounded-lg px-6 py-2 font-semibold shadow"
      >
        View Bookings
      </button>
    </div>

    <div
      class="w-full bg-gray-800 border rounded-lg p-4 xl:mb-0"
      style="height: 500px"
    >
      <div class="h-full w-full bg-plan parent">
        <button name="RekEvents1" class="div1 child-button space-x-2">
          <div class="flex flex-row items-center space-x-2">
            <div
              class="circle"
              :class="[isOccupied ? 'bg-green-400' : 'bg-red-400']"
            ></div>
            <p>RekEvents 1</p>
          </div>
          <div
            class="flex flex-col space-y-2 mt-8 bg-blue-600 p-4 border rounded-lg"
          >
            <div class="flex flex-row items-center space-x-2">
              <button
                class="focus:outline-none"
                @click="isLightsOn = !isLightsOn"
              >
                <div
                  class="circle"
                  :class="[isLightsOn ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>Lights</p>
            </div>
            <div class="flex flex-row items-center space-x-2">
              <button class="focus:outline-none" @click="isAcOn = !isAcOn">
                <div
                  class="circle"
                  :class="[isAcOn ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>A/C</p>
            </div>
            <div class="flex flex-row items-center space-x-2">
              <button
                class="focus:outline-none"
                @click="isDoorUnlocked = !isDoorUnlocked"
              >
                <div
                  class="circle"
                  :class="[isDoorUnlocked ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>Door lock</p>
            </div>
          </div>
        </button>
        <tippy to="RekEvents1" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="circle"
                  :class="[isOccupied ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </li>
              <li>Room capacity: 80</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x80</li>
                  <li>- PA System x2</li>
                  <li>- Whiteboard x2</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekevents1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>

        <button name="RekMeeting" class="div2 child-button space-x-2">
          <div class="circle bg-green-400"></div>
          <p>RekMeeting</p>
        </button>
        <tippy to="RekMeeting" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-green-500"
                ></div>
              </li>
              <li>Room capacity: 10</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x10</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x2</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekmeeting.jpg" alt="" class="mt-4" />
          </div>
        </tippy>

        <button name="RekWork1" class="div3 child-button space-x-2">
          <div class="circle bg-red-400"></div>
          <p>RekWork 1</p>
        </button>
        <tippy to="RekWork1" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-red-500"
                ></div>
              </li>
              <li>Room capacity: 6</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x6</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x1</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekwork1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>
        <button name="RekWork2" class="div4 child-button space-x-2">
          <div class="circle bg-gray-400"></div>
          <p>RekWork 2</p>
        </button>
        <tippy to="RekWork2" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-gray-500"
                ></div>
              </li>
              <li>Room capacity: 6</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x6</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x1</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekwork1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>

        <button name="RekStudy1" class="div5 child-button space-x-2">
          <div class="circle bg-green-400"></div>
          <p>RekStudy 1</p>
        </button>
        <tippy to="RekStudy1" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-green-500"
                ></div>
              </li>
              <li>Room capacity: 6</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x6</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x1</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekstudy1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>
        <button name="RekStudy2" class="div6 child-button space-x-2">
          <div class="circle bg-red-400"></div>
          <p>RekStudy 2</p>
        </button>
        <tippy to="RekStudy2" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-red-500"
                ></div>
              </li>
              <li>Room capacity: 6</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x6</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x1</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekstudy1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>

        <button name="RekEvents2" class="div7 child-button space-x-2">
          <div class="flex flex-row items-center space-x-2">
            <div
              class="circle"
              :class="[isOccupied2 ? 'bg-green-400' : 'bg-red-400']"
            ></div>
            <p>RekEvents 2</p>
          </div>
          <div
            class="flex flex-col space-y-2 bg-blue-600 p-4 border rounded-lg"
          >
            <div class="flex flex-row items-center space-x-2">
              <button
                class="focus:outline-none"
                @click="isLightsOn2 = !isLightsOn2"
              >
                <div
                  class="circle"
                  :class="[isLightsOn2 ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>Lights</p>
            </div>
            <div class="flex flex-row items-center space-x-2">
              <button class="focus:outline-none" @click="isAcOn2 = !isAcOn2">
                <div
                  class="circle"
                  :class="[isAcOn2 ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>A/C</p>
            </div>
            <div class="flex flex-row items-center space-x-2">
              <button
                class="focus:outline-none"
                @click="isDoorUnlocked2 = !isDoorUnlocked2"
              >
                <div
                  class="circle"
                  :class="[isDoorUnlocked2 ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </button>

              <p>Door lock</p>
            </div>
          </div>
        </button>
        <tippy to="RekEvents2" arrow>
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="circle"
                  :class="[isOccupied2 ? 'bg-green-400' : 'bg-red-400']"
                ></div>
              </li>
              <li>Room capacity: 80</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x80</li>
                  <li>- PA System x2</li>
                  <li>- Whiteboard x2</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekevents2.jpg" alt="" class="mt-4" />
          </div>
        </tippy>

        <button name="RekCreate" class="div8 child-button space-x-2">
          <div class="circle bg-red-400"></div>
          <p>RekCreate</p>
        </button>
        <tippy to="RekCreate" arrow class="bg-white">
          <div class="w-full">
            <ul class="text-left">
              <li class="flex space-x-2 items-center">
                <p>Occupied:</p>
                <div
                  class="rounded-full h-3 w-3 flex items-center justify-center bg-green-500"
                ></div>
              </li>
              <li>Room capacity: 10</li>
              <li>
                Equipment:
                <ul>
                  <li>- Projector x1</li>
                  <li>- Table & chairs x10</li>
                  <li>- PA System x1</li>
                  <li>- Whiteboard x2</li>
                  <li>- Podcast Microphone x1</li>
                </ul>
              </li>
            </ul>
            <img src="../assets/rekcreate1.jpg" alt="" class="mt-4" />
          </div>
        </tippy>
      </div>
    </div>
    <div class="flex justify-center py-2 space-x-2">
      <button class="focus:outline-none main-dblue" @click="toggleEquip()">
        toggle Equip
      </button>
      <button
        class="p-2 bg-blue-700 hover:bg-blue-500 text-white rounded-lg focus:outline-none hover:font-semibold"
        @click="toggleAllAc()"
      >
        Toggle all A/C
      </button>
      <button
        class="p-2 bg-blue-700 hover:bg-blue-500 text-white rounded-lg focus:outline-none hover:font-semibold"
        @click="toggleAllDoor()"
      >
        Toggle all door locks
      </button>
      <button
        class="p-2 bg-blue-700 hover:bg-blue-500 text-white rounded-lg focus:outline-none hover:font-semibold"
        @click="toggleAllLights()"
      >
        Toggle all lights
      </button>
      <button class="focus:outline-none main-dblue" @click="toggleNoti()">
        toggle noti
      </button>
    </div>
    <vue-snotify></vue-snotify>
  </div>
</template>

<script>
import 'vue-snotify/styles/material.css'

export default {
  layout: 'home',
  data() {
    return {
      isOccupied: false,
      isOccupied2: true,
      isLightsOn: false,
      isAcOn: false,
      isDoorUnlocked: false,
      isLightsOn2: true,
      isAcOn2: true,
      isDoorUnlocked2: false,
    }
  },
  methods: {
    toggleAllLights() {
      this.isLightsOn = !this.isLightsOn
      this.isLightsOn2 = !this.isLightsOn2
    },
    toggleAllAc() {
      this.isAcOn = !this.isAcOn
      this.isAcOn2 = !this.isAcOn2
    },
    toggleAllDoor() {
      this.isDoorUnlocked = !this.isDoorUnlocked
      this.isDoorUnlocked2 = !this.isDoorUnlocked2
    },
    toggleNoti() {
      this.isOccupied = true
      this.isDoorUnlocked = true
      this.$snotify.info(
        'Guest Khairul Nazran just unlocked the room.',
        'RekEvents 1 is now occupied',
        {
          timeout: 5000,
          showProgressBar: false,
          closeOnClick: true,
          titleMaxLength: 30,
          icon: 'naz.png', // 'https://a7sas.net/wp-content/uploads/2019/07/4060.jpeg', // 'assets/mujahid.jpeg', // 'http://placeholde.it/48x100',
        }
      )
    },
    toggleEquip() {
      this.$snotify.warning(
        'Podcast Mic Blue x10s was taken out of RekEvents 1',
        'Warning: equipment taken out!',
        {
          timeout: 5000,
          showProgressBar: false,
          closeOnClick: true,
          titleMaxLength: 30,
        }
      )
    },
  },
}
</script>

<style scoped>
.bg-plan {
  background-color: #102e5e;
}
.snotify-icon {
  object-fit: cover;
  width: 100%;
  height: 100%;
  object-position: center;
}

.tooltip.popover .popover-inner {
  background: #f9f9f9;
  color: black;
  padding: 24px;
  border-radius: 5px;
  box-shadow: 0 5px 30px rgba(0, 0, 0, 0.1);
}
.tooltip.popover .popover-arrow {
  border-color: #f9f9f9;
}

.parent {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  grid-template-rows: repeat(6, 1fr);
  grid-column-gap: 0px;
  grid-row-gap: 0px;
}

.div1 {
  grid-area: 1 / 1 / 4 / 3;
}
.div2 {
  grid-area: 4 / 1 / 7 / 2;
}
.div3 {
  grid-area: 6 / 2 / 7 / 3;
}
.div4 {
  grid-area: 5 / 3 / 7 / 4;
}
.div5 {
  grid-area: 5 / 4 / 7 / 5;
}
.div6 {
  grid-area: 5 / 5 / 7 / 6;
}
.div7 {
  grid-area: 1 / 3 / 3 / 5;
}
.div8 {
  grid-area: 1 / 5 / 4 / 6;
}

.child-button {
  @apply flex flex-row items-center justify-center border border-gray-100 bg-plan text-gray-100 border-dashed;
}

.child-button:hover {
  @apply bg-blue-700;
}

.child-button:focus {
  @apply outline-none;
}

.circle {
  @apply rounded-full h-3 w-3 flex items-center justify-center;
}
</style>
