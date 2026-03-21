<template>
  <div class="min-h-screen text-white">
    <!-- Navbar -->
    <nav class="fixed top-0 left-0 right-0 z-50 px-4 md:px-8 py-3">
      <div
        class="max-w-7xl mx-auto flex items-center justify-between glass px-6 py-3"
      >
        <!-- Logo -->
        <button
          @click="redirectToHome"
          class="text-[#ffdb70] font-semibold text-lg hover:text-amber-200 transition"
        >
          Ananda Anugrah Handyanto
        </button>

        <!-- Right -->
        <div class="flex items-right gap-4">
          <a href="https://github.com/AnandaAnugrahHandyanto" target="_blank">
            <img
              class="w-9 rounded-full hover:scale-110 transition"
              src="https://seeklogo.com/images/G/github-logo-2E3852456C-seeklogo.com.png"
            />
          </a>
        </div>

        <!-- Menu -->
        <div class="hidden md:flex gap-8 text-sm text-white/70">
          <router-link to="/" class="nav-link">Home</router-link>
          <router-link to="/about" class="nav-link">About</router-link>
          <router-link to="/portfolio" class="nav-link">Portfolio</router-link>
          <router-link to="/certification" class="nav-link"
            >Certification</router-link
          >
        </div>
      </div>
    </nav>

    <!-- Content -->
    <main class="pt-24 px-4 md:px-0 max-w-7xl mx-auto">
      <router-view />
    </main>

    <!-- Mobile Nav -->
    <footer class="md:hidden fixed bottom-0 left-0 right-0 z-50 px-4 pb-3">
      <div class="glass flex justify-around py-3 text-xs">
        <router-link to="/" class="mobile-link">Home</router-link>
        <router-link to="/about" class="mobile-link">About</router-link>
        <router-link to="/portfolio" class="mobile-link">Portfolio</router-link>
        <router-link to="/certification" class="mobile-link"
          >Certification</router-link
        >
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  methods: {
    redirectToHome() {
      this.$router.push("/");
    },
  },
};
</script>

<style>
*,
*::before,
*::after {
  box-sizing: border-box;
}

/* Scrollbar */
::-webkit-scrollbar {
  width: 5px;
}
::-webkit-scrollbar-thumb {
  background: #ffdb70;
  border-radius: 10px;
}

/* Liquid glass */
.glass {
  background: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(8px);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;
}

/* Active route */
.router-link-exact-active {
  color: white;
}
.router-link-exact-active::after {
  content: "";
  display: block;
  height: 3px;
  margin-top: 4px;
  border-radius: 2px;
  background: #ffdb70;
}

/* Mobile link */
.mobile-link {
  color: rgba(255, 255, 255, 0.6);
  transition: 0.3s;
}
.mobile-link:hover {
  color: white;
}

/* Smooth Ui */
* {
  transition: all 0.25s ease;
}
</style>
