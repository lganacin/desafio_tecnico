<template>
  <div class="main-container">
    <h1>Gestão de Usuários</h1>
    <FormUsers/> 
    <Dashboard/> 
    <div id="btn">
      <button class="save-btn">Salvar</button>
      <button class="delete-btn">Excluir</button>
    </div>
  </div>
</template>

<script>
import FormUsers from '@/components/FormUsers.vue';
import Dashboard from '@/components/Dashboard.vue';

export default {
  name: 'Users',
  components: {
    FormUsers,
    Dashboard
}

}
</script>

<style scoped>
.save-btn, .delete-btn {
  background-color: rgb(184, 180, 180);
  margin-top: 30px;
  padding: 10px;
  font-weight: bold;
}

.delete-btn {
  margin-left: 20px;
}


</style>
