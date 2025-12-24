<script>
  import { CheckCircle, Users, Zap, Eye } from 'lucide-svelte';

  const benefits = [
    {
      title: 'One-Time Verification',
      description:
        'Submit documents once and use them across multiple applications without repeated verification processes.',
      color: 'bg-green-500',
      icon: CheckCircle
    },
    {
      title: 'Reduced Authority Workload',
      description:
        'Government offices process fewer duplicate requests, enabling faster service delivery for all citizens.',
      color: 'bg-blue-600',
      icon: Users
    },
    {
      title: 'Faster Approvals',
      description:
        'Pre-verified documents mean instant access for education admissions and scholarship applications.',
      color: 'bg-orange-500',
      icon: Zap
    },
    {
      title: 'Transparent Tracking',
      description:
        'Real-time status updates for all certificate applications with complete visibility into processing stages.',
      color: 'bg-gray-600',
      icon: Eye
    }
  ];
</script>

<section class="bg-gray-50 py-16 px-4">
  <div class="max-w-6xl mx-auto">

    <div class="text-center mb-12">
      <h2 class="text-4xl font-bold text-gray-900 mb-4">
        Why Choose Shardha DigiSetu?
      </h2>
      <p class="text-gray-600 text-lg max-w-2xl mx-auto">
        A unified platform designed to simplify document management for students,
        schools, and government authorities.
      </p>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
      {#each benefits as benefit}
        <div
          class="bg-white border border-gray-200 rounded-xl p-6
                 shadow-md hover:shadow-lg transition-shadow text-left"
        >
          
          <div
            class="{benefit.color} w-12 h-12 rounded-xl
                   flex items-center justify-center mb-4"
          >
            <svelte:component
              this={benefit.icon}
              class="w-6 h-6 text-white"
            />
          </div>

          <h3 class="text-lg font-semibold text-gray-900 mb-2">
            {benefit.title}
          </h3>

          <p class="text-sm text-gray-600">
            {benefit.description}
          </p>
        </div>
      {/each}
    </div>

  </div>
</section>