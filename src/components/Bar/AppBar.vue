<template>
  <div>
    <v-card class=" overflow-hidden">
      <v-app-bar
        fixed
        color="white"
        elevate-on-scroll
        v-if="$vuetify.breakpoint.xsOnly"
      >
        <v-app-bar-nav-icon
          style="color:#ff6600"
          @click="drawer = true"
        ></v-app-bar-nav-icon>
        <v-spacer></v-spacer>

        <a @click.prevent="homeClick">
          <v-img
            alt="JetRack Logo"
            contain
            src="./JetRack.svg"
            transition="scale-transition"
            width="30vh"
        /></a>

        <v-navigation-drawer
          style="margin-top:55px"
          width="100%"
          height="auto"
          v-model="drawer"
          absolute
          temporary
        >
          <v-list>
            <v-list-item-group v-model="group" color="#ff6600">
              <v-list-item @click.prevent="homeClick">
                <v-list-item-icon>
                  <v-icon style="color:#ff6600">mdi-home</v-icon>
                </v-list-item-icon>
                <v-list-item-title style="color:#ff6600"
                  >Inicio</v-list-item-title
                >
              </v-list-item>
              <v-list-item @click.prevent="productosClick">
                <v-list-item-icon>
                  <v-icon style="color:#ff6600">mdi-desk</v-icon>
                </v-list-item-icon>
                <v-list-item-title style="color:#ff6600"
                  >Productos</v-list-item-title
                >
              </v-list-item>
              <v-list-item @click.prevent="contactoClick">
                <v-list-item-icon>
                  <v-icon style="color:#ff6600">mdi-account</v-icon>
                </v-list-item-icon>
                <v-list-item-title style="color:#ff6600"
                  >Contacto</v-list-item-title
                >
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
      </v-app-bar>
    </v-card>
    <v-app-bar align="center" height="125" fixed v-if="!$vuetify.breakpoint.xs">
      <a @click.prevent="homeClick">
        <v-img
          alt="Arbras Logo"
          class="shrink"
          contain
          :src="require('./JetRack.svg')"
          transition="scale-transition"
          width="45vh"
      /></a>
      <v-spacer></v-spacer>

      <v-hover v-slot:default="{ hover }">
        <v-btn
          class="text-capitalize"
          text
          @click.prevent="homeClick"
          :color="`${hover ? '#ff6600' : 'black'}`"
        >
          <h2 class="ml-2 font-weight-light">Inicio</h2>
        </v-btn>
      </v-hover>

      <v-hover v-slot:default="{ hover }">
        <v-btn
          class="text-capitalize"
          text
          @click.prevent="productosClick"
          :color="`${hover ? '#ff6600' : 'black'}`"
        >
          <h2 class="ml-2 font-weight-light">Catalogo</h2>
        </v-btn>
      </v-hover>

      <v-hover v-slot:default="{ hover }">
        <v-btn
          class="text-capitalize"
          text
          @click.prevent="contactoClick"
          :color="`${hover ? '#ff6600' : 'black'}`"
        >
          <h2 class="ml-2 font-weight-light">Contacto</h2>
        </v-btn>
      </v-hover>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "AppBar",
  data: () => ({ drawer: false, group: null }),
  methods: {
    homeClick() {
      this.$emit("on-home-click");
    },
    productosClick() {
      this.$emit("on-productos-click");
    },
    contactoClick() {
      this.$emit("on-contacto-click");
    },
  },
};
</script>
