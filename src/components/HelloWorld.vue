<template>
  <v-app id="inspire">
    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-flex xs12 sm8 md4>
            <v-card class="elevation-12">
              <v-toolbar dark color="primary">
                <v-toolbar-title>Switching stuff</v-toolbar-title>
              </v-toolbar>
              <v-card-text>
                <v-form>

                  <v-text-field v-if="showingInputs" v-model="input1" prepend-icon="person" name="input1" label="Type stuff here" type="text"></v-text-field>

                  <p v-if="!showingInputs">{{input1}}</p>

                  <v-text-field v-if="showingInputs" v-model="input2" prepend-icon="lock" name="input2" label="Type here too" type="text"></v-text-field>

                  <p v-if="!showingInputs">{{input2}}</p>

                </v-form>
              </v-card-text>
              <v-card-actions>
                <v-spacer></v-spacer>

                <v-btn v-on:click.prevent="showingInputs = !showingInputs" color="primary">Switch</v-btn>

              </v-card-actions>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    input1: '',
    input2: '',
    showingInputs: true,
  })
}
</script>
