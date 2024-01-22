<template>
  <div>
    <HeadAndMeta />
    <!-- <Head>
      <component
        :is="'script'"
        src="https://cdn.jsdelivr.net/npm/pikaday/pikaday.js"
      ></component>
    </Head> -->
    <div
      class="flex flex-col bg-white dark:bg-neutral-950 text-neutral-900 dark:text-neutral-50"
    >
      <!-- <NavBar class="fixed bg-white dark:bg-neutral-950 shadow z-20" /> -->
      <!-- <main class="mt-24 shadow"> -->
      <main>
        <slot />
      </main>
      <!-- </main> -->
      <!-- <TheFooter /> -->
    </div>
  </div>
</template>
<!-- 
<style>
  @import 'pikaday/css/pikaday.css';
  @import 'pikaday/css/theme.css';
</style> -->
