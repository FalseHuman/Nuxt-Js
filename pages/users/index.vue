<template>
  <section>
    <h1>Страница пользователей</h1>

    <ul>
      <li v-for="user of 10" :key="user">
        Пользователь №{{user}}
      </li>
    </ul>
  </section>
</template>