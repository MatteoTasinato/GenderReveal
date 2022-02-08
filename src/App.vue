<template>
  <div class="wheel_wrap">
    <h1>Baby T Wheel</h1>

    <Wheel
      ref="wheel"
      :gift="gift"
      :data="data"
      :imgParams="logo"
      @done="done"
      @click="spinTheWheel"
      :animDuration=12500
    />

        <span>BigBear GmbH, 2022</span>
  </div>
</template>

<script>
import { Wheel } from "vue3-fortune-wheel";
import "vue3-fortune-wheel/dist/library.css";

export default {
  name: "App",
  components: {
    Wheel,
  },
  data() {
    return {
      gift: 1,
      logo: {
      height: 180,
      width: 180,
        src: require('./assets/logo.png'),
      },
      data: [
        {
          id: 1,
          value: "Bambina",
          bgColor: "#f472b6",
          color: "#ffffff",
        },
        {
          id: 2,
          value: "Bambino",
          bgColor: "#60a5fa",
          color: "#ffffff",
        },
        {
          id: 3,
          value: "Bambina",

          bgColor: "#f472b6",
          color: "#ffffff",
        },
        {
          id: 4,
          value: "Bambino",
          bgColor: "#60a5fa",
          color: "#ffffff",
        },
        {
          id: 5,
          value: "Bambina",
          bgColor: "#f472b6",
          color: "#ffffff",
        },
        {
          id: 6,
          value: "Bambino",
          bgColor: "#60a5fa",
          color: "#ffffff",
        },
      ],
    };
  },
  methods: {
    done(params) {
      console.log(params);
    },
    spinTheWheel() {
      this.$refs.wheel.spin();
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.wheel_wrap {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
