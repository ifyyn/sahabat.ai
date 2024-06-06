<template>
  <div class="carousel-container">
    <div class="carousel" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
      <div class="carousel-item" v-for="(author, index) in authors" :key="index">
        <div class="shadow-md rounded-md xl:w-[400px] w-[250px] h-[150px] p-10 mx-auto mt-24">
            <h3 class="text-xl font-bold text-[#151515]">{{ author.name }}</h3>
            <p class=" p-1 rounded-md mt-2 text-[#438eb5] font-bold">{{ author.description }}</p>
        </div>
      </div>
      <img src="../assets/img/image1.jpeg" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'AuthorCarousel',
  data() {
    return {
      currentIndex: 0,
      authors: [
        { name: 'Husain', description: 'Description for Author 1' },
        { name: 'Aini', description: 'Description for Author 2' },
        { name: 'Farhan', description: 'Mechine Learning Engineer' },
        { name: 'Fathul Arifin', description: 'Mechine Learning Ops (MLOps)' }
      ]
    };
  },
  mounted() {
    this.startCarousel();
  },
  methods: {
    startCarousel() {
      setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % this.authors.length;
      }, 3000); // Change slide every 3 seconds
    }
  }
};
</script>

<style scoped>
    .carousel-container {
  width: 100%;
  overflow: hidden;
}

.carousel {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.carousel-item {
  min-width: 100%;
  box-sizing: border-box;
  text-align: center;
}
</style>