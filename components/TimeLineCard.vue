<template>
  <v-timeline-item>
    <v-card>
      <v-card-title class="primary white--text">
        <slot name="title" />
      </v-card-title>
      <v-card-text>
        <slot />
      </v-card-text>
    </v-card>
  </v-timeline-item>
</template>
