<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld title="Hi! all is well?" />

      <HelloWorld msg="If you found my luggage, you can contact me by:" />

      <nav>
        <button class="btn-success"><a href="https://api.whatsapp.com/send?phone=5581986552822&text=Hello.">Whatsapp</a></button> &nbsp;
        <button class="btn-warning"><a href="https://www.instagram.com/lucas_lrrc/">Instagram</a></button>
      </nav>

      <br>

      <div class="footer" >
        <Footer title="or" />
        <Footer msg="Call to:" />
        <nav>
          <button class="btn-success"><a href="tel:5581985421393">My contact</a></button>
        </nav>

        <br>

        <Footer title="Thank you!" />

        <Footer msg="Lucas Cardozo" />

      </div>

    </div>
  </header>


  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
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
  color: white;
}

nav a {
  color: white;
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


.footer{
  text-align: left;
}

@media (max-width: 1024px) {
  .footer{
    text-align: center;
  }
}

button {
  padding: 10px 20px;
  font-size: 16px;
  border: none;
  border-radius: 4px;
  color: white;
  cursor: pointer;
}

.btn-success {
  background-color: #4CAF50;
  color: white;
}

.btn-warning {
  background-color: #afa04c;
  color: white;
}

button:hover {
  background-color: #253526;
}
  
</style>
