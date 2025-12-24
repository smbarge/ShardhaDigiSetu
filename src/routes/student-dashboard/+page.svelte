<script>
  import { GraduationCap, LayoutDashboard, Route, User, ChevronDown, TrendingUp, Clock, AlertTriangle, Plus, Compass, Search, FileText, Trophy, FolderOpen, Building, Calendar, Hash, MapPin, CheckCircle, Eye, Download } from 'lucide-svelte';

  let expandedSections = {
    academic: true,
    sports: false,
    government: false,
    other: false
  };

  function toggleSection(section) {
    expandedSections[section] = !expandedSections[section];
  }

  const academicCertificates = [
    {
      title: "10th Standard Marksheet",
      authority: "Maharashtra State Board of Secondary Education",
      issued: "15 May 2023",
      status: "Active",
      priority: true,
      icon: "📄"
    },
    {
      title: "12th Standard Marksheet",
      authority: "Maharashtra State Board of Higher Secondary...",
      issued: "20 May 2025",
      status: "Active",
      priority: true,
      icon: "📄"
    },
    {
      title: "School Bonafide Certificate",
      authority: "St. Xavier's High School, Mumbai",
      issued: "10 Jan 2025",
      validUntil: "10 Jan 2026",
      status: "Active",
      icon: "🎓"
    },
    {
      title: "School Leaving Certificate",
      authority: "St. Xavier's High School, Mumbai",
      issued: "01 Jun 2025",
      status: "Active",
      icon: "📋"
    },
    {
      title: "Migration Certificate",
      authority: "Maharashtra State Board",
      issued: "15 Jun 2025",
      status: "Active",
      icon: "🔄"
    },
    {
      title: "Transfer Certificate",
      authority: "Modern High School, Pune",
      issued: "15 Mar 2023",
      status: "Expired",
      icon: "➡️"
    }
  ];

  const sportsCertificates = [
    {
      title: "NCC Certificate",
      authority: "National Cadet Corps, Maharashtra Directorate",
      issued: "01 Dec 2024",
      validUntil: "01 Dec 2027",
      status: "Active",
      icon: "🛡️"
    },
    {
      title: "NSS Certificate",
      authority: "National Service Scheme, Mumbai University",
      issued: "20 Nov 2024",
      validUntil: "20 Nov 2027",
      status: "Active",
      icon: "💙"
    },
    {
      title: "State Level Sports Certificate",
      authority: "Maharashtra State Sports Authority",
      issued: "10 Sept 2024",
      status: "Active",
      icon: "🏆"
    }
  ];

  const governmentDocs = [
    {
      title: "Domicile Certificate",
      authority: "Tahsildar Office, Mumbai Suburban",
      issued: "05 Aug 2024",
      validUntil: "05 Aug 2027",
      appNo: "DOM/2024/12345",
      status: "Active",
      icon: "📍"
    },
    {
      title: "Income Certificate",
      authority: "Tahsildar Office, Mumbai Suburban",
      issued: "15 Jul 2024",
      validUntil: "15 Jul 2025",
      appNo: "INC/2024/67890",
      status: "Active",
      icon: "💰"
    },
    {
      title: "Caste Certificate",
      authority: "Tahsildar Office, Mumbai Suburban",
      issued: "20 Jun 2023",
      validUntil: "20 Jun 2026",
      appNo: "CST/2023/11223",
      status: "Active",
      icon: "👥"
    },
    {
      title: "Orphan Certificate",
      authority: "Social Welfare Department, Mumbai",
      issued: "20 Sept 2025",
      appNo: "ORP/2025/99001",
      status: "Pending",
      icon: "💙"
    },
    {
      title: "Caste Validity Certificate",
      authority: "Caste Scrutiny Committee, Maharashtra",
      issued: "10 Aug 2025",
      appNo: "CSV/2025/22334",
      status: "Pending",
      icon: "✓"
    },
    {
      title: "UDID Disability Certificate",
      authority: "Department of Empowerment of Persons with...",
      issued: "05 Jul 2024",
      validUntil: "05 Jul 2029",
      appNo: "UDID/2024/44556",
      status: "Active",
      icon: "♿"
    }
  ];

  const otherCertificates = [
    {
      title: "Character Certificate",
      authority: "St. Xavier's High School, Mumbai",
      issued: "01 Jun 2025",
      status: "Active",
      icon: "⭐"
    },
    {
      title: "Gap Certificate",
      authority: "Self Declaration",
      issued: "01 Jul 2025",
      status: "Active",
      icon: "📅"
    }
  ];
</script>

<div class="min-h-screen bg-gray-50">
  <!-- Header -->
  <header class="bg-white border-b border-gray-200 sticky top-0 z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
      <div class="flex items-center justify-between">
        <div class="flex items-center gap-2">
          <GraduationCap class="w-8 h-8 text-blue-600" />
          <span class="text-2xl font-bold text-gray-900">EduLocker</span>
        </div>
        <div class="flex items-center gap-4">
          <button class="px-4 py-2 bg-blue-600 text-white rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center gap-2">
            <LayoutDashboard class="w-4 h-4" />
            Dashboard
          </button>
          <button class="px-4 py-2 text-gray-700 rounded-lg font-medium hover:bg-gray-100 transition-colors flex items-center gap-2">
            <Route class="w-4 h-4" />
            Educational Pathways
          </button>
          <button class="w-10 h-10 bg-gray-100 rounded-full flex items-center justify-center hover:bg-gray-200 transition-colors">
            <User class="w-5 h-5 text-gray-600" />
          </button>
        </div>
      </div>
    </div>
  </header>

  <!-- Main Content -->
  <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
    <!-- Hero Section -->
    <div class="mb-8">
      <h1 class="text-4xl font-bold text-gray-900 mb-2">My Digital Locker</h1>
      <p class="text-gray-600">Manage all your academic and government certificates in one secure place</p>
    </div>

    <!-- Stats Cards -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
      <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6">
        <div class="flex items-center justify-between mb-4">
          <div>
            <p class="text-gray-600 text-sm mb-1">Total Documents</p>
            <p class="text-4xl font-bold text-gray-900">24</p>
          </div>
          <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center">
            <FileText class="w-6 h-6 text-blue-600" />
          </div>
        </div>
        <div class="flex items-center gap-1 text-green-600 text-sm">
          <TrendingUp class="w-4 h-4" />
          <span>+3 this month</span>
        </div>
      </div>

      <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6">
        <div class="flex items-center justify-between mb-4">
          <div>
            <p class="text-gray-600 text-sm mb-1">Pending Applications</p>
            <p class="text-4xl font-bold text-gray-900">5</p>
          </div>
          <div class="w-12 h-12 bg-orange-100 rounded-lg flex items-center justify-center">
            <Clock class="w-6 h-6 text-orange-600" />
          </div>
        </div>
        <div class="flex items-center gap-1 text-orange-600 text-sm">
          <span>2 require action</span>
        </div>
      </div>

      <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6">
        <div class="flex items-center justify-between mb-4">
          <div>
            <p class="text-gray-600 text-sm mb-1">Expiring Soon</p>
            <p class="text-4xl font-bold text-gray-900">2</p>
          </div>
          <div class="w-12 h-12 bg-red-100 rounded-lg flex items-center justify-center">
            <AlertTriangle class="w-6 h-6 text-red-600" />
          </div>
        </div>
        <div class="flex items-center gap-1 text-red-600 text-sm">
          <span>Within 30 days</span>
        </div>
      </div>
    </div>

    <!-- Action Buttons -->
    <div class="flex gap-4 mb-8">
      <button class="flex-1 bg-blue-600 text-white py-4 px-6 rounded-xl font-semibold hover:bg-blue-700 transition-colors flex items-center justify-center gap-2">
        <Plus class="w-5 h-5" />
        Apply for Certificate
      </button>
      <button class="flex-1 bg-purple-600 text-white py-4 px-6 rounded-xl font-semibold hover:bg-purple-700 transition-colors flex items-center justify-center gap-2">
        <Compass class="w-5 h-5" />
        Explore Pathways
      </button>
    </div>

    <!-- Search and Filters -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 mb-8">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
        <div class="relative">
          <Search class="absolute left-3 top-1/2 transform -translate-y-1/2 w-5 h-5 text-gray-400" />
          <input
            type="text"
            placeholder="Search certificates by name or authority..."
            class="w-full pl-10 pr-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
          />
        </div>
        <select class="px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
          <option>All Certificate Types</option>
          <option>Academic</option>
          <option>Sports & Activity</option>
          <option>Government</option>
          <option>Other</option>
        </select>
        <select class="px-4 py-3 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500">
          <option>All Status</option>
          <option>Active</option>
          <option>Pending</option>
          <option>Expired</option>
        </select>
      </div>
    </div>

    <!-- Academic Certificates Section -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 mb-6">
      <div 
        class="flex items-center justify-between cursor-pointer hover:bg-gray-50 p-4 rounded-lg transition-colors"
        on:click={() => toggleSection('academic')}
        on:keydown={(e) => e.key === 'Enter' && toggleSection('academic')}
        role="button"
        tabindex="0"
      >
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
            <GraduationCap class="w-5 h-5 text-blue-600" />
          </div>
          <div>
            <h2 class="text-xl font-bold text-gray-900">Academic Certificates</h2>
            <p class="text-sm text-gray-600">6 documents</p>
          </div>
        </div>
        <ChevronDown class="w-5 h-5 text-gray-400 transition-transform {expandedSections.academic ? 'rotate-180' : ''}" />
      </div>
      {#if expandedSections.academic}
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
          {#each academicCertificates as cert}
            <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden hover:shadow-md transition-shadow">
              <div class="relative h-48 bg-gradient-to-br from-blue-50 to-indigo-50 flex items-center justify-center">
                <div class="text-6xl">{cert.icon}</div>
                {#if cert.priority}
                  <span class="absolute top-3 left-3 bg-orange-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Priority
                  </span>
                {/if}
                {#if cert.status === "Active"}
                  <span class="absolute top-3 right-3 bg-green-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Active
                  </span>
                {:else if cert.status === "Expired"}
                  <span class="absolute top-3 right-3 bg-red-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Expired
                  </span>
                {:else if cert.status === "Pending"}
                  <span class="absolute top-3 right-3 bg-purple-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Pending
                  </span>
                {/if}
              </div>
              <div class="p-4">
                <h3 class="font-semibold text-gray-900 mb-2 text-lg">{cert.title}</h3>
                <p class="text-sm text-gray-600 mb-3">{cert.authority}</p>
                <div class="space-y-1 text-sm text-gray-600">
                  <div class="flex items-center gap-2">
                    <Calendar class="w-4 h-4" />
                    <span>Issued: {cert.issued}</span>
                  </div>
                  {#if cert.validUntil}
                    <div class="flex items-center gap-2">
                      <Clock class="w-4 h-4" />
                      <span>Valid until: {cert.validUntil}</span>
                    </div>
                  {/if}
                  {#if cert.appNo}
                    <div class="flex items-center gap-2">
                      <Hash class="w-4 h-4" />
                      <span>App No: {cert.appNo}</span>
                    </div>
                  {/if}
                </div>
                <div class="flex gap-2 mt-4">
                  <button class="flex-1 bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center justify-center gap-2">
                    <Eye class="w-4 h-4" />
                    View
                  </button>
                  <button class="px-4 py-2 border border-gray-300 rounded-lg font-medium hover:bg-gray-50 transition-colors flex items-center justify-center gap-2">
                    <Download class="w-4 h-4" />
                    Download
                  </button>
                </div>
              </div>
            </div>
          {/each}
        </div>
      {/if}
    </div>

    <!-- Sports & Activity Certificates Section -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 mb-6">
      <div 
        class="flex items-center justify-between cursor-pointer hover:bg-gray-50 p-4 rounded-lg transition-colors"
        on:click={() => toggleSection('sports')}
        on:keydown={(e) => e.key === 'Enter' && toggleSection('sports')}
        role="button"
        tabindex="0"
      >
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
            <Trophy class="w-5 h-5 text-blue-600" />
          </div>
          <div>
            <h2 class="text-xl font-bold text-gray-900">Sports & Activity Certificates</h2>
            <p class="text-sm text-gray-600">3 documents</p>
          </div>
        </div>
        <ChevronDown class="w-5 h-5 text-gray-400 transition-transform {expandedSections.sports ? 'rotate-180' : ''}" />
      </div>
      {#if expandedSections.sports}
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
          {#each sportsCertificates as cert}
            <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden hover:shadow-md transition-shadow">
              <div class="relative h-48 bg-gradient-to-br from-blue-50 to-indigo-50 flex items-center justify-center">
                <div class="text-6xl">{cert.icon}</div>
                {#if cert.status === "Active"}
                  <span class="absolute top-3 right-3 bg-green-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Active
                  </span>
                {/if}
              </div>
              <div class="p-4">
                <h3 class="font-semibold text-gray-900 mb-2 text-lg">{cert.title}</h3>
                <p class="text-sm text-gray-600 mb-3">{cert.authority}</p>
                <div class="space-y-1 text-sm text-gray-600">
                  <div class="flex items-center gap-2">
                    <Calendar class="w-4 h-4" />
                    <span>Issued: {cert.issued}</span>
                  </div>
                  {#if cert.validUntil}
                    <div class="flex items-center gap-2">
                      <Clock class="w-4 h-4" />
                      <span>Valid until: {cert.validUntil}</span>
                    </div>
                  {/if}
                </div>
                <div class="flex gap-2 mt-4">
                  <button class="flex-1 bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center justify-center gap-2">
                    <Eye class="w-4 h-4" />
                    View
                  </button>
                  <button class="px-4 py-2 border border-gray-300 rounded-lg font-medium hover:bg-gray-50 transition-colors flex items-center justify-center gap-2">
                    <Download class="w-4 h-4" />
                    Download
                  </button>
                </div>
              </div>
            </div>
          {/each}
        </div>
      {/if}
    </div>

    <!-- Government Documents Section -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 mb-6">
      <div 
        class="flex items-center justify-between cursor-pointer hover:bg-gray-50 p-4 rounded-lg transition-colors"
        on:click={() => toggleSection('government')}
        on:keydown={(e) => e.key === 'Enter' && toggleSection('government')}
        role="button"
        tabindex="0"
      >
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
            <Building class="w-5 h-5 text-blue-600" />
          </div>
          <div>
            <h2 class="text-xl font-bold text-gray-900">Government Documents</h2>
            <p class="text-sm text-gray-600">6 documents</p>
          </div>
        </div>
        <ChevronDown class="w-5 h-5 text-gray-400 transition-transform {expandedSections.government ? 'rotate-180' : ''}" />
      </div>
      {#if expandedSections.government}
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
          {#each governmentDocs as cert}
            <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden hover:shadow-md transition-shadow">
              <div class="relative h-48 bg-gradient-to-br from-blue-50 to-indigo-50 flex items-center justify-center">
                <div class="text-6xl">{cert.icon}</div>
                {#if cert.status === "Active"}
                  <span class="absolute top-3 right-3 bg-green-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Active
                  </span>
                {:else if cert.status === "Pending"}
                  <span class="absolute top-3 right-3 bg-purple-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Pending
                  </span>
                {/if}
              </div>
              <div class="p-4">
                <h3 class="font-semibold text-gray-900 mb-2 text-lg">{cert.title}</h3>
                <p class="text-sm text-gray-600 mb-3">{cert.authority}</p>
                <div class="space-y-1 text-sm text-gray-600">
                  <div class="flex items-center gap-2">
                    <Calendar class="w-4 h-4" />
                    <span>Issued: {cert.issued}</span>
                  </div>
                  {#if cert.validUntil}
                    <div class="flex items-center gap-2">
                      <Clock class="w-4 h-4" />
                      <span>Valid until: {cert.validUntil}</span>
                    </div>
                  {/if}
                  {#if cert.appNo}
                    <div class="flex items-center gap-2">
                      <Hash class="w-4 h-4" />
                      <span>App No: {cert.appNo}</span>
                    </div>
                  {/if}
                </div>
                <div class="flex gap-2 mt-4">
                  {#if cert.status === "Pending"}
                    <button class="flex-1 bg-purple-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-purple-700 transition-colors flex items-center justify-center gap-2">
                      <MapPin class="w-4 h-4" />
                      Track Application
                    </button>
                  {:else}
                    <button class="flex-1 bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center justify-center gap-2">
                      <Eye class="w-4 h-4" />
                      View
                    </button>
                    <button class="px-4 py-2 border border-gray-300 rounded-lg font-medium hover:bg-gray-50 transition-colors flex items-center justify-center gap-2">
                      <Download class="w-4 h-4" />
                      Download
                    </button>
                  {/if}
                </div>
              </div>
            </div>
          {/each}
        </div>
      {/if}
    </div>

    <!-- Other Certificates Section -->
    <div class="bg-white rounded-xl shadow-sm border border-gray-200 p-6 mb-6">
      <div 
        class="flex items-center justify-between cursor-pointer hover:bg-gray-50 p-4 rounded-lg transition-colors"
        on:click={() => toggleSection('other')}
        on:keydown={(e) => e.key === 'Enter' && toggleSection('other')}
        role="button"
        tabindex="0"
      >
        <div class="flex items-center gap-3">
          <div class="w-10 h-10 bg-blue-100 rounded-lg flex items-center justify-center">
            <FolderOpen class="w-5 h-5 text-blue-600" />
          </div>
          <div>
            <h2 class="text-xl font-bold text-gray-900">Other Certificates</h2>
            <p class="text-sm text-gray-600">2 documents</p>
          </div>
        </div>
        <ChevronDown class="w-5 h-5 text-gray-400 transition-transform {expandedSections.other ? 'rotate-180' : ''}" />
      </div>
      {#if expandedSections.other}
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-6">
          {#each otherCertificates as cert}
            <div class="bg-white rounded-xl shadow-sm border border-gray-200 overflow-hidden hover:shadow-md transition-shadow">
              <div class="relative h-48 bg-gradient-to-br from-blue-50 to-indigo-50 flex items-center justify-center">
                <div class="text-6xl">{cert.icon}</div>
                {#if cert.status === "Active"}
                  <span class="absolute top-3 right-3 bg-green-500 text-white text-xs px-2 py-1 rounded-full font-medium">
                    Active
                  </span>
                {/if}
              </div>
              <div class="p-4">
                <h3 class="font-semibold text-gray-900 mb-2 text-lg">{cert.title}</h3>
                <p class="text-sm text-gray-600 mb-3">{cert.authority}</p>
                <div class="space-y-1 text-sm text-gray-600">
                  <div class="flex items-center gap-2">
                    <Calendar class="w-4 h-4" />
                    <span>Issued: {cert.issued}</span>
                  </div>
                </div>
                <div class="flex gap-2 mt-4">
                  <button class="flex-1 bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition-colors flex items-center justify-center gap-2">
                    <Eye class="w-4 h-4" />
                    View
                  </button>
                  <button class="px-4 py-2 border border-gray-300 rounded-lg font-medium hover:bg-gray-50 transition-colors flex items-center justify-center gap-2">
                    <Download class="w-4 h-4" />
                    Download
                  </button>
                </div>
              </div>
            </div>
          {/each}
        </div>
      {/if}
    </div>
  </main>
</div>