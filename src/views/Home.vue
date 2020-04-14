<template>
  <div class="home">
    <v-container>
      <div class="jumbotron myJumbo mt-n6 px-8 py-12 my-n9">
        <h1 class="display-1 text-center">Lorem ipsum dolor sit amet</h1>
        <p class="text-center lead text-break">
          Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem  <br/>
          <v-btn rounded color="#F7E1D0" class="mt-3">Get Started</v-btn>
        </p>
        <p class="text-center">Lorem ipsum dolor sit amet <strong>Lorem ipsum dolor sit amet</strong></p>
        
      </div>
    </v-container>

    <v-spacer></v-spacer>

    <v-container>
            <v-layout row wrap>
            <v-flex xs12 sm6 md6 order-md2 order-sm2>
                <v-card class="ma-4">
                <v-img src="https://picsum.photos/510/300?random" aspect-ratio="1.4"></v-img>
                </v-card>
            </v-flex>
            <v-flex xs12 sm6 md6 order-md1 order-sm1>
                <v-card tile flat color="" class="move">
                <v-card-text>#2</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            </v-layout>
        </v-container>

        <v-container class="move">
            <v-layout row wrap>
            <v-flex xs12 sm6 md6 order-md1 order-sm1>
                <v-card tile flat color="">
                <v-card class="ma-4">
                <v-img src="https://picsum.photos/510/300?random" aspect-ratio="1.4"></v-img>
                </v-card>
                </v-card>
            </v-flex>
            <v-flex xs12 sm6 md6 order-md2 order-sm2>
                <v-card tile flat color="">
                <v-card-text>#2</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            </v-layout>
        </v-container>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  data: () => ({
      lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`
    }),
  components: {}
}
</script>

<style scoped>
.myJumbo{
  background: white;
}
</style>
