<!-- =========================
     CINEMATIC LYRIC ANIMATION
     ========================= -->

<style>

.lyric {
  opacity: 0;
  transform-box: fill-box;
  transform-origin: center;
}

/* Line 1 */
.l1 {
  animation:
    lyricIn 1.4s ease-out 0.8s forwards,
    lyricOut 1s ease-in 5.2s forwards;
}

/* Line 2 */
.l2 {
  animation:
    lyricIn 1.4s ease-out 5.8s forwards,
    lyricOut 1s ease-in 10.2s forwards;
}

/* Line 3 */
.l3 {
  animation:
    lyricIn 1.4s ease-out 10.8s forwards,
    lyricOut 1s ease-in 16.2s forwards;
}

/* Line 4 */
.l4 {
  animation:
    lyricIn 1.6s ease-out 16.8s forwards,
    finalGlow 3s ease-in-out 18.5s infinite;
}

@keyframes lyricIn {
  0% {
    opacity: 0;
    transform: translateY(18px);
    filter: blur(8px);
  }

  60% {
    opacity: .75;
    filter: blur(2px);
  }

  100% {
    opacity: 1;
    transform: translateY(0);
    filter: blur(0);
  }
}

@keyframes lyricOut {
  0% {
    opacity: 1;
    filter: blur(0);
  }

  100% {
    opacity: 0;
    filter: blur(7px);
  }
}

@keyframes finalGlow {
  0%, 100% {
    opacity: .8;
    filter: drop-shadow(0 0 4px #9b8cff);
  }

  50% {
    opacity: 1;
    filter:
      drop-shadow(0 0 12px #b9a7ff)
      drop-shadow(0 0 25px #6c63ff);
  }
}

</style>

<!-- Lyrics -->

<g
  text-anchor="middle"
  font-family="Georgia, serif"
  font-size="29"
  fill="url(#textGradient)"
>

  <text class="lyric l1" x="600" y="410">
    Moon, tell me if I could
  </text>

  <text class="lyric l2" x="600" y="410">
    Send up my heart to you?
  </text>

  <text class="lyric l3" x="600" y="410">
    So, when I die, which I must do
  </text>

  <text class="lyric l4" x="600" y="410">
    Could it shine down here with you?
  </text>

</g>
