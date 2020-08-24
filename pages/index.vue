<template>
  <v-row justify="center" align="center">
    <v-col cols="12" md="11">
      <v-card>
        <v-card-title>
          <h3>
            Yuga Iwata
          </h3>
        </v-card-title>
        <v-card-subtitle>
          <h4>
            a.k.a awataki
          </h4>
        </v-card-subtitle>
        <v-card-text>
          <v-timeline dense>
            <Skills />
            <Hobbies />
            <Links />
          </v-timeline>
        </v-card-text>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Vue from 'vue'
import Skills from '~/components/Skills.vue'
import Hobbies from '~/components/Hobbies.vue'
import Links from '~/components/Links'

export default Vue.extend({
  components: {
    Skills,
    Hobbies,
    Links
  }
})
</script>
