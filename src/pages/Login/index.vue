<template>
  <v-container fluid class="fill-height">
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="4">
        <v-card class="mt-5 mx-auto">
          <v-toolbar color="primary" dark flat>
            <v-toolbar-title>Login</v-toolbar-title>
          </v-toolbar>
          <v-card-text>
            <v-form>
              <v-text-field
                label="Username"
                prepend-icon="mdi-account-circle"
              />
              <v-text-field
                :type="showPassword ? 'text' : 'password'"
                label="Password"
                prepend-icon="mdi-lock"
                :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPassword = !showPassword"
              />
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-btn color="info" primary large block>Login</v-btn>
            <v-spacer />
            <nuxt-link to="/">Forgot Password</nuxt-link>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false,
    }
  },
  head: {
    title: 'Login',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Login Description',
      },
    ],
  },
}
</script>
