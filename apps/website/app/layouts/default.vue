<script lang="ts" setup></script>

<template>
  <div class="bg:#ffe min-h:100vh flex flex:col">
    <header class="shadow:md">
      <div class="center-content flex jc:space-between max-w:screen-lg mx:auto p:4x">
        <div class="center-content flex gap:2x">
          <img src="/favicon-32x32.png" alt="Logo" />
          <span>alanlu-dev</span>
        </div>
        <nav>
          <ul class="center-content flex gap:4x">
            <li>
              <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about">About</NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </header>

    <main class="flex:1 max-w:screen-lg min-h:full mx:auto pt:4x">
      <NuxtPage />
    </main>

    <footer>
      <div class="max-w:screen-lg mx:auto p:4x t:center">
        <p>© 2024-{{ new Date().getFullYear() }} <a class="link" href="https://github.com/alanlu-tw" target="_blank">Alan Lu</a>. All rights reserved.</p>
      </div>
    </footer>
  </div>
</template>
