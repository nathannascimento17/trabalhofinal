<template>
  <div id="app">
      <!-- navbar -->
    <div class="navbar navbar-expand-lg fixed-top navbar-dark bg-dark">
        <div class="container">
          <router-link to="/" class="navbar-brand">Pagina Inicial</router-link>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" to="/blog">Serviços</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/services">Quem Somos</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/contact">Contato</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/contact">Cadastre-se</router-link>
            </li>
            <li class="nav-item">
              <div class="collapse navbar-collapse" id="conteudoNavbarSuportado">
                <form class="form-inline my-2 my-lg-0">
                  <input class="form-control mr-sm-2" type="search" placeholder="Pesquisar" aria-label="Pesquisar">
                  </form>
                </div>
            </li>
          </ul>
        </div>
      </div>
    </div>
      <div class="container">
        <transition name="moveInUp">
          <router-view/>
        </transition>
      </div>
</div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.moveInUp-enter-active{
  animation: fadeIn 2s ease-in;
}
@keyframes fadeIn{
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.5;
  }
  100%{
    opacity: 1;
  }
}

.moveInUp-leave-active{
  animation: moveInUp .3s ease-in;
}
@keyframes moveInUp{
 0%{
  transform: translateY(0);
 }
  100%{
  transform: translateY(-400px);
 }
}

.navbar{
   box-shadow: 0 4px 20px 0 rgb(7, 241, 38);
}

</style>
