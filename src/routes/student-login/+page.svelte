<script>
  import { Lock, FileText, TrendingUp, Shield, Clock, Download, Eye, ChevronRight, UserPlus, Globe } from 'lucide-svelte';
    import { goto } from '$app/navigation';
  let showPassword = false;
  let email = '';
  let password = '';
  let rememberMe = false;
  let selectedLanguage = 'English';
  
  function handleLogin() {
    console.log('Login attempt:', { email, password, rememberMe });
  }
  
  function togglePassword() {
    showPassword = !showPassword;
  }
</script>

<svelte:head>
  <title>Student Login - Shardha DigiSetu</title>
</svelte:head>

<div class="min-h-screen bg-gray-50 flex flex-col">
  <!-- Header -->
  <header class="bg-white border-b border-gray-200 sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-4 flex items-center justify-between">
      <a href="/" class="flex items-center gap-3">
        <div class="w-12 h-12 bg-blue-600 rounded-xl flex items-center justify-center">
          <Lock class="w-6 h-6 text-white" />
        </div>
        <h1 class="text-xl font-bold text-gray-900">Shardha DigiSetu</h1>
      </a>
      
      <a href="/school-login" class="flex items-center gap-2 px-4 py-2 border border-gray-300 rounded-lg hover:bg-gray-50 text-gray-700 font-medium">
        <FileText class="w-5 h-5" />
        School Login
      </a>
    </div>
  </header>

  <!-- Breadcrumb -->
  <div class="bg-white border-b border-gray-200">
    <div class="max-w-7xl mx-auto px-4 py-3 flex items-center gap-2 text-sm">
      <a href="/" class="text-gray-600 hover:text-blue-600">Home</a>
      <ChevronRight class="w-4 h-4 text-gray-400" />
      <span class="text-gray-900 font-medium">Student Login</span>
    </div>
  </div>

  <!-- Main Content -->
  <main class="flex-1">
    <div class="max-w-7xl mx-auto px-4 py-12">
      <!-- Student Portal Badge -->
      <div class="flex items-center gap-2 text-blue-600 mb-6">
        <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M12 14l9-5-9-5-9 5 9 5z"/>
          <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"/>
        </svg>
        <span class="font-medium">Student Portal</span>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 items-start">
        <!-- Left Column - Login Form -->
        <div class="bg-white rounded-2xl shadow-lg border border-gray-200 p-8">
          <h1 class="text-3xl font-bold text-gray-900 mb-2">Student Login</h1>
          <p class="text-gray-600 mb-8">Access your unified digital document locker securely</p>

          <form on:submit|preventDefault={handleLogin}>
            <!-- Student ID / Email Field -->
            <div class="mb-6">
              <label for="email" class="block text-sm font-medium text-gray-900 mb-2">
                Email or Phone Number <span class="text-red-500">*</span>
              </label>
              <input
                type="text"
                id="email"
                bind:value={email}
                placeholder="Enter your email or phone"
                class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none"
                required
              />
            </div>

            <!-- Password Field -->
            <div class="mb-4">
              <label for="password" class="block text-sm font-medium text-gray-900 mb-2">
                Password <span class="text-red-500">*</span>
              </label>
              <div class="relative">
                <input
                  type={showPassword ? 'text' : 'password'}
                  id="password"
                  bind:value={password}
                  placeholder="Enter your password"
                  class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-transparent outline-none pr-12"
                  required
                />
                <button
                  type="button"
                  on:click={togglePassword}
                  class="absolute right-3 top-1/2 -translate-y-1/2 text-gray-500 hover:text-gray-700"
                >
                  <Eye class="w-5 h-5" />
                </button>
              </div>
            </div>

            <!-- Remember Me & Forgot Password -->
            <div class="flex items-center justify-between mb-6">
              <label class="flex items-center gap-2 cursor-pointer">
                <input
                  type="checkbox"
                  bind:checked={rememberMe}
                  class="w-4 h-4 text-blue-600 border-gray-300 rounded focus:ring-blue-500"
                />
                <span class="text-sm text-gray-700">Remember me</span>
              </label>
              <a href="/forgot-password" class="text-sm text-blue-600 hover:text-blue-700 font-medium">
                Forgot Password?
              </a>
            </div>

            <!-- Login Button -->
            <button
              type="submit"
              class="w-full bg-blue-600 text-white py-3 rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center justify-center gap-2"
              on:click={() => goto('/student-dashboard')}
            >
              Login to Dashboard
              <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M15 3h6v6M9 21H3v-6M21 3l-7 7M3 21l7-7"/>
              </svg>
            </button>
          </form>

          <!-- Register Link -->
          <div class="mt-6 text-center">
            <p class="text-gray-600 mb-4">New to Shardha DigiSetu?</p>
            <a href="/register" class="inline-flex items-center gap-2 text-blue-600 hover:text-blue-700 font-medium">
              <UserPlus class="w-5 h-5" />
              Create New Account
            </a>
          </div>

          <!-- Security Badges -->
          <div class="mt-8 pt-6 border-t border-gray-200">
            <div class="flex justify-center gap-6 mb-3">
              <div class="flex flex-col items-center">
                <Shield class="w-8 h-8 text-green-500 mb-1" />
              </div>
              <div class="flex flex-col items-center">
                <Lock class="w-8 h-8 text-blue-500 mb-1" />
              </div>
              <div class="flex flex-col items-center">
                <svg class="w-8 h-8 text-purple-500 mb-1" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                  <circle cx="12" cy="12" r="10"/>
                  <path d="M9 12l2 2 4-4"/>
                </svg>
              </div>
            </div>
            <p class="text-center text-sm text-gray-600 mb-1">Secured by Government of India</p>
            <p class="text-center text-xs text-gray-500">ISO 27001 Certified | GDPR Compliant</p>
          </div>
        </div>

            <!-- Right Column - Benefits (Before the form) -->
            <div class="mb-8">
             <div class="flex items-start gap-4 mb-6">
              <div class="bg-blue-600 p-3 rounded-xl">
                 <svg class="w-6 h-6 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                    <path d="M12 14l9-5-9-5-9 5 9 5z"/>
                    <path d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"/>
                    </svg>
              </div>
              <div>
                <h2 class="text-2xl font-bold text-gray-900 mb-2">Welcome to Shardha DigiSetu</h2>
                <p class="text-gray-600">Secure Digital Document Management for Students</p>
              </div>
            </div>
            <!-- <h2 class="text-3xl font-bold text-gray-900 mb-3">Welcome to Shardha DigiSetu</h2>
            <p class="text-gray-600 mb-8">Secure Digital Document Management for Students</p> -->

            <!-- Benefits List -->
            <div class="space-y-6">
                <!-- Benefit 1 - Secure Document Storage -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-green-50 rounded-lg flex items-center justify-center">
                     <FileText class="w-6 h-6 text-blue-600" />
                        <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
                   
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1"> Unified Digital Locker</h3>
                    <p class="text-sm text-gray-600">Access all your education certificates in one secure place</p>
                </div>
                </div>

                <!-- Benefit 2 -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-blue-50 rounded-lg flex items-center justify-center">
                     <Clock class="w-6 h-6 text-blue-600" />
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Instant Accesst</h3>
                    <p class="text-sm text-gray-600"> View and download certificates anytime, anywhere</p>
                </div>
                </div>

                <!-- Benefit 3 - Educational Pathways -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-purple-50 rounded-lg flex items-center justify-center">
                    <Shield class="w-6 h-6 text-blue-600" />
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Secure & Verified</h3>
                    <p class="text-sm text-gray-600">Government-verified documents with blockchain security</p>
                </div>
                </div>
                 <!-- Benefit 4 - Educational Pathways -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-purple-50 rounded-lg flex items-center justify-center">
                    <Download class="w-6 h-6 text-blue-600" />
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Easy Downloads</h3>
                    <p class="text-sm text-gray-600">Download official certificates in PDF format instantly</p>
                </div>
                </div>
            </div>

        <!-- Image -->
        <div class="mt-8 rounded-2xl overflow-hidden shadow-lg">
            <img
            src="https://images.unsplash.com/photo-1522202176988-66273c2fd55f?w=600&h=400&fit=crop"
            alt="Student studying"
            class="w-full h-50 object-cover"
            />
        </div>
            </div>

        </div>
        
        </div>
    </main>

  <!-- Footer -->
  <footer class="bg-white border-t border-gray-200 mt-auto">
    <div class="max-w-7xl mx-auto px-4 py-6">
      <div class="flex flex-wrap justify-between items-center text-sm text-gray-600">
        <p>© 2025 Shardha DigiSetu. All rights reserved. | Government of India Initiative</p>
        <div class="flex gap-4">
          <a href="/help" class="hover:text-blue-600">Help Center</a>
          <span class="text-gray-400">•</span>
          <a href="/contact" class="hover:text-blue-600">Contact Us</a>
        </div>
      </div>
    </div>
  </footer>
</div>