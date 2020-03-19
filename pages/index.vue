<template>
  <div class="container">
    <div>
      <sf-section
        title-heading="tech-for-rescue"
        subtitle-heading="Tech companies for help during corona time"
        level-haeding="2"
      >
        Łączę ponownie… IT is here to help 100% We need a lot of new tools to
        help People go through the crisis. Software Companies are eager to help
        here. We've collected a list of super-talented companies that are open
        to help NGOs, Gov, and others. Please share it. If you run a Software
        Company, feel free to add yourself here too. Add your company here:
        https://docs.google.com/forms/d/e/1FAIpQLSePKBbiJy8Phazb8c3ngH6eSgI8dwwVRKWpeCYttsji6YWnqQ/viewform?fbclid=IwAR0obUDdn9XnXXNTKEvP9LRkTDyZ_Wk8qoGASDOuxfxWm3LTo0XpufWwwwI
        If you need any help, you can contact me at Linkedin:
        https://www.linkedin.com/in/tkarwatka/ Aby włączyć obsługę czytnika
        ekranu, naciśnij Ctrl+Alt+Z. Aby uzyskać informacje o skrótach
        klawiszowych, naciśnij Ctrl+ukośnik.
      </sf-section>
    </div>
  </div>
</template>

<script>
import { SfSection } from '@storefront-ui/vue'

export default {
  components: {
    SfSection
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
