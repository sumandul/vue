<script>
import InpuitField from "../components/InpuitField.vue";
export default {
    data(){
        return {
            show:true,
        name:"My name is suman",
        surnane:"my surname is fulal",
 coun :101
        }
    },
  methods:{
    incrementValue(){
        this.coun++
    },
    toogleValue(){
this.show= !this.show
this.name="hello world"
    },

  }

//   data() {
//     return {
//       firstName: "",
//       lastName: "",
//       email: "",
//       gender:""
//     };
//   },
};
</script>
<template>
      <div class="container">
    <span>{{ coun }}</span>
    <div v-if="show">{{ name }}</div>
    <p v-show="show">Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit esse sequi nulla inventore ut doloremque impedit, dolor unde culpa porro iusto distinctio tempore sint voluptate, quibusdam eveniet ratione blanditiis earum!</p>
    <button class=" bg-red-400  text-white px-2" @click="toogleValue">toogle</button>
    <p><button class=" bg-green-500  text-white px-2" @click="incrementValue">Click</button></p>
    <p>The button has been clicked {{ counter }} times</p>
      <span>firstname: {{firstName}}</span>
      <p>email: {{email}}   </p>

  <div class=" grid gap-10  grid-cols-2 pt-10 ">
    <div  class="">
        <img src="../assets/2.webp" class=" w-full h-full rounded-2xl"/>
    </div>
 <div class="  border rounded-md px-10 py-2">
    <form>
 <div class=" flex flex-col gap-6">
    <div class="">
        <label class="capitalize"> first name </label>
        <input
          class="border-2 px-2 border-green-600 py-2 w-full rounded-2xl"
          type=" text"
          v-model="firstName"
        />
      </div>
      <div>
        
        <label class="capitalize"> Last name </label>
        <input
          class="border-2 px-2 border-green-600 py-2 w-full rounded-2xl"
          type=" text"
          v-model="lastName"
        />
      </div>
      <div>
        
        <label class="capitalize"> Email </label>
        <input
          class="border-2 px-2 border-green-600 py-2 w-full rounded-2xl"
          type=" text"
          v-model="email"
        />
      </div>
      <div>
        
        <label class="capitalize"> Gender</label>
        <input type="radio" v-model="gender" v-bind:value="male"  />man
  <input type="radio"  v-model="gender"   v-bind:value="female"  />woman
      </div>
      <button  class=" bg-green-500  text-white px-10 py-2 rounded-md text-base  font-semibold">Submit</button>
 </div>

    </form>
 </div>
  </div>
 
  </div>
</template>
