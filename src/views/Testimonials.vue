<template>
    <div class="testimonials">
     <div ><h1>Testimonials </h1></div>
       <div class="cards">
            <div v-for="testimonial in $store.state.testimonials" :key="testimonial.id" class="testimonial-card">
                <img :src="testimonial.url" class="testimonial-image" alt="testimage">
                <div class="testinfo">
                    <h2 class="test-name">{{ testimonial.name }}</h2>
                    <p class="test-text">{{ testimonial.message }}</p>
                </div>
            </div>
       </div>
       <footers/>
    </div>
</template>

<script>
import footers from '@/components/footer.vue'
import spinners from '@/components/spinner.vue'
export default{
    // data() {
    //     return {
    //         testimonialData: testimonialData,
    //     };
    // },
    components:{
      footers,
      spinners
    },
    computed:{
        fetchTestimonials(){
            this.$store.dispatch('fetchTestimonials')
        }
    },
    mounted(){
        this.fetchTestimonials
    }
};

/*
div use v-if chuck!== '' 
disply
div

div v-else
spinner
div
*/
</script>

<style scoped>
 h1{
  margin-top: 1px;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
 }
 .testimonials {
  padding: 20px;
  color: #fff;
  text-align: center;
  background: fixed;
  width: auto;
  background-size: cover;
  background-position: center;
  background-image: url('https://i.postimg.cc/sxxwmG6y/Tropical-Leaf-Wandbild-f-r-das-Dschungel-Feeling-zu-Hause.jpg');
  animation: fadeInLeft 1s ease-in-out; /* Apply the fade-in animation */
}


.cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 30px; 
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  grid-gap: 154px;
  margin-top: 60px;
}

.testimonial-card {
  margin: 15px; 
  background: #fff;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
.testimonial-card:hover {
  box-shadow: 0 8px 16px rgba(10, 10, 10, 0.2);
  transform: scale(1.10); 
}

.testimonial-image {
  width: 100%;
  max-width: 200px; 
  border-radius: 50%;
  margin-bottom: 10px; 
}

.test-info {
  text-align: left;
}

.test-name {
  color: #555;
  font-size: 1.5em;
  margin-bottom: 5px; 
}

.test-text {
  font-style: italic;
  color: #555;
}
@keyframes fadeInLeft {
  from {
    opacity: 0;
    transform: translateX(-20px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}



</style>