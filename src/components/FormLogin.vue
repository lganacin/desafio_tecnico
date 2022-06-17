<template>
    <form id="form-login">
        <div class="form">
            <label for="username">Login:</label>
            <input type="text" id="username" placeholder="Login">
        
        
            <label for="pass">Senha:</label>
            <input type="password" id="pass" placeholder="Senha">

            <input type="submit" value="Entrar">
        </div>
        
    </form>
    
</template>

<script>
export default {
    name:"FormLogin"
}
</script>

<style scoped>
#form-login {
    display: flex;
    align-items: flex-start;
    width: 50%;
    margin: 100px auto;
    border-width: 2px;
    border-style: solid;
    border-color: black;
    padding: 80px; 
       
}

#form {
    margin-bottom: 20px;
}

div {
    margin-bottom: 20px;
}

label {
    font-weight: bold;
    margin-bottom: 15px;
    
}

input {
    height: 30px;
    width: 250px;
    margin-bottom: 20px;
}
</style>