<template>
  <section>
    <h1>{{ PageTitle }}</h1>

    <ul>
      <li v-for="user of users" :key="user.id">
        <a href="#" @click.prevent="openUser(user)">Пользователь {{user.name}}</a>
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  async fetch({store}) {
    if (store.getters['users/users'].length === 0) {
      await store.dispatch('users/fetch')
    }
  },
  data: () => ({
    PageTitle: 'Страница пользователей',
}),
  computed: {
    users() {
      return this.$store.getters['users/users']
    }
  },
    methods:{
        openUser(user){
            this.$router.push('/users/' + user.id)
        }
    }
}
</script>