<script>
  import {
    BookOpen,
    FileText,
    User,
    CheckCircle,
    Accessibility,
    Flag,
    Trophy
  } from 'lucide-svelte';

  const documents = [
    {
      title: 'Migration Certificate',
      description: 'Required when changing educational boards or universities',
      icon: FileText
    },
    {
      title: '12th Marksheet',
      description: 'Essential for college admissions and competitive exams',
      icon: User
    },
    {
      title: 'Caste Validity Certificate',
      description: 'Verification of caste certificate for higher education reservations',
      icon: CheckCircle
    },
    {
      title: 'Disability Certificate (UDID)',
      description: 'For PWD quota benefits in admissions and examinations',
      icon: Accessibility
    },
    {
      title: 'Nationality Certificate',
      description: 'Required for certain professional courses and government jobs',
      icon: Flag
    },
    {
      title: 'Sports / NCC / NSS Certificates',
      description: 'For sports quota and extracurricular activity credits',
      icon: Trophy
    }
  ];
</script>

<section class="pt-8 pb-16 px-4 bg-gray-50">

  <div class="max-w-6xl mx-auto">

    <div class="bg-white rounded-2xl border border-gray-200 p-10">

    
      <div class="flex items-start gap-4 mb-10">
        <div class="bg-blue-600 p-4 rounded-xl">
          <BookOpen class="w-7 h-7 text-white" />
        </div>
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-2">
            After 12th Required Documents & Higher Education Options
          </h2>
          <p class="text-gray-600">
            Critical documents for college admissions, professional courses, competitive exams, and career opportunities
          </p>
        </div>
      </div>

      
      <div class="grid md:grid-cols-2 gap-y-10 gap-x-16">
        {#each documents as doc}
          <div class="flex items-start gap-4">
            <svelte:component
              this={doc.icon}
              class="w-6 h-6 text-blue-600 mt-1"
            />
            <div>
              <h3 class="font-semibold text-gray-900">
                {doc.title}
              </h3>
              <p class="text-gray-600 text-sm mt-1">
                {doc.description}
              </p>
            </div>
          </div>
        {/each}
      </div>

    </div>
  </div>
</section>
