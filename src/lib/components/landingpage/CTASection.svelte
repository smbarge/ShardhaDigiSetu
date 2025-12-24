<!-- src/lib/components/CTASection.svelte -->
<script>
  import { User, FileText } from 'lucide-svelte';
</script>

<section class="bg-gradient-to-r from-blue-600 via-blue-400 to-blue-200 py-16 px-4">
  <div class="max-w-4xl mx-auto text-center text-white">
    <h2 class="text-4xl font-bold mb-4">Ready to Get Started?</h2>
    <p class="text-xl mb-8 text-blue-100">
      Join thousands of students and schools already using Shardha DigiSetu for seamless document management.
    </p>
    
    <div class="flex flex-wrap justify-center gap-4 mb-6">
      <button class="bg-gray-800 text-white px-8 py-3 rounded-lg font-medium hover:bg-gray-900 flex items-center gap-2">
        <User class="w-5 h-5" />
        Access Student Portal
      </button>
      <button class="bg-white text-blue-600 px-8 py-3 rounded-lg font-medium hover:bg-gray-50 flex items-center gap-2">
        <FileText class="w-5 h-5" />
        Access School Portal
      </button>
    </div>
    
    <p class="text-blue-100">
      Need help? Contact support: <span class="font-semibold">1800-XXX-XXXX</span>
    </p>
  </div>
</section>