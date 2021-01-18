<template>
  <section>
    <h1>Страница пользователей</h1>

    <ul>
      <li v-for="user of users" :key="user.id">
        <a href="#" @click.prevent="openUser(user)">Пользователь {{user.name}}</a>
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  data: () => ({
  users: []
}),
async mounted() {
  this.users = await this.$axios.$get('http://jsonplaceholder.typicode.com/users')
},
    methods:{
        openUser(user){
            this.$router.push('/users/' + user)
        }
    }
}
</script>