<template>
  <div>
    <v-btn
      fab
      href="#"
      dark
      large
      color="green"
      fixed
      right
      bottom
      target="_blank"
    >
      <v-icon dark>mdi-whatsapp</v-icon>
    </v-btn>
    <appBar
      @on-home-click="homeBody()"
      @on-productos-click="productosBody()"
      @on-contacto-click="contactoBody()"
    />
    <div v-if="body == 'Home'">
      <background
        firstTextP="BIENVENIDOS A "
        secondTextP="JetRack"
        thirdTextH1="INNOVACION & OPTIMIZACIÓN"
        fourthTextH1="EN ALMACENAMIENTO"
        textColor="#ff6600"
      />
      <Caption />
      <products />
    </div>

    <div v-if="body == 'Productos'">
      <background
        firstTextP="BIENVENIDOS A "
        secondTextP="JetRack"
        thirdTextH1="SOLUCIONES"
        fourthTextH1="EN ALMACENAMIENTO"
        textColor="#ff6600"
      />
      <catalogo></catalogo>
    </div>
    <div v-if="body == 'Contacto'">
      <background
        firstTextP="BIENVENIDOS A "
        secondTextP="JetRack"
        thirdTextH1="SOLICITA TU"
        fourthTextH1="COTIZACIÓN"
        textColor="#ff6600"
      />
      <contacto />
    </div>

    <Footer />
  </div>
</template>

<script>
import AppBar from "../components/Bar/AppBar";
import Background from "../components/Background/Background";
import Caption from "../components/Home/HomeCaption";
import Products from "../components/Home/HomeProducts";
import Catalogo from "../components/Productos/Catalogo";
import Footer from "../components/Footer/Footer";
import Contacto from "../views/Contacto";

export default {
  name: "Home",
  components: {
    Caption,
    Products,
    AppBar,
    Footer,
    Background,
    Contacto,
    Catalogo,
  },
  data: () => ({
    body: "Home",
  }),
  methods: {
    homeBody() {
      this.body = "Home";
    },
    productosBody() {
      this.body = "Productos";
    },
    contactoBody() {
      this.body = "Contacto";
    },
  },
};
</script>

<style scoped>
#fixedContainer {
  position: fixed;
}
</style>
