<template>
  <TimeLineCard>
    <template v-slot:title>
      <v-icon color="white" class="mr-2">
        mdi-code-json
      </v-icon>
      Skills
    </template>
    <v-list>
      <h3>Backend</h3>
      <v-list-item>
        <img src="~assets/logos/logos/kotlin.svg" class="svg mr-3"> Kotlin
      </v-list-item>
      <v-list-item>
        <img src="~assets/ppl/go/go.svg" class="svg mr-3"> Golang
      </v-list-item>
      <v-list-item>
        <img src="~assets/logos/logos/java.svg" class="svg mr-3"> Java (1.8~)
      </v-list-item>
      <h3>Frontend</h3>
      <v-list-item>
        <img src="~assets/logos/logos/typescript-icon.svg" class="svg mr-3"> Type Script
      </v-list-item>
      <v-list-item>
        <img src="~assets/logos/logos/nuxt-icon.svg" class="svg mr-3"> Nuxt.js
      </v-list-item>
      <h3>Infra</h3>
      <v-list-item>
        <img src="~assets/logos/logos/docker-icon.svg" class="svg mr-3"> Docker
      </v-list-item>
      <v-list-item>
        <img src="~assets/logos/logos/linux-tux.svg" class="svg mr-3"> Linux
      </v-list-item>
      <v-list-item>
        <img src="~assets/logos/logos/nginx.svg" class="svg mr-3"> Nginx
      </v-list-item>
    </v-list>
  </TimeLineCard>
</template>

<script lang="ts">
import Vue from 'vue'
import TimeLineCard from '@/components/TimeLineCard.vue'

export default Vue.extend({
  components: {
    TimeLineCard
  }
}
)
</script>

<style scoped>
.svg {
  height: 32px;
  width: 32px;
}
</style>
