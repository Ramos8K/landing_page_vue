<template>
  <div id="section1">
    <div class="container mx-auto">
        <div class="flex flex-col px-10 items-center pt-20 lg:h-section-desktop h-section-mobile md:h-section-tablet">
            <video class="sm:w-4/5 w-4/5 lg:w-3/5 h-auto rounded-lg" controls autoPlay>
                <source src="https://docs.material-tailwind.com/demo.mp4" type="video/mp4"/>
                    Your browser does not support the video tag.
            </video>
            <div class="text-center max-w-screen-md pt-20 space-y-4">
                <h1 class="md:text-primary md:text-3xl text-primary text-xl">DOMINE AS TÉCNICAS DE VENDAS PELA INTERNET E NUNCA MAIS DEPENDA DE UMA FACULDADE OU EMPREGO COMUM.</h1>
                <h3 class="md:text-secundary text-secundary md:text-2xl text-lg">Gerar renda pela internet já é uma realidade para milhares de brasileiros, mas muitas pessoas insistem em continuar parados. <br> E todas elas apresentam as mesmas desculpas:</h3>
            </div>
            <div class="md:flex md:max-w-screen-xl w-4/5 space-x-4">
                <div class="mini-container">
                    <img src="/src/assets/networking.png" alt="" class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Acham que precisam de milhões de seguidores para ter resultado</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/financial.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Pensam que a única forma de vender é investindo muito dinheiro</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/smartphone.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Acreditam que o seu celular atual não é o suficiente para começar</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/hourglass.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Sentem que não tem tempo o suficiente para trabalhar na internet</p>
                </div>
            </div>
              <div class="text-center max-w-screen-lg pt-20 space-y-4">
                <h1 class="md:text-primary md:text-3xl text-primary text-xl">MAS EU VOU TE MOSTRAR QUE NADA DISSO É VERDADE, E QUE VOCÊ PODE COMEÇAR A FATURAR AINDA HOJE, MESMO QUE SEJA UM COMPLETO INICIANTE.</h1>
            </div>
            <div class="md:flex md:max-w-screen-xl w-4/5 space-x-4">
                <div class="mini-container">
                    <img src="/src/assets/money-bag.png" alt="" class="md:w-2/5 w-1/5">
                    <p class="text-secundary  md:text-xl tex-lg">Acham que precisam de milhões de seguidores para ter resultado</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/pay.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Pensam que a única forma de vender é investindo muito dinheiro</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/megaphone.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Acreditam que o seu celular atual não é o suficiente para começar</p>
                </div>
                <div class="mini-container">
                    <img src="/src/assets/clock.png" alt=""  class="md:w-2/5 w-1/5">
                    <p class="text-secundary md:text-xl tex-lg">Sentem que não tem tempo o suficiente para trabalhar na internet</p>
                </div>
            </div>
            <div class="text-center max-w-screen-lg pt-20 space-y-4">
                <a href="#" class="md:px-56 px-36 py-4 bg-primary rounded-full text-secundary hover:text-secundary text-center border-b-4 border-black hover:border-secundary hover:bg-black  ">Comprar Agora</a>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
#section1 {
    background-image: url("/src/assets/section.png") ;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
}
.mini-container {
    background: rgba( 255, 255, 255, 0.05 );
    box-shadow: 0 8px 32px 0 rgba( 31, 38, 135, 0.37 );
    backdrop-filter: blur( 13.5px );
    border: 5px solid #000;
    border-radius: 40px;
    padding: 50px 25px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    margin-top: 50px;
    text-align: center;
}
</style>