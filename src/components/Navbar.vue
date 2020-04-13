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
                    <a class="nav-item nav-link" href="../views/help">HELP</a>
                    <a class="nav-item nav-link" href="../views/privacy">PRIVACY</a>
                    <a class="nav-item nav-link" href="../views/blog">Blog</a>
                    <a class="nav-item nav-link" href="../views/login">Login</a>
                    <a class="nav-item nav-link" href="../views/SignUp">CREATE ACCOUNT</a>
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