<template>
  <div>
    <button>{{nav}}</button>
    <input v-model="username" type="text" />
    <p>{{username}}</p>
    <nuxt-link :to="`/user/${username}`">Send username</nuxt-link>
    {{name}}
    <button type="button" @click="checkthis">child to parent</button>
    {{num}}
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: "Home",
      username: ""
    };
  },
  props:{
      name: String,
      num:String  
  },
  methods:{
      checkthis(){
            this.$emit("loadInParent","123")
      }
  }
//   beforeUpdate() {
//     console.log("before update");
//   },
//   updated() {
//     console.log("updated");
//   }
};
</script>