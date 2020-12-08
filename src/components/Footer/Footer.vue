<template>
  <v-footer dark padless>
    <v-card
      width="100%"
      flat
      tile
      color="#0D47A1"
      class="white--text text-center"
    >
      <v-card-text class="white--text">
        <v-row>
          <v-col cols="12" md="4" class="text-center">
            <h3 class="text-center">Contactenos</h3>
          </v-col>
          <v-col cols="12" md="4" class="text-center">
            <h3 class="text-center">
              Gracias por su visita
            </h3>
          </v-col>
          <v-col cols="12" md="4" class="text-center">
            <h3 class="text-center">
              Horarios
            </h3>
          </v-col>
        </v-row>
        <v-row align="center">
          <v-col cols="12" md="4" class="text-left">
            <v-btn target="_blank" icon href="#">
              <v-icon size="24px" color="green"> mdi-whatsapp </v-icon>
            </v-btn>
            set phone
            <br />
            <v-btn
              target="_blank"
              href="mailto:JetRackInformacion@gmail.com"
              icon
            >
              <v-icon size="24px" color="#B23121"> mdi-gmail </v-icon>
            </v-btn>
            JetRackInformacion@gmail.com
            <br />
            <v-btn icon>
              <v-icon size="24px" color="light-blue"> mdi-phone </v-icon>
            </v-btn>
            set phone
            <br />
            <v-btn target="_blank" href="#" icon>
              <v-icon size="24px" color="yellow">
                mdi-map-marker
              </v-icon>
            </v-btn>
            a designar, Cordoba, Argentina - CP:5009
          </v-col>
          <v-col cols="12" md="4">
            <br />
            <h3 class="text-center">
              JetRack se ha forjado de una reputación de vender productos
              fabricados con precisión de alta calidad para su uso en una gran
              variedad de industrias.
            </h3>
          </v-col>
          <v-spacer></v-spacer>
          <v-col cols="12" md="3">
            <br />
            <v-col cols="12" md="9">
              <v-row justify="start" align="center" class="mx-0">
                <v-btn target="_blank" icon href="#">
                  <v-icon size="24px" color="white"> mdi-clock </v-icon>
                </v-btn>
                Lunes a Viernes: 9:00 AM - 4:00 PM
              </v-row>
              <v-row justify="start" align="center" class="mx-0">
                <v-btn target="_blank" icon href="#">
                  <v-icon size="24px" color="white"> mdi-clock </v-icon>
                </v-btn>
                Sábados: 9:00 AM - 12:00 PM
              </v-row>
            </v-col>
          </v-col>
        </v-row>
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }}
        <strong style="color:#ff6600">JetRack</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data: () => ({}),
};
</script>
