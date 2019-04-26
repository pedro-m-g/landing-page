<template>
  <main>
    <AppHero @more="$refs.highlights.$el.scrollIntoView()" />
    <div class="container">
      <AppHighlights ref="highlights" />
    </div>
  </main>
</template>
<script>
import AppHero from '@/components/AppHero'
import AppHighlights from '@/components/AppHighlights'
export default {
  components: {
    AppHero,
    AppHighlights
  }
}
</script>
