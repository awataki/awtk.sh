<template>
  <TimeLineCard>
    <template v-slot:title>
      <v-icon color="white" class="mr-2">
        mdi-heart
      </v-icon>
      Hobbies
    </template>
    <v-list>
      <v-list-group
        v-for="item in hobbies"
        :key="item.title"
        v-model="item.active"
        :prepend-icon="item.icon"
        no-action
      >
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </template>
        <h3 class="black--text ma-5 mx-10" style="font-weight: 300;">
          {{ item.description }}
        </h3>
        <v-list-item
          v-for="subItem in item.likes"
          :key="subItem.title"
          no-action
        >
          <v-list-item-content>
            <v-list-item-title v-text="subItem.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list-group>
    </v-list>
  </TimeLineCard>
</template>

<script lang="ts">
import Vue from 'vue'
import TimeLineCard from '@/components/TimeLineCard.vue'

export default Vue.extend({
  components: {
    TimeLineCard
  },
  data () {
    return {
      hobbies: [

        {
          icon: 'mdi-headphones',
          title: 'Music',
          description: '青天井の趣味その1:傾向としてはFuture BassとかEDM系',
          likes: [
            { title: 'AKG K702' },
            { title: 'AKG N5005' },
            { title: 'Fostex HP-A4' },
            { title: '椎名林檎' },
            { title: '中村さんそ' }
          ],
          active: false
        },
        {
          icon: 'mdi-network-outline',
          title: 'Network',
          description: '青天井の趣味その2:自宅ラック勢。OpenStack移行計画進行中…',
          active: false
        },
        {
          icon: 'mdi-camera',
          title: 'Photograph',
          description: '青天井の趣味その3:風景写真メインで撮ってます。',
          likes: [
            { title: 'EOS 40D' }
          ],
          active: false
        },

        {
          icon: 'mdi-book',
          title: 'Reading',
          description: '比較的ミステリーが好きです。',
          likes: [
            { title: '米沢穂信' },
            { title: '有栖川有栖' },
            { title: '冲方丁' }
          ],
          active: false
        }
      ]
    }
  }
}
)
</script>
