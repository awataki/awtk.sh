<template>
  <TimeLineCard>
    <template v-slot:title>
      <v-icon color="white" class="mr-2">
        mdi-link
      </v-icon>
      Links
    </template>
    <v-list>
      <v-list-item>
        <link-btn href="https://twitter.com/awataki1206">
          <img src="~assets/logos/logos/twitter.svg" class="svg mr-3"> Twitter
        </link-btn>
      </v-list-item>
      <v-list-item>
        <link-btn href="https://github.com/awataki">
          <img src="~assets/logos/logos/github-icon.svg" class="svg mr-3"> Github
        </link-btn>
      </v-list-item>
    </v-list>
  </TimeLineCard>
</template>

<script lang="ts">
import Vue from 'vue'
import TimeLineCard from '@/components/TimeLineCard.vue'
import LinkBtn from '~/components/LinkBtn.vue'

export default Vue.extend({
  components: {
    TimeLineCard,
    LinkBtn
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
