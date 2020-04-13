<template>
    <div class="nav">
        <v-container>
            <nav class="navbar  navbar-expand-sm navbar-light">
                <a href="/" class="LogoBtn">SIME</a>
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                    <div class="navbar-nav subLinks">
                        <v-btn class="nav-item nav-link" text to="/help">HELP</v-btn>
                        <v-btn class="nav-item nav-link" text to="/privacy">PRIVACY</v-btn>
                        <v-btn class="nav-item nav-link" text to="/blog">Blog</v-btn>
                        <v-btn class="nav-item nav-link" text to="/login">Login</v-btn>
                        <v-btn class="nav-item nav-link" rounded text to="/SignUp">CREATE ACCOUNT</v-btn>
                    <!-- <a class="nav-item nav-link" href="/help">HELP</a>
                    <a class="nav-item nav-link" href="/privacy">PRIVACY</a>
                    <a class="nav-item nav-link" href="/blog">Blog</a>
                    <a class="nav-item nav-link" href="/login">Login</a>
                    <a class="nav-item nav-link" href="/SignUp">CREATE ACCOUNT</a> -->
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
</style>