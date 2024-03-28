<script lang="ts" setup></script>

<template>
  <div class="bg:#ffe min-h:100vh">
    <header class="shadow:md">
      <div class="center-content flex jc:space-between max-w:screen-lg mx:auto p:4x">
        <div class="center-content flex gap:2x">
          <img src="/favicon-32x32.png" alt="Logo" />
          <span>alanlu-dev</span>
        </div>
        <nav>
          <ul class="center-content flex gap:4x">
            <li><NuxtLink to="/">Home</NuxtLink></li>
            <li><NuxtLink to="/about">About</NuxtLink></li>
          </ul>
        </nav>
      </div>
    </header>

    <main class="max-w:screen-lg min-h:full mx:auto pt:4x">
      <NuxtPage />
    </main>
  </div>
</template>
