<template>
  <main class="home">
    <banner id="inicio"></banner>
    <about id="acerca-de"></about>
    <speakers id="comunidades"></speakers>
    <events id="eventos"></events>
    <news-letter id="newsletter"></news-letter>
    <pricings id="pricings"></pricings>
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
import NewsLetter from '@/components/NewsLetter.vue';
import Pricings from '@/components/Pricings.vue';

export default {
  name: 'home',
  components: {
    Banner,
    About,
    Speakers,
    Events,
    NewsLetter,
    Pricings
  }
}
</script>
