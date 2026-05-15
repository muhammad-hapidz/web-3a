<template>
  <div class="min-h-screen bg-slate-950 font-merriweather selection:bg-button/30 overflow-hidden">
    <!-- Navbar Spacer -->
    <div class="h-20 lg:h-24"></div>

    <!-- Hero Section -->
    <section class="relative py-20 lg:py-32">
      <div class="absolute top-0 left-1/2 -translate-x-1/2 w-full h-full max-w-7xl">
        <div class="absolute top-0 left-0 w-96 h-96 bg-button/20 rounded-full blur-[120px] -mt-20 -ml-20"></div>
        <div class="absolute bottom-0 right-0 w-96 h-96 bg-blue-500/10 rounded-full blur-[120px] -mb-20 -mr-20"></div>
      </div>
      
      <div class="container mx-auto px-6 lg:px-12 relative z-10 text-center">
        <span class="inline-block px-4 py-1.5 mb-8 text-xs font-black tracking-[0.4em] text-button uppercase bg-button/10 border border-button/20 rounded-full animate-fade-in">
          STRATEGIC PARTNER
        </span>
        <h1 class="text-4xl md:text-7xl font-black text-white italic tracking-tighter leading-tight mb-8">
          Beyond <span class="text-button text-shadow-glow">Automation.</span><br>
          Meet the AI That Works.
        </h1>
        <p class="max-w-3xl mx-auto text-slate-400 text-lg md:text-xl font-medium leading-relaxed mb-12">
          Automa AI Agent bridges the gap between raw data and decisive action. We unify fragmented workflows into a governed, intelligent execution layer.
        </p>
        <div class="flex flex-wrap justify-center gap-6">
          <a href="#ai-agent" class="py-4 px-10 bg-button text-white font-black rounded-2xl shadow-2xl shadow-button/30 hover:bg-button/90 hover:-translate-y-1 transition-all">
            AI AGENT
          </a>
          <a href="#rpa" class="py-4 px-10 bg-white/10 text-white font-black rounded-2xl border border-white/10 backdrop-blur-md hover:bg-white/20 transition-all">
            INTELLIGENT RPA
          </a>
        </div>
      </div>
    </section>

    <!-- Part 1: Automa AI Agent -->
    <section id="ai-agent" class="py-24 relative">
      <div class="container mx-auto px-6 lg:px-12">
        <div class="flex items-center gap-4 mb-16">
          <div class="h-px flex-1 bg-gradient-to-r from-transparent to-button/50"></div>
          <h2 class="text-3xl font-black text-white italic">Automa <span class="text-button">AI Agent</span></h2>
          <div class="h-px flex-1 bg-gradient-to-l from-transparent to-button/50"></div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 mb-24">
          <div class="space-y-8">
            <h3 class="text-4xl font-black text-white leading-tight">The Intelligent Core of Enterprise Execution</h3>
            <p class="text-slate-400 text-lg leading-relaxed">
              Automa AI Agent is the enterprise command center for AI execution. We provide the architecture and control layer; customers retain model choice, data ownership, and cost transparency.
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
              <div class="p-6 bg-white/5 border border-white/10 rounded-3xl hover:border-button/40 transition-colors">
                <h4 class="text-button font-black mb-2">LLM-Agnostic</h4>
                <p class="text-xs text-slate-500">Connect OpenAI, Claude, Llama, or private models without markups.</p>
              </div>
              <div class="p-6 bg-white/5 border border-white/10 rounded-3xl hover:border-button/40 transition-colors">
                <h4 class="text-button font-black mb-2">Enterprise RAG</h4>
                <p class="text-xs text-slate-500">Grounded in private documents and operational data for accuracy.</p>
              </div>
            </div>
          </div>
          <div class="relative">
            <div class="absolute inset-0 bg-button/20 blur-[100px] rounded-full"></div>
            <div class="relative bg-slate-900/50 backdrop-blur-2xl border border-white/10 p-8 rounded-[3rem] shadow-2xl">
              <h4 class="text-white font-black mb-6 italic">Architecture Flow</h4>
              <div class="space-y-6">
                <div v-for="(step, i) in ['Ingest Knowledge', 'Reason via RAG', 'Execute via Agents', 'Optimize via Logs']" :key="i" class="flex items-center gap-4">
                  <div class="w-10 h-10 rounded-xl bg-button/10 text-button flex items-center justify-center font-black">{{ i + 1 }}</div>
                  <div class="text-slate-300 font-bold">{{ step }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Specialized Agents -->
        <h3 class="text-center text-2xl font-black text-white mb-12 italic">Specialized AI Agents</h3>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-24">
          <div v-for="agent in specializedAgents" :key="agent.name" class="group p-8 bg-white/5 border border-white/10 rounded-[2.5rem] hover:bg-button transition-all duration-500">
            <div class="w-16 h-16 bg-button/20 rounded-2xl mb-6 flex items-center justify-center text-button group-hover:bg-white group-hover:text-button transition-colors font-black text-xl italic">
              {{ agent.name[0] }}
            </div>
            <h4 class="text-xl font-black text-white group-hover:text-white mb-3">{{ agent.name }}</h4>
            <p class="text-slate-400 group-hover:text-white/80 text-sm leading-relaxed">
              <span class="font-bold text-white group-hover:text-white">{{ agent.sub }}</span> — {{ agent.desc }}
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Part 2: Automa AI-Powered RPA -->
    <section id="rpa" class="py-24 bg-slate-900/50">
      <div class="container mx-auto px-6 lg:px-12">
        <div class="flex items-center gap-4 mb-16">
          <div class="h-px flex-1 bg-gradient-to-r from-transparent to-blue-500/50"></div>
          <h2 class="text-3xl font-black text-white italic">AI-Powered <span class="text-blue-500">RPA</span></h2>
          <div class="h-px flex-1 bg-gradient-to-l from-transparent to-blue-500/50"></div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
          <div class="order-2 lg:order-1">
            <img src="/img/portofolio2.jpg" class="rounded-[3rem] shadow-2xl border border-white/10" alt="RPA Interface">
          </div>
          <div class="order-1 lg:order-2 space-y-8">
            <h3 class="text-4xl font-black text-white leading-tight">This is Intelligent Action.</h3>
            <p class="text-slate-400 text-lg leading-relaxed">
              Automa bridges human creativity and digital execution with an AI workforce designed for everyone. Automate across desktops, web apps, and legacy systems with no silos.
            </p>
            <ul class="space-y-4">
              <li v-for="pillar in rpaPillars" :key="pillar" class="flex items-start gap-4 text-slate-300">
                <svg class="w-6 h-6 text-blue-500 mt-1 shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                </svg>
                <span class="font-bold">{{ pillar }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Industry Grid -->
    <section class="py-24">
      <div class="container mx-auto px-6 lg:px-12 text-center">
        <h2 class="text-3xl font-black text-white mb-16 italic">Real-World Industry Applications</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div v-for="app in industryApps" :key="app.industry" class="p-8 bg-white/5 border border-white/10 rounded-3xl text-left hover:border-button transition-colors">
            <h4 class="text-button font-black text-xl mb-4">{{ app.industry }}</h4>
            <p class="text-slate-400 text-sm leading-relaxed">{{ app.useCases }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Comparison Table -->
    <section class="py-24 bg-white/5">
      <div class="container mx-auto px-6 lg:px-12">
        <h2 class="text-center text-3xl font-black text-white mb-16 italic">Why Automa Wins</h2>
        <div class="overflow-x-auto">
          <table class="w-full text-left border-collapse min-w-[800px]">
            <thead>
              <tr class="border-b border-white/10">
                <th class="py-6 px-4 text-slate-400 font-black uppercase text-xs tracking-widest">Dimension</th>
                <th class="py-6 px-4 text-button font-black uppercase text-xs tracking-widest">Automa AI Agent</th>
                <th class="py-6 px-4 text-slate-400 font-black uppercase text-xs tracking-widest">Standard Copilots</th>
                <th class="py-6 px-4 text-slate-400 font-black uppercase text-xs tracking-widest">iPaaS / Bots</th>
              </tr>
            </thead>
            <tbody class="text-slate-300">
              <tr v-for="row in comparisonData" :key="row.dim" class="border-b border-white/5 hover:bg-white/5 transition-colors">
                <td class="py-6 px-4 font-black">{{ row.dim }}</td>
                <td class="py-6 px-4 text-white font-bold">{{ row.automa }}</td>
                <td class="py-6 px-4 text-slate-500">{{ row.copilot }}</td>
                <td class="py-6 px-4 text-slate-500">{{ row.bots }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- Final CTA -->
    <section class="py-32 relative">
      <div class="absolute inset-0 bg-button opacity-10"></div>
      <div class="container mx-auto px-6 lg:px-12 text-center relative z-10">
        <h2 class="text-4xl md:text-6xl font-black text-white italic mb-8">Stop Experimenting.<br>Start Executing Intelligently.</h2>
        <div class="flex flex-wrap justify-center gap-6">
          <a href="/contact-us" class="py-5 px-12 bg-button text-white font-black rounded-2xl shadow-2xl shadow-button/40 hover:scale-105 transition-all">
            BUILD YOUR FIRST AGENT & BOOK A STRATEGY SESSION
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
const specializedAgents = [
  { name: 'FORMA', sub: 'Knowledge Enablement', desc: 'Converts SOPs, manuals, and training files into interactive learning and Q&A.' },
  { name: 'DATAWISE', sub: 'Analytics for Everyone', desc: 'Enables teams to query data and generate insights using natural language.' },
  { name: 'GLOSSA', sub: 'Language Control', desc: 'Enforces consistent terminology and tone across regions and products.' }
]

const rpaPillars = [
  'AI Magic Command: Instructions to workflow logic automatically.',
  'Visual Canvas: Drag-and-drop complexity into simplicity.',
  'Smart Capture: Record keystrokes for zero-effort creation.',
  'Polyglot Power: Python-ready advanced customization.'
]

const industryApps = [
  { industry: 'Finance', useCases: 'Forecast variance analysis, automated management reporting, anomaly investigation.' },
  { industry: 'Sales', useCases: 'Lead qualification, personalized outreach drafting, CRM data enrichment.' },
  { industry: 'HR', useCases: 'Resume screening, onboarding coordination, policy Q&A.' },
  { industry: 'IT Ops', useCases: 'Alert triage, root-cause summarization, remediation orchestration.' },
  { industry: 'Operations', useCases: 'Cross-system task coordination, exception handling, performance insights.' }
]

const comparisonData = [
  { dim: 'Model Strategy', automa: 'Multi-LLM, customer-chosen', copilot: 'Single provider', bots: 'No native AI' },
  { dim: 'Knowledge Grounding', automa: 'Deep RAG + DBs', copilot: 'Limited context', bots: 'None' },
  { dim: 'Execution', automa: 'Agent + RPA + API', copilot: 'Suggest only', bots: 'Rule-based' },
  { dim: 'Governance', automa: 'Enterprise console & audit', copilot: 'Minimal', bots: 'Basic' }
]
</script>

<style scoped>
.text-shadow-glow {
  text-shadow: 0 0 30px rgba(255, 110, 108, 0.5);
}
@keyframes fade-in {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in {
  animation: fade-in 1s ease-out forwards;
}
</style>
