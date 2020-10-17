<template>
  <v-card width="450" class="mx-auto mt-5">
    <v-card-title>
      <h1 class="display-1">登入</h1>
    </v-card-title>
    <v-card-text>
      <v-form>
        <v-text-field 
          label="Email"
          prepend-icon="mdi-email"
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
    <v-divider></v-divider>
    <v-card-actions>
      <v-btn color="success">註冊</v-btn>
      <v-spacer></v-spacer>
      <v-btn color="info">登入</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
  export default {
    name: 'Login',

    data: () => ({
      showPassword: false
    }),
  }
</script>
