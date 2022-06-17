<template>
    <div id="nav">
    <router-link to="/">Tela de Login</router-link> |
    <router-link to="/users">Gestão de Usuários</router-link>
  </div>
</template>

<script>
export default {
    name: "Navbar"
}
</script>

<style scoped>
    #nav {
        background-color:darkcyan;
        padding: 30px;
        text-align: center;
        color:midnightblue;
        margin: 12px;
        text-decoration: none;
        font-weight: bold;
        
    }

    a.router-link-exact-active {
        color:darkgrey;
}
</style>