<template>
  <div>
    <!-- Static sidebar for desktop -->
    <div
      class="hidden lg:fixed lg:inset-y-0 lg:z-50 lg:flex lg:w-24 lg:flex-col"
    >
      <!-- Sidebar component, swap this element with another sidebar if you like -->
      <Sidebar />
    </div>

    <div class="lg:pl-24">
      <Header />
      <main>
        <slot />
      </main>
    </div>
  </div>
</template>
