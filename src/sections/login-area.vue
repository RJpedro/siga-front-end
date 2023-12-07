<script lang="ts">
export default {
    name: "LoginArea",
}
</script>

<template>
    <section class="login-area bg-white w-full h-screen">
        <div class="container mx-auto w-full h-full flex justify-center">
            <form action="" method="post">
                <!-- <div> -->
                    <img src="@/images/logo-siga-black.png" alt="Imagem principal do siga" class="w-[450px] mt-[15%] fill-black">
                <!-- </div> -->
                <div class="w-full flex flex-col mb-10 mt-[15%]">
                    <label for="user" class="text-xl mb-4">Usuário: </label>
                    <input type="user" name="user" id="user" placeholder="Digite seu CPF" class="rounded-2xl bg-[#DFDFDF] h-12 p-4">
                </div>
                <div class="w-full flex flex-col">
                    <label for="password" class="text-xl mb-4">Senha: </label>
                    <input type="password" name="password" id="password" placeholder="Digite sua senha" class="rounded-2xl bg-[#DFDFDF] h-12 p-4">
                </div>
                <div class="w-full flex justify-end">
                    <a href="#" class="text-black">Esqueceu sua senha?</a>
                </div>
                <div class="w-full rounded-2xl bg-siga-7 h-12 flex justify-center items-center mt-12">
                    <button type="submit" class="text-white text-xl">Confirmar</button>
                </div>
                <div class="w-full flex justify-center items-center mt-12">
                    <span>Problemas com o acesso?</span>
                </div>
            </form>
        </div>
    </section>
</template>

