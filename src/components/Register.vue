<template>
    <v-card>
        <v-card-title>
            <h1 class="display-1">註冊</h1>
        </v-card-title>
        <v-card-text>
            <v-form>
                <v-text-field
                  label="名稱"
                  prepend-icon="mdi-account-circle" 
                />
                <v-text-field 
                  label="電子郵件"
                  prepend-icon="mdi-email"
                />
                <v-text-field 
                  :type="showPassword ? 'text' : 'password'"
                  label="密碼"
                  prepend-icon="mdi-lock"
                  :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                  @click:append="showPassword = !showPassword"
                />
            </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
            <v-btn color="success">送出</v-btn>
        </v-card-actions>
    </v-card>
</template>

<script>
export default {
    name: 'Reigster',
    data: () => ({
        showPassword: false
    }),
}
</script>