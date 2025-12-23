<script>
  import { Shield, Lock, Award, CheckCircle } from 'lucide-svelte';

  const badges = [
    { text: 'Government Approved', icon: Shield },
    { text: 'SSL Secured', icon: Lock },
    { text: 'ISO Certified', icon: Award },
    { text: 'DigiLocker Compatible', icon: CheckCircle }
  ];
</script>

<section class="py-10 border-t  bg-gray-50 border-gray-200">
  <div class="max-w-6xl mx-auto px-4">
    <div class="flex flex-wrap justify-center gap-10">

      {#each badges as badge}
        <div class="flex items-center gap-4">
          
          <div class="w-12 h-12 rounded-xl bg-blue-600 flex items-center justify-center">
            <svelte:component
              this={badge.icon}
              class="w-6 h-6 text-white"
            />
          </div>

          <span class="text-lg font-medium text-gray-900">
            {badge.text}
          </span>

        </div>
      {/each}

    </div>
  </div>
</section>
