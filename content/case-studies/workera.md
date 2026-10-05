---
title: "Cross-Provider RAG Recommender"
weight: 4
context: "Workera needed a production system to sync courses, data, and metadata across various content providers (Udemy, Udacity, Coursera, DataCamp, etc.)."
deliverable: "Built a Retrieval-Augmented Generation (RAG) pipeline and recommender system."
challenge: "Closing assessed skill gaps requires matching users with the exactly right content from diverse, siloed catalogs, demanding a unified data pipeline and intelligent recommendation engine."
solution:
  - "**Production System:** Built the RAG pipeline syncing data across multiple providers."
  - "**Skill Gap Closing:** Powered a recommender that automatically closes assessed skill gaps with the right content from each client's available catalog."
html_diagram: |
  <div class="bg-slate-900 border border-slate-700 rounded-xl p-8 shadow-xl overflow-x-auto">
    <div class="flex flex-col md:flex-row gap-8 items-stretch justify-between min-w-[800px]">
      
      <!-- Extraction Pipeline (Left) -->
      <div class="flex-1 w-full border border-slate-700/50 bg-slate-800/20 rounded-xl p-6 relative flex flex-col">
        <h3 class="text-white font-bold mb-6 text-center text-lg uppercase tracking-wider text-kortex-blue">RAG Pipeline</h3>
        <div class="flex flex-col gap-4 flex-grow justify-between">
          <!-- Sources -->
          <div class="grid grid-cols-3 gap-2">
              <div class="bg-slate-800 border border-slate-700 rounded-lg p-3 text-center shadow-md">
                  <span class="text-slate-300 font-medium text-sm">Udemy</span>
              </div>
              <div class="bg-slate-800 border border-slate-700 rounded-lg p-3 text-center shadow-md">
                  <span class="text-slate-300 font-medium text-sm">Coursera</span>
              </div>
              <div class="bg-slate-800 border border-slate-700 rounded-lg p-3 text-center shadow-md">
                  <span class="text-slate-300 font-medium text-sm">DataCamp</span>
              </div>
          </div>
          
          <!-- Down Arrow -->
          <div class="flex justify-center text-slate-500">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
          </div>
          
          <!-- Ingestion -->
          <div class="bg-kortex-blue/10 border border-kortex-blue/30 rounded-lg p-4 text-center shadow-lg hover:border-kortex-blue transition-colors">
              <span class="text-kortex-blue font-bold">Ingest & Extract Metadata</span>
          </div>
          
          <!-- Down Arrow -->
          <div class="flex justify-center text-slate-500">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
          </div>

          <!-- Vector DB -->
          <div class="bg-slate-800 border border-slate-600 rounded-lg p-4 text-center shadow-lg relative flex items-center justify-center gap-3">
              <svg class="w-5 h-5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 7v10c0 2.21 3.582 4 8 4s8-1.79 8-4V7M4 7c0 2.21 3.582 4 8 4s8-1.79 8-4M4 7c0-2.21 3.582-4 8-4s8 1.79 8 4m0 5c0 2.21-3.582 4-8 4s-8-1.79-8-4"></path></svg>
              <span class="text-white font-bold">Vector Database</span>
          </div>
        </div>
      </div>

      <!-- Connection Arrow -->
      <div class="hidden md:flex flex-col items-center justify-center text-slate-500 min-w-[60px]">
          <div class="text-xs uppercase tracking-widest text-slate-400 mb-2 font-semibold">Query</div>
          <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
      </div>

      <!-- Recommender System (Right) -->
      <div class="flex-1 w-full border border-slate-700/50 bg-slate-800/20 rounded-xl p-6 relative flex flex-col">
        <h3 class="text-white font-bold mb-6 text-center text-lg uppercase tracking-wider text-kortex-blue">Recommender Engine</h3>
        <div class="flex flex-col gap-4 flex-grow justify-between">
          
          <!-- User Input -->
          <div class="bg-slate-800 border border-slate-700 rounded-lg p-4 text-center shadow-md">
              <span class="text-slate-300 font-medium">User Skill Gap Assessment</span>
          </div>
          
          <!-- Down Arrow -->
          <div class="flex justify-center text-slate-500">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
          </div>

          <!-- Semantic Search -->
          <div class="bg-kortex-blue/10 border border-kortex-blue/30 rounded-lg p-4 text-center shadow-lg hover:border-kortex-blue transition-colors">
              <span class="text-kortex-blue font-bold">Semantic Search & Match</span>
          </div>
          
          <!-- Down Arrow -->
          <div class="flex justify-center text-slate-500">
              <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path></svg>
          </div>

          <!-- Goal -->
          <div class="bg-slate-800 border border-slate-600 rounded-lg p-4 text-center shadow-lg flex items-center justify-center gap-3">
              <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
              <span class="text-white font-bold">Close Skill Gaps</span>
          </div>
        </div>
      </div>
      
    </div>
  </div>
---
