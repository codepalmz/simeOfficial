<template>
    <div class="nav">
        <v-container>
            <nav class="navbar  navbar-expand-sm navbar-light">
                <a href="/" class="LogoBtn" style="font-size: 40px;">SIME</a>
                
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse collapseSpace" id="navbarNavAltMarkup">
                    <!-- <div class="navbar-nav subLinks"> -->
                    <div class="navbar-nav subLinks">
                        <v-btn class="nav-item nav-link" text to="/help">HELP</v-btn>
                        <v-btn class="nav-item nav-link" text to="/privacy">PRIVACY</v-btn>
                        <v-btn class="nav-item nav-link" text to="/blog">Blog</v-btn>
                        <v-btn class="nav-item nav-link" text to="/login">Login</v-btn>
                        <v-btn class="nav-item nav-link" rounded text to="/signup">CREATE ACCOUNT</v-btn>
                    </div>
                </div>
            </nav>
        </v-container>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scoped>
a{
    color: black;
}
.LogoBtn a{
    font-size: 30px;
    font-weight: bold;
    color: #636463;
    text-decoration: none;
}
.subLinks a{
    color: black;
}
.collapseSpace{
    margin-left: 350px;
}
/* @media (min-width:800px) and (min-width:400px)  {
    .collapseSpace{
    margin-left: 230px;
    }
} */
@media (min-width:600px){
    .collapseSpace{
    margin-left: 100px;
    }
}
@media (min-width:400px){
    .collapseSpace{
    margin-left: 10px;
    }
}
@media (min-width:300px){
    .collapseSpace{
    margin-left: -5px;
    }
}
</style>