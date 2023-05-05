<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="8" lg="6">
        <Carousel />
        <v-card class="mx-auto" outlined>
          <v-card-title>About Engineering Week</v-card-title>
          <v-card-text>
            Engineering Week is an annual event that celebrates the field of engineering and its contributions to society. Join us for a week of exciting events and activities that showcase the innovative and creative side of engineering!
          </v-card-text>
        </v-card>
        <v-card-subtitle class="mb-2">Follow us on:</v-card-subtitle>
        <v-row align="center" justify="start">
          <v-col cols="12" sm="6" class="d-flex align-left justify-left">
            <v-btn icon href="https://www.facebook.com/engineeringweek2022">
              <v-icon size="24">mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon href="https://www.instagram.com/engineeringweek_2023/">
              <v-icon size="24">mdi-instagram</v-icon>
            </v-btn>
          </v-col>
        
          <v-col cols="12" class="my-4">
            <h2 class="text-center">Upcoming Event</h2>
            <v-card class="my-4" outlined>
              <v-card-title>Event 1</v-card-title>
              <v-card-subtitle>May 13, 2023 11:00:00</v-card-subtitle>
                <v-col cols="12" sm="6" class="d-flex align-left justify-center">
                  <v-icon size="24" class="mr-2">mdi-clock-time-four-outline</v-icon>
                  <div>{{ countdown }}</div>
                </v-col>
              <v-card-text>
                Description of event 1.
              </v-card-text>
            </v-card>
            <v-card class="my-4" outlined>
              <v-card-title>Event 2</v-card-title>
              <v-card-subtitle>May 14, 2023 14:30:00</v-card-subtitle>
              <v-card-text>
                Description of event 2.
              </v-card-text>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      countdown: '',
      eventDate: new Date('May 13, 2023 11:00:00').getTime()
    }
  },
  mounted() {
    this.startCountdown()
  },
  methods: {
    startCountdown() {
      let interval = setInterval(() => {
        let now = new Date().getTime()
        let distance = this.eventDate - now
        let days = Math.floor(distance / (1000 * 60 * 60 * 24))
        let hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))
        let minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))
        let seconds = Math.floor((distance % (1000 * 60)) / 1000)
        this.countdown = `${days}d ${hours}h ${minutes}m ${seconds}s`         
        if (distance < 0) {
          clearInterval(interval)
          this.countdown = 'EXPIRED'
        }
      }, 1000)
    }
  }
}
</script>