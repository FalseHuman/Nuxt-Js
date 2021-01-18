<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#"> Nuxt-Project</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <nuxt-link  exact no-prefetch active-class="active" class="nav-link" to="/">
            Главная страница
        </nuxt-link>
      </li>
      <li class="nav-item">
        <nuxt-link active-class="active" class="nav-link" to="/about">
            Основное
        </nuxt-link>
      </li>
        <li class="nav-item">
        <nuxt-link active-class="active" class="nav-link" to="/users">
            Пользователи
        </nuxt-link>
      </li>
        <li class="nav-item">
        <nuxt-link active-class="active" class="nav-link" to="/login">
            Регистрация
        </nuxt-link>
      </li>
    </ul>
  </div>
</nav>
</template>