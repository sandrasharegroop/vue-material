<template>
  <md-content md-tag="section" class="home-sponsors">
    <div class="page-wrapper">
      <h2 class="home-title md-headline">
        <md-icon>monetization_on</md-icon>
        {{ $t('pages.home.sponsors') }} &amp; {{ $t('pages.home.backers') }}
      </h2>

      <div class="home-sponsors-description">
        <i18n path="pages.home.sponsorsDescription" tag="p">
          <a href="https://www.github.com/marcosmoura" target="_blank">Marcos Moura</a>
        </i18n>

        <p>{{ $t('pages.home.beAPatron') }}:</p>

        <a href="https://www.patreon.com/bePatron?u=4832202" target="_blank" class="home-sponsors-patreon">
          <md-ripple>
            <img src="/assets/sponsors/patreon.png">
          </md-ripple>
        </a>
      </div>
    </div>
  </md-content>
</template>

<script>
  import MdSvgLoader from 'vue-material/components/MdSvgLoader/MdSvgLoader'

  export default {
    name: 'HomeSponsors',
    components: {
      MdSvgLoader
    }
  }
</script>

<style lang="scss" scoped>
  @import "~vue-material/components/MdAnimation/variables";
  @import "~vue-material/components/MdLayout/mixins";

  .home-sponsors {
    width: calc(100% + 32px);
    margin: 0 -16px -16px;
    padding-bottom: 28px;
  }

  .home-sponsors-patreon {
    max-width: 180px;
    margin: 24px 0;
    display: inline-block;
  }

  .home-sponsors-backers {
    margin-top: 36px;
  }

  .home-sponsor {
    color: #000 !important;

    + .home-sponsor {
      margin-left: 16px;
    }

    .md-ripple {
      padding: 12px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      background: #fff;
      border-radius: 2px;
    }

    img,
    >>> svg,
    .md-svg-loader {
      max-width: 256px;
      max-height: 96px;
      display: block;
    }
  }

  .home-sponsor-list {
    margin-bottom: 36px;
  }
</style>
