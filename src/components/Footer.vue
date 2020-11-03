<template>
  <footer id="footer">
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
    <div class="copy">
      <small>Copyright 2019 estra inc. All Rights Reserved</small>
    </div>
  </footer>
</template>


<style scoped>

.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
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

.copy {
  color: #fff;
  background-color: black;
  text-align: center;
  width: 
}

@media screen and (max-width: 480px) {

.menu-nav {
  display: none;
}

#footer .logo {
  display: block;
  margin: 0 auto;
}
   
}
</style>