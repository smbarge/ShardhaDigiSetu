<script>
  import {
    GraduationCap,
    FileText,
    User,
    Home,
    IndianRupee,
    Users,
    ShieldCheck
  } from 'lucide-svelte';

  const documents = [
    {
      title: 'School Leaving Certificate',
      description: 'Required for admission to higher secondary schools and colleges',
      icon: FileText
    },
    {
      title: '10th Marksheet',
      description: 'Academic performance record for further education applications',
      icon: User
    },
    {
      title: 'Domicile Certificate',
      description: 'Proof of residence for state quota admissions and scholarships',
      icon: Home
    },
    {
      title: 'Income Certificate',
      description: 'Required for fee concessions and scholarship eligibility',
      icon: IndianRupee
    },
    {
      title: 'Caste Certificate',
      description: 'For reservation benefits in admissions and fee waivers',
      icon: Users
    },
    {
      title: 'Bonafide Certificate',
      description: 'Proof of student status for various applications',
      icon: ShieldCheck
    }
  ];
</script>

<section class="pt-16 pb-8 px-4 bg-gray-50">
  <div class="max-w-6xl mx-auto">

    <div class="bg-white rounded-2xl border border-gray-200 p-10">

      <div class="flex items-start gap-4 mb-10">
        <div class="bg-blue-600 p-4 rounded-xl">
          <GraduationCap class="w-7 h-7 text-white" />
        </div>
        <div>
          <h2 class="text-3xl font-bold text-gray-900 mb-2">
            After 10th Required Documents & Next Education Options
          </h2>
          <p class="text-gray-600">
            Essential certificates needed for higher secondary admissions, ITI, Diploma, and skill development programs
          </p>
        </div>
      </div>

      <div class="grid md:grid-cols-2 gap-y-4 gap-x-4">
        {#each documents as doc}
            <div
              class="flex items-start gap-4 p-4 rounded-xl cursor-pointer transition
                    hover:bg-blue-50"
            >
            <svelte:component
              this={doc.icon}
              class="w-6 h-6 text-blue-600 mt-1 group-hover:text-blue-700"
            />
            <div>
            <h3 class="font-semibold text-gray-900 group-hover:text-blue-700">
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
