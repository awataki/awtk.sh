<template>
  <v-container fluid>
    <v-row justify="center" align="start">
      <v-col cols="12">
        <v-card>
          <v-card-title class="primary white--text">
            Services
          </v-card-title>
          <v-card-text>
            <v-list>
              <h3>Active</h3>
              <v-list-item v-for="i in activeServices" :key="i">
                <link-btn :href="i.link">
                  {{ i.title }}
                </link-btn>
              </v-list-item>
              <h3>Inactive</h3>
              <v-list-item v-for="i in inactiveServices" :key="i">
                <link-btn :href="i.link" disabled>
                  {{ i.title }}
                </link-btn>
              </v-list-item>
            </v-list>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import LinkBtn from '~/components/LinkBtn'

export default {
  components: {
    LinkBtn
  },
  data () {
    return {
      activeServices: [
        {
          title: '投票ツール Vothemis',
          link: 'https://vothemis.awtk.sh'
        },
        {
          title: '人狼ツール Fenrir',
          link: 'https://fenrir.awtk.sh'
        }
      ],
      inactiveServices: [
        {
          title: '神奈川工科大学バス時刻 KaitBusTime',
          link: 'https://bus.awtk.sh'
        }
      ]
    }
  }
}
</script>
