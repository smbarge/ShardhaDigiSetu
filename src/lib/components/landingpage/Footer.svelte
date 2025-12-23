<script>
  import { Lock } from 'lucide-svelte';
</script>

<footer class=" bg-white border-t border-gray-200 py-12 px-4">
  <div class="max-w-6xl mx-auto">
    <div class="grid md:grid-cols-4 gap-8 mb-8">
      <div>
        <div class="flex items-center gap-3 mb-4">
          <div class="w-12 h-12 rounded-xl bg-blue-600 flex items-center justify-center">
            <Lock class="w-6 h-6 text-white" />
          </div>
          <h3 class="font-bold text-gray-900">Shardha DigiSetu</h3>
        </div>
        <p class="text-gray-600 text-sm mb-4">
          Unified digital document management platform for Indian students and educational institutions.
        </p>
        <div class="flex gap-3">
          <div class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center hover:bg-blue-600 hover:text-white cursor-pointer transition-colors">
            <span class="font-semibold">f</span>
          </div>
          <div class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center hover:bg-blue-600 hover:text-white cursor-pointer transition-colors">
            <span class="font-semibold">t</span>
          </div>
          <div class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center hover:bg-blue-600 hover:text-white cursor-pointer transition-colors">
            <span class="font-semibold">in</span>
          </div>
        </div>
      </div>
      
      <div>
        <h4 class="font-semibold text-gray-900 mb-4">Quick Links</h4>
        <ul class="space-y-2 text-gray-600 text-sm">
          <li><a href="#" class="hover:text-blue-600">Student Login</a></li>
          <li><a href="#" class="hover:text-blue-600">School Login</a></li>
          <li><a href="#" class="hover:text-blue-600">Education Pathways</a></li>
        </ul>
      </div>
      
      <div>
        <h4 class="font-semibold text-gray-900 mb-4">Resources</h4>
        <ul class="space-y-2 text-gray-600 text-sm">
          <li><a href="#" class="hover:text-blue-600">Help Center</a></li>
          <li><a href="#" class="hover:text-blue-600">Privacy Policy</a></li>
          <li><a href="#" class="hover:text-blue-600">Terms of Service</a></li>
        </ul>
      </div>
      
      <div>
        <h4 class="font-semibold text-gray-900 mb-4">Contact</h4>
        <ul class="space-y-2 text-gray-600 text-sm">
          <li>Support: 1800-XXX-XXXX</li>
          <li>Email: support@edulocker.gov.in</li>
          <li>Office Hours: 9 AM - 6 PM</li>
        </ul>
      </div>
    </div>
    
    <div class="border-t border-gray-200 pt-6 flex flex-wrap justify-between items-center text-sm text-gray-600">
      <p>© 2025 EduLocker. All rights reserved. Government of India Initiative.</p>
      <p>Powered by <span class="text-blue-600 font-medium">Digital India</span></p>
    </div>
  </div>
</footer>