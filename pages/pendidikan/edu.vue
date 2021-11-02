<template>
  <v-container style="max-width: 600px;">
    <v-timeline
      dense
      clipped
    >
      <v-timeline-item
        fill-dot
        class="white--text mb-12"
        color="orange"
        large
      >
        <template v-slot:icon>
          <span>JL</span>
        </template>
       
          <template v-slot:append>
            <v-btn
              class="mx-0"
              depressed
              @click="comment"
            >
              Post
            </v-btn>
          </template>
        </v-text-field>
      </v-timeline-item>

      <v-timeline-item
        class="mb-4"
        color="grey"
        small
      >
        <v-row justify="space-between">
          <v-col cols="7">
           SD Waikabubak III
          </v-col>
          <v-col
            class="text-right"
            cols="5"
          >
            2006-2011
          </v-col>
        </v-row>
      </v-timeline-item>

<v-timeline-item
        class="mb-4"
        color="grey"
        small
      >
        <v-row justify="space-between">
          <v-col cols="7">
          SMA Stella Duce 2 Yogyakarta
          </v-col>
          <v-col
            class="text-right"
            cols="5"
          >
            2014-2017
          </v-col>
        </v-row>
      </v-timeline-item>



      <v-timeline-item
        color="grey"
        small
      >
        <v-row justify="space-between">
          <v-col cols="7">
            Universitas Sanata Dharma
          </v-col>
          <v-col
            class="text-right"
            cols="5"
          >
            2017-2021
          </v-col>
        </v-row>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      events: [],
      input: null,
      nonce: 0,
    }),

    computed: {
      timeline () {
        return this.events.slice().reverse()
      },
    },

    methods: {
      comment () {
        const time = (new Date()).toTimeString()
        this.events.push({
          id: this.nonce++,
          text: this.input,
          time: time.replace(/:\d{2}\sGMT-\d{4}\s\((.*)\)/, (match, contents, offset) => {
            return ` ${contents.split(' ').map(v => v.charAt(0)).join('')}`
          }),
        })

        this.input = null
      },
    },
  }
</script>