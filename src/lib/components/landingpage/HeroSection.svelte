<script>
  import { Shield, User, FileText, Award } from 'lucide-svelte';
  import FeatureCard from './FeatureCard.svelte';
</script>

<section class="bg-gray-50 py-16 px-4">
  <div class="max-w-6xl mx-auto">
    <div class="flex items-center gap-2 mb-6">
        <Shield class="w-5 h-5 text-blue-600" />
        <span class="text-blue-600 font-medium">
            Government Approved Platform
        </span>
        </div>

    
    <div class="grid md:grid-cols-2 gap-12 items-start">
      <div>
        <h1 class="text-5xl font-bold text-gray-900 mb-6 leading-tight">
          A Trusted Digital Platform for Student Certificates
        </h1>
        <p class="text-lg text-gray-600 mb-8">
          A single verified system connecting students, schools, and authorities for certificates and education services across India.
        </p>
        
        <div class="flex flex-wrap gap-4 mb-8">
          <button class="bg-blue-600 text-white px-6 py-3 rounded-lg font-medium hover:bg-blue-700 flex items-center gap-2">
            Get Started
            <span>→</span>
          </button>
          <button class="border border-gray-300 text-gray-700 px-6 py-3 rounded-lg font-medium hover:bg-gray-50 flex items-center gap-2">
            <User class="w-5 h-5" />
            Student Login
          </button>
          <button class="border border-gray-300 text-gray-700 px-6 py-3 rounded-lg font-medium hover:bg-gray-50 flex items-center gap-2">
            <FileText class="w-5 h-5" />
            School Login
          </button>
        </div>
        
        <div class="flex flex-wrap gap-6 text-sm">
          <div class="flex items-center gap-2 text-green-600">
            <Shield class="w-5 h-5" />
            <span>100% Secure</span>
          </div>
          <div class="flex items-center gap-2 text-blue-600">
            <Shield class="w-5 h-5" />
            <span>Government Verified</span>
          </div>
          <div class="flex items-center gap-2 text-purple-600">
            <User class="w-5 h-5" />
            <span>Free for Students</span>
          </div>
        </div>
      </div>
      
      <div class="space-y-4">
        
        <FeatureCard
          title="Unified Certificate Workflow"
          description="School, revenue, and special certificates managed through one transparent process."
        >
          <FileText slot="icon" class="w-6 h-6 text-blue-600" />
        </FeatureCard>
        <FeatureCard
          title="Government Documents"
          description="Apply for official certificates online"
        >
          <FileText slot="icon" class="w-6 h-6 text-blue-600" />
        </FeatureCard>
        <FeatureCard
          title="Educational Pathways"
          description="Personalized career guidance and planning"
        >
          <Award slot="icon" class="w-6 h-6 text-blue-600" />
        </FeatureCard>
      </div>
    </div>
  </div>
</section>