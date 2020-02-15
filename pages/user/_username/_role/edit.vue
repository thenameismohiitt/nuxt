<template>
  <div>
    <p>{{roles}}</p>
    <p>{{username}}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      roles: this.$route.params.role,
      username: this.$route.params.username
    };
  }
};
</script>>