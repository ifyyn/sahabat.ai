<template>
  <div class="navbar flex justify-between mt-4 text-[#151515] ">
    <div class="brand xl:ml-0 ml-4 xl:mt-2">
        <img src="../assets/img/image1.jpeg" alt="" class="w-14">
    </div>
    <div class="nav-link flex m-4  xl:flex xl:items-center xl:w-auto" :class="{'block':isActive, 'hidden': !isActive}">
        <ul class="xl:flex gap-5 block xl:mt-0 mt-16 text-center font-bold">
            <li class="xl:pt-0 pt-2  xl:mt-2 mt-0 hover:text-[#246b95]">
                <RouterLink to="/">Home</RouterLink>
            </li>
            <li>
            <RouterLink to="/chatbot">
                <Button class="p-2 items-center xl:mt-0 mt-2">Get Started</Button>
            </RouterLink>
            </li>
        </ul>
    </div>
    <div class="xl:hidden block m-3" @click="toggleMenu">
        <Toggle/>
    </div>
  </div>
</template>

<script>
import { RouterLink } from 'vue-router';
import Toggle from '../components/icons/Toggle.vue';
import Button from '../components/Button.vue';
export default{
    components:{
        RouterLink,
        Toggle,
        Button
    },
    data(){
        return{
            isActive:false,
        };
    },
    methods:{
        toggleMenu(){
            this.isActive = !this.isActive;
        }
    }
}
</script>

<style>

</style>