<template>
  <svg class="main-logo" width="40" height="29.3" viewBox="0 0 30 22" xmlns="http://www.w3.org/2000/svg">
    <g>
      <path class="main-logo__decorator" d="M4.969,9.684L0,4.842L4.969,0h2.846L2.824,4.842l4.991,4.842H4.969z" />
      <path class="main-logo__decorator" d="M22.185,22l4.991-4.842l-4.991-4.842h2.846L30,17.158L25.031,22H22.185z" />
      <!-- <path class="main-logo__h-letter" d="M11.72,7.56c-.1-1.88-.22-4.14-.2-5.82h-.06C11,3.32,10.44,5,9.76,6.86L7.38,13.4H6.06L3.88,7C3.24,5.08,2.7,3.34,2.32,1.74h0c0,1.68-.14,3.94-.26,6l-.36,5.78H0L.94,0H3.16l2.3,6.52c.56,1.66,1,3.14,1.36,4.54h.06C7.22,9.7,7.7,8.22,8.3,6.52L10.7,0h2.22l.84,13.48h-1.7Z"/> -->
      <path
        class="main-logo__h-letter"
        d="M10.907,17.336V4.664h1.866v5.35c0.293-0.504,0.701-0.9,1.223-1.188c0.522-0.287,1.1-0.431,1.733-0.431
			c1.044,0,1.866,0.329,2.464,0.986c0.598,0.657,0.897,1.637,0.897,2.939v5.016h-1.848v-4.822c0-1.69-0.675-2.535-2.024-2.535
			c-0.704,0-1.287,0.246-1.751,0.739c-0.463,0.493-0.695,1.196-0.695,2.112v4.505H10.907z"
      />
    </g>
  </svg>
</template>

<style lang="scss">
.dark-mode .main-logo {
  --main-logo-h-letter-background: #{$text-color-dark};
}

.main-logo {
  --main-logo-h-letter-background: #{$text-color};

  width: 100%;
  height: 100%;
  animation: 1s appear;
  margin: auto;

  &__decorator {
    fill: $main-color;
  }

  &__h-letter {
    fill: var(--main-logo-h-letter-background);
  }
}

@keyframes appear {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
