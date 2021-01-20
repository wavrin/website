<template>
  <!-- This example requires Tailwind CSS v2.0+ -->
  <div class="h-screen flex overflow-hidden bg-white">
    <!-- Off-canvas menu for mobile, show/hide based on off-canvas menu state. -->
    <!-- Static sidebar for desktop -->
    <div class="hidden md:flex md:flex-shrink-0">
      <div class="flex flex-col w-64">
        <!-- Sidebar component, swap this element with another sidebar if you like -->
        <div class="flex flex-col h-0 flex-1 border-r border-gray-200 bg-white">
          <div class="flex-shrink-0 flex border-t border-gray-200 p-4">
            <div class="flex-shrink-0 w-full group block">
              <div class="flex items-center">
                <NuxtLink to="/">
                  <div>
                    <img class="inline-block h-9 w-9 rounded-full" src="~/assets/wavrin.jpeg" alt="">
                  </div>
                </NuxtLink>
                <div class="ml-3">
                  <NuxtLink to="/">
                    <p class="text-sm font-medium text-gray-700 group-hover:text-gray-900">
                      Christopher Wavrin
                    </p>
                  </NuxtLink>
                  <div class="flex items-center">
                    <div class="p-2">
                      <a href="https://twitter.com/wavrin">
                        <font-awesome-icon :icon="['fab', 'twitter']" />
                      </a>
                    </div>
                    <div class="p-2">
                      <a href="https://www.linkedin.com/in/wavrin/">
                        <font-awesome-icon :icon="['fab', 'linkedin']" />
                      </a>
                    </div>
                    <div class="p-2">
                      <a href="https://github.com/wavrin">
                        <font-awesome-icon :icon="['fab', 'github']" />
                      </a>
                    </div>
                  </div>
                </div>
              </div>
              <div class="py-4 text-gray-700">
                <p>Hello. I'm a software development consultant in Minneapolis and this is my website.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="flex flex-col w-0 flex-1 overflow-hidden">
      <main class="flex-1 relative z-0 overflow-y-auto focus:outline-none" tabindex="0">
        <div class="py-6">
          <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
            <!-- Replace with your content -->
            <div class="md:hidden flex items-center">
              <NuxtLink to="/">
                <div>
                  <img class="inline-block h-10 w-10 rounded-full" src="~/assets/wavrin.jpeg" alt="">
                </div>
              </NuxtLink>
              <div class="ml-3">
                <NuxtLink to="/">
                  <p class="text-sm font-medium text-gray-700 group-hover:text-gray-900">
                    Christopher Wavrin
                  </p>
                </NuxtLink>
                <div class="flex items-center">
                  <div class="p-2">
                    <a href="https://twitter.com/wavrin">
                      <font-awesome-icon :icon="['fab', 'twitter']" />
                    </a>
                  </div>
                  <div class="p-2">
                    <a href="https://www.linkedin.com/in/wavrin/">
                      <font-awesome-icon :icon="['fab', 'linkedin']" />
                    </a>
                  </div>
                  <div class="p-2">
                    <a href="https://github.com/wavrin">
                      <font-awesome-icon :icon="['fab', 'github']" />
                    </a>
                  </div>
                </div>
              </div>
            </div>
            <div class="md:hidden p-2 text-gray-700">
              <p>Hello. I'm a software development consultant in Minneapolis and this is my website.</p>
            </div>
            <Nuxt />
            <!-- /End replace -->
          </div>
        </div>
      </main>
      <footer class="bg-white">
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 md:flex md:items-center md:justify-between lg:px-8">
          <div class="mt-8 md:mt-0 md:order-1">
            <p class="text-center text-base text-gray-400">
              &copy; 2021 Christopher Wavrin
            </p>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<style>
html {
  font-family:
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
