<template>
    <div>
        <v-container>
            <v-layout row wrap>
            <v-flex xs12 sm6 md6 order-md2 order-sm2>
                <v-card dark tile flat color="blue">
                <v-card-text>#1</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            <v-flex xs12 sm6 md6 order-md1 order-sm1>
                <v-card dark tile flat color="black">
                <v-card-text>#2</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            </v-layout>
        </v-container>

        <v-container>
            <v-layout row wrap>
            <v-flex xs12 sm6 md6 order-md1 order-sm2>
                <v-card dark tile flat color="blue">
                <v-card-text>#1</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            <v-flex xs12 sm6 md6 order-md2 order-sm1>
                <v-card dark tile flat color="black">
                <v-card-text>#2</v-card-text>
                <v-card-text>{{ lorem }}</v-card-text>
                </v-card>
            </v-flex>
            </v-layout>
        </v-container>
    </div>
</template>
<script>
export default {
    data: () => ({
      lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`
    })
}
</script>