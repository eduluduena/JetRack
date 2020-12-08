<template>
  <div>
    <v-row class="mx-10" align="center" justify="center">
      <template v-for="(item, index) in items">
        <v-col v-bind:key="index" cols="12" md="3">
          <v-hover v-slot:default="{ hover }">
            <v-card min-height="400" class="mb-4" color="white" max-width="400">
              <v-img :aspect-ratio="16 / 9" contain :src="item.src">
                <v-expand-transition>
                  <div
                    v-if="hover"
                    class="d-flex orange darken-2 v-card--reveal white--text text-center"
                    style="height: 100%"
                  >
                    <h4>
                      {{ item.text }}
                    </h4>
                  </div>
                </v-expand-transition>
              </v-img>

              <v-card-text class="pt-6" style="position: relative">
                <h3
                  style="color:#ff6600"
                  class="display-1 font-weight-light mb-2"
                >
                  {{ item.title }}
                </h3>
                <div class="font-weight-light mb-2">
                  <h3>{{ item.text }}</h3>
                </div>
              </v-card-text>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "Products",
  data: () => ({
    dialog: false,
    items: [
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/CompleteRack.gif",
        text:
          "Sistema pensado para utilizarlo con cargas manuales. Logramos con él optimizar los lugares reducidos.",
        title: "Racks",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/Estanteria.png",
        text:
          "Posibilidad de montar los estantes en cantidad y separación más conveniente.",
        title: "Estanterias Metalicas",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/Puntera.png",
        text:
          "El mejor producto para exponer sus artículos. Góndolas centrales, punteras y góndolas laterales",
        title: "Gondolas",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/rieles.png",
        text:
          "Muy útiles en oficinas, farmacias, librerías, kioscos, bazares, minimercados, etc.",
        title: "Rieles y Mensulas",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/Slider-1.jpeg",
        text:
          "Sistema pensado para utilizarlo con cargas manuales. Logramos con él optimizar los lugares reducidos.",
        title: "Mini-Racks",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/WhatsApp-Image-2020-10-19-at-4.17.45-PM.jpeg",
        text:
          "Posibilidad de montar los estantes en cantidad y separación más conveniente.",
        title: "Entrepisos Metalicos",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/locker.jpg",
        text:
          "Está pensado para utilizarlo con cargas manuales. Logramos con él optimizar los lugares reducidos",
        title: "Lockers",
      },
      {
        src:
          "http://c1740202.ferozo.com/asdasd/wp-content/uploads/2020/10/exhibidor.png",
        text:
          "Aplicaciones: perfumerías, bazares, mercerías, kioscos, boutiques, autoservicios, jugueterías y muchas más. Ideal para ubicarlo en espacios reducidos.",
        title: "Exhibidores de alambre",
      },
    ],
  }),
  methods: {
    scroll() {
      window.scrollTo(0, 500);
    },
  },
};
</script>

<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.65;
  position: absolute;
  width: 100%;
}
</style>
