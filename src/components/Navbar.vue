<template>
  <nav :class="{'main-navbar': true, 'scrolled': scrolled}">
    <div class="main-navbar__container">
      <div class="main-navbar__brand">
        <a href="#">
          <img src alt>
          ClawUI for Events
        </a>
        <div :class="{'burger-menu': true, 'show': isShowMenu }" @click="showMenu()">
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
      <ul :class="{'nav': true, 'show': isShowMenu }">
        <li class="nav-item">
          <a @blur="close" href="#inicio" class="nav-link">About</a>
        </li>
        <li class="nav-item">
          <a @blur="close" href="#comunidades" class="nav-link">Speakers</a>
        </li>
        <li class="nav-item">
          <a @blur="close" href="#eventos" class="nav-link">Schedule</a>
        </li>
        <li class="nav-item">
          <a @blur="close" href="#" class="nav-link">Sponsors</a>
        </li>
        <li class="nav-item">
          <a @blur="close" href="#" class="nav-link">Contact</a>
        </li>
        <li class="nav-item">
          <a @blur="close" href="#" class="button--primary">Tickets</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      scrolled: false,
      isShowMenu: false
    };
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 0;
    },
    showMenu() {
      this.isShowMenu = !this.isShowMenu;
    },
    close() {
      this.isShowMenu = false;
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss" scoped>
</style>