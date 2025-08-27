<template>
  <UContainer>
    <UPage>
      <UPageHeader title="Nuxt 4 Boilerplate" description="A modern starter template with Nuxt UI, Pinia, and server-side APIs" />

      <UPageBody>
        <div class="space-y-8">
          <UCard>
            <template #header>
              <h2 class="text-xl font-semibold">
                Welcome to your Nuxt 4 Boilerplate
              </h2>
            </template>

            <p class="text-gray-600 dark:text-gray-400 mb-6">
              This boilerplate includes everything you need to build modern web applications with Nuxt 4,
              featuring beautiful UI components, state management, and server-side functionality.
            </p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <UCard class="hover:shadow-lg transition-shadow">
                <div class="flex items-start gap-4">
                  <div class="p-2 rounded-lg bg-primary-100 dark:bg-primary-900">
                    <UIcon name="i-lucide-bar-chart-3" class="w-6 h-6 text-primary" />
                  </div>
                  <div class="flex-1">
                    <h3 class="font-semibold mb-2">
                      Counter Store Demo
                    </h3>
                    <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                      Explore Pinia state management with a simple counter example.
                      Demonstrates reactive state updates and component composition.
                    </p>
                    <UButton
                      to="/counter"
                      variant="outline"
                      size="sm"
                      trailing-icon="i-lucide-arrow-right"
                    >
                      View Counter
                    </UButton>
                  </div>
                </div>
              </UCard>

              <UCard class="hover:shadow-lg transition-shadow">
                <div class="flex items-start gap-4">
                  <div class="p-2 rounded-lg bg-success-100 dark:bg-success-900">
                    <UIcon name="i-lucide-activity" class="w-6 h-6 text-success" />
                  </div>
                  <div class="flex-1">
                    <h3 class="font-semibold mb-2">
                      Server API Integration
                    </h3>
                    <p class="text-sm text-gray-600 dark:text-gray-400 mb-3">
                      See how server-side APIs work with real-time pageview tracking.
                      Demonstrates Nitro server functions and data fetching.
                    </p>
                    <UButton
                      to="/pageview"
                      variant="outline"
                      size="sm"
                      trailing-icon="i-lucide-arrow-right"
                    >
                      View API Demo
                    </UButton>
                  </div>
                </div>
              </UCard>
            </div>
          </UCard>

          <UCard>
            <template #header>
              <h2 class="text-xl font-semibold">
                Features Included
              </h2>
            </template>

            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-zap" class="w-5 h-5 text-yellow-500" />
                <span class="text-sm">Nuxt 4 with Vite</span>
              </div>
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-palette" class="w-5 h-5 text-purple-500" />
                <span class="text-sm">Nuxt UI Components</span>
              </div>
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-database" class="w-5 h-5 text-blue-500" />
                <span class="text-sm">Pinia State Management</span>
              </div>
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-server" class="w-5 h-5 text-green-500" />
                <span class="text-sm">Nitro Server Functions</span>
              </div>
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-shield-check" class="w-5 h-5 text-red-500" />
                <span class="text-sm">TypeScript First</span>
              </div>
              <div class="flex items-center gap-3">
                <UIcon name="i-lucide-smartphone" class="w-5 h-5 text-indigo-500" />
                <span class="text-sm">PWA Ready</span>
              </div>
            </div>
          </UCard>
        </div>
      </UPageBody>
    </UPage>
  </UContainer>
</template>
