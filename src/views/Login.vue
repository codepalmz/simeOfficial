

<template>

    <div class="login">
        <div class="split left">
      <div class="centered"></div>
    </div>

    <div class="split right">
      <div class="centered">
        <div class="content">
          <div class="welcome">
              <v-container fluid>
                <v-layout row>
                <v-flex xs6 order-lg2>
                    <v-card tile class="mt-n3 ml-7" flat color="#f4f7f6">
                    <a href="/" class="logoBtn">SIME</a>
                    </v-card>
                </v-flex>
                <v-flex xs6>
                    <v-card tile flat color="#f4f7f6" align="end">
                        <a href="/signup" class="createBtn">Create an account</a>
                    </v-card>
                </v-flex>
                </v-layout>
              </v-container>

              <v-spacer></v-spacer>

              <v-container fluid>
                <v-layout row>
                <v-flex xs12 order-lg2>
                    <v-card tile flat class="ml-5" color="#f4f7f6" align="start">
                    <v-card-text class="mt-10 font-weight-black details">Login to Sime</v-card-text>
                    <v-card-text class="mt-n5">Enter your credentials below</v-card-text>
                    </v-card>
                </v-flex>
                </v-layout>
              </v-container>

              <v-spacer></v-spacer>

              <v-container fluid>
                <v-layout row>
                <v-flex md8 sm10 xs10 order-lg2>
                    <v-card tile flat class="ml-9" color="#f4f7f6" align="start">
                        <form>
                            <v-text-field
                            v-model="name"
                            :error-messages="nameErrors"
                            label="Name"
                            outlined
                            required
                            class="mt-n4"
                            color="#636463"
                            @input="$v.name.$touch()"
                            @blur="$v.name.$touch()"
                            ></v-text-field>
                            <v-text-field
                            v-model="email"
                            :error-messages="emailErrors"
                            label="E-mail"
                            outlined
                            required
                            class="mt-n2"
                            color="#636463"
                            @input="$v.email.$touch()"
                            @blur="$v.email.$touch()"
                            ></v-text-field>

                        <v-btn rounded color="#636463" class="mt-n2 mr-4 loginBtn" @click="submit"><span class="btnText">Submit</span></v-btn>
                    </form>
                    </v-card>
                </v-flex>
                </v-layout>
              </v-container>

              <v-spacer></v-spacer>

              <v-container fluid>
                <v-layout row>
                <v-flex xs12 order-lg2>
                    <v-card tile flat class="mt-n3 ml-5" color="#f4f7f6" align="start">
                    <v-card-text class="ForgotPwdDetails">
                        Forgot your Password?
                        <a href="/blog">Reset Now</a>
                        <!-- <v-btn text class="ml-n9 mt-n1 resetBtn">Reset Now</v-btn>     -->
                    </v-card-text>
                    <v-card-text class="mt-n5 termsCond">
                        <span>By using Wiza you agree to our <a href="#">Terms of services</a> and <a href="#">Privacy policy</a></span>
                    </v-card-text>
                    </v-card>
                </v-flex>
                </v-layout>
                <!--  -->
              </v-container>
          </div>
        </div>
        
      </div>
    </div>
    </div>
</template>

<script>

import { validationMixin } from 'vuelidate'
import { required, maxLength, email } from 'vuelidate/lib/validators'

  export default {
    mixins: [validationMixin],

    validations: {
      name: { required, maxLength: maxLength(40) },
      email: { required, email },
    },

    data: () => ({
      name: '',
      email: '',
    }),

    computed: {
      nameErrors () {
        const errors = []
        if (!this.$v.name.$dirty) return errors
        !this.$v.name.maxLength && errors.push('Name must be at most 10 characters long')
        !this.$v.name.required && errors.push('Name is required.')
        return errors
      },
      emailErrors () {
        const errors = []
        if (!this.$v.email.$dirty) return errors
        !this.$v.email.email && errors.push('Must be valid e-mail')
        !this.$v.email.required && errors.push('E-mail is required')
        return errors
      },
    },

    methods: {
      submit () {
        this.$v.$touch()
      },
      clear () {
        this.$v.$reset()
        this.name = ''
        this.email = ''
      },
    },
  }
</script>

<style scoped>
.logoBtn{
    font-size: 30px;
    font-weight: bold;
    color: #636463;
    text-decoration: none;
}
.createBtn{
    color: #636463;
    text-decoration: none;
    font-weight: 600;
}
.split{
    height: 100%;
    width: 50%;
    position: fixed;
    z-index: 1;
    top: 0;
    overflow-x: hidden;
    padding-top: 20px;
}

.left{
    left: 0;
    background: url('../assets/1.jpeg') no-repeat;
    background-position: center;
    background-size: cover;
}

.right{
    right: 0;
    background-color: #f4f7f6;
}

.loginBtn{
    max-width: 200px;
}

.resetBtn{
    color: #636463;
    max-width: 30%;
}
.termsCond{
    font-size: 13px;
}

.termsCond a{
    color: #2d2e2d;
}
/* btn on smaller screens */
@media (max-width: 700px){
    .loginBtn{
    max-width: 50%;
}
.resetBtn{
    max-width: 20%;
    margin-left: 20px;
}
}

.btnText{
    color: white;
    font-size: 20px;
}

.details{
    font-weight: 900;
    font-size: 35px;
}

.ForgotPwdDetails{
    font-size: 16px;
}
/* .centered{
    position: absolute;
    top: 26.5%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
} */

.centered button{
    width: 100%;
}

@media (max-width: 700px){
    .split {
        width: 100%;
    }
}

.welcome a:visited {
    color: #636463;
}

.content-right{
    right: 50%;
    margin-top: 20px;
}

.content-left{
    left: 50%;
    margin-left: -50px;
    margin-top: -24px;
}

.form-control{
    width: 100%;
}
</style>