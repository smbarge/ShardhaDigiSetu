<!-- src/routes/school-login/+page.svelte -->
<script>
  import { Lock, FileText, Building2, Shield, Users, Eye, ChevronRight,Clock,Download } from 'lucide-svelte';
  
  let showPassword = false;
  let schoolId = '';
  let password = '';
  let rememberMe = false;
  
  function handleLogin() {
    console.log('School login attempt:', { schoolId, password, rememberMe });
  }
  
  function togglePassword() {
    showPassword = !showPassword;
  }
</script>

<svelte:head>
  <title>School Login - Shardha DigiSetu</title>
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
      
      <a href="/student-login" class="flex items-center gap-2 px-4 py-2 border border-gray-300 rounded-lg hover:bg-gray-50 text-gray-700 font-medium">
        <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/>
          <circle cx="12" cy="7" r="4"/>
        </svg>
        Student Login
      </a>
    </div>
  </header>

  <!-- Breadcrumb -->
  <div class="bg-white border-b border-gray-200">
    <div class="max-w-7xl mx-auto px-4 py-3 flex items-center gap-2 text-sm">
      <a href="/" class="text-gray-600 hover:text-blue-600">Home</a>
      <ChevronRight class="w-4 h-4 text-gray-400" />
      <span class="text-gray-900 font-medium">School Login</span>
    </div>
  </div>

  <!-- Main Content -->
  <main class="flex-1">
    <div class="max-w-7xl mx-auto px-4 py-12">
      <!-- School Portal Badge -->
      <div class="flex items-center gap-2 text-blue-600 mb-6">
        <Building2 class="w-5 h-5" />
        <span class="font-medium">School Portal</span>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 items-start">
        <!-- Left Column - Login Form -->
        <div class="bg-white rounded-2xl shadow-sm border border-gray-200 p-8">
          <h1 class="text-3xl font-bold text-gray-900 mb-2">School Login</h1>
          <p class="text-gray-600 mb-8">Access your school administration dashboard</p>

          <form on:submit|preventDefault={handleLogin}>
            <!-- School ID Field -->
            <div class="mb-6">
              <label for="schoolId" class="block text-sm font-medium text-gray-900 mb-2">
                School ID <span class="text-red-500">*</span>
              </label>
              <input
                type="text"
                id="schoolId"
                bind:value={schoolId}
                placeholder="Enter your School ID"
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
            >
              Login to Dashboard
              <svg class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M15 3h6v6M9 21H3v-6M21 3l-7 7M3 21l7-7"/>
              </svg>
            </button>
          </form>

          <!-- Register Link -->
          <div class="mt-6 text-center">
            <p class="text-gray-600 mb-4">New school?</p>
            <a href="/school-register" class="inline-flex items-center gap-2 text-blue-600 hover:text-blue-700 font-medium">
              <Building2 class="w-5 h-5" />
              Register Your School
            </a>
          </div>

          <!-- Security Badges -->
          <div class="mt-8 pt-6 border-t border-gray-200">
            <div class="flex justify-center gap-6 mb-3">
              <Shield class="w-8 h-8 text-green-500" />
              <Lock class="w-8 h-8 text-blue-500" />
              <svg class="w-8 h-8 text-purple-500" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <circle cx="12" cy="12" r="10"/>
                <path d="M9 12l2 2 4-4"/>
              </svg>
            </div>
            <p class="text-center text-sm text-gray-600 mb-1">Secured by Government of India</p>
            <p class="text-center text-xs text-gray-500">ISO 27001 Certified | GDPR Compliant</p>
          </div>
        </div>

        <!-- Right Column - School Benefits -->
        <div>
          <div class="mb-8">
            <div class="flex items-start gap-4 mb-6">
              <div class="bg-blue-600 p-3 rounded-xl">
                <Building2 class="w-6 h-6 text-white" />
              </div>
              <div>
                <h2 class="text-2xl font-bold text-gray-900 mb-2">Welcome to Shardha DigiSetu</h2>
                <p class="text-gray-600">Streamline your institution's document management</p>
              </div>
            </div>

            <div class="space-y-6">
                <!-- Benefit 1 - Secure Document Storage -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-green-50 rounded-lg flex items-center justify-center">
                     <Users class="w-6 h-6 text-blue-600" />
                        <path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/>
                   
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Student Management</h3>
                    <p class="text-sm text-gray-600">Manage student records and certificates efficiently</p>
                </div>
                </div>

                <!-- Benefit 2 -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-blue-50 rounded-lg flex items-center justify-center">
                     <FileText class="w-6 h-6 text-blue-600" />
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Digital Certificates</h3>
                    <p class="text-sm text-gray-600">Issue and verify certificates digitally</p>
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
                    <h3 class="font-semibold text-gray-900 mb-1">Secure & Compliant</h3>
                    <p class="text-sm text-gray-600">Government-approved secure platform</p>
                </div>
                </div>
                 <!-- Benefit 4 - Educational Pathways -->
                <div class="flex gap-3">
                <div class="flex-shrink-0">
                    <div class="w-10 h-10 bg-purple-50 rounded-lg flex items-center justify-center">
                    <svg class="w-6 h-6 text-blue-600" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                      <polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/>
                    </svg>
                    </div>
                </div>
                <div>
                    <h3 class="font-semibold text-gray-900 mb-1">Real-time Analytics</h3>
                    <p class="text-sm text-gray-600">Track and monitor certificate requests</p>
                </div>
                </div>
            </div>
          </div>

          <!-- Image -->
          <div class="rounded-2xl overflow-hidden shadow-lg">
            <img 
              src="https://images.unsplash.com/photo-1509062522246-3755977927d7?w=600&h=400&fit=crop" 
              alt="School building"
              class="w-full h-65 object-cover"
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