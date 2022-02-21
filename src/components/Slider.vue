<template>
  <div>
    <div
      class="test"
      v-for="testimonial in testimonials"
      :key="testimonial.img"
    >
      <figure>
        <img alt="testimonial" class="testimonial" :src="testimonial.img" />
      </figure>
      <p>{{ testimonial.parag }}</p>
      <p>{{ testimonial.desc }}</p>
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
  },
};
</script>

<style lang="scss" scoped>
.testimonial {
  height: 120px;
  width: 120px;
  border-radius: 50%;
}
</style>