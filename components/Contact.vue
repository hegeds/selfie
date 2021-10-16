<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>Contact</h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-form name="contact" method="POST" data-netlify="true">
          <v-row>
            <v-col sm="6" cols="12">
              <v-text-field type="text" name="name" label="Name" filled />
            </v-col>
            <v-col>
              <v-text-field type="email" name="email" label="Email" filled />
            </v-col>
          </v-row>
          <v-row>
            <v-col>
              <v-textarea name="message" label="Message" filled />
            </v-col>
          </v-row>
          <v-btn
            type="submit"
            color="blue-grey darken-4"
            x-large
          >
            Submit
          </v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>
