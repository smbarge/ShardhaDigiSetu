<script>
  export let title;
  export let description;
</script>

<div
  class="bg-white border border-blue-100 rounded-2xl p-6
         shadow-[0_0_0_1px_rgba(59,130,246,0.05)]"
>
  <div class="flex items-start gap-4">
    
    <div
      class="w-12 h-12 rounded-full bg-blue-50 flex items-center justify-center shrink-0"
    >
      <slot name="icon" />
    </div>

    <div>
      <h3 class="font-semibold text-gray-900 mb-1">
        {title}
      </h3>
      <p class="text-gray-600 text-sm leading-relaxed">
        {description}
      </p>
    </div>

  </div>
</div>
