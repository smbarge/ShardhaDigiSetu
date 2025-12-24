<script>
  import { Shield, User, FileText, Award } from 'lucide-svelte';
  import FeatureCard from './FeatureCard.svelte';
</script>

    <section class="bg-gray-50 py-12 md:py-16 lg:py-24 px-4">
    <div class="max-w-7xl mx-auto px-4 md:px-6 lg:px-8">
      <div class="inline-flex items-center gap-2 mb-6 justify-center lg:justify-start">
        <Shield class="w-5 h-5 text-blue-600" />
        <span class="text-blue-600 font-medium">
            Government Approved Platform
        </span>
        </div>

    
        <div class="grid lg:grid-cols-2 gap-8 lg:gap-12 items-center">
        <div class="text-center lg:text-left">

          <h1 class ="text-3xl md:text-4xl lg:text-5xl font-serif font-bold text-foreground mb-4 md:mb-6">
          A Trusted Digital Platform for Student Certificates
        </h1>
        <p class="text-base md:text-lg text-gray-600 mb-8 md:mb-10">
          A single verified system connecting students, schools, and authorities for certificates and education services across India.
        </p>
        
          <div class="flex flex-col sm:flex-row items-center lg:items-start justify-center lg:justify-start gap-4 md:gap-6 mb-8 md:mb-10">
          <button class="bg-blue-600 text-white px-5 py-3 rounded-lg font-medium hover:bg-blue-700 flex items-center gap-2">
            Get Started
            <span>→</span>
          </button>
          <button class="border border-gray-300 text-gray-700 px-5 py-3 rounded-lg font-medium hover:bg-gray-50 flex items-center gap-2">
            <User class="w-5 h-5" />
            Student Login
          </button>
          <button class="border border-gray-300 text-gray-700 px-5 py-3 rounded-lg font-medium hover:bg-gray-50 flex items-center gap-2">
            <FileText class="w-5 h-5" />
            School Login
          </button>
        </div>
        
<div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 md:gap-6 lg:gap-8 text-sm mt-8 md:mt-10">
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
      
        <div class="space-y-4 mt-8 lg:mt-0">

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