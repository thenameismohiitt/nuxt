<template>
  <div class="welcome">
      <br/>
    <welcome name="mohit" @loadInParent="increment"></welcome>
    <button type="button" @click="childs" number="num">Parent to child</button>
    <hr>
    <br/>
    {{num}}
  </div>
</template>

<script>
import welcome from "@/components/WelcomeComponent.vue";
export default {
  data(){
      return{
      num : "246"
      }
  },
  components: {
    welcome
  },
  methods:{
      increment(value){
          this.num = value
  },
  childs(){
      return this.num
  }
//   beforeCreate() {
//     console.log("before created");
//   },
//   created() {
//     console.log("created");
//   },
//   beforeMount() {
//     console.log("mounted");
//   },
//   mounted() {
//     console.log("mounted");
//   }
  }
};
</script>