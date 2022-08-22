<template>
  <header class="container-fluid bg-dark p-4">
    <h1 href="#" class="text-white me-5 d-inline">MyWeb</h1>
    <nav class="text-white d-inline">
      <ul class="d-inline">
        <li><router-link to="/">Home</router-link></li>
        <li><a href="#" @click="showMenu">Section</a><i :class="show?'d-none':''" class="bi bi-arrow-right-short"></i><i :class="show?'':'d-none'" class="bi bi-arrow-down-short"></i>
          <div :class="show?'d-inline-block':'d-none'" class="toggle_menu">
            <ul>
              <li><router-link to="/section">Section</router-link></li>
              <li><router-link to="/section">Section</router-link></li>
              <li><router-link to="/section">Section</router-link></li>
            </ul>
          </div>
        </li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>  
    </nav>
  </header>
</template>

<script>
export default {
    name: 'MyHeader',
    data() {
      return {
        show: false,
      }
    },
    methods: {
      showMenu() {
        if(this.show == false) {
          this.show = true;
        } else {
          this.show = false;
        }
      }
    }
}
</script>

<style lang="scss">
header {
  height: 100px;
  position: fixed;
  top: 0px;
  nav {
    vertical-align: super;
    li {
      .toggle_menu {
        ul {
          list-style: square;
          a {
            color: #000;
            display: inline-block;
          }
        }
        background-color: #fff;
        position: absolute;
        top: 30px;
        left: 0px;
        border: 1px solid #000;
        border-radius: 10px;
      }
      display: inline;
      margin-right: 1.5rem;
      position: relative;
      i {
        color: #fff;
      }
      a {
        font-weight: bold;
        color: #fff;
  
        &.router-link-exact-active {
          color: #42b983;
        }
      }
    }
  }
}
</style>