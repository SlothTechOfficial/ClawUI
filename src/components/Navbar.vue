<template>
  <nav :class="{'main-navbar': true, 'scrolled': scrolled}">
    <div class="main-navbar__container">
      <div class="main-navbar__brand">
        <a href="#">
          <img src alt />
          ClawUI for Events
        </a>
        <div :class="{'burger-menu': true, 'show': isShowMenu }" @click="showMenu()">
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
      <ul :class="{'nav': true, 'show': isShowMenu }">
        <li v-for="item in menuLinks" :key="item.title" class="nav-item">
          <a @blur="close" :href="item.slug" class="nav-link">{{item.title}}</a>
        </li>      
        <li class="nav-item">
          <a @blur="close" href="#tickets" class="button--primary">Tickets</a>
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
      isShowMenu: false,
      menuLinks: [
        {
          title: "Home",
          slug: "#home"
        },
        {
          title: "About",
          slug: "#about"
        },
        {
          title: "Speakers",
          slug: "#speakers"
        },
        {
          title: "Schedule",
          slug: "#schedule"
        },
        {
          title: "Newsletter",
          slug: "#newsletter"
        }
      ]
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
