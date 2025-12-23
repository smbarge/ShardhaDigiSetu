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
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-900 mb-4">
      Why Choose EduLocker?
    </h2>
    <p class="text-gray-600 text-lg mb-12">
      A unified platform designed to simplify document management for students,
      schools, and government authorities.
    </p>

    <div class="grid md:grid-cols-4 gap-6">
      {#each benefits as benefit}
        <div
          class="bg-white border border-gray-200 rounded-xl p-6
                 hover:shadow-lg transition-shadow"
        >
          <div
            class="{benefit.color} w-12 h-12 rounded-xl
                   flex items-center justify-center mx-auto mb-4"
          >
            <svelte:component
              this={benefit.icon}
              class="w-6 h-6 text-white"
            />
          </div>

          <h3 class="font-bold text-gray-900 mb-3">
            {benefit.title}
          </h3>
          <p class="text-gray-600 text-sm">
            {benefit.description}
          </p>
        </div>
      {/each}
    </div>
  </div>
</section>
