<template>
  <div>
    <div
      class="test"
      v-for="(testimonial, index) in testimonials"
      :key="testimonial.img"
    >
      <div v-if="isIndex(index)">
        <figure>
          <img alt="testimonial" class="testimonial" :src="testimonial.img" />
        </figure>
        <p class="italic">{{ testimonial.parag }}</p>
        <p>{{ testimonial.desc }}</p>
      </div>
    </div>
    <div class="dots">
      <div
        class="dot"
        :class="{ white: isIndex(index) }"
        v-for="(dot, index) in 2"
        :key="index"
        @click="setIndex(index)"
      ></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider",
  data() {
    return {
      currentIndex: 0,
      testimonials: [
        {
          img: require("../assets/test2.jpg"),
          parag:
            "Many novice real estate investors soon quit the profession and invest. When you invest in real estate, you often see a side of humanity that stocks, bonds, mutual funds, and saving money shelter you from.",
          desc: "JOHN DOE • PROPERTY INVESTOR",
        },
        {
          img: require("../assets/test1.jpg"),
          parag:
            "No man feels more of a man in the world if he have but a bit of ground that he can call his own. However small it is on the surface, it is four thousand miles deep: and that is a very handsome property.",
          desc: "HARRY SMITH • NEW HOME OWNER",
        },
      ],

      currentTest: [],
    };
  },
  methods: {
    newArray(index) {
      const newArr = this.testimonials.filter(() => {
        if (index === this.currentIndex) {
          return true;
        } else {
          return false;
        }
      });
      return newArr;
    },

    getCurrentTest(index, testimonial) {
      if (index === this.currentIndex) {
        this.currentTest.push(testimonial);
      }
    },
    isIndex(index) {
      return index === this.currentIndex;
    },
    nextPic() {
      if (this.currentIndex === this.testimonials.length - 1) {
        this.currentIndex = 0;
      } else {
        this.currentIndex++;
      }
    },
    setIndex(index) {
      this.currentIndex = index;
    },
    startAutoPlay() {
      setInterval(this.nextPic, 4000);
    },
  },
  created() {
    this.startAutoPlay();
  },
};
</script>

<style lang="scss" scoped>
.testimonial {
  height: 120px;
  width: 120px;
  border-radius: 50%;
  font-weight: 500;
}

.italic {
  font-size: 18px;
  font-style: italic;
}

.white {
  background-color: white;
}

.dots {
  display: flex;
  justify-content: center;
  .dot {
    height: 10px;
    width: 10px;
    margin: 0 5px;
    border: 1px solid white;
    border-radius: 50%;
  }
}
</style>