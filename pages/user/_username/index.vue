<template>
    <div class="user">
    <p>
    <label>roles {{roles}}</label><br/>
    <input v-model="roles" type="text" />
    </p>
    <label>username {{username}}</label><br/>
    <input v-model="username" type="text" />
    <nuxt-link :to="`/user/${username}/${roles}/edit`">Sed role and username</nuxt-link>
    </div>
</template>

<script>
export default {
    data(){
        return{
            username: this.$route.params.username,
            roles: ''
        }
    }
}
</script>