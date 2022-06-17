<template>
    <div id="users-table">
       <div>
           <div id="users-table-heading">
               <div class="order-id">Código</div>
               <div>Nome</div>
               <div>E-mail</div>
               <div>Status</div>
               <div>Ações</div>
           </div>
       </div> 
       <div id="users-table-rows">
           <div class="users-table-row">
               <div id="order-number">1</div>
               <div>José da Silva</div>
               <div>jose@email.com</div>
               <div>Ativo</div>
               <button class="edit-btn">Editar</button>
           </div>
           <div class="users-table-row">
               <div id="order-number">2</div>
               <div>Maria da Silva</div>
               <div>maria@email.com</div>
               <div>Ativo</div>
               <button class="edit-btn">Editar</button>
           </div>
       </div>
    </div>
</template>

<script>
export default {
    name: "Dashboard"
}
</script>

<style scoped>
    #users-table {
        max-width: 1200px;
        margin: 0 auto;
        border-width: 2px;
        border-style: solid;
        border-color: black;
    }

    #users-table-heading,
    #users-table-rows,
    .users-table-row {
        display: flex;
        flex-wrap: wrap;
    }

    #users-table-heading {
        font-weight: bold;
        padding: 12px;
        border-bottom: 3px solid #333;
    }

    #users-table-heading div,
    .users-table-row div {
        width: 19%;        
    }

    .users-table-row {
        width: 100%;
        padding: 12px;
        border-bottom: 1px solid #ccc;
    }

    .edit-btn {
        background-color: rgb(184, 180, 180);
        font-weight: bold;
        padding: 2px;        
    }

</style>