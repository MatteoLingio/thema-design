<template>
  <div class="grid">
    <slot></slot>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/styles/_spacing.scss";
@import "../assets/styles/_mixins.scss";

.grid {
  display: flex;
  flex-direction: row;
  background-color: blue;
  height: 100vh;
  width: 100%;
  flex-wrap: wrap;

  &--vertical {
    flex-direction: column;
  }
}

.col {
  margin: $grid_margin;
  &--no-gap {
    margin: 0;
  }
}

// @media (max-width: 768px) {
//   @for $i from 1 through 12 {
//     .sm-#{$i} {
//       @include column-width($i);
//     }
//   }
// }

@include for-phone-only {
  @for $i from 1 through 12 {
    .sm-#{$i} {
      @include column-width($i, false);
    }
  }
}

@include for-tablet-portrait-up {
  @for $i from 1 through 12 {
    .md-#{$i} {
      @include column-width($i, false);
    }
  }
}

@include for-big-desktop-up {
  @for $i from 1 through 12 {
    .xl-#{$i} {
      @include column-width($i, false);
    }
  }
}

@include for-desktop-up {
  @for $i from 1 through 12 {
    .lg-#{$i} {
      @include column-width($i, false);
    }
  }
}
</style>
