<template>

    <div id="login">
        <form class="card">
            <div class="card-header">
                <h2>Login</h2>
            </div>
            <div class="card-content">
                <div class="card-content-area">
                    <label for="email" >Email</label>
                    <input type="text" placeholder="ex: usuária@gmail.com" id="email" autocomplete="off" >
                </div>
                <div class="card-content-area">
                    <label for="password">Senha</label>
                    <input type="password" id="password" autocomplete="off" placeholder="ex: 1234">

                    <p>
                        <input type="checkbox" name="manterlogado" id="manterlogado" value="" />
                        <label for="manterlogado">Manter-me logado</label>
                    </p>
                </div>
            </div>

            <div class="card-footer">
                <NuxtLink to="/tela-menu"><input type="submit" value="Login" class="submit"></NuxtLink>
            </div>
            <div id="cadastro">
                <p>Ainda não tem uma conta?</p>
                <NuxtLink to="/tela-cadastros"><button>Cadastre-se</button></NuxtLink>
            </div>
            
        </form>
    </div>
</template>

<script>
</script>

<style>
body {
    padding: 0;
    margin: 0;
    background-image: linear-gradient(to right, #f7a1a1, #efc2c2, #fbf3f3);
}
#login {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;

}
.card {
    background-color: rgba(19, 19, 19, 0.3);
    padding: 40px;
    width: 400px;

}
.card-header {
    padding-bottom: 50px;
    opacity: 0.8;
    color: #fff;
    border-radius: 15px;

}
.card-header::after {
    content: "";
    width: 70px;
    height: 1px;
    display: block;
    margin-top: -30px;
    margin-left: -5px;

}
.card-content label {
    color: #fff;
    font-size: 12px;
    opacity: 0.7;

}
.card-content-area {
    display: flex;
    flex-direction: column;
    padding: 10px 0;
}
.card-content-area input {
    margin-top: 10px;
    padding: 0 5px;
    background-color: transparent;
    border: none;
    border-bottom: 1px solid #e1e1e1;
    outline: none;
    color: #fff;

}
.card-footer {
    display: flex;
    flex-direction: column;
}
.card-footer .submit {
    width: 100%;
    height: 40px;
    background-color: #fafafa;
    font-size: 16px;
    border: none;
    color: #000000;
    margin: 10px 0;
}
.card-footer a {
    text-align: center;
    font-size: 12px;
    opacity: 0.8;
    color: #fff;
    text-decoration: none;
}
#cadastro{
    margin-top: 3em;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
}
#cadastro p {
    color: #fff; 
    font-size: 13px;
}
#cadastro button{
    background-color: #fff;
    color: rgba(41, 38, 38, 0.808); 
    font-size: 14px;
    border: none;
    border-radius: 5px;
    font-family:Arial, Helvetica, sans-serif;
}
</style>