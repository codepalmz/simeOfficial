<template>
    <div class="nav">
        <v-container>
            <v-toolbar dense flat>
            <!-- <v-spacer></v-spacer> -->
            <v-toolbar-title>
                    <v-btn text to="/">SIME</v-btn>
                </v-toolbar-title>

                <v-spacer></v-spacer>

            <v-btn text class="text-right gray" to="/help">HELP</v-btn>
            <v-btn text class="gray" to="/privacy">PRIVACY</v-btn>
            <v-btn text class="gray" to="/blog">Blog</v-btn>
            <v-btn text class="gray" to="/login">Login</v-btn>
            <v-btn rounded dark to="/SignUp">CREATE ACCOUNT</v-btn>
            </v-toolbar>
        </v-container>
        
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
/* .v-btn:hover:before,
.v-btn:focus:before{
    color: black;
    background: white;
}
.v-btn:active,
.v-btn:focus{
    outline: none;
} */
/* .gray{
    color: #80809F;
    background-color: white;
} */
/* .gray::before{
    color: #80809F; */
    /* color: transparent; */
/* } */
/* .gray:hover{
    color: black;
    background: none;
    border-color: none;
} */
/* .gray:hover:before{
    color: red;
} */
</style>