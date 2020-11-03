<template>
  <div id="header">
    <div class="menu-contents flex">
      <div class="logo">
        <p>estra inc.</p>
      </div>
      <div class="menu-nav">
        <ul class="menu-list flex">
          <a href="#"><li class="menu">home</li></a>
          <a href="#"><li class="menu">about</li></a>
          <a href="#"><li class="menu">service</li></a>
          <a href="#"><li class="menu">works</li></a>
          <a href="#"><li class="menu">price</li></a>
          <a href="#"><li class="menu">contact</li></a>
        </ul>
      </div>
    </div>
    <div id="hamburger" @click="menuOpen()" :class="{'active':isClass }">
      <span></span>
      <span></span>
      <span></span>
    </div>
    <div class="openMenu" :class="{'open':isClass}">
      <h2>estra inc.</h2>
      <ul class="menu-list">
        <a href="#"><li class="menu">home</li></a>
        <a href="#"><li class="menu">about</li></a>
        <a href="#"><li class="menu">service</li></a>
        <a href="#"><li class="menu">works</li></a>
        <a href="#"><li class="menu">price</li></a>          
        <a href="#"><li class="menu">contact</li></a>
      </ul>
      
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isClass: false,
    };
  },
  methods: {
    menuOpen() {
      this.isClass = ! this.isClass;
    },
  },
};
</script>

<style scoped>
.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

#header {
  width: 100%;
}

.menu-contents {
  background-color: #000;
  color: #fff;
  padding: 0 20px;
  height: 52px;
}

.menu {
  color: #fff;
  margin-left: 30px;
  list-style: none;
}

.menu-list a {
  text-decoration: none;
}

.menu-list {
  padding: 0;
}

.openMenu {
  display: none;
}

@media screen and (max-width: 480px) {
  .menu-nav {
    display: none;
  }

  #hamburger {
    width: 40px;
    height: 40px;
    position: absolute;
    top: 13px;
    right: 20px;
  }

  #hamburger span {
    position: absolute;
    display: block;
    background-color: #fff;
    width: 100%;
    height: 3px;
    border-radius: 5px;
    transition: 0.8s;
  }

  #hamburger span:nth-of-type(1) {
    top: 10px;
  }

  #hamburger span:nth-of-type(2) {
    top: 20px;
  }

  #hamburger span:nth-of-type(3) {
    top: 30px;
  }

  #hamburger.active span:nth-of-type(1) {
    top: 20px;
    transform: rotate(45deg);
  }

  #hamburger.active span:nth-of-type(2) {
    opacity: 0;
  }

  #hamburger.active span:nth-of-type(3) {
    top: 20px;
    transform: rotate(-45deg);
  }

  .menu {
    color: #000;
  }

  .openMenu {    
    display: block;
    width: calc(100% - 80px);
    height: 100%;
    background: #343434;
    position: fixed;
    top: 0;
    left: calc(-100% - 80px);
    transition: 0.5s;
    z-index: 999;
    color: #fff;
  }

  .openMenu h2 {
    margin-left: 25px;
  }

  .openMenu .menu {
    color: #fff;
    border-bottom: #fff solid 1px;
    margin-bottom: 20px;
  }

  .open {
    left: 0;
  }

}
</style>