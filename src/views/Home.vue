<template>
  <main class="home">
    <banner id="inicio"></banner>
    <about id="acerca-de"></about>
    <speakers id="comunidades"></speakers>
    <events id="eventos"></events>
    <footer class="main-footer">
      <div class="container">
        <p>
            Hecho con <i class="fas fa-heart"></i> en Cancún
        </p>
      </div>
    </footer>
  </main>
</template>

<script>
// @ is an alias to /src
import Banner from '@/components/Banner.vue';
import About from '@/components/About.vue';
import Speakers from '@/components/Speakers.vue';
import Events from '@/components/Events.vue';

export default {
  name: 'home',
  components: {
    Banner,
    About,
    Speakers,
    Events
  }
}
</script>
