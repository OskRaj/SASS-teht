# SASS OMINAISUUDET - BISTRO AURORA PROJEKTI

## 1. MUUTTUJAT (_variables.scss)
- Värimuuttujat: `$primary-color`, `$secondary-color`, `$text-color`
- Typografiamuuttujat: `$main-font`, `$heading-font`, `$font-size`
- Mittamuuttujat: `$container-width`, `$padding`, `$margin`, `$border-radius`

## 2. MIXINS + INCLUDE (_mixins.scss)

- `@mixin button($bg-color, $text-color: white)` - nappi parametreilla
- `@mixin container` - keskitetty säiliö
- `@mixin mobile` - media query responsiivisuuteen

## 3. SISÄKKÄISET VALITSIMET & & PARENT (_layout.scss)
```scss
.site-header {
  .container {           // Sisäkkäinen valitsin
    .logo {             // Syvempi nesting
      &:hover { }       // Parent selector hover-tilalle
      span { }          // Sisäkkäinen elementti
    }
  }
}

.nav-link {
  &.is-active { }       // Parent selector modifierille
  &:hover { }           // Parent selector pseudo-classille
}
```

## 4. OSITTAISET TIEDOSTOT JA IMPORT (style.scss)
- `@import 'variables'` - tuo _variables.scss
- `@import 'mixins'` - tuo _mixins.scss  
- `@import 'layout'` - tuo _layout.scss


## 5. FUNKTIOT JA OPERAATTORIT (style.scss)
- `@function make-darker($color, $amount: 10%)` - oma funktio
- `darken($color, 10%)` - Sass sisäänrakennettu funktio
- `lighten($color, 30%)` - värien vaalentaminen
- Värilaskut: `$btn-color: $primary-color`

## 6. RESPONSIIVISUUS
- Media query mixin: `@mixin mobile`
- CSS Grid: `grid-template-columns: 2fr 1fr`
- Responsiivinen muutos: mobiilissa `grid-template-columns: 1fr`

## 7. KOMPONENTIT
- `.btn` - perusnappi
- `.btn-primary`, `.btn-secondary` - nappivariantit
- `.hero` - hero-osio gradientilla
- `.card` - korttikomponentit hover-efekteillä
- `.grid` - responsiivinen layout-systeemi
