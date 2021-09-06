<template>
  <v-footer id="footer" :fixed=true>
    <v-col class="text-center" cols="12">
      <img width="16" height="12" class="locale" v-for="(locale) in locales" :key="locale.code" @click="$i18n.locale = locale.code" :src="locale.image">
      {{ $t('footer.version') }}
      <strong>Alpha 1.0</strong>
      {{ ' — ' }}
      {{ $t('footer.madeby') }}
      <strong>Henry is cool?</strong>
      {{ ' — ' }}
      <a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" target="_blank"><strong>{{ $t('footer.discord') }}</strong></a>
      {{ ' — ' }}
    </v-col>
  </v-footer>
</template>

<script>
export default {
  name: 'Footer',
  data () {
    return {
      locales: [
        {
          code: 'en',
          image: require('@/assets/locales/en.png')
        },
        {
          code: 'pt',
          image: require('@/assets/locales/pt.png')
        }
      ]
    }
  }
}
</script>

<style>
.locale {
  margin-right: 8px;
  cursor: pointer;
}
</style>
