<template>
  <v-btn depressed color="white" :href="href" class="text-capitalize">
    <slot />
    <v-icon>mdi-open-in-new</v-icon>
  </v-btn>
</template>

<script>
export default {
  props: {
    href: {
      type: String,
      required: true
    }
  }
}
</script>
