<template>
  <div>
    <upload v-show="avataredit" :server="upload.server" :api="upload.api" :filename="upload.filename" :params="upload.params" @success="upsuccess" v-model="newavatar" :crop="upload.crop" :width="upload.width" :height="upload.height" :ok="upload.ok" :cancel="upload.cancel">
        <button class="upavatar hdfont"></button>
    </upload>
  </div>
</template>
<script>
import upload from './uploadavatar.vue'
export default {
  components: { upload },
  data () {
    return {
      // 上传成功后的URL
      newavatar: null,
      upload: {
        server: '',
        api: '',
        params: {
          token: ''
        },
        preview: true,
        crop: true,
        width: 400,
        height: 400,
        cancel: '取消',
        ok: '裁剪',
        filename: 'MultiPart File'
      }
    }
  },

  methods: {
    // 上传成功后触发
    upsuccess () {
      console.log('success')
    }
  }
}
</script>
<style lang="stylus">
  i, em
    font-style normal
  html
    -webkit-tap-highlight-color transparent
    -ms-text-size-adjust 100%
    -webkit-text-size-adjust 100%
    font-size 10px
  body, sub, sup
    position relative
  b, dt, optgroup, strong
    font-weight 700
  hr, legend, td, th
    padding 0
  hr, iframe, img, legend
    border 0
  button, img, input:not([type=radio]):not([type=checkbox]), select
    vertical-align middle
  table
    border-spacing 0
  *
    box-sizing border-box
  body, html
    min-height 100%
    width 100%
    height 100%
  article, aside, details, figcaption, figure, footer, header, hgroup, main, menu, nav, section, summary
    display block
  audio, canvas, progress, video
    display inline-block
    vertical-align baseline
  audio:not([controls])
    display none
    height 0
  [hidden], script, template
    display none
  a
    background-color transparent
    color #095f8a
    &:active,
    &:hover,
    &:focus
      outline 0
  a, ins
    text-decoration none
  q
    quotes "\201C" "\201D" "\2018" "\2019"
  small
    font-size 80%
  sub, sup
    font-size 75%
    line-height 0
    vertical-align baseline
  sup
    top -.5em
  sub
    bottom -.25em
  svg:not(:root)
    overflow hidden
  fieldset
    padding .35em .625em .75em
  button, input, optgroup, select, textarea
    color inherit
    margin 0
    outline none
    text-rendering optimizeLegibility
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    -moz-font-feature-settings "liga", "kern"
  button
    overflow visible
  button, input
    line-height:normal
  button, select
    text-transform none
  button, html input[type=button], input[type=reset], input[type=submit]
    -webkit-appearance button
    cursor pointer
  input[type=checkbox], input[type=radio]
    cursor pointer
    padding 0
  button[disabled], html input[disabled]
    cursor default
  button::-moz-focus-inner, input::-moz-focus-inner
    border 0
    padding 0
  input[type=search]
    -webkit-appearance textfield
  input[type=search]::-webkit-search-cancel-button, input[type=search]::-webkit-search-decoration
    -webkit-appearance none
  textarea
    overflow auto
    vertical-align top
    resize vertical
  body
    margin:0
    font-family Arial, "Segoe UI", "Lucida Grande", Helvetica, "Microsoft YaHei", FreeSans, Arimo, "Droid Sans", "wenquanyi micro hei", "Hiragino Sans GB", "Hiragino Sans GB W3", sans-serif, 'Helvetica Neue', STHeiti
    font-weight 400
    color #333
    font-size 1.6rem
  .mine
    max-width 1200px
    margin 0 auto
@font-face {
  font-family: 'hdfont';  /* project id 210692 */
  src: url('//at.alicdn.com/t/font_c5zd9f9othvndn29.eot');
  src: url('//at.alicdn.com/t/font_c5zd9f9othvndn29.eot?#iefix') format('embedded-opentype'),
  url('//at.alicdn.com/t/font_c5zd9f9othvndn29.woff') format('woff'),
  url('//at.alicdn.com/t/font_c5zd9f9othvndn29.ttf') format('truetype'),
  url('//at.alicdn.com/t/font_c5zd9f9othvndn29.svg#hdfont') format('svg');
}
  .hdfont:after,
  .hdfont:before
    font-family hdfont
    font-style normal
    -webkit-font-smoothing antialiased
    -webkit-text-stroke-width .2px
    -moz-osx-font-smoothing grayscale
  #app
    width 100%
    height 100%
  .fade-enter-active,
  .fade-leave-active,
  .v-enter-active,
  .v-leave-active
    transition: opacity .5s
  .fade-enter,
  .fade-leave-active,
  .v-enter,
  .v-leave-active
    opacity: 0
.upavatar
  background none
  border 0
  &:before
    content '\e635'
    font-size 35px
</style>
