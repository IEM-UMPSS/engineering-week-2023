<template>
	<Carousel />
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