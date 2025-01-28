<script setup lang="ts">
import {RouterView} from 'vue-router'
import Card from 'primevue/card';
import Button from 'primevue/button';
import 'primeicons/primeicons.css';
</script>

<template>
  <div class="root">
    <header>
      <div class="wrapper">
        <nav>
        </nav>
      </div>
    </header>
    <div class="username-main">
      <h1 class="username">Karbn</h1>
    </div>
    <div class="description-main">
    </div>
    <div class="socials-cards">
      <Card class="social-card">
        <template #title>YouTube</template>
        <template #content>
          <iframe src="http://www.youtube.com/embed/videoseries?list=UU9FThw_xrLXcXvN99JB2YGw" width="480"
                  height="400"></iframe>
        </template>
      </Card>
      <Card class="social-card">

        <template #title>Discord</template>

        <template #content>
          <div class="discord-friend-div">
            <span class="add-me-discord">Karbn</span>
            <Button class="add-me-discord-button" icon="pi pi-user" label="Add as friend" href="https://discord.com/user/530975000778506273"/>
          </div>
        </template>
      </Card>
    </div>
  </div>


  <RouterView/>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400..900&display=swap');

.root {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  flex-grow: 1;
}

.username-main {
  display: flex;
  justify-content: center;
  flex: 0 0 100%;
  flex-grow: 1;
}

.username {
  font-size: 10em;
  font-family: "Orbitron", serif;
  text-align: center;
}

.description-main {
  display: flex;
  flex-grow: 1;
}

.socials-cards {
  display: flex;
  flex-grow: 1;
}

.social-card {
  background-color: #2c3e50;
  border: 1px solid black;
  border-radius: 20px;
  width: 50%
}

.discord-friend-div {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.add-me-discord {
  font-size: 3em;
  padding-left: 10px;
}

.add-me-discord-button {
  width: 30%;
  height: 50%;

}

header {
  line-height: 1.5;
  max-height: 100vh;
  flex: 0 0 100%
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
