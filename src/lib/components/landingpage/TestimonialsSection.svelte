<script>
  const testimonials = [
    {
      rating: 5,
      text: 'Shardha DigiSetu made it so easy to apply for my migration certificate. Got it within 5 days!',
      name: 'Priya Sharma',
      location: 'Delhi',
      initials: 'PS',
      color: 'bg-purple-600'
    },
    {
      rating: 5,
      text: 'All my certificates in one place. The educational pathways feature helped me choose the right college.',
      name: 'Rahul Verma',
      location: 'Maharashtra',
      initials: 'RV',
      color: 'bg-blue-600'
    },
    {
      rating: 5,
      text: 'Secure, fast, and reliable. This is exactly what students need for document management.',
      name: 'Anjali Patel',
      location: 'Gujarat',
      initials: 'AP',
      color: 'bg-blue-500'
    }
  ];
</script>

<section class="bg-gray-50 pt-6 pb-16 px-4">
  <div class="max-w-6xl mx-auto text-center">
    <h2 class="text-4xl font-bold text-gray-900 mb-3">
      What Students Say
    </h2>
    <p class="text-gray-600 text-lg mb-12">
      Trusted by thousands of students across India
    </p>

    <div class="grid md:grid-cols-3 gap-6">
      {#each testimonials as t}
        <div class="bg-white border border-gray-200 rounded-lg p-6 text-left hover:shadow-lg transition-shadow">
          
          <div class="flex gap-1 mb-4">
            {#each Array(t.rating) as _}
              <span class="text-blue-500 text-xl">★</span>
            {/each}
          </div>

          <p class="text-gray-700 mb-6">{t.text}</p>

          <div class="flex items-center gap-3">
            <div class="{t.color} w-12 h-12 rounded-full flex items-center justify-center text-white font-bold">
              {t.initials}
            </div>
            <div>
              <p class="font-semibold text-gray-900">{t.name}</p>
              <p class="text-sm text-gray-600">{t.location}</p>
            </div>
          </div>

        </div>
      {/each}
    </div>
  </div>
</section>
