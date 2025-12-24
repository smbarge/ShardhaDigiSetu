<script>
  import { Shield, Lock, Award, CheckCircle } from 'lucide-svelte';

  const badges = [
    { text: 'Government Approved', icon: Shield },
    { text: 'SSL Secured', icon: Lock },
    { text: 'ISO Certified', icon: Award },
    { text: 'DigiLocker Compatible', icon: CheckCircle }
  ];
</script>

<section class="py-8 md:py-10 lg:py-12 bg-gray-50 border-y border-gray-200">
  <div class="max-w-6xl mx-auto px-4 md:px-6 lg:px-8">
    
    <div class="flex flex-wrap items-center justify-center gap-6 md:gap-8 lg:gap-12">
      
      {#each badges as badge}
        <div class="flex items-center gap-2 md:gap-3">
          
          <!-- Icon Box -->
          <div class="w-8 h-8 md:w-10 md:h-10 bg-blue-600 rounded-md flex items-center justify-center">
            <svelte:component
              this={badge.icon}
              class="w-4 h-4 md:w-5 md:h-5 text-white"
            />
          </div>

          <!-- Text -->
          <span class="text-sm md:text-base font-medium text-gray-900 whitespace-nowrap">
            {badge.text}
          </span>

        </div>
      {/each}

    </div>
  </div>
</section>
