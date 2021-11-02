<template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
      height="200px"
    ></v-img>

    <v-card-title>
      Data Diri
    </v-card-title>

    <v-card-subtitle>
      
    </v-card-subtitle>
    Fresh Graduate program strata 1 yang tertarik dengan programming.
    Ingin berkontribusi dan mengembangkan kemampuan programming melalui berlajar dan berusaha dengan giat.
    <v-card-actions>

      <v-spacer></v-spacer>

      <v-btn
        icon
        @click="show = !show"
      >
        <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
         <p> Nama : Zefanya Devendra P.N </p>
         <p> Tempat, Tanggal Lahir : Cancar, 18 Mei 1999
         <p> Alamat Domisili : Jl. Dinoyo Lor 3 No.30, Surabaya
         <p> Email : zefanyadevendra@gmail.com
         <p> No.Telp : 082227683132
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      show: false,
    }),
  }
</script>