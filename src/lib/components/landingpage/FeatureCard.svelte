<!-- src/lib/components/FeatureCard.svelte -->
<script>
  export let title;
  export let description;
</script>

<div class="bg-gray-50 border border-gray-200 rounded-lg p-6 hover:shadow-md transition-shadow">
  <div class="flex items-start gap-4">
    <div class="bg-white p-3 rounded-lg border border-gray-200">
      <slot name="icon" />
    </div>
    <div>
      <h3 class="font-semibold text-gray-900 mb-2">{title}</h3>
      <p class="text-gray-600 text-sm">{description}</p>
    </div>
  </div>
</div>