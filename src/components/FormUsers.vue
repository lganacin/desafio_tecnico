<template>
    <form id="form-users">
        <div class="left">
            <label for="username">Login:</label>
            <input type="text" id="username">

            <label for="fullname">Nome Completo:</label>
            <input type="text" id="fullname">

            <label for="pass">Senha:</label>
            <input type="password" id="pass">            
        </div>

        <div class="right">
            <label for="unit">Unidade:</label>
            <select name="unit" id="unit" v-model="unit">
                <option value="#">Selecione</option>
                <option v-for="productionunit in list" :Key="productionunit.id" :value="productionunit">
                {{ productionunit}} 
                </option>                
            </select>

            <label for="email">E-mail:</label>
            <input type="email" id="email">

            <label for="pass">Confirmação de Senha:</label>
            <input type="password" id="pass">
        </div>
    </form>
        <section>
            <div>
                <label for="count">Tempo de Token</label>
                <button onclick="menos()">-</button>
                <p id="resultado">0</p>
                <button onclick="mais()">+</button> 
            </div>
            <div>
                <label for="alerta">Receber Alertas?</label>
                <input type="checkbox" name="alertas" id="alertas">

                <label for="ocorrencias">Tratar Ocorrências?</label>
                <input type="checkbox" name="ocorrencias" id="ocorrencias">

                <label for="desabilitar">Desabilitar Usuário?</label>
                <input type="checkbox" name="desabilitar" id="desabilitar">
            </div>
        </section>
</template>

<script>
export default {
    name: "FormUsers",
    data () {
        return {
            productionunit: ""
        }
    },
    methods: {
        async getproductionunitlist () {
            
            const req = await fetch("http://186.237.58.167:65129/getproductionunitlist");
            const data = await req.json();
            this.productionunit = data;
        }
    },
    mounted () {
        this.getproductionunitlist()
    }
    
}
</script>

<style scoped>
#form-users {
    width: 100%;
    margin: 50px auto;
    border-width: 2px;
    border-style: solid;
    border-color: black;
    padding: 80px;
    
}

div {
    display: inline-block;
}

#left {
    margin-bottom: 20px;
    margin-left: 20px;
}

#right {
    margin-bottom: 20px;
    margin-left: 40px;
    
}

label {
    font-weight: bold;
    margin-bottom: 10px;
    flex-direction: column;
    display: flex;
    margin-left: 20px;
    
}

input {
    height: 30px;
    width: 300px;
    margin-bottom: 20px;
    margin-left: 20px;
}

select {
    margin-left: 20px;
    height: 30px;
    width: 300px;
    margin-bottom: 20px;
}

section {
    display: inline-block;
    align-items: center;
    margin-bottom: 30px;
    margin-left: 90px;
    
}

button {
    background-color: rgb(184, 180, 180);
    margin-top: 30px;
    padding: 10px;
    font-weight: bold;
    margin-bottom: 20px;
    margin-left: 20px;
}

p {
    height: 30px;
    width: 300px;
    margin-bottom: 20px;
    margin-left: 20px; 
    font-size: 300%;
}
</style>