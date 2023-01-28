<template>
  <div class="header">
    <h1>cadastre seu cartão</h1>
  </div>


  <div class="card">
    <img class="chip" src="./assets/chip.png">
    <span class="name">{{ cardNumber? cardNumber: "#### #### #### ####" }}</span>
    <span class="number">{{ cardName? cardName: "name" }}</span>
    <span class="date">{{ cardDueDate? cardDueDate: "date" }}</span>
    <span class="cvv">{{ cardCVV? cardCVV: "cvv" }}</span>
  </div>

  <div>
    <div class="inputs">
      <input v-model="cardName" class="form-control form-control-lg" type="text" placeholder="Nome do cartão">

      <input v-model="cardNumber" class="form-control form-control-lg" type="number" placeholder="Número do cartão">

      <input v-model="cardDueDate" class="form-control form-control-2lg" type="date" placeholder="Data de vencimento">

      <input v-model="cardCVV" class="form-control form-control-lg" type="number" placeholder="CVV">

      <center> <button type="button" class="btn btn-primary btn-lg btn-block">Cadastrar</button>
      </center>
    </div>
  </div>


</template>

<script>



export default {



  name: 'twoWay',
  data() {
    return {
      cardCVV: null,
      cardDueDate: "",
      cardNumber: null,
      cardName: "",
    }
  }
}






/*import axios from "axios";
axios
  .get("url")
  .then((res) => {
          console.log(res.data)
  })
  .catch((error) => {
          console.log(error);
  });*/

</script> 




<style>
* {
  padding: 0;
  margin: 0;
}

@font-face {
  font-family: 'Cardium';
  src: url(fonts/Cardium\ A\ Regular.otf)
}


@font-face {
  font-family: 'Leo';
  src: url(fonts/LeoSemiRounded-Bold.ttf);
}

.chip {
  height: 40px;
  width: 50px;
  margin: 30px;

}

.card {
  border-style: none;
  margin: 20px;
  height: 12em;
  background-image: linear-gradient(to right, rgb(165, 5, 214), rgb(255, 0, 242), rgb(212, 181, 3));
}

h1 {
  padding: 1em;
  font-family: 'Leo';
  text-align: center;
}

.header {
  background-color: rgba(214, 205, 205, 0.411);
  box-shadow: 3px 3px 3px rgba(97, 93, 93, 0.568);

}

.name {
  font-family: 'Cardium';
  color: white;
  font-size: 23px;
  padding-left: 1em;
  position: relative;
  bottom: 1em;
}

.date {
  font-family: 'Cardium';
  color: white;
  font-size: 20px;
  text-align: end;
  padding-right: 1em;
  position: relative;
  bottom: 2.4em;
}

.number {
  font-family: 'Cardium';
  color: white;
  font-size: 20px;
  position: relative;
  bottom: 1em;
  padding-left: 1.4em;

}

.cvv {
  font-family: 'Cardium';
  color: white;
  font-size: 20px;
  text-align: end;
  padding-right: 1.4em;
  position: relative;
  bottom: 2.5em;

}

button {
  width: 90%;
  margin-top: 30px;
}

.form-control-lg {
  margin-top: 30px;
  height: 60px;
}

.form-control-2lg {
  margin-top: 30px;
  height: 60px;
  font-size: 22px;
  color: gray;
}
</style>

