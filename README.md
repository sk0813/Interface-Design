<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PolyU Design — Student Competition Subsidy & Reimbursement Portal</title>
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            brand: {
              50: '#f0fdfa',
              100: '#ccfbf1',
              500: '#14b8a6',
              600: '#0d9488',
              700: '#0f766e',
              800: '#115e59',
              900: '#134e4a',
            },
            polyu: {
              red: '#8b0000',
              burgundy: '#7f1d1d',
              dark: '#0f172a'
            }
          }
        }
      }
    }
  </script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap');

    body {
      font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
    }

    .custom-scrollbar::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }

    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: #cbd5e1;
      border-radius: 4px;
    }
  </style>
</head>

<body class="bg-[#f8fafc] text-slate-800 antialiased min-h-screen flex flex-col justify-between">

  <!-- ========================================================================= -->
  <!-- FLOATING QUICK NAVIGATION TOOLBAR (For seamless evaluation & walkthrough) -->
  <!-- ========================================================================= -->
  <aside
    class="fixed bottom-3 right-3 z-50 bg-slate-900/90 backdrop-blur-md text-white px-3 py-2 rounded-xl shadow-2xl border border-slate-700 text-xs flex items-center space-x-2">
    <span class="text-slate-400 font-medium">Quick Nav:</span>
    <select id="quickNavSelect" onchange="showScreen(this.value)" class="bg-slate-800 text-slate-200 border border-slate-600 rounded px-2 py-1 text-xs focus:outline-none focus:border-brand-500">
      <option value="screen-1">1. SSO Authentication</option>
      <option value="screen-2">2. Student Dashboard</option>
      <option value="screen-3">3. Step 1: Academic & Project Info</option>
      <option value="screen-4">4. Step 2: Competition & Tier</option>
      <option value="screen-5">5. Step 3: Budget & Estimator</option>
      <option value="screen-6">6. Step 4: Faculty Endorsement</option>
      <option value="screen-7">7. Step 5: Review & Declaration</option>
      <option value="screen-8">8. Result Reporting & Showcase Archive</option>
      <option value="screen-9">9. Submission Confirmation</option>
    </select>
  </aside>

  <!-- ========================================================================= -->
  <!-- SCREEN 1: PolyU Institutional Authentication — Single Sign-On (SSO) Portal -->
  <!-- ========================================================================= -->
  <section id="screen-1" class="min-h-screen flex flex-col justify-between bg-[#f8fafc]">
    <!-- Top SSO Header -->
    <header
      class="bg-white border-b border-slate-200 py-3 px-6 md:px-12 flex justify-between items-center text-xs text-slate-600">
      <div class="flex items-center space-x-4">
        <div class="flex items-center space-x-2">
          <div class="w-8 h-8 rounded bg-slate-900 text-white font-bold flex items-center justify-center text-sm">PU
          </div>
          <div>
            <div class="font-bold text-slate-900 leading-tight">PolyU Design</div>
            <div class="text-[10px] text-teal-700 font-medium">Competition Subsidy Portal</div>
          </div>
        </div>
        <span class="inline-block bg-slate-100 text-slate-600 px-2 py-0.5 rounded text-[11px] font-medium">AY 2024/25</span>
      </div>
      <div class="flex items-center space-x-6">
        <a href="#" class="hover:text-slate-900">Scheme Guidelines</a>
        <a href="#" class="hover:text-slate-900">FAQs</a>
        <a href="#" class="hover:text-slate-900">IT Service Desk</a>
        <div class="w-7 h-7 rounded-full bg-slate-200 flex items-center justify-center text-slate-600 font-bold">?</div>
      </div>
    </header>

    <!-- Sub-status Bar -->
    <div
      class="bg-slate-100/90 border-b border-slate-200 px-6 md:px-12 py-1.5 flex justify-between items-center text-[11px] text-slate-500">
      <div class="flex items-center space-x-2">
        <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
        <span>POLYU UNIFIED SINGLE SIGN-ON (CAS) • Academic Year 2024/25 • System operational with Duo 2FA</span>
      </div>
      <div class="flex items-center space-x-3">
        <span>🔒 Encrypted TLS 1.3</span>
        <span>Node CAS-HK-04</span>
      </div>
    </div>

    <!-- Main Content Container -->
    <main class="max-w-6xl w-full mx-auto p-6 md:p-10 grid grid-cols-1 lg:grid-cols-12 gap-8 my-auto">

      <!-- Left Column: Login Card -->
      <div
        class="lg:col-span-7 bg-white rounded-2xl border border-slate-200/80 shadow-sm p-6 sm:p-8 flex flex-col justify-between">
        <div>
          <div class="flex items-center justify-between mb-4">
            <span class="inline-flex items-center gap-1.5 px-2.5 py-1 rounded-md text-xs font-medium bg-teal-50 text-teal-700 border border-teal-200">
              <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/></svg>
              POLYU CENTRAL AUTHENTICATION SERVICE
            </span>
            <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">SECURE GATEWAY</span>
          </div>

          <h1 class="text-2xl font-bold text-slate-900 tracking-tight">Sign In with PolyU NetID</h1>
          <p class="text-xs text-slate-500 mt-1">Access the School of Design Competition Subsidy Scheme & Reimbursement
            Management System for active grants, reimbursements, and faculty reviews.</p>

          <!-- Identity Selector -->
          <div class="mt-6">
            <label class="block text-[11px] font-semibold text-slate-500 uppercase tracking-wider mb-2">Select Authorized Identity</label>
            <div class="grid grid-cols-3 gap-2 p-1 bg-slate-100 rounded-xl border border-slate-200">
              <button type="button" class="bg-white text-slate-900 shadow-sm py-2 px-3 rounded-lg text-center font-medium text-xs border border-slate-200/60">
                <div class="font-bold">Student Applicant</div>
                <div class="text-[10px] text-slate-500">BA / MDes / PhD</div>
              </button>
              <button type="button" class="text-slate-600 hover:text-slate-900 py-2 px-3 rounded-lg text-center font-medium text-xs">
                <div class="font-bold">Faculty Endorser</div>
                <div class="text-[10px] text-slate-500">Tutors & Leaders</div>
              </button>
              <button type="button" class="text-slate-600 hover:text-slate-900 py-2 px-3 rounded-lg text-center font-medium text-xs">
                <div class="font-bold">Finance & Admin</div>
                <div class="text-[10px] text-slate-500">Secretariat & Bursar</div>
              </button>
            </div>
          </div>

          <!-- Alert Note -->
          <div
            class="mt-4 p-3 bg-teal-50/60 border border-teal-100 rounded-xl flex items-start space-x-2 text-xs text-teal-800">
            <svg class="w-4 h-4 text-teal-600 mt-0.5 shrink-0" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z"
                clip-rule="evenodd" />
            </svg>
            <span>Logged in as a current SD Student. Grants are auto-routed to your programme leader upon NetID verification.</span>
          </div>

          <!-- Input Fields -->
          <div class="mt-5 space-y-4">
            <div>
              <div class="flex justify-between items-center text-xs mb-1">
                <label class="font-medium text-slate-700">PolyU NetID (Student / Staff ID) <span class="text-rose-500">*</span></label>
                <a href="#" class="text-teal-700 hover:underline text-[11px]">ID Format Help</a>
              </div>
              <div class="relative">
                <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-slate-400">
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z" />
                  </svg>
                </div>
                <input id="loginNetId" type="text" value="22048192D" class="w-full pl-9 pr-3 py-2 bg-slate-50 border border-slate-300 rounded-lg text-sm text-slate-800 font-medium focus:bg-white focus:outline-none focus:ring-2 focus:ring-teal-600 focus:border-teal-600">
              </div>
            </div>

            <div>
              <div class="flex justify-between items-center text-xs mb-1">
                <label class="font-medium text-slate-700">NetPassword <span class="text-rose-500">*</span></label>
                <a href="#" class="text-teal-700 hover:underline text-[11px]">Forgot NetPassword?</a>
              </div>
              <div class="relative">
                <div class="absolute inset-y-0 left-0 pl-3 flex items-center pointer-events-none text-slate-400">
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                      d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
                  </svg>
                </div>
                <input type="password" value="••••••••••••" class="w-full pl-9 pr-10 py-2 bg-slate-50 border border-slate-300 rounded-lg text-sm text-slate-800 font-medium focus:bg-white focus:outline-none focus:ring-2 focus:ring-teal-600 focus:border-teal-600">
                <button type="button" class="absolute inset-y-0 right-0 pr-3 flex items-center text-slate-400 hover:text-slate-600">
                  <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"/></svg>
                </button>
              </div>
            </div>

            <!-- MFA Options -->
            <div>
              <label class="block text-xs font-medium text-slate-700 mb-1.5">Multi-Factor Authentication (Duo 2FA)</label>
              <div class="grid grid-cols-3 gap-2">
                <label class="border-2 border-teal-600 bg-teal-50/30 rounded-lg p-2 flex flex-col justify-between cursor-pointer">
                  <div class="flex items-center justify-between">
                    <span class="text-xs font-bold text-slate-900">Duo Push</span>
                    <span class="w-2.5 h-2.5 rounded-full bg-teal-600"></span>
                  </div>
                  <span class="text-[10px] text-teal-700 mt-1 font-medium">Recommended</span>
                </label>
                <label class="border border-slate-200 hover:border-slate-300 rounded-lg p-2 flex flex-col justify-between cursor-pointer">
                  <div class="flex items-center justify-between">
                    <span class="text-xs font-semibold text-slate-700">FIDO2 / Key</span>
                    <span class="w-2.5 h-2.5 rounded-full border border-slate-300"></span>
                  </div>
                  <span class="text-[10px] text-slate-500 mt-1">YubiKey / Passkey</span>
                </label>
                <label class="border border-slate-200 hover:border-slate-300 rounded-lg p-2 flex flex-col justify-between cursor-pointer">
                  <div class="flex items-center justify-between">
                    <span class="text-xs font-semibold text-slate-700">SMS OTP</span>
                    <span class="w-2.5 h-2.5 rounded-full border border-slate-300"></span>
                  </div>
                  <span class="text-[10px] text-slate-500 mt-1">+852 / +86 mobile</span>
                </label>
              </div>
            </div>

            <div class="flex items-center justify-between text-xs pt-1">
              <label class="flex items-center space-x-2 text-slate-600 cursor-pointer">
                <input type="checkbox" checked class="rounded text-teal-600 focus:ring-teal-500">
                <span>Remember my NetID on this workstation (valid for 14 days)</span>
              </label>
              <a href="#" class="text-teal-700 hover:underline">Security Notice</a>
            </div>
          </div>
        </div>

        <!-- Submit Button -->
        <div class="mt-6 pt-4 border-t border-slate-100">
          <button id="btnSignInSSO" onclick="showScreen('screen-2')" class="w-full py-3 px-4 bg-slate-900 hover:bg-slate-800 text-white font-semibold rounded-xl text-sm shadow-md flex items-center justify-center space-x-2 transition-all">
            <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"/></svg>
            <span>Sign In with NetID SSO</span>
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
          </button>

          <div class="mt-3 text-center">
            <span class="text-[10px] text-slate-400 uppercase tracking-widest font-semibold">OR CAMPUS TERMINAL</span>
            <button type="button" class="mt-2 w-full py-2 px-3 border border-slate-200 hover:bg-slate-50 rounded-lg text-xs font-medium text-slate-700 flex items-center justify-center space-x-2">
              <svg class="w-4 h-4 text-teal-600" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z"/></svg>
              <span>Authenticate with PolyU Smart Card / NFC Reader</span>
            </button>
          </div>
          <p class="text-[11px] text-slate-400 text-center mt-3">By logging in, you agree to comply with the <a href="#"
              class="underline">Acceptable Use of IT Resources</a> of PolyU.</p>
        </div>
      </div>

      <!-- Right Column: Policy & Guidelines Highlights -->
      <div class="lg:col-span-5 space-y-4">

        <!-- Funding Cap Card -->
        <div class="bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm">
          <div class="flex justify-between items-center mb-2">
            <span class="text-[11px] font-bold text-slate-500 uppercase tracking-wider">Policy & Funding Caps</span>
            <span class="px-2 py-0.5 rounded text-[10px] font-semibold bg-emerald-100 text-emerald-800">AY 2024/25 Active</span>
          </div>
          <h2 class="text-base font-bold text-slate-900 leading-snug">Student Competition Subsidy Policy</h2>
          <p class="text-xs text-slate-500 mt-1">Applicable to all full-time & part-time SD students (BA Design, MDes,
            and PhD Candidates).</p>

          <div class="grid grid-cols-2 gap-3 mt-4">
            <div class="p-3 bg-slate-50 border border-slate-200/60 rounded-xl">
              <span class="text-[10px] font-semibold text-slate-500 uppercase">Annual Student Cap</span>
              <div class="text-xl font-extrabold text-slate-900 mt-0.5">HK$5,000</div>
              <span class="text-[10px] text-slate-500">Per registered student / yr</span>
            </div>
            <div class="p-3 bg-teal-50/50 border border-teal-100 rounded-xl">
              <span class="text-[10px] font-semibold text-teal-700 uppercase">Tier 1 International</span>
              <div class="text-xl font-extrabold text-teal-800 mt-0.5">HK$1,500</div>
              <span class="text-[10px] text-teal-600">Max entry fee per claim</span>
            </div>
          </div>

          <div
            class="mt-4 p-3 bg-amber-50/70 border border-amber-200/60 rounded-xl flex items-start space-x-2.5 text-xs text-amber-900">
            <svg class="w-4 h-4 text-amber-600 shrink-0 mt-0.5" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm1-12a1 1 0 10-2 0v4a1 1 0 00.293.707l2.828 2.829a1 1 0 101.415-1.415L11 9.586V6z"
                clip-rule="evenodd" />
            </svg>
            <div>
              <span class="font-bold">Application Cycle 2025</span>
              <p class="text-[11px] text-amber-800 mt-0.5">Semester 2 & Summer Term: Claims for Red Dot, iF, D&AD,
                Golden Pin, and approved competitions open until 15 July 2025.</p>
            </div>
          </div>
        </div>

        <!-- Checklist Card -->
        <div class="bg-white rounded-2xl border border-slate-200/80 p-6 shadow-sm">
          <h3 class="text-xs font-bold text-slate-900 uppercase tracking-wider mb-3 flex items-center space-x-1.5">
            <svg class="w-4 h-4 text-teal-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
            </svg>
            <span>Pre-Application Checklist</span>
          </h3>
          <p class="text-xs text-slate-500 mb-3">Ensure your university student record satisfies gatekeeping conditions
            before drafting a proposal:</p>
          <ul class="space-y-2 text-xs">
            <li class="flex items-start space-x-2 text-slate-700">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-900">Active SD Enrolment:</strong> Enrolled in BA (Hons) Design Scheme,
                MDes, or Research programmes.</div>
            </li>
            <li class="flex items-start space-x-2 text-slate-700">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-900">Competition Pre-Approval:</strong> Event must belong to Tier 1 / Tier
                2 institutional list or hold studio leader endorsement.</div>
            </li>
            <li class="flex items-start space-x-2 text-slate-700">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-900">Direct Bank Auto-Pay Info:</strong> Linked HKD bank account registered
                in PolyU Student Information System (SIS).</div>
            </li>
          </ul>
        </div>

        <!-- Security Card -->
        <div class="p-4 bg-slate-900 text-white rounded-2xl flex items-center space-x-3 text-xs">
          <div
            class="w-10 h-10 rounded-xl bg-slate-800 flex items-center justify-center text-teal-400 shrink-0 font-mono font-bold text-lg">
            🛡️</div>
          <div>
            <div class="font-bold text-slate-200">ITS Cyber Security Shield</div>
            <div class="text-[11px] text-slate-400">ISO 27001 Certified • PolyU CAS v5.4 • Session idle timeout 20 mins.
            </div>
          </div>
        </div>

      </div>
    </main>

    <!-- Support Banner Footer -->
    <div class="bg-white border-t border-slate-200 py-6 px-6 md:px-12 mt-auto">
      <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6 text-xs text-slate-600">
        <div>
          <div class="font-bold text-slate-900 flex items-center gap-1 mb-1">
            <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
            ITS SERVICE DESK
          </div>
          <div>NetID & MFA Assistance: +852 2766 5900</div>
          <a href="mailto:itservicedesk@polyu.edu.hk"
            class="text-teal-700 hover:underline">itservicedesk@polyu.edu.hk</a>
        </div>
        <div>
          <div class="font-bold text-slate-900 flex items-center gap-1 mb-1">
            <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4" />
            </svg>
            SD SUBSIDY SECRETARIAT
          </div>
          <div>V810, Jockey Club Innovation Tower</div>
          <a href="mailto:sd.subsidy@polyu.edu.hk" class="text-teal-700 hover:underline">sd.subsidy@polyu.edu.hk</a>
        </div>
        <div>
          <div class="font-bold text-slate-900 flex items-center gap-1 mb-1">
            <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M12 10v6m0 0l-3-3m3 3l3-3m2 8H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z" />
            </svg>
            SCHEME DOCUMENTATION
          </div>
          <div>Download Guidelines & Tiers PDF</div>
          <span class="text-[11px] text-slate-500">AY 2024/25 student competition manual (3.2 MB)</span>
        </div>
      </div>
      <div class="border-t border-slate-100 mt-5 pt-4 text-center text-[11px] text-slate-400">
        © 2024-2025 The Hong Kong Polytechnic University. School of Design. All rights reserved.
      </div>
    </div>
  </section>

  <!-- ========================================================================= -->
  <!-- SHARED APP HEADER (Screens 2 - 9) -->
  <!-- ========================================================================= -->
  <header id="app-global-header"
    class="hidden bg-white border-b border-slate-200 sticky top-0 z-40 px-6 lg:px-12 py-3 shadow-xs">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <div class="flex items-center space-x-6">
        <!-- Logo -->
        <div class="flex items-center space-x-2.5 cursor-pointer" onclick="showScreen('screen-2')">
          <div class="w-8 h-8 rounded bg-slate-900 text-white font-bold flex items-center justify-center text-sm">PU
          </div>
          <div>
            <div class="font-bold text-slate-900 text-xs leading-none">PolyU Design</div>
            <div class="text-[9px] text-teal-700 font-bold uppercase tracking-wider">Subsidy Portal</div>
          </div>
        </div>

        <!-- Navigation Tabs -->
        <nav class="hidden md:flex items-center space-x-1 text-xs font-semibold text-slate-600">
          <button onclick="showScreen('screen-2')" class="px-3 py-1.5 rounded-lg bg-slate-100 text-slate-900 font-bold">Dashboard</button>
          <button onclick="showScreen('screen-3')" class="px-3 py-1.5 rounded-lg hover:bg-slate-50 text-slate-600">New Application</button>
          <button class="px-3 py-1.5 rounded-lg hover:bg-slate-50 text-slate-600">Claims & Reimbursement</button>
          <button class="px-3 py-1.5 rounded-lg hover:bg-slate-50 text-slate-600">Competition Directory</button>
          <button class="px-3 py-1.5 rounded-lg hover:bg-slate-50 text-slate-600">Scheme Guidelines</button>
        </nav>
      </div>

      <!-- Right User Menu -->
      <div class="flex items-center space-x-4">
        <span class="hidden sm:inline-block bg-teal-50 text-teal-800 border border-teal-200 text-[11px] font-semibold px-2.5 py-1 rounded-full">AY 2024/25 • SEMESTER 2</span>

        <!-- Bell Notification -->
        <button class="relative p-1.5 text-slate-500 hover:text-slate-800 rounded-lg hover:bg-slate-100">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"/></svg>
          <span class="absolute top-1 right-1 w-2 h-2 bg-rose-500 rounded-full"></span>
        </button>

        <!-- User Profile Pill -->
        <div class="flex items-center space-x-2 pl-2 border-l border-slate-200">
          <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=100&auto=format&fit=crop&q=80" alt="Chloe Wong" class="w-8 h-8 rounded-full object-cover border border-slate-300">
          <div class="text-left text-xs leading-tight hidden lg:block">
            <div class="font-bold text-slate-900">Chloe Wong</div>
            <div class="text-[10px] text-slate-500">BA Design, Y3 • 22048192D</div>
          </div>
          <button onclick="showScreen('screen-1')" title="Log Out" class="text-slate-400 hover:text-rose-600 p-1">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"/></svg>
          </button>
        </div>
      </div>
    </div>
  </header>

  <!-- ========================================================================= -->
  <!-- SCREEN 2: Student Subsidy Dashboard -->
  <!-- ========================================================================= -->
  <main id="screen-2" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">

    <!-- Breadcrumb & Page Title -->
    <div>
      <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
        <span class="inline-block w-2 h-2 rounded-full bg-teal-500"></span>
        <span class="font-semibold text-slate-700">STUDENT PORTAL</span>
        <span>•</span>
        <span>POLYU SCHOOL OF DESIGN</span>
      </div>
      <div class="flex flex-col md:flex-row md:items-center justify-between gap-4">
        <div>
          <h1 class="text-2xl lg:text-3xl font-extrabold text-slate-900">Welcome back, Chloe</h1>
          <p class="text-xs text-slate-500 mt-0.5">BA (Hons) in Design (Interactive Media) • Year 3 • NetID: 22048192D
          </p>
        </div>
        <div class="flex items-center space-x-3">
          <button class="px-4 py-2 bg-white border border-slate-200 hover:bg-slate-50 rounded-xl text-xs font-semibold text-slate-700 shadow-xs flex items-center space-x-1.5">
            <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
            <span>Endorsement Guide</span>
          </button>
          <button id="btnNewSubsidy" onclick="showScreen('screen-3')" class="px-4 py-2 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold shadow-sm flex items-center space-x-1.5 transition">
            <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"/></svg>
            <span>+ New Subsidy Application</span>
          </button>
        </div>
      </div>
    </div>

    <!-- 4 Stats Cards -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
      <!-- Card 1 -->
      <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs">
        <div class="flex justify-between items-center text-xs text-slate-500 font-semibold mb-2">
          <span>ANNUAL QUOTA REMAINING</span>
          <svg class="w-4 h-4 text-teal-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M3 10h18M7 15h1m4 0h1m-7 4h12a3 3 0 003-3V8a3 3 0 00-3-3H6a3 3 0 00-3 3v8a3 3 0 003 3z" />
          </svg>
        </div>
        <div class="text-2xl font-black text-slate-900">HK$ 3,200
          <span class="text-xs font-normal text-slate-400">/ 5,000</span></div>
        <div class="w-full bg-slate-100 rounded-full h-1.5 mt-3 overflow-hidden">
          <div class="bg-teal-600 h-1.5 rounded-full" style="width: 64%"></div>
        </div>
        <div class="text-[11px] text-slate-400 mt-2">ⓘ Max HK$ 1,500 per approved claim</div>
      </div>

      <!-- Card 2 -->
      <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs">
        <div class="flex justify-between items-center text-xs text-slate-500 font-semibold mb-2">
          <span>ACTIVE SUBMISSIONS</span>
          <svg class="w-4 h-4 text-teal-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2" />
          </svg>
        </div>
        <div class="text-2xl font-black text-slate-900">2
          <span class="text-xs font-medium text-slate-500">In Progress</span></div>
        <div class="text-[11px] text-amber-600 font-medium mt-3 flex items-center space-x-1">
          <span class="w-1.5 h-1.5 rounded-full bg-amber-500"></span>
          <span>1 Awaiting Academic Endorsement</span>
        </div>
        <div class="text-[11px] text-teal-700 font-medium">1 Action required from student</div>
      </div>

      <!-- Card 3 -->
      <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs">
        <div class="flex justify-between items-center text-xs text-slate-500 font-semibold mb-2">
          <span>DISBURSED (YTD)</span>
          <svg class="w-4 h-4 text-emerald-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
        </div>
        <div class="text-2xl font-black text-slate-900">HK$ 1,800</div>
        <div class="text-[11px] text-slate-500 mt-3">2 applications processed & deposited</div>
        <div class="text-[11px] text-slate-400">AY 2024/25 Sem 1 records archived</div>
      </div>

      <!-- Card 4 -->
      <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs border-l-4 border-l-rose-500">
        <div class="flex justify-between items-center text-xs text-slate-500 font-semibold mb-2">
          <span class="text-rose-600">PRIORITY WINDOW</span>
          <svg class="w-4 h-4 text-rose-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
        </div>
        <div class="text-2xl font-black text-rose-600">6 Days Left</div>
        <div class="text-[11px] text-slate-500 mt-3">Red Dot payment receipt window</div>
        <a href="#action-banner" class="text-[11px] text-rose-600 font-bold hover:underline">RESOLVE NOW →</a>
      </div>
    </div>

    <!-- Pre-Approval Action Required Alert -->
    <div id="action-banner"
      class="p-4 bg-amber-50/90 border border-amber-200 rounded-2xl flex flex-col md:flex-row md:items-center justify-between gap-4">
      <div class="flex items-start space-x-3">
        <div class="w-8 h-8 rounded-lg bg-amber-100 text-amber-700 flex items-center justify-center shrink-0 mt-0.5">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
              d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" />
          </svg>
        </div>
        <div>
          <div class="flex items-center space-x-2">
            <span class="bg-amber-200 text-amber-900 text-[10px] font-bold px-2 py-0.5 rounded">ACTION REQUIRED</span>
            <h2 class="text-xs font-bold text-slate-900">Pre-Approval Granted for Red Dot Concept Award 2025</h2>
          </div>
          <p class="text-xs text-slate-600 mt-1">Your supervisor
            <strong class="text-slate-900">Prof. Marcus Lee</strong> endorsed your submission on
            <strong>Feb 24</strong>. Please upload official tax receipts for entry fees and material expenses within the
            next 6 days to confirm your <strong>HK$ 1,250</strong> direct disbursement.</p>
        </div>
      </div>
      <div class="flex items-center space-x-2 shrink-0">
        <button class="px-3 py-1.5 bg-white border border-slate-300 hover:bg-slate-50 rounded-lg text-xs font-semibold text-slate-700">View Approval Dossier</button>
        <button onclick="showScreen('screen-8')" class="px-3.5 py-1.5 bg-slate-900 hover:bg-slate-800 text-white rounded-lg text-xs font-semibold flex items-center space-x-1 shadow-sm">
          <svg class="w-3.5 h-3.5 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"/></svg>
          <span>Upload Receipts</span>
        </button>
      </div>
    </div>

    <!-- Active Submissions & Sidebar Section -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Submissions List (Left 8 Cols) -->
      <div class="lg:col-span-8 space-y-4">
        <div class="flex items-center justify-between">
          <h2 class="text-base font-bold text-slate-900">Active Submissions</h2>
          <div class="flex space-x-1 text-xs">
            <button class="px-2.5 py-1 bg-slate-900 text-white rounded-md font-semibold">All (3)</button>
            <button class="px-2.5 py-1 text-slate-500 hover:bg-slate-100 rounded-md">Under Review (1)</button>
            <button class="px-2.5 py-1 text-slate-500 hover:bg-slate-100 rounded-md">Pre-Approved (1)</button>
            <button class="px-2.5 py-1 text-slate-500 hover:bg-slate-100 rounded-md">Draft (1)</button>
          </div>
        </div>

        <!-- Submission Card 1: Under Review -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-3">
          <div class="flex flex-wrap items-center justify-between gap-2">
            <div class="flex items-center space-x-2">
              <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-teal-50 text-teal-800 border border-teal-200">INTERNATIONAL TIER 1</span>
              <span class="text-xs text-slate-500">Individual Project • Submitted Mar 01, 2025</span>
            </div>
            <span class="inline-flex items-center text-xs font-semibold text-amber-700 bg-amber-50 px-2.5 py-0.5 rounded-full border border-amber-200">
              <span class="w-1.5 h-1.5 rounded-full bg-amber-500 mr-1.5 animate-pulse"></span> PENDING ENDORSEMENT
            </span>
          </div>
          <h3 class="text-base font-bold text-slate-900">iF Student Design Award 2025 — Smart Campus Mobility</h3>

          <div class="grid grid-cols-3 gap-2 py-2 px-3 bg-slate-50 rounded-xl text-xs">
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Endorsing Faculty</span>
              <div class="font-bold text-slate-800">Dr. Wendy Kwan</div>
              <div class="text-[10px] text-slate-500">Associate Professor (SD)</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Requested Subsidy</span>
              <div class="font-bold text-slate-800">HK$ 1,180</div>
              <div class="text-[10px] text-slate-500">Entry Fee & Digital Prep</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Approval Timeline</span>
              <div class="font-bold text-slate-800">Est. 3 Working Days</div>
              <div class="text-[10px] text-slate-500">Batch review cutoff: Mar 07</div>
            </div>
          </div>

          <div class="flex justify-between items-center text-xs pt-1">
            <span class="text-[11px] text-slate-400 flex items-center gap-1">
              <svg class="w-3.5 h-3.5 text-slate-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
              Automated faculty ping scheduled in 48 hours
            </span>
            <div class="flex space-x-2">
              <button class="px-3 py-1 bg-white border border-slate-200 rounded-lg text-slate-700 font-medium hover:bg-slate-50">View Details</button>
              <button class="px-3 py-1 bg-slate-900 text-white rounded-lg font-medium hover:bg-slate-800">Resend Reminder</button>
            </div>
          </div>
        </div>

        <!-- Submission Card 2: Pre-Approved with Stepper Pipeline -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-4">
          <div class="flex flex-wrap items-center justify-between gap-2">
            <div class="flex items-center space-x-2">
              <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-teal-50 text-teal-800 border border-teal-200">INTERNATIONAL TIER 1</span>
              <span class="text-xs text-slate-500">Group Project (Lead: Chloe Wong + 3 Members) • Approved Feb 24, 2025</span>
            </div>
            <span class="inline-flex items-center text-xs font-semibold text-teal-700 bg-teal-50 px-2.5 py-0.5 rounded-full border border-teal-200">
              <svg class="w-3 h-3 text-teal-600 mr-1" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/></svg>
              PRE-APPROVED BY FACULTY
            </span>
          </div>

          <h3 class="text-base font-bold text-slate-900">Red Dot Award: Design Concept 2025 — Haptic Navigation Ring
          </h3>

          <!-- Stepper Graphic -->
          <div class="bg-slate-50 p-3 rounded-xl border border-slate-100">
            <div class="flex justify-between items-center text-[11px] font-semibold text-slate-500 mb-2">
              <span>REIMBURSEMENT MILESTONE PIPELINE</span>
              <span class="text-rose-600 font-bold">● STEP 2 INGESTION PENDING</span>
            </div>
            <div class="grid grid-cols-3 gap-2">
              <div class="border-t-2 border-emerald-500 pt-1 text-[11px]">
                <div class="font-bold text-emerald-700">1. Pre-Approval</div>
                <div class="text-[10px] text-slate-400">Complete (Feb 24)</div>
              </div>
              <div class="border-t-2 border-rose-500 pt-1 text-[11px]">
                <div class="font-bold text-rose-600">2. Receipt Proof</div>
                <div class="text-[10px] text-rose-500 font-medium">6 Days Left</div>
              </div>
              <div class="border-t-2 border-slate-200 pt-1 text-[11px]">
                <div class="font-bold text-slate-400">3. Disbursed</div>
                <div class="text-[10px] text-slate-400">Final Stage</div>
              </div>
            </div>
          </div>

          <div class="grid grid-cols-3 gap-2 text-xs">
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Academic Lead</span>
              <div class="font-bold text-slate-800">Prof. Marcus Lee</div>
              <div class="text-[10px] text-slate-500">Dean of Design Research</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Allocated Grant</span>
              <div class="font-bold text-slate-800">HK$ 1,500
                <span class="text-[10px] font-normal text-slate-500">(Capped)</span></div>
              <div class="text-[10px] text-slate-500">Registration & Prototyping</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Team Allocation</span>
              <div class="font-bold text-slate-800">Lead Disburser</div>
              <div class="text-[10px] text-slate-500">HSBC direct bank credit</div>
            </div>
          </div>

          <div class="flex justify-between items-center text-xs pt-1 border-t border-slate-100">
            <span class="text-rose-600 font-medium text-[11px] flex items-center gap-1">
              <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"/></svg>
              Requires payment receipt and proof of participation
            </span>
            <div class="flex space-x-2">
              <button class="px-3 py-1 bg-white border border-slate-200 rounded-lg text-slate-700 font-medium hover:bg-slate-50">View Dossier</button>
              <button onclick="showScreen('screen-8')" class="px-3 py-1 bg-slate-900 text-white rounded-lg font-medium hover:bg-slate-800 flex items-center space-x-1">
                <svg class="w-3.5 h-3.5 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-8l-4-4m0 0L8 8m4-4v12"/></svg>
                <span>Upload Payment Receipts</span>
              </button>
            </div>
          </div>
        </div>

        <!-- Submission Card 3: Draft Card (User navigates to Screen 8 via 'Continue Application') -->
        <div class="bg-white p-5 rounded-2xl border border-dashed border-slate-300 shadow-xs space-y-3">
          <div class="flex flex-wrap items-center justify-between gap-2">
            <div class="flex items-center space-x-2">
              <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-slate-100 text-slate-700">LOCAL RECOGNIZED</span>
              <span class="text-xs text-slate-500">Coursework-based (SD3102 Studio III) • Last saved 4 hours ago</span>
            </div>
            <span class="text-xs font-semibold text-slate-500 bg-slate-100 px-2.5 py-0.5 rounded-full">
              DRAFT (STEP 2 OF 5)
            </span>
          </div>

          <h3 class="text-base font-bold text-slate-900">Hong Kong Smart Design Awards 2025 — EcoPackaging System</h3>

          <div class="grid grid-cols-3 gap-2 py-2 px-3 bg-slate-50 rounded-xl text-xs">
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Current Stage</span>
              <div class="font-bold text-slate-800">Competition Details</div>
              <div class="text-[10px] text-slate-500">Budget & supervisor pending</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Estimated Claim</span>
              <div class="font-bold text-slate-800">HK$ 750</div>
              <div class="text-[10px] text-slate-500">Standard Student Rate</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Competition Deadline</span>
              <div class="font-bold text-slate-800">Apr 15, 2025</div>
              <div class="text-[10px] text-slate-500">38 days remaining to apply</div>
            </div>
          </div>

          <div class="flex justify-between items-center text-xs pt-1">
            <button class="text-rose-600 font-medium hover:underline">Discard Draft</button>
            <div class="flex space-x-2">
              <button class="px-3 py-1 bg-white border border-slate-200 rounded-lg text-slate-700 font-medium hover:bg-slate-50">Preview</button>
              <!-- Primary Trigger for screen 8 per prompt -->
              <button id="btnContinueAppTo8" onclick="showScreen('screen-8')" class="px-3 py-1 bg-slate-900 text-white rounded-lg font-medium hover:bg-slate-800 flex items-center space-x-1">
                <span>Continue Application</span>
                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/></svg>
              </button>
            </div>
          </div>
        </div>

      </div>

      <!-- Right Column Sidebar (Right 4 Cols) -->
      <div class="lg:col-span-4 space-y-4">

        <!-- Showcase Building Card -->
        <div class="bg-white rounded-2xl border border-slate-200/80 overflow-hidden shadow-xs">
          <div class="h-32 bg-cover bg-center relative"
            style="background-image: url('https://images.unsplash.com/photo-1522071820081-009f0129c71c?w=600&auto=format&fit=crop&q=80')">
            <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 to-transparent flex items-end p-3">
              <span class="text-white text-xs font-bold">Jockey Club Innovation Tower</span>
            </div>
          </div>
          <div class="p-4 space-y-2">
            <span class="text-[10px] font-bold text-slate-400 uppercase">ELIGIBILITY GUIDELINE TIP</span>
            <p class="text-xs text-slate-600">Every subsidized entry must credit
              <strong>The Hong Kong Polytechnic University School of Design</strong> in competition registry credits to
              qualify for disbursement.</p>
          </div>
        </div>

        <!-- Past Subsidies & Results -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-3">
          <div class="flex justify-between items-center text-xs">
            <h3 class="font-bold text-slate-900">Past Subsidies & Results</h3>
            <span class="text-[10px] text-slate-400">Archived in AY 2024/25</span>
          </div>

          <div class="space-y-2.5">
            <div class="p-2.5 bg-slate-50 rounded-xl text-xs flex justify-between items-center">
              <div>
                <div class="font-bold text-slate-800">D&AD New Blood Awards 2024</div>
                <div class="text-[10px] text-slate-500">Graphite Pencil Winner</div>
                <div class="text-[10px] text-teal-700 font-semibold mt-0.5">● Outcome verified & archived</div>
              </div>
              <div class="text-right">
                <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-amber-100 text-amber-800">PENCIL WINNER</span>
                <div class="font-bold text-slate-900 mt-1">HK$ 1,500 Disbursed</div>
              </div>
            </div>

            <div class="p-2.5 bg-slate-50 rounded-xl text-xs flex justify-between items-center">
              <div>
                <div class="font-bold text-slate-800">K-Design Award 2024</div>
                <div class="text-[10px] text-slate-500">Medical Assist UI/UX</div>
                <div class="text-[10px] text-teal-700 font-semibold mt-0.5">● Outcome verified & archived</div>
              </div>
              <div class="text-right">
                <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-slate-200 text-slate-700">FINALIST</span>
                <div class="font-bold text-slate-900 mt-1">HK$ 920 Disbursed</div>
              </div>
            </div>
          </div>

          <div class="p-3 bg-amber-50/60 rounded-xl border border-amber-200/50 text-[11px] text-amber-900">
            <strong>REPORTING OBLIGATION:</strong> Competition results must be reported within 30 days of the official
            announcement to protect subsequent grant privileges.
          </div>
        </div>

        <!-- Administrative Guidance -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-2">
          <h3 class="text-xs font-bold text-slate-900 uppercase">Need Administrative Guidance?</h3>
          <p class="text-xs text-slate-500">Faculty endorsing coordinators review applications every Tuesday and Friday
            during term time.</p>
          <div class="pt-2 space-y-1.5">
            <a href="mailto:sd.subsidy@polyu.edu.hk"
              class="flex items-center justify-between p-2 rounded-lg bg-slate-50 hover:bg-slate-100 text-xs font-medium text-slate-700">
              <span class="flex items-center gap-1.5">✉️ Contact Scheme Administrator</span>
              <span>→</span>
            </a>
            <a href="#"
              class="flex items-center justify-between p-2 rounded-lg bg-slate-50 hover:bg-slate-100 text-xs font-medium text-slate-700">
              <span class="flex items-center gap-1.5">📄 Download Tier Criteria Matrix</span>
              <span>→</span>
            </a>
          </div>
        </div>

      </div>

    </div>

  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 3: Step 1: Academic & Project Info -->
  <!-- ========================================================================= -->
  <main id="screen-3" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Wizard Header -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">New Application</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">New Subsidy Application</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-xs">
        <span class="text-slate-500 flex items-center gap-1">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> Auto-saved just now • Ref:
        <strong class="text-slate-800">#SUB-2025-0892</strong>
        </span>
        <button class="px-3 py-1.5 bg-white border border-slate-300 rounded-lg font-semibold text-slate-700 hover:bg-slate-50">Save as Draft</button>
        <button onclick="showScreen('screen-2')" class="text-slate-400 hover:text-slate-600">✕</button>
      </div>
    </div>

    <!-- 3-Column Layout: Stepper | Form | Rules -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">APPLICATION STAGE</span>
            <span class="font-extrabold text-teal-700">Step 1 of 5 (20%)</span>
          </div>

          <!-- Step Items -->
          <nav class="space-y-3 text-xs">
            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">1</span>
              <div>
                <div class="font-bold text-teal-900">Academic & Project</div>
                <div class="text-[10px] text-teal-700">Currently Editing</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">2</span>
              <div>
                <div class="font-medium text-slate-600">Competition Details</div>
                <div class="text-[10px]">Tier, organizers & dates</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">3</span>
              <div>
                <div class="font-medium text-slate-600">Budget & Claim Estimator</div>
                <div class="text-[10px]">Breakdown & caps</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">4</span>
              <div>
                <div class="font-medium text-slate-600">Faculty Endorsement</div>
                <div class="text-[10px]">Studio leader review</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">5</span>
              <div>
                <div class="font-medium text-slate-600">Review & Sign-off</div>
                <div class="text-[10px]">Declarations</div>
              </div>
            </div>
          </nav>
        </div>

        <!-- Quota Tracker -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">ANNUAL SUBSIDY CAP</span>
            <span class="text-[10px] font-semibold text-teal-700">Tier A Allowance</span>
          </div>
          <div class="text-xl font-black text-slate-900">HK$ 3,200
            <span class="text-xs font-normal text-slate-400">Remaining / HK$ 5,000</span></div>
          <p class="text-[11px] text-slate-500">Max claim per application: <strong>HK$ 1,500</strong> for Individual /
            <strong>HK$ 3,000</strong> for Collaborative groups.</p>
        </div>
      </div>

      <!-- Main Step 1 Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- Applicant Verified Profile -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-3">
            <div class="flex items-center space-x-2">
              <span class="text-teal-600 font-bold">🛡️</span>
              <h2 class="text-sm font-bold text-slate-900">Student Applicant & Profile</h2>
            </div>
            <span class="text-[10px] bg-emerald-50 text-emerald-700 font-bold px-2 py-0.5 rounded border border-emerald-200">● Verified Sync</span>
          </div>

          <div class="grid grid-cols-2 gap-4 text-xs">
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Full Legal Name</span>
              <div class="font-bold text-slate-900">Chloe Wong (黃凱晴)</div>
              <div class="text-[10px] text-slate-500">Primary Disburser Account</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Student NetID / ID Number</span>
              <div class="font-bold text-slate-900">22048192D</div>
              <div class="text-[10px] text-slate-500">chloe.wong@connect.polyu.hk</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Enrolled Academic Programme</span>
              <div class="font-bold text-slate-900">BA (Hons) in Design (Interactive Media)</div>
              <div class="text-[10px] text-slate-500">Scheme Code: 14401-IM</div>
            </div>
            <div>
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Study Year & Academic Cluster</span>
              <div class="font-bold text-slate-900">Year 3 (Full-time Undergraduate)</div>
              <div class="text-[10px] text-teal-700 font-medium">Cluster: Info & Interaction Design</div>
            </div>
          </div>
          <p class="text-[10px] text-slate-400 pt-2 border-t border-slate-100">Information locked according to Academic
            Registry records. <a href="#" class="text-teal-700 underline">Report data discrepancy</a></p>
        </div>

        <!-- Project Nature & Team Composition -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <h2 class="text-sm font-bold text-slate-900">Project Nature & Team Composition</h2>
            <p class="text-xs text-slate-500">Select collaboration model and curriculum alignment</p>
          </div>

          <div class="grid grid-cols-2 gap-3">
            <label class="border border-slate-200 p-3 rounded-xl cursor-pointer hover:border-slate-300">
              <div class="flex items-center space-x-2">
                <input type="radio" name="proj_nature" class="text-teal-600">
                <span class="text-xs font-bold text-slate-800">Individual Project</span>
              </div>
              <p class="text-[10px] text-slate-500 mt-1 pl-5">Single applicant. Disbursed directly to student account. Max HK$1,500.</p>
            </label>
            <label class="border-2 border-teal-600 bg-teal-50/20 p-3 rounded-xl cursor-pointer">
              <div class="flex items-center space-x-2">
                <input type="radio" name="proj_nature" checked class="text-teal-600">
                <span class="text-xs font-bold text-slate-900">Group / Collaborative</span>
              </div>
              <p class="text-[10px] text-slate-600 mt-1 pl-5">Multi-student collective. Up to HK$3,000 pooled claim.</p>
            </label>
          </div>

          <!-- Team Members & Split -->
          <div class="space-y-2 pt-2">
            <div class="flex justify-between items-center text-xs">
              <span class="font-bold text-slate-700">Team Members & Contribution Split</span>
              <span class="text-[10px] font-semibold text-teal-700">3 Members Enrolled (100% Total)</span>
            </div>

            <!-- Member 1 -->
            <div class="p-2.5 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between text-xs">
              <div class="flex items-center space-x-2">
                <div
                  class="w-7 h-7 rounded-full bg-slate-900 text-white font-bold flex items-center justify-center text-[10px]">
                  CW</div>
                <div>
                  <div class="font-bold text-slate-900">Chloe Wong
                    <span class="text-[10px] font-normal text-teal-700">(Lead / Submitter)</span></div>
                  <div class="text-[10px] text-slate-500">22048192D • BA Design (Interactive Media)</div>
                </div>
              </div>
              <div class="font-bold text-slate-900">40% Share</div>
            </div>

            <!-- Member 2 -->
            <div class="p-2.5 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between text-xs">
              <div class="flex items-center space-x-2">
                <div
                  class="w-7 h-7 rounded-full bg-slate-700 text-white font-bold flex items-center justify-center text-[10px]">
                  KL</div>
                <div>
                  <div class="font-bold text-slate-900">Ken Ka-Ho Leung</div>
                  <div class="text-[10px] text-slate-500">22051189D • BA Design (Product Design)</div>
                </div>
              </div>
              <div class="font-bold text-slate-900">30% Share</div>
            </div>

            <!-- Member 3 -->
            <div class="p-2.5 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between text-xs">
              <div class="flex items-center space-x-2">
                <div
                  class="w-7 h-7 rounded-full bg-slate-700 text-white font-bold flex items-center justify-center text-[10px]">
                  AC</div>
                <div>
                  <div class="font-bold text-slate-900">Anson Chun-Kit Chan</div>
                  <div class="text-[10px] text-slate-500">22039914D • BEng Electronic & Info Eng</div>
                </div>
              </div>
              <div class="font-bold text-slate-900">30% Share</div>
            </div>

            <button type="button" class="w-full py-2 border border-dashed border-slate-300 text-slate-600 hover:border-slate-400 rounded-xl text-xs font-semibold flex items-center justify-center space-x-1">
              <span>+ Add Teammate via PolyU Student NetID</span>
            </button>
          </div>

          <!-- Academic Origin -->
          <div class="pt-2 space-y-2">
            <label class="block text-xs font-bold text-slate-700">Academic Origin / Coursework Context <span class="text-rose-500">*</span></label>
            <div class="grid grid-cols-2 gap-3 text-xs">
              <label class="border-2 border-teal-600 bg-teal-50/20 p-2.5 rounded-xl cursor-pointer">
                <input type="radio" name="academic_origin" checked class="text-teal-600">
                <span class="font-bold text-slate-900 ml-1">Curricular / Studio Subject</span>
                <p class="text-[10px] text-slate-500 mt-1 pl-4">Developed in an approved credit-bearing design subject.</p>
              </label>
              <label class="border border-slate-200 p-2.5 rounded-xl cursor-pointer">
                <input type="radio" name="academic_origin" class="text-teal-600">
                <span class="font-bold text-slate-700 ml-1">Extracurricular / Independent</span>
                <p class="text-[10px] text-slate-500 mt-1 pl-4">Conducted outside formal class. Requires tutor endorsement.</p>
              </label>
            </div>
          </div>

          <div class="space-y-2 text-xs">
            <label class="font-medium text-slate-700">PolyU Subject Code & Title <span class="text-rose-500">*</span></label>
            <select class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium">
              <option selected>SD3102 — Design Studio III: Smart Living & Well-being (AY 2024/25 Sem 1)</option>
              <option>SD3101 — Interaction Design Fundamental</option>
              <option>SD4100 — Capstone Graduation Project</option>
            </select>
          </div>

          <div class="grid grid-cols-2 gap-3 text-xs">
            <div>
              <label class="font-medium text-slate-700">Subject Tutor / Studio Leader</label>
              <input type="text" value="Prof. Marcus Lee" readonly class="mt-1 w-full p-2 bg-slate-100 border border-slate-200 rounded-lg text-slate-700 font-medium">
            </div>
            <div>
              <label class="font-medium text-slate-700">Academic Term Completed</label>
              <input type="text" value="Semester 1, AY 2024/25" readonly class="mt-1 w-full p-2 bg-slate-100 border border-slate-200 rounded-lg text-slate-700 font-medium">
            </div>
          </div>
        </div>

        <!-- Project Profile & Metadata -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <h2 class="text-sm font-bold text-slate-900">Project Profile & Metadata</h2>
            <p class="text-xs text-slate-500">Key titles, discipline tags, and visual preview</p>
          </div>

          <div class="text-xs space-y-1">
            <label class="font-bold text-slate-700">Project Working Title <span class="text-rose-500">*</span></label>
            <input type="text" value="AuraRing: Haptic Spatial Guidance Ring for Visually Impaired Commuters" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium">
          </div>

          <div class="text-xs space-y-1.5">
            <label class="font-bold text-slate-700">Primary Design Disciplines (Multi-Select)</label>
            <div class="flex flex-wrap gap-1.5">
              <span class="px-2.5 py-1 bg-slate-900 text-white rounded-lg text-[11px] font-medium">Interaction & UI/UX ✓</span>
              <span class="px-2.5 py-1 bg-slate-900 text-white rounded-lg text-[11px] font-medium">Industrial & Product ✓</span>
              <span class="px-2.5 py-1 bg-slate-100 text-slate-700 rounded-lg text-[11px]">AI & Smart IoT</span>
              <span class="px-2.5 py-1 bg-slate-100 text-slate-700 rounded-lg text-[11px]">Healthcare & Social Innovation</span>
              <span class="px-2.5 py-1 bg-slate-100 text-slate-700 rounded-lg text-[11px]">Spatial & Environment</span>
            </div>
          </div>

          <div class="text-xs space-y-1">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700">Project Abstract / Executive Summary <span class="text-rose-500">*</span></label>
              <span class="text-[10px] text-slate-400">142 / 300 words</span>
            </div>
            <textarea rows="3" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 text-xs font-normal">AuraRing is a wearable assistive navigation interface tailored for low-vision urban navigators. By translating ultrasonic depth signals and real-time transit telemetry into micro-vibrational pulses across three phalanges, AuraRing provides intuitive, silent spatial orientation without obstructing ambient hearing or drawing unnecessary social stigma.</textarea>
          </div>

          <!-- Hero Upload Preview -->
          <div class="text-xs space-y-2">
            <label class="font-bold text-slate-700">Project Hero Render or Prototype Photo (1 Required)</label>
            <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between">
              <div class="flex items-center space-x-3">
                <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?w=100&auto=format&fit=crop&q=80" alt="Ring Render" class="w-12 h-12 object-cover rounded-lg border border-slate-300">
                <div>
                  <div class="font-bold text-slate-900">AuraRing_Render_Hero_v03.png</div>
                  <div class="text-[10px] text-slate-500">Uploaded 10 mins ago • 2400 x 1600 px • 3.8 MB</div>
                </div>
              </div>
              <div class="flex space-x-2">
                <button class="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-700 hover:bg-slate-50 text-[11px]">Replace</button>
                <button class="px-2.5 py-1 text-rose-600 hover:bg-rose-50 rounded text-[11px]">Remove</button>
              </div>
            </div>
          </div>

        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3">
          <div class="flex items-center space-x-1.5 text-xs font-bold text-slate-900 uppercase">
            <svg class="w-4 h-4 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zm-7-4a1 1 0 11-2 0 1 1 0 012 0zM9 9a1 1 0 000 2v3a1 1 0 001 1h1a1 1 0 100-2v-3a1 1 0 00-1-1H9z"
                clip-rule="evenodd" />
            </svg>
            <span>Rules & Guidelines</span>
          </div>

          <div class="space-y-2.5 text-xs">
            <div class="p-2.5 bg-slate-50 rounded-xl">
              <strong class="text-slate-900 block mb-0.5">Tier-Recognized Contests:</strong>
              <span class="text-slate-500 text-[11px]">Competitions must belong to Red Dot, iF Design, D&AD, Core77, or School Recognized Tier Lists.</span>
            </div>

            <div class="p-2.5 bg-slate-50 rounded-xl">
              <strong class="text-slate-900 block mb-0.5">Mandatory School Credit:</strong>
              <span class="text-slate-500 text-[11px]">Submissions must include "The Hong Kong Polytechnic University School of Design" in official credits.</span>
            </div>

            <div class="p-2.5 bg-slate-50 rounded-xl">
              <strong class="text-slate-900 block mb-0.5">Receipt Authenticity:</strong>
              <span class="text-slate-500 text-[11px]">Official payment invoices with currency conversion slips will be requested in Step 3.</span>
            </div>
          </div>
        </div>

        <div class="bg-teal-50/50 p-5 rounded-2xl border border-teal-200 space-y-2 text-xs">
          <div class="font-bold text-teal-900">REQUIRED FOR NEXT STEPS</div>
          <ul class="space-y-1.5 text-teal-800 text-[11px]">
            <li>• Official Competition Brief URL / PDF</li>
            <li>• Invoice or Entry Fee Schedule</li>
            <li>• Faculty Tutor Email for Digital Endorsement</li>
            <li>• Bank account details (for disbursement)</li>
          </ul>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-2')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Return to Dashboard</span>
      </button>
      <div class="flex items-center space-x-3">
        <button class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50">Save Draft</button>
        <!-- Nav to Step 2 -->
        <button id="btnStep1Next" onclick="showScreen('screen-4')" class="px-5 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold flex items-center space-x-2 shadow-sm">
          <span>Continue to Step 2: Competition</span>
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 4: Step 2: Competition Details & Tier Verification -->
  <!-- ========================================================================= -->
  <main id="screen-4" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Header -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">New Application</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">New Subsidy Application</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
          <span class="text-xs bg-amber-100 text-amber-800 font-bold px-2 py-0.5 rounded">TIER 1 INTERNATIONAL</span>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-xs">
        <span class="text-slate-500 flex items-center gap-1">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> Auto-saved just now • Ref:
        <strong class="text-slate-800">#SUB-2025-0892</strong>
        </span>
        <button class="px-3 py-1.5 bg-white border border-slate-300 rounded-lg font-semibold text-slate-700 hover:bg-slate-50">Save as Draft</button>
        <button onclick="showScreen('screen-2')" class="text-slate-400 hover:text-slate-600">✕</button>
      </div>
    </div>

    <!-- 3-Column Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">APPLICATION FLOW</span>
            <span class="font-extrabold text-teal-700">Step 2 of 5</span>
          </div>

          <nav class="space-y-3 text-xs">
            <div onclick="showScreen('screen-3')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">1. Academic & Project Info</div>
                <div class="text-[10px] text-emerald-600">Completed & Verified</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">2</span>
              <div>
                <div class="font-bold text-teal-900">2. Competition & Tier</div>
                <div class="text-[10px] text-teal-700">Currently Editing</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">3</span>
              <div>
                <div class="font-medium text-slate-600">3. Budget & Estimator</div>
                <div class="text-[10px]">Reimbursement caps</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">4</span>
              <div>
                <div class="font-medium text-slate-600">4. Faculty Endorsement</div>
                <div class="text-[10px]">Tutor sign-off</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">5</span>
              <div>
                <div class="font-medium text-slate-600">5. Review & Declaration</div>
                <div class="text-[10px]">Final declaration</div>
              </div>
            </div>
          </nav>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">ANNUAL QUOTA TRACKER</span>
            <span class="text-[10px] font-semibold text-teal-700">AY24/25</span>
          </div>
          <div class="text-xl font-black text-slate-900">HK$ 3,200
            <span class="text-xs font-normal text-slate-400">/ HK$ 5,000</span></div>
          <div class="w-full bg-slate-100 rounded-full h-1.5 mt-2 overflow-hidden">
            <div class="bg-teal-600 h-1.5 rounded-full" style="width: 64%"></div>
          </div>
          <p class="text-[11px] text-slate-500">Tier 1 Eligibility: This entry qualifies for up to 100% registration
            subsidy (capped at HK$1,500/claim).</p>
        </div>
      </div>

      <!-- Main Step 2 Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- 2.1 Competition Identification -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-3">
            <h2 class="text-sm font-bold text-slate-900 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-slate-900 text-white text-xs flex items-center justify-center font-bold">2.1</span>
              Competition Identification
            </h2>
            <span class="text-[10px] bg-emerald-50 text-emerald-700 font-bold px-2 py-0.5 rounded border border-emerald-200">✓ SD Pre-Approved</span>
          </div>

          <p class="text-xs text-slate-500">Select a recognized design award from the PolyU School of Design Registry or
            register an unlisted international brief.</p>

          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700">RECOGNIZED COMPETITION REGISTRY <span class="text-rose-500">*</span></label>
            <div class="relative">
              <select class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-900 font-bold">
                <option selected>🏆 Red Dot Award: Design Concept 2025</option>
                <option>iF Student Design Award 2025</option>
                <option>D&AD New Blood Awards 2025</option>
                <option>Core77 Design Awards 2025</option>
                <option>James Dyson Award 2025</option>
              </select>
            </div>
          </div>

          <!-- Metadata Pillbox -->
          <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl space-y-2 text-xs">
            <div class="flex justify-between items-center text-[11px] text-slate-500">
              <span>REGISTRY STATUS: <strong class="text-slate-800">Verified International Tier 1 (ID: RD-CON-25)</strong></span>
              <a href="https://www.red-dot.org/design-concept" target="_blank"
                class="text-teal-700 font-semibold hover:underline">Visit Portal ↗</a>
            </div>
            <div class="grid grid-cols-2 gap-3 pt-1">
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Organizing Body</span>
                <div class="font-bold text-slate-800">Design Zentrum Nordrhein Westfalen</div>
              </div>
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Country / Jurisdiction</span>
                <div class="font-bold text-slate-800">Germany • International</div>
              </div>
            </div>
            <div class="pt-1">
              <span class="text-[10px] text-slate-400 uppercase font-semibold">Official Submission URL</span>
              <div class="flex items-center space-x-2 mt-0.5">
                <input type="text" value="https://www.red-dot.org/design-concept" readonly class="w-full p-1.5 bg-white border border-slate-200 rounded text-slate-700 text-xs">
                <button class="px-2.5 py-1.5 bg-slate-200 rounded text-slate-700 hover:bg-slate-300 text-xs font-semibold shrink-0">Test Link</button>
              </div>
            </div>
          </div>
        </div>

        <!-- 2.2 Tier Verification & Scope -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="border-b border-slate-100 pb-2">
            <h2 class="text-sm font-bold text-slate-900 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-slate-900 text-white text-xs flex items-center justify-center font-bold">2.2</span>
              Tier Verification & Scope
            </h2>
            <p class="text-xs text-slate-500 mt-0.5">The subsidy reimbursement percentage is pegged directly to the
              verified competition recognition level.</p>
          </div>

          <div class="space-y-3">
            <!-- Tier 1 -->
            <label class="block p-3 rounded-xl border-2 border-teal-600 bg-teal-50/20 cursor-pointer">
              <div class="flex items-center justify-between">
                <div class="flex items-center space-x-2">
                  <input type="radio" name="comp_tier" checked class="text-teal-600">
                  <span class="font-bold text-xs text-slate-900">Tier 1 • International Prestigious</span>
                  <span class="text-[10px] bg-teal-600 text-white font-bold px-1.5 py-0.5 rounded">AUTO-MATCHED</span>
                </div>
                <span class="font-bold text-xs text-teal-800">Up to 100% (HK$1,500)</span>
              </div>
              <p class="text-[11px] text-slate-600 mt-1 pl-5">Red Dot, iF Design, D&AD, IDEA, Core77, James Dyson Award. Highly prestigious global competitions recognized by PolyU SD Research & Executive Board.</p>
            </label>

            <!-- Tier 2 -->
            <label class="block p-3 rounded-xl border border-slate-200 hover:border-slate-300 cursor-pointer">
              <div class="flex items-center justify-between">
                <div class="flex items-center space-x-2">
                  <input type="radio" name="comp_tier" class="text-teal-600">
                  <span class="font-bold text-xs text-slate-700">Tier 2 • International & Regional Specialized</span>
                </div>
                <span class="font-bold text-xs text-slate-700">Up to 70% (HK$1,000)</span>
              </div>
              <p class="text-[11px] text-slate-500 mt-1 pl-5">K-Design Award, Golden Pin, Good Design Award (Japan/Australia), regional biennial design awards.</p>
            </label>

            <!-- Tier 3 -->
            <label class="block p-3 rounded-xl border border-slate-200 hover:border-slate-300 cursor-pointer">
              <div class="flex items-center justify-between">
                <div class="flex items-center space-x-2">
                  <input type="radio" name="comp_tier" class="text-teal-600">
                  <span class="font-bold text-xs text-slate-700">Tier 3 • Local & Institutional (Hong Kong)</span>
                </div>
                <span class="font-bold text-xs text-slate-700">Up to 50% (HK$800)</span>
              </div>
              <p class="text-[11px] text-slate-500 mt-1 pl-5">HKDA Global Design Awards, Hong Kong Smart Design Awards, local professional institute competitions.</p>
            </label>
          </div>

          <div class="grid grid-cols-2 gap-4 text-xs pt-2">
            <div>
              <label class="font-bold text-slate-700">Submission Category in Competition <span class="text-rose-500">*</span></label>
              <input type="text" value="Interaction & Communication Design / Smart Product" class="mt-1 w-full p-2 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium">
            </div>
            <div>
              <label class="font-bold text-slate-700">Participant Category Level <span class="text-rose-500">*</span></label>
              <div class="flex space-x-4 mt-2">
                <label class="flex items-center space-x-1 cursor-pointer">
                  <input type="radio" name="part_level" checked class="text-teal-600">
                  <span class="text-slate-800 font-semibold">Student / Junior Concept</span>
                </label>
                <label class="flex items-center space-x-1 cursor-pointer">
                  <input type="radio" name="part_level" class="text-teal-600">
                  <span class="text-slate-600">Professional / Open</span>
                </label>
              </div>
            </div>
          </div>
        </div>

        <!-- 2.3 Milestone Dates & Regulations -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="border-b border-slate-100 pb-2">
            <h2 class="text-sm font-bold text-slate-900 flex items-center gap-2">
              <span class="w-6 h-6 rounded-full bg-slate-900 text-white text-xs flex items-center justify-center font-bold">2.3</span>
              Milestone Dates & Regulations
            </h2>
            <p class="text-xs text-slate-500 mt-0.5">Reimbursement eligibility strictly requires advance application
              prior to the official organizer deadline.</p>
          </div>

          <div class="grid grid-cols-2 gap-4 text-xs">
            <div>
              <label class="font-bold text-slate-700">OFFICIAL SUBMISSION DEADLINE <span class="text-rose-500">*</span></label>
              <div class="relative mt-1">
                <input type="text" value="April 24, 2025 (Standard)" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium">
              </div>
              <span class="text-[10px] text-emerald-600 font-bold mt-1 block">✓ Submitted 32 days in advance (compliant)</span>
            </div>
            <div>
              <label class="font-bold text-slate-700">RESULTS / WINNER ANNOUNCEMENT DATE <span class="text-rose-500">*</span></label>
              <div class="relative mt-1">
                <input type="text" value="July 09, 2025" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium">
              </div>
              <span class="text-[10px] text-slate-400 mt-1 block">Final results must be submitted for claim release</span>
            </div>
          </div>

          <!-- Call for Entries Brief Upload -->
          <div class="space-y-2 text-xs pt-2">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700">OFFICIAL CALL FOR ENTRIES BRIEF / FEE SCHEDULE <span class="text-rose-500">*</span></label>
              <span class="text-[10px] text-slate-400">PDF, JPG, PNG • Max 10MB</span>
            </div>
            <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between">
              <div class="flex items-center space-x-3">
                <span class="w-9 h-9 rounded-lg bg-rose-100 text-rose-700 font-bold flex items-center justify-center text-xs">PDF</span>
                <div>
                  <div class="font-bold text-slate-900">RedDot_DesignConcept_2025_EntryGuide.pdf</div>
                  <div class="text-[10px] text-slate-500">2.4 MB • Uploaded & Scanned for Deadlines</div>
                </div>
              </div>
              <div class="flex space-x-2">
                <button class="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-700 hover:bg-slate-50 text-[11px]">View</button>
                <button class="px-2.5 py-1 text-slate-600 hover:bg-slate-100 rounded text-[11px]">Replace</button>
              </div>
            </div>
          </div>

          <!-- Crediting Agreement Checkbox -->
          <div class="p-3 bg-slate-50 rounded-xl border border-slate-200 flex items-start space-x-3 text-xs">
            <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
            <div>
              <strong class="text-slate-900">Mandatory School Affiliation Credit Agreement</strong>
              <p class="text-[11px] text-slate-600 mt-0.5">I confirm that our team's official entry credits, exhibition
                panels, and digital submission forms will prominently include:
                <strong>"School of Design, The Hong Kong Polytechnic University"</strong>. Reimbursement claims will be
                voided if school crediting is absent from the final certificate or publication.</p>
            </div>
          </div>
        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3">
          <div class="flex items-center space-x-1.5 text-xs font-bold text-slate-900 uppercase">
            <svg class="w-4 h-4 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                clip-rule="evenodd" />
            </svg>
            <span>Tier 1 Benefits</span>
          </div>
          <p class="text-xs text-slate-600">Red Dot Concept is classified as a top-tier international milestone award by
            PolyU SD.</p>
          <ul class="space-y-1.5 text-xs text-slate-600">
            <li class="flex items-start gap-1.5">✓
              <span>100% reimbursement on official entry fees (up to HK$1,500)</span></li>
            <li class="flex items-start gap-1.5">✓
              <span>Eligible for prototype logistics grant if nominated/shortlisted</span></li>
            <li class="flex items-start gap-1.5">✓ <span>Automatic feature on PolyU Design Annual Showcase portal</span>
            </li>
          </ul>
        </div>

        <div class="p-4 bg-amber-50/70 border border-amber-200 rounded-2xl text-xs space-y-1 text-amber-900">
          <div class="font-bold flex items-center gap-1">
            <span>⏱️</span> 14-Day Advance Rule
          </div>
          <p class="text-[11px] text-amber-800">Applications must be endorsed by the Studio Lead at least
            <strong>14 working days</strong> prior to the official fee transaction. Retrospective applications after
            competition close are not permitted.</p>
          <div class="text-[10px] font-bold text-emerald-700 pt-1">● Current Status: Compliant (32 Days)</div>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="text-[10px] font-bold text-slate-400 uppercase">REQUIRED CREDITING</div>
          <p class="text-[11px] text-slate-500">Use this exact wording when submitting your team profile and project
            sheets:</p>
          <div class="p-2.5 bg-slate-100 rounded-lg text-slate-800 text-[11px] font-mono select-all">
            Chloe Wong, BA (Hons) in Design, School of Design, The Hong Kong Polytechnic University
          </div>
          <button class="text-[11px] text-teal-700 font-bold hover:underline">Copy Wording</button>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-3')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Back to Step 1</span>
      </button>
      <div class="flex items-center space-x-3">
        <button class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50">Save Draft</button>
        <!-- Nav to Step 3 -->
        <button id="btnStep2Next" onclick="showScreen('screen-5')" class="px-5 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold flex items-center space-x-2 shadow-sm">
          <span>Continue to Step 3</span>
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 5: Step 3: Budget & Claim Estimator -->
  <!-- ========================================================================= -->
  <main id="screen-5" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Header -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">New Application</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">New Subsidy Application</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
          <span class="text-xs bg-teal-100 text-teal-800 font-bold px-2 py-0.5 rounded">TIER 1 INTERNATIONAL</span>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-xs">
        <span class="text-slate-500 flex items-center gap-1">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> Auto-saved just now • Ref:
        <strong class="text-slate-800">#SUB-2025-0892</strong>
        </span>
        <button class="px-3 py-1.5 bg-white border border-slate-300 rounded-lg font-semibold text-slate-700 hover:bg-slate-50">Save as Draft</button>
        <button onclick="showScreen('screen-2')" class="text-slate-400 hover:text-slate-600">✕</button>
      </div>
    </div>

    <!-- 3-Column Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">APPLICATION FLOW</span>
            <span class="font-extrabold text-teal-700">Step 3 of 5 (60%)</span>
          </div>

          <nav class="space-y-3 text-xs">
            <div onclick="showScreen('screen-3')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">1. Academic Info</div>
                <div class="text-[10px] text-emerald-600">Verified NetID Profile</div>
              </div>
            </div>

            <div onclick="showScreen('screen-4')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">2. Competition & Tier</div>
                <div class="text-[10px] text-emerald-600">Red Dot Design (Tier 1)</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">3</span>
              <div>
                <div class="font-bold text-teal-900">3. Budget & Estimator</div>
                <div class="text-[10px] text-teal-700">Currently Editing</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">4</span>
              <div>
                <div class="font-medium text-slate-600">4. Faculty Sign-off</div>
                <div class="text-[10px]">Studio tutor review</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">5</span>
              <div>
                <div class="font-medium text-slate-600">5. Review & Declaration</div>
                <div class="text-[10px]">Formal e-signature</div>
              </div>
            </div>
          </nav>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">ANNUAL QUOTA TRACKER</span>
            <span class="text-[10px] font-semibold text-slate-400">AY24/25</span>
          </div>
          <div class="text-xl font-black text-slate-900">HK$ 3,200
            <span class="text-xs font-normal text-slate-400">/ HK$ 5,000</span></div>
          <div class="pt-2 text-xs space-y-1 text-slate-600 border-t border-slate-100">
            <div class="flex justify-between"><span>Requested Claim Grant:</span>
              <strong class="text-emerald-700">+HK$ 1,500</strong></div>
            <div class="flex justify-between"><span>Projected Remaining:</span>
              <strong class="text-slate-900">HK$ 1,700</strong></div>
          </div>
        </div>
      </div>

      <!-- Main Step 3 Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- 3.1 Expense Itemization -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-3">
            <h2 class="text-sm font-bold text-slate-900">3.1 Expense Itemization</h2>
            <span class="text-[10px] bg-slate-100 text-slate-700 font-bold px-2 py-0.5 rounded">Live Calculations</span>
          </div>
          <p class="text-xs text-slate-500">Specify eligible competition expenditures. Only direct registration fees,
            submission entry charges, and physical prototype packaging/shipping qualify for SD Scheme claims.</p>

          <!-- Expense 1: Entry Fee -->
          <div class="p-4 bg-slate-50 border border-slate-200 rounded-xl space-y-3">
            <div class="flex justify-between items-center">
              <div class="flex items-center space-x-2">
                <span class="w-5 h-5 rounded-full bg-slate-900 text-white text-[10px] font-bold flex items-center justify-center">1</span>
                <div>
                  <strong class="text-xs text-slate-900">Standard Entry Fee (Red Dot: Design Concept)</strong>
                  <div class="text-[10px] text-slate-500">CATEGORY: ENTRY / REGISTRATION FEE</div>
                </div>
              </div>
              <span class="text-[10px] bg-teal-100 text-teal-800 font-bold px-2 py-0.5 rounded">100% ELIGIBLE</span>
            </div>

            <div class="grid grid-cols-3 gap-3 text-xs bg-white p-3 rounded-lg border border-slate-200">
              <div>
                <label class="text-[10px] text-slate-400 uppercase font-semibold">Invoice Currency & Amount</label>
                <div class="flex items-center space-x-1 mt-0.5">
                  <span class="font-bold text-slate-700">EUR €</span>
                  <input type="text" value="450.00" class="w-full font-bold text-slate-900 p-1 border border-slate-200 rounded">
                </div>
              </div>
              <div>
                <label class="text-[10px] text-slate-400 uppercase font-semibold">PolyU Pegged Rate</label>
                <div class="text-slate-700 mt-1.5 font-medium">1 EUR = <strong class="text-slate-900">HK$ 8.42</strong>
                </div>
              </div>
              <div>
                <label class="text-[10px] text-slate-400 uppercase font-semibold">HKD Gross Equivalent</label>
                <div class="text-base font-black text-teal-800 mt-0.5">HK$ 3,789.00</div>
              </div>
            </div>

            <!-- Upload Quote File -->
            <div class="flex items-center justify-between text-xs p-2 bg-white rounded border border-slate-200">
              <div class="flex items-center space-x-2">
                <span class="text-rose-600 font-bold text-[10px]">PDF</span>
                <span class="font-medium text-slate-800">RedDot_Invoice_Quote_2025.pdf</span>
                <span class="text-[10px] text-slate-400">• 1.2 MB • Uploaded & OCR verified</span>
              </div>
              <button class="text-[11px] text-teal-700 font-bold hover:underline">View</button>
            </div>

            <div class="flex justify-between items-center text-[11px] pt-1 text-slate-500">
              <span>ⓘ Capped at standard individual ceiling: Max HK$1,500.00</span>
              <span class="font-bold text-slate-800">Claimable: <span class="text-teal-700">HK$ 1,500.00</span></span>
            </div>
          </div>

          <!-- Expense 2: Prototype Shipping -->
          <div class="p-4 bg-slate-50 border border-slate-200 rounded-xl space-y-3">
            <div class="flex justify-between items-center">
              <div class="flex items-center space-x-2">
                <span class="w-5 h-5 rounded-full bg-slate-400 text-white text-[10px] font-bold flex items-center justify-center">2</span>
                <div>
                  <strong class="text-xs text-slate-700">Courier & Physical Prototype Shipping (to Essen, Germany)</strong>
                  <div class="text-[10px] text-slate-400">CATEGORY: PHYSICAL MOCKUP / PROTOTYPE FREIGHT</div>
                </div>
              </div>
              <span class="text-[10px] bg-amber-100 text-amber-800 font-bold px-2 py-0.5 rounded">OPTIONAL / POST-SHORTLIST</span>
            </div>

            <div class="grid grid-cols-2 gap-3 text-xs bg-white p-3 rounded-lg border border-slate-200">
              <div>
                <label class="text-[10px] text-slate-400 uppercase font-semibold">Estimated Shipping Cost</label>
                <div class="flex items-center space-x-1 mt-0.5">
                  <span class="font-bold text-slate-700">HKD $</span>
                  <input type="text" value="680.00" class="w-full font-bold text-slate-900 p-1 border border-slate-200 rounded">
                </div>
              </div>
              <div class="text-[10px] text-slate-500 flex items-center">
                Provisional item. Eligible for secondary claims round if your entry passes first jury shortlist.
              </div>
            </div>

            <div class="text-right">
              <button class="text-[11px] text-rose-600 hover:underline">Remove Item</button>
            </div>
          </div>

          <button class="w-full py-2 border border-dashed border-slate-300 rounded-xl text-xs font-semibold text-slate-600 hover:border-slate-400 flex items-center justify-center space-x-1">
            <span>+ Add Another Eligible Expense Item</span>
          </button>
        </div>

        <!-- 3.2 Real-Time Subsidy Calculator -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <h2 class="text-sm font-bold text-slate-900">3.2 Real-Time Subsidy Calculator</h2>
            <span class="text-[10px] font-bold text-teal-700 uppercase">AUTOMATED FORMULA</span>
          </div>

          <div class="space-y-2 text-xs">
            <div class="flex justify-between py-1 border-b border-slate-100">
              <span class="text-slate-600">Total Gross Project Expenditure:</span>
              <span class="font-bold text-slate-900">HK$ 3,789.00</span>
            </div>
            <div class="flex justify-between py-1 border-b border-slate-100">
              <span class="text-slate-600">Tier 1 Match Rate (Design Concept): <strong class="text-teal-700 font-semibold">100%</strong></span>
              <span class="font-bold text-slate-900">HK$ 3,789.00</span>
            </div>
            <div class="flex justify-between py-1 border-b border-slate-100 text-rose-600">
              <span>School of Design Individual Cap: <span class="text-[10px] text-slate-400">(Per Entry Maximum Allowance)</span></span>
              <span class="font-bold">- HK$ 2,289.00 (Exceeds Cap)</span>
            </div>
            <div class="flex justify-between py-1 border-b border-slate-100">
              <span class="text-slate-600">Available Annual Quota:</span>
              <span class="font-medium text-slate-800">HK$ 3,200.00 (Sufficient)</span>
            </div>

            <!-- Net Subsidy Highlight Box -->
            <div class="p-4 bg-teal-50 border border-teal-200 rounded-xl flex justify-between items-center mt-3">
              <div>
                <div class="text-[10px] font-bold text-teal-800 uppercase tracking-wider">NET SUBSIDY TO BE DISBURSED
                </div>
                <div class="text-[11px] text-teal-700">Direct credit upon proof of submission receipt</div>
              </div>
              <div class="text-2xl font-black text-teal-900">HK$ 1,500.00</div>
            </div>

            <div class="flex justify-between items-center text-[11px] text-slate-500 pt-1">
              <span>Student Out-of-Pocket Balance:</span>
              <span class="font-bold text-slate-700">HK$ 2,289.00</span>
            </div>
          </div>

          <div class="p-3 bg-amber-50/60 rounded-xl border border-amber-200/50 text-[11px] text-amber-900">
            <strong>SD Regulation Clause 4.2.1:</strong> Under School of Design Regulations 2024/25: Individual
            applications for Tier 1 international competitions are capped at HK$1,500 per approved entry. Co-funding or
            supplementary studio material grants may be requested through Subject Tutor endorsement in Step 4.
          </div>
        </div>

        <!-- 3.3 Disbursement & Auto-Pay Details -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <h2 class="text-sm font-bold text-slate-900">3.3 Disbursement & Auto-Pay Details</h2>
            <span class="text-slate-400 text-xs">🔒</span>
          </div>
          <p class="text-xs text-slate-500">Funds are remitted via the PolyU Student Auto-pay Direct Credit System.
            Information is retrieved from your PolyU SIS single sign-on profile.</p>

          <div class="p-4 bg-slate-50 rounded-xl border border-slate-200 space-y-3 text-xs">
            <div class="flex justify-between items-center">
              <span class="text-[10px] font-bold text-slate-500 uppercase">POLYU AUTO-PAY / FPS PROFILE</span>
              <span class="text-[10px] font-semibold text-emerald-700 bg-emerald-50 px-2 py-0.5 rounded border border-emerald-200">✓ Verified SIS Record</span>
            </div>

            <div class="grid grid-cols-2 gap-3">
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Designated Bank</span>
                <div class="font-bold text-slate-800">HSBC (Hongkong and Shanghai Banking Corp)</div>
              </div>
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Account Holder Name</span>
                <div class="font-bold text-slate-800">Chloe Wong 🔒</div>
              </div>
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Bank & Account Number</span>
                <div class="font-bold font-mono text-slate-800">004 - 821-394821-833</div>
              </div>
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Registered FPS Mobile ID</span>
                <div class="font-bold font-mono text-slate-800">+852 9482 ••••</div>
              </div>
            </div>

            <div class="text-[11px] text-slate-500 pt-1">
              ⏱️ Estimated reimbursement turnaround: 14 working days following final faculty endorsement & finance
              office audit.
            </div>
          </div>

          <label class="flex items-start space-x-2 text-xs text-slate-600 cursor-pointer">
            <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
            <span>I confirm that the bank account above is active and solely held under my registered student identity (<strong>NetID 22048192D</strong>). I understand that incorrect banking records will delay grant issuance.</span>
          </label>
        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="font-bold text-slate-900 uppercase">Subsidy Ceiling Rules</div>
          <p class="text-slate-500 text-[11px]">Annual cap is HK$5,000 per academic year per student across all
            competitive submissions.</p>

          <div class="space-y-2 border-t border-slate-100 pt-2">
            <div class="flex justify-between items-center">
              <div>
                <div class="font-bold text-slate-800">Tier 1 International</div>
                <div class="text-[10px] text-slate-400">Red Dot, iF, IDEA, D&AD</div>
              </div>
              <div class="text-right font-black text-teal-800">HK$ 1,500 <div
                  class="text-[9px] font-normal text-slate-400">PER ENTRY</div>
              </div>
            </div>

            <div class="flex justify-between items-center">
              <div>
                <div class="font-bold text-slate-800">Tier 2 Regional</div>
                <div class="text-[10px] text-slate-400">Good Design (G-Mark), K-Design</div>
              </div>
              <div class="text-right font-bold text-slate-800">HK$ 1,000 <div
                  class="text-[9px] font-normal text-slate-400">PER ENTRY</div>
              </div>
            </div>

            <div class="flex justify-between items-center">
              <div>
                <div class="font-bold text-slate-800">Tier 3 Local HK</div>
                <div class="text-[10px] text-slate-400">HKDA Global Design Awards</div>
              </div>
              <div class="text-right font-bold text-slate-800">HK$ 600 <div
                  class="text-[9px] font-normal text-slate-400">PER ENTRY</div>
              </div>
            </div>
          </div>
          <div class="text-[11px] text-slate-500 pt-1">
            <strong>Collaborative Projects:</strong> Pooled maximum HK$3,000 per entry split proportionally among PolyU
            co-authors.
          </div>
        </div>

        <!-- Exchange Rates Box -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2 text-xs">
          <div class="flex justify-between items-center">
            <span class="font-bold text-slate-900 uppercase">Official Pegged Rates</span>
            <span class="text-[10px] text-slate-400">Q1 2025</span>
          </div>
          <p class="text-slate-500 text-[11px]">Standard quarterly exchange rates established by the PolyU Finance
            Office:</p>
          <div class="grid grid-cols-2 gap-2 text-slate-700 text-[11px] font-mono">
            <div class="p-1.5 bg-slate-50 rounded">1 EUR = <strong>8.42 HKD</strong></div>
            <div class="p-1.5 bg-slate-50 rounded">1 USD = <strong>7.82 HKD</strong></div>
            <div class="p-1.5 bg-slate-50 rounded">1 GBP = <strong>9.95 HKD</strong></div>
            <div class="p-1.5 bg-slate-50 rounded">100 JPY = <strong>5.20 HKD</strong></div>
          </div>
          <div class="text-[10px] text-slate-400">Updated quarterly by PolyU Bursar.</div>
        </div>

        <div class="bg-teal-50/50 p-5 rounded-2xl border border-teal-200 space-y-2 text-xs">
          <div class="font-bold text-teal-900 uppercase">Audit Requirements</div>
          <ul class="space-y-1.5 text-teal-800 text-[11px]">
            <li class="flex items-start gap-1">✓
              <span>Must display official organizer: <strong>Design Zentrum Nordrhein Westfalen</strong>.</span></li>
            <li class="flex items-start gap-1">✓ <span>Must state student name or approved project design code.</span>
            </li>
            <li class="flex items-start gap-1">✓ <span>Proof of debit must show timestamp and masked card digits.</span>
            </li>
          </ul>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-4')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Back to Step 2: Competition</span>
      </button>
      <div class="flex items-center space-x-3">
        <span class="text-xs text-slate-500 hidden sm:inline">Claim Estimated: <strong class="text-slate-900">HK$ 1,500.00</strong> (Draft #SUB-2025-0892)</span>
        <!-- Nav to Step 4 -->
        <button id="btnStep3Next" onclick="showScreen('screen-6')" class="px-5 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold flex items-center space-x-2 shadow-sm">
          <span>Continue to Step 4: Faculty Endorsement</span>
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 6: Step 4: Faculty Endorsement -->
  <!-- ========================================================================= -->
  <main id="screen-6" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Header -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">New Application</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">New Subsidy Application</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
          <span class="text-xs bg-amber-100 text-amber-800 font-bold px-2 py-0.5 rounded">TIER 1 INTERNATIONAL</span>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-xs">
        <span class="text-slate-500 flex items-center gap-1">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> Auto-saved just now • Ref:
        <strong class="text-slate-800">#SUB-2025-0892</strong>
        </span>
        <button class="px-3 py-1.5 bg-white border border-slate-300 rounded-lg font-semibold text-slate-700 hover:bg-slate-50">Save as Draft</button>
        <button onclick="showScreen('screen-2')" class="text-slate-400 hover:text-slate-600">✕</button>
      </div>
    </div>

    <!-- 3-Column Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">STEP 4 OF 5</span>
            <span class="font-extrabold text-teal-700">80% Complete</span>
          </div>

          <nav class="space-y-3 text-xs">
            <div onclick="showScreen('screen-3')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">1. Academic Info</div>
                <div class="text-[10px] text-emerald-600">Verified NetID Profile</div>
              </div>
            </div>

            <div onclick="showScreen('screen-4')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">2. Competition & Tier</div>
                <div class="text-[10px] text-emerald-600">Red Dot Award (Tier 1)</div>
              </div>
            </div>

            <div onclick="showScreen('screen-5')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">3. Budget & Estimator</div>
                <div class="text-[10px] text-emerald-600">Capped at HK$1,500</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">4</span>
              <div>
                <div class="font-bold text-teal-900">4. Faculty Sign-off</div>
                <div class="text-[10px] text-teal-700">Currently Editing</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">5</span>
              <div>
                <div class="font-medium text-slate-600">5. Review & Declaration</div>
                <div class="text-[10px]">Formal e-signature</div>
              </div>
            </div>
          </nav>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">ANNUAL QUOTA TRACKER</span>
            <span class="text-[10px] font-semibold text-slate-400">AY 24/25</span>
          </div>
          <div class="text-xl font-black text-slate-900">HK$ 3,200
            <span class="text-xs font-normal text-slate-400">of HK$ 5,000</span></div>
          <div class="pt-2 text-xs space-y-1 text-slate-600 border-t border-slate-100">
            <div class="flex justify-between"><span>This Application Claim:</span>
              <strong class="text-emerald-700">+HK$ 1,500</strong></div>
            <div class="flex justify-between"><span>Projected Remaining:</span>
              <strong class="text-slate-900">HK$ 1,700</strong></div>
          </div>
        </div>
      </div>

      <!-- Main Step 4 Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- Section 4.1 Designated Faculty Endorser -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <div class="flex items-center space-x-2 text-[10px] font-bold text-teal-700 uppercase tracking-wider">
              <span>SECTION 4.1</span>
              <span>•</span>
              <span>ACADEMIC OVERSIGHT</span>
            </div>
            <h2 class="text-base font-bold text-slate-900 mt-1">Designated Faculty Endorser</h2>
            <p class="text-xs text-slate-500 mt-0.5">Every student competition submission requires academic endorsement
              by an active studio tutor, subject leader, or discipline coordinator.</p>
          </div>

          <!-- Endorser Profile Card -->
          <div class="p-4 bg-slate-50 border border-slate-200 rounded-2xl space-y-3">
            <div class="flex items-start justify-between">
              <div class="flex items-center space-x-3">
                <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&auto=format&fit=crop&q=80" alt="Prof Marcus Lee" class="w-12 h-12 rounded-xl object-cover border border-slate-300">
                <div>
                  <h3 class="font-bold text-sm text-slate-900">Prof. Marcus Lee (李銘教授)</h3>
                  <div class="text-xs text-slate-600 font-medium">Studio Tutor & Associate Professor, School of Design
                  </div>
                  <div class="text-[11px] text-slate-400">marcus.lee@polyu.edu.hk • Office: V812 Jockey Club Innovation
                    Tower</div>
                </div>
              </div>
              <span class="text-[10px] bg-teal-100 text-teal-800 font-bold px-2 py-0.5 rounded">✓ Matched from Step 1</span>
            </div>

            <div class="grid grid-cols-2 gap-3 text-xs pt-2 border-t border-slate-200">
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Academic Cluster</span>
                <div class="font-bold text-slate-800">Information & Interaction Design</div>
              </div>
              <div>
                <span class="text-[10px] text-slate-400 uppercase font-semibold">Associated Subject</span>
                <div class="font-bold text-slate-800">SD3102 — Design Studio III: Smart Living</div>
              </div>
            </div>
          </div>

          <!-- Channel Selection -->
          <div class="space-y-2 pt-1 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">Select Endorsement Channel</label>
            <div class="space-y-2">
              <label class="flex items-start space-x-2 p-3 bg-teal-50/20 border border-teal-600 rounded-xl cursor-pointer">
                <input type="radio" name="endorsement_channel" checked class="mt-0.5 text-teal-600">
                <div>
                  <strong class="text-slate-900">Studio Subject Leader (Prof. Marcus Lee - Recommended)</strong>
                  <p class="text-[11px] text-slate-500 mt-0.5">Primary studio instructor overseeing submitted prototype.</p>
                </div>
              </label>
              <label class="flex items-start space-x-2 p-3 border border-slate-200 rounded-xl cursor-pointer hover:border-slate-300">
                <input type="radio" name="endorsement_channel" class="mt-0.5 text-teal-600">
                <div>
                  <strong class="text-slate-700">Programme Leader / Scheme Director (Dr. Wendy Kwan)</strong>
                  <p class="text-[11px] text-slate-500 mt-0.5">Direct escalation for multidisciplinary or self-initiated entries.</p>
                </div>
              </label>
              <label class="flex items-start space-x-2 p-3 border border-slate-200 rounded-xl cursor-pointer hover:border-slate-300">
                <input type="radio" name="endorsement_channel" class="mt-0.5 text-teal-600">
                <div>
                  <strong class="text-slate-700">Search Directory / Other Faculty Member</strong>
                  <p class="text-[11px] text-slate-500 mt-0.5">Designate an affiliated co-supervisor, visiting fellow, or lab lead.</p>
                </div>
              </label>
            </div>
          </div>
        </div>

        <!-- Section 4.2 Academic Merit & Project Context -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <div class="flex items-center space-x-2 text-[10px] font-bold text-teal-700 uppercase tracking-wider">
              <span>SECTION 4.2</span>
              <span>•</span>
              <span>CONTEXT DOSSIER</span>
            </div>
            <h2 class="text-base font-bold text-slate-900 mt-1">Academic Merit & Project Context</h2>
          </div>

          <div
            class="p-3 bg-slate-50 rounded-xl border border-slate-200 text-xs text-slate-600 flex items-start space-x-2">
            <span class="text-teal-600 font-bold">ⓘ</span>
            <span>Note for Prof. Marcus Lee: The following summary dossier will be dispatched with your automated review request.</span>
          </div>

          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">Relevance to Curricular Learning Outcomes</label>
            <div class="flex flex-wrap gap-2">
              <span class="px-2.5 py-1 bg-slate-900 text-white rounded-lg text-xs font-semibold">✓ Core Studio Output [SD3102]</span>
              <span class="px-2.5 py-1 bg-slate-100 text-slate-700 rounded-lg text-xs">Graduation Capstone Exploration</span>
              <span class="px-2.5 py-1 bg-slate-100 text-slate-700 rounded-lg text-xs">Extracurricular Research Innovation</span>
            </div>
          </div>

          <div class="space-y-1 text-xs">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700 uppercase text-[10px]">Student Statement to Endorser / Academic Justification <span class="text-rose-500">*</span></label>
              <span class="text-[10px] text-slate-400">184 / 500 characters</span>
            </div>
            <textarea rows="4" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 text-xs">This entry adapts our haptic accessibility interface developed during SD3102 into an international benchmark design concept, representing PolyU SD's human-centered technology ethos at Red Dot 2025.</textarea>
            <p class="text-[10px] text-slate-400">Briefly explain how this competition entry advances your academic
              research or design practice at PolyU SD.</p>
          </div>

          <label class="flex items-start space-x-2 text-xs text-slate-600 cursor-pointer pt-2">
            <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
            <div>
              <strong class="text-slate-900">Intellectual Property & PolyU Affiliation Confirmation</strong>
              <p class="text-[11px] text-slate-500 mt-0.5">Project was conceived and executed using PolyU School of Design studio facilities and adheres to the PolyU IP Policy for Student Works.</p>
            </div>
          </label>
        </div>

        <!-- Section 4.3 Endorsement Routing & SLA Timeline -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <div class="flex items-center space-x-2 text-[10px] font-bold text-teal-700 uppercase tracking-wider">
              <span>SECTION 4.3</span>
              <span>•</span>
              <span>ROUTING MECHANICS</span>
            </div>
            <h2 class="text-base font-bold text-slate-900 mt-1">Endorsement Routing & SLA Timeline</h2>
          </div>

          <div class="grid grid-cols-4 gap-2 text-center text-xs">
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <span class="text-[9px] font-bold text-slate-400 uppercase">STAGE 1</span>
              <div class="font-bold text-slate-800 mt-0.5">Dispatched</div>
              <div class="text-[9px] text-slate-500">Upon Step 5 final e-submission</div>
            </div>
            <div class="p-2.5 bg-teal-50 rounded-xl border border-teal-200">
              <span class="text-[9px] font-bold text-teal-700 uppercase">STAGE 2</span>
              <div class="font-bold text-teal-900 mt-0.5">Review SLA</div>
              <div class="text-[9px] text-teal-700">5 Working Days (Staff Portal & Outlook)</div>
            </div>
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <span class="text-[9px] font-bold text-slate-400 uppercase">STAGE 3</span>
              <div class="font-bold text-slate-800 mt-0.5">Endorsement</div>
              <div class="text-[9px] text-slate-500">1-Click sign via PolyU CAS</div>
            </div>
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <span class="text-[9px] font-bold text-slate-400 uppercase">STAGE 4</span>
              <div class="font-bold text-slate-800 mt-0.5">Finance Office</div>
              <div class="text-[9px] text-slate-500">Instant grant fund lock</div>
            </div>
          </div>

          <div class="flex justify-between items-center text-xs p-3 bg-slate-50 rounded-xl">
            <div class="flex items-center space-x-2">
              <span class="text-teal-600 font-bold">🔔</span>
              <div>
                <span class="font-bold text-slate-800">Automated Chaser Ping</span>
                <p class="text-[10px] text-slate-500">Send reminder nudge via Outlook if unreviewed after 72 hours.</p>
              </div>
            </div>
            <label class="relative inline-flex items-center cursor-pointer">
              <input type="checkbox" checked class="sr-only peer">
              <div class="w-9 h-5 bg-slate-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-slate-300 after:border after:rounded-full after:h-4 after:w-4 after:transition-all peer-checked:bg-teal-600"></div>
            </label>
          </div>

          <button class="w-full py-2 border border-dashed border-slate-300 rounded-xl text-xs font-semibold text-slate-600 hover:border-slate-400 flex items-center justify-center space-x-1">
            <span>+ Add Secondary Endorser (Optional Co-Instructor / Lab Specialist)</span>
          </button>
        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="font-bold text-slate-900 uppercase">Faculty Evaluation Criteria</div>
          <ul class="space-y-2 text-slate-600 text-[11px]">
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-800">Direct Academic Relevance:</strong> Work aligns with PolyU SD
                pedagogical standards.</div>
            </li>
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-800">Authentic Authorship:</strong> Validated individual or team
                contribution share.</div>
            </li>
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-800">Tier Standing:</strong> Fits designated Tier 1 international
                competition scope.</div>
            </li>
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-800">Affiliation Crediting:</strong> PolyU School of Design strictly
                verified.</div>
            </li>
          </ul>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="text-[10px] font-bold text-slate-400 uppercase">FACULTY SLA & DEADLINES</div>
          <div class="p-3 bg-slate-50 rounded-xl space-y-1">
            <div class="font-bold text-slate-800">Target Endorsement Cutoff</div>
            <div class="text-sm font-extrabold text-teal-800">April 10, 2025</div>
            <div class="text-[10px] text-slate-500">14 days prior to Red Dot deadline of April 24, 2025.</div>
          </div>
          <div class="flex justify-between items-center text-[11px]">
            <span class="text-slate-500">Review Buffer:</span>
            <span class="font-bold text-emerald-700">10 working days available</span>
          </div>
          <div class="p-2.5 bg-rose-50 border border-rose-200 rounded-xl text-[11px] text-rose-800">
            ⚠️ Late applications without faculty endorsement before deadline cannot be subsidized retrospectively.
          </div>
        </div>

        <!-- Staff Portal Preview -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2 text-xs">
          <div class="flex justify-between items-center text-[10px] font-bold text-slate-400 uppercase">
            <span>STAFF PORTAL PREVIEW</span>
            <span>👁️</span>
          </div>
          <p class="text-slate-500 text-[11px]">See how your application dossier, attached materials, and justification
            will render inside the faculty dashboard.</p>
          <div
            class="p-2 bg-slate-100 rounded-lg border border-slate-200 text-center text-[10px] text-slate-400 font-mono">
            [Staff Review Interface Simulation]
          </div>
          <button class="w-full py-1.5 bg-slate-50 hover:bg-slate-100 border border-slate-200 rounded-lg text-slate-700 font-semibold text-[11px]">Preview Staff View Modal ↗</button>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-5')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Back to Step 3: Budget & Estimator</span>
      </button>
      <div class="flex items-center space-x-3">
        <span class="text-xs text-slate-500 hidden sm:inline">Faculty Review Target: <strong class="text-slate-900">Prof. Marcus Lee</strong> • SLA: 5 Working Days</span>
        <!-- Nav to Step 5 -->
        <button id="btnStep4Next" onclick="showScreen('screen-7')" class="px-5 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold flex items-center space-x-2 shadow-sm">
          <span>Continue to Step 5: Review & Declaration</span>
          <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 7: Step 5: Review & Declaration -->
  <!-- ========================================================================= -->
  <main id="screen-7" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Header -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">New Application</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">New Subsidy Application</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
          <span class="text-xs bg-amber-100 text-amber-800 font-bold px-2 py-0.5 rounded">TIER 1 INTERNATIONAL</span>
        </div>
      </div>
      <div class="flex items-center space-x-3 text-xs">
        <span class="text-slate-500 flex items-center gap-1">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> Auto-saved just now • Ref:
        <strong class="text-slate-800">#SUB-2025-0892</strong>
        </span>
        <button class="px-3 py-1.5 bg-white border border-slate-300 rounded-lg font-semibold text-slate-700 hover:bg-slate-50">Save as Draft</button>
        <button onclick="showScreen('screen-2')" class="text-slate-400 hover:text-slate-600">✕</button>
      </div>
    </div>

    <!-- 3-Column Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">STEP 5 OF 5</span>
            <span class="font-extrabold text-teal-700">100% Complete</span>
          </div>

          <nav class="space-y-3 text-xs">
            <div onclick="showScreen('screen-3')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">1. Academic & Project</div>
                <div class="text-[10px] text-emerald-600">AuraRing • 3 Members</div>
              </div>
            </div>

            <div onclick="showScreen('screen-4')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">2. Competition & Tier</div>
                <div class="text-[10px] text-emerald-600">Red Dot Award (Tier 1)</div>
              </div>
            </div>

            <div onclick="showScreen('screen-5')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">3. Budget & Estimator</div>
                <div class="text-[10px] text-emerald-600">Capped at HK$1,500</div>
              </div>
            </div>

            <div onclick="showScreen('screen-6')"
              class="flex items-start space-x-3 p-2 text-slate-700 cursor-pointer hover:bg-slate-50 rounded-xl">
              <span class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0">✓</span>
              <div>
                <div class="font-semibold">4. Faculty Sign-off</div>
                <div class="text-[10px] text-emerald-600">Prof. Marcus Lee</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">5</span>
              <div>
                <div class="font-bold text-teal-900">5. Review & Declaration</div>
                <div class="text-[10px] text-teal-700">ACTIVE • SIGN-OFF</div>
              </div>
            </div>
          </nav>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500">ANNUAL QUOTA TRACKER</span>
            <span class="text-[10px] font-semibold text-slate-400">AY 24/25</span>
          </div>
          <div class="text-xl font-black text-slate-900">HK$ 3,200
            <span class="text-xs font-normal text-slate-400">of HK$ 5,000 cap</span></div>
          <div class="pt-2 text-xs space-y-1 text-slate-600 border-t border-slate-100">
            <div class="flex justify-between"><span>This Application Claim:</span>
              <strong class="text-emerald-700">+HK$ 1,500.00</strong></div>
            <div class="flex justify-between"><span>Projected Remaining:</span>
              <strong class="text-slate-900">HK$ 1,700.00</strong></div>
          </div>
        </div>
      </div>

      <!-- Main Step 5 Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- Section 5.1 Application Summary Dossier -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 5.1</span>
              <h2 class="text-base font-bold text-slate-900">Application Summary Dossier</h2>
            </div>
            <span class="text-[10px] bg-emerald-50 text-emerald-800 font-bold px-2 py-0.5 rounded border border-emerald-200">AUDIT CHECK PASSED</span>
          </div>
          <p class="text-xs text-slate-500">Please inspect each section before executing your student legal undertaking.
            Click 'Edit' on any module to adjust parameters.</p>

          <!-- Module A: Academic & Project Info -->
          <div class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 space-y-2 text-xs">
            <div class="flex justify-between items-center">
              <span class="font-bold text-slate-900 flex items-center gap-1.5"><span class="w-4 h-4 rounded bg-slate-900 text-white text-[9px] flex items-center justify-center">A</span>
              Academic & Project Info</span>
              <button onclick="showScreen('screen-3')" class="text-teal-700 font-bold text-[11px] hover:underline">Edit</button>
            </div>
            <div class="grid grid-cols-2 gap-2 text-[11px] pt-1">
              <div><span class="text-slate-400">Principal Applicant:</span>
                <strong class="text-slate-800 block">Chloe Wong (22048192D)</strong></div>
              <div><span class="text-slate-400">Registered Coursework:</span>
                <strong class="text-slate-800 block">SD3102 Design Studio III</strong></div>
            </div>
            <div class="text-[11px] pt-1">
              <span class="text-slate-400">Project Title:</span>
              <strong class="text-slate-800 block">AuraRing: Haptic Spatial Guidance Ring</strong>
            </div>
            <div class="text-[10px] text-slate-500 pt-1 flex gap-2">
              <span>Split: Chloe Wong (40%), Ken Leung (30%), Anson Chan (30%)</span>
            </div>
          </div>

          <!-- Module B: Competition & Tier -->
          <div class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 space-y-2 text-xs">
            <div class="flex justify-between items-center">
              <span class="font-bold text-slate-900 flex items-center gap-1.5"><span class="w-4 h-4 rounded bg-slate-900 text-white text-[9px] flex items-center justify-center">B</span>
              Competition & Tier Verification</span>
              <button onclick="showScreen('screen-4')" class="text-teal-700 font-bold text-[11px] hover:underline">Edit</button>
            </div>
            <div class="grid grid-cols-2 gap-2 text-[11px] pt-1">
              <div><span class="text-slate-400">Event:</span>
                <strong class="text-slate-800 block">Red Dot Award: Design Concept 2025</strong></div>
              <div><span class="text-slate-400">Recognition Tier:</span>
                <strong class="text-teal-800 block">Tier 1 • 100% Eligible</strong></div>
            </div>
            <div class="grid grid-cols-2 gap-2 text-[11px] pt-1">
              <div><span class="text-slate-400">Submission Deadline:</span>
                <span class="text-slate-800 font-medium block">April 24, 2025 (32 days advance)</span></div>
              <div><span class="text-slate-400">Discipline Field:</span>
                <span class="text-slate-800 font-medium block">Interaction & Communication</span></div>
            </div>
          </div>

          <!-- Module C: Budget & Disbursement Summary -->
          <div class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 space-y-2 text-xs">
            <div class="flex justify-between items-center">
              <span class="font-bold text-slate-900 flex items-center gap-1.5"><span class="w-4 h-4 rounded bg-slate-900 text-white text-[9px] flex items-center justify-center">C</span>
              Budget & Disbursement Summary</span>
              <button onclick="showScreen('screen-5')" class="text-teal-700 font-bold text-[11px] hover:underline">Edit</button>
            </div>
            <div class="grid grid-cols-2 gap-2 text-[11px] pt-1">
              <div><span class="text-slate-400">Gross Registration Entry Fee:</span>
                <strong class="text-slate-800 block">EUR €450.00 (Pegged HK$ 3,789.00)</strong></div>
              <div><span class="text-slate-400">PolyU SD Tier 1 Individual Grant Ceiling:</span>
                <strong class="text-slate-800 block">HK$ 1,500.00</strong></div>
            </div>
            <div class="p-2.5 bg-teal-50 border border-teal-200 rounded-lg flex justify-between items-center mt-2">
              <div>
                <span class="text-[9px] font-bold text-teal-800 uppercase">Net Grant to be Reserved & Disbursed</span>
                <div class="text-[10px] text-teal-700">Payable upon post-competition receipt validation</div>
              </div>
              <span class="text-base font-black text-teal-900">HK$ 1,500.00</span>
            </div>
          </div>

          <!-- Module D: Endorsement Routing -->
          <div class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 space-y-1 text-xs">
            <div class="flex justify-between items-center">
              <span class="font-bold text-slate-900 flex items-center gap-1.5"><span class="w-4 h-4 rounded bg-slate-900 text-white text-[9px] flex items-center justify-center">D</span>
              Endorsement Routing</span>
              <button onclick="showScreen('screen-6')" class="text-teal-700 font-bold text-[11px] hover:underline">Edit</button>
            </div>
            <div class="flex items-center justify-between pt-1 text-[11px]">
              <div>
                <strong class="text-slate-800">Prof. Marcus Lee</strong>
                <span class="text-slate-500"> — Subject Lecturer SD3102</span>
              </div>
              <span class="text-[10px] bg-slate-200 text-slate-700 px-2 py-0.5 rounded font-semibold">5 Working Days SLA</span>
            </div>
          </div>
        </div>

        <!-- Section 5.2 Terms, Legal Undertakings & Student Declarations -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 5.2</span>
            <h2 class="text-base font-bold text-slate-900">Terms, Legal Undertakings & Student Declarations</h2>
            <p class="text-xs text-slate-500 mt-0.5">You must carefully review and affirm each statutory clause. All
              declarations are legally binding under the PolyU Student Code of Conduct.</p>
          </div>

          <div class="space-y-3 text-xs">
            <label class="flex items-start space-x-2.5 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
              <div>
                <strong class="text-slate-900">1. Affiliation & Crediting Undertaking</strong>
                <p class="text-[11px] text-slate-600 mt-0.5">I declare that all official competition submissions, public exhibition materials, and PR releases prominently credit <strong>"School of Design, The Hong Kong Polytechnic University"</strong> in strict accordance with the PolyU Brand Identity Guidelines.</p>
              </div>
            </label>

            <label class="flex items-start space-x-2.5 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
              <div>
                <strong class="text-slate-900">2. Originality & Intellectual Property Authorship</strong>
                <p class="text-[11px] text-slate-600 mt-0.5">I certify that the submitted project is an original creative work authored exclusively by the declared student team and does not infringe any third-party intellectual property, patent, or copyright.</p>
              </div>
            </label>

            <label class="flex items-start space-x-2.5 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
              <div>
                <strong class="text-slate-900">3. No Dual-Funding / Single Claim Certification</strong>
                <p class="text-[11px] text-slate-600 mt-0.5">I confirm that this project entry has not received full financial sponsorship from external corporate partners or concurrent university subsidy schemes covering the same registration fees.</p>
              </div>
            </label>

            <label class="flex items-start space-x-2.5 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
              <div>
                <strong class="text-slate-900">4. Mandatory Post-Competition Reporting & Archive (Clause 5.4)</strong>
                <p class="text-[11px] text-slate-600 mt-0.5">I undertake to submit the official competition result notification, certificates, and proof of participation to this portal within <strong>30 calendar days</strong> of official announcement.</p>
              </div>
            </label>

            <label class="flex items-start space-x-2.5 p-3 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer">
              <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
              <div>
                <strong class="text-slate-900">5. Receipt Authenticity & Disciplinary Accountability</strong>
                <p class="text-[11px] text-slate-600 mt-0.5">I understand that funding disbursement is contingent upon submitting authentic official payment receipts and bank transaction proofs. False claims will result in immediate grant revocation, full clawback, and formal university disciplinary proceedings.</p>
              </div>
            </label>
          </div>
        </div>

        <!-- Section 5.3 Formal E-Signature & Authentication -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div>
            <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 5.3</span>
            <h2 class="text-base font-bold text-slate-900">Formal E-Signature & Authentication</h2>
            <p class="text-xs text-slate-500 mt-0.5">Type your full legal name as it appears on your PolyU Student
              Identity Card to digitally sign this document.</p>
          </div>

          <div class="grid grid-cols-2 gap-4 text-xs">
            <div>
              <label class="font-bold text-slate-700 uppercase text-[10px]">Full Legal Name (Digital Signature) <span class="text-rose-500">*</span></label>
              <input type="text" value="Chloe Wong" class="mt-1 w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-900 font-bold">
              <span class="text-[10px] text-teal-700 mt-1 block">Affirms authority to sign on behalf of team</span>
            </div>
            <div>
              <label class="font-bold text-slate-700 uppercase text-[10px]">PolyU Student NetID (Verified SSO)</label>
              <input type="text" value="22048192D" readonly class="mt-1 w-full p-2.5 bg-slate-100 border border-slate-200 rounded-lg text-slate-700 font-mono font-bold">
              <span class="text-[10px] text-slate-400 mt-1 block">Locked to logged-in session account</span>
            </div>
          </div>

          <div class="p-3 bg-slate-50 rounded-xl border border-slate-200 flex justify-between items-center text-xs">
            <div>
              <div class="text-[10px] font-bold text-slate-400 uppercase">DIGITAL AUDIT STAMP</div>
              <div class="font-mono text-slate-700 text-[11px] mt-0.5">Timestamp:
                <span id="currentTimestamp">2025-04-12 14:32:08 HKT</span> • Generated upon submission</div>
            </div>
            <span class="text-[10px] bg-slate-200 text-slate-700 font-bold px-2 py-1 rounded">SHA256 SECURED</span>
          </div>

          <div
            class="p-3 bg-teal-50 border border-teal-100 rounded-xl text-[11px] text-teal-800 flex items-start space-x-2">
            <span class="text-teal-600 font-bold">ⓘ</span>
            <span>By clicking <strong>"Submit Subsidy Application"</strong>, you legally bind this electronic dossier under PolyU Academic Policy and authorize the School of Design to process this grant application.</span>
          </div>
        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="font-bold text-slate-900 uppercase">Submission Checklist</div>
          <ul class="space-y-1.5 text-[11px] text-slate-600">
            <li class="flex items-center gap-1.5 text-emerald-700 font-semibold">✓ Academic Info Completed</li>
            <li class="flex items-center gap-1.5 text-emerald-700 font-semibold">✓ Tier 1 Verification Matched</li>
            <li class="flex items-center gap-1.5 text-emerald-700 font-semibold">✓ Budget & Cap Calculated</li>
            <li class="flex items-center gap-1.5 text-emerald-700 font-semibold">✓ Faculty Assignee Endorsed</li>
          </ul>
        </div>

        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="text-[10px] font-bold text-slate-400 uppercase">NEXT STEPS</div>
          <div class="font-bold text-slate-900">What Happens Next?</div>
          <ol class="space-y-2 text-[11px] text-slate-600 list-decimal pl-4">
            <li><strong>Instant Receipt:</strong> Acknowledgment sent to chloe.wong@connect.polyu.hk</li>
            <li><strong>Faculty Endorsement:</strong> Prof. Marcus Lee evaluates (5 working days SLA)</li>
            <li><strong>SD Finance Audit:</strong> Reservation of HK$1,500.00 grant quota</li>
            <li><strong>Post-Award Disbursement:</strong> Direct credit after proof upload</li>
          </ol>
        </div>

        <div class="p-4 bg-amber-50/70 border border-amber-200 rounded-2xl text-xs space-y-1 text-amber-900">
          <div class="font-bold flex items-center gap-1">🔒 Submission Lock Policy</div>
          <p class="text-[11px] text-amber-800">Once submitted, your application fields cannot be altered without an
            administrative unlock request to the SD Academic Secretariat.</p>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-6')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Back to Step 4: Faculty Endorsement</span>
      </button>
      <div class="flex items-center space-x-3">
        <span class="text-xs text-slate-500 hidden sm:inline">All 5 Sections Verified & Ready for Sign-off</span>
        <button class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50">Save Draft & Exit</button>
        <!-- Per Prompt: press "Submit Subsidy Application" to submit the application and return to Screen 1 -->
        <button id="btnSubmitToScreen1" onclick="submitApplicationToScreen1()" class="px-6 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-bold flex items-center space-x-2 shadow-lg transition transform hover:-translate-y-0.5">
          <span>Submit Subsidy Application</span>
          <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 8: Competition Result Reporting & Showcase Submission Form -->
  <!-- ========================================================================= -->
  <main id="screen-8" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Header Banner -->
    <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 border-b border-slate-200 pb-4">
      <div>
        <div class="flex items-center space-x-2 text-xs text-slate-500 mb-1">
          <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
          <span>/</span>
          <span>Subsidies</span>
          <span>/</span>
          <span>#SUB-2025-0892</span>
          <span>/</span>
          <span class="font-semibold text-slate-800">Competition Result Reporting</span>
        </div>
        <div class="flex items-center space-x-3">
          <h1 class="text-2xl font-black text-slate-900">Competition Result Reporting & Showcase Archive</h1>
          <span class="text-xs bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded border border-teal-200">AY 2024/25 SCHEME</span>
          <span class="text-xs bg-rose-50 text-rose-800 font-bold px-2 py-0.5 rounded border border-rose-200">★ RED DOT: DESIGN CONCEPT</span>
        </div>
        <p class="text-xs text-slate-500 mt-1">Official filing for project
          <strong>AuraRing: Haptic Spatial Guidance Ring</strong>. Submitting validated certification unlocks the
          Faculty Dean's Archive endorsement and initiates the final <strong>HK$1,500.00</strong> subsidy disbursement
          audit.</p>
      </div>

      <div class="flex items-center space-x-3 text-xs shrink-0">
        <div class="text-right">
          <span class="text-[10px] text-slate-400 uppercase font-semibold">GRANT APPROVED</span>
          <div class="text-lg font-black text-slate-900">HK$ 1,500.00</div>
          <span class="text-[10px] text-teal-700 font-medium">● Claim Release Pending Result</span>
        </div>
      </div>
    </div>

    <!-- Alert / Clause 5.4 notice -->
    <div
      class="p-3 bg-teal-50/70 border border-teal-200 rounded-xl flex items-center justify-between text-xs text-teal-900">
      <div class="flex items-center space-x-2">
        <span class="font-bold">CLAUSE 5.4 PROTOCOL:</span>
        <span>30-Day Mandatory Reporting Window: <strong>18 Days Remaining</strong> (Strict Deadline: August 8, 2025 • 23:59 HKT)</span>
      </div>
      <span class="text-[11px] text-teal-700 font-medium">Draft auto-saved 2 mins ago</span>
    </div>

    <!-- 3-Column Layout -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Stepper Left Nav (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center text-xs">
            <span class="font-bold text-slate-500 uppercase">VERIFICATION STEPS</span>
            <span class="font-extrabold text-teal-700">2 of 4 Active</span>
          </div>

          <nav class="space-y-3 text-xs">
            <div class="flex items-start space-x-3 p-2 bg-teal-50/50 rounded-xl border border-teal-200">
              <span class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0">1</span>
              <div>
                <div class="font-bold text-teal-900">1. Official Standing</div>
                <div class="text-[10px] text-teal-700">Winner Confirmed</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 bg-slate-50 rounded-xl border border-slate-200">
              <span class="w-6 h-6 rounded-full bg-slate-900 text-white font-bold flex items-center justify-center shrink-0">2</span>
              <div>
                <div class="font-bold text-slate-900">2. Proof & Credentials</div>
                <div class="text-[10px] text-slate-500">Certificate Uploaded</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">3</span>
              <div>
                <div class="font-medium text-slate-600">3. Showcase Media</div>
                <div class="text-[10px]">High-Res Render & PR</div>
              </div>
            </div>

            <div class="flex items-start space-x-3 p-2 text-slate-400">
              <span class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0">4</span>
              <div>
                <div class="font-medium text-slate-600">4. Sign & Release</div>
                <div class="text-[10px]">Audit Endorsement</div>
              </div>
            </div>
          </nav>
        </div>

        <!-- Project Meta Card -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2 text-xs">
          <div class="flex justify-between items-center">
            <span class="font-bold text-slate-400 uppercase text-[10px]">SUBSIDIZED PROJECT</span>
            <span class="text-[10px] font-mono text-slate-500">TEAM ID: 0892</span>
          </div>
          <div class="font-bold text-slate-900 text-sm">AuraRing: Haptic Spatial Guidance Ring</div>
          <div class="text-[11px] text-slate-500">PolyU School of Design • Interaction Design Lab</div>

          <div class="pt-2 border-t border-slate-100 space-y-1 text-[11px]">
            <div><strong class="text-slate-800">Team Members:</strong> Chloe Wong (Lead, 22048192D), Ken Ka-Ho Leung
              (22051189D), Anson Chun-Kit Chan (220399010D)</div>
            <div><strong class="text-slate-800">Academic Advisor:</strong> Prof. Marcus Lee (Associate Professor)</div>
          </div>
          <a href="#" class="text-[11px] text-teal-700 font-bold block pt-1 hover:underline">View Initial Pre-Approval
            Form ↗</a>
        </div>

        <div class="p-4 bg-teal-50/50 rounded-2xl border border-teal-200 text-xs space-y-1">
          <div class="font-bold text-teal-900 flex items-center gap-1">🛡️ Clause 5.4 Archiving</div>
          <p class="text-[11px] text-teal-800">All award recipients must archive high-resolution visual evidence with
            PolyU Design Communications within 30 calendar days to finalize financial reimbursement ledger
            reconciliation.</p>
          <a href="#" class="text-[11px] text-teal-700 font-bold hover:underline block pt-1">Download Showcase Spec
            Guide (PDF)</a>
        </div>
      </div>

      <!-- Main Step Form (6 Cols) -->
      <div class="lg:col-span-6 space-y-6">

        <!-- SECTION 01: Official Competition Outcome -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 01</span>
              <h2 class="text-base font-bold text-slate-900">Official Competition Outcome</h2>
            </div>
            <span class="text-[10px] bg-slate-100 text-slate-700 font-bold px-2 py-0.5 rounded">STAGE 1 OF 4</span>
          </div>

          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">OFFICIAL AWARD STANDING <span class="text-rose-500">*</span></label>
            <div class="grid grid-cols-3 gap-2">
              <label class="p-3 border-2 border-teal-600 bg-teal-50/30 rounded-xl cursor-pointer">
                <div class="flex justify-between items-center">
                  <span class="text-xs font-bold text-slate-900">Winner / Awardee</span>
                  <span class="w-3.5 h-3.5 rounded-full bg-teal-600 text-white flex items-center justify-center text-[9px]">✓</span>
                </div>
                <p class="text-[10px] text-slate-600 mt-1">Awarded Grand Prize, Winner, or Honorable Mention.</p>
              </label>
              <label class="p-3 border border-slate-200 rounded-xl cursor-pointer hover:border-slate-300">
                <div class="flex justify-between items-center">
                  <span class="text-xs font-bold text-slate-700">Finalist / Shortlisted</span>
                  <span class="w-3.5 h-3.5 rounded-full border border-slate-300"></span>
                </div>
                <p class="text-[10px] text-slate-400 mt-1">Selected for final round / nominee catalog.</p>
              </label>
              <label class="p-3 border border-slate-200 rounded-xl cursor-pointer hover:border-slate-300">
                <div class="flex justify-between items-center">
                  <span class="text-xs font-bold text-slate-700">Participant Only</span>
                  <span class="w-3.5 h-3.5 rounded-full border border-slate-300"></span>
                </div>
                <p class="text-[10px] text-slate-400 mt-1">Entry completed with official submission proof.</p>
              </label>
            </div>
          </div>

          <div class="text-xs space-y-1">
            <label class="font-bold text-slate-700 uppercase text-[10px]">OFFICIAL AWARD TITLE & CATEGORY <span class="text-rose-500">*</span></label>
            <input type="text" value="Red Dot Award: Winner — Design Concept 2025 (Category: Interaction & Telecommunications)" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-900 font-bold">
            <span class="text-[10px] text-slate-400">Please match the verbatim text listed on your official diploma or winner plaque.</span>
          </div>

          <div class="grid grid-cols-2 gap-3 text-xs">
            <div>
              <label class="font-bold text-slate-700 uppercase text-[10px]">Official Announcement Date <span class="text-rose-500">*</span></label>
              <input type="text" value="July 09, 2025" class="mt-1 w-full p-2 bg-slate-50 border border-slate-300 rounded-lg font-medium text-slate-800">
            </div>
            <div>
              <div class="flex justify-between items-center">
                <label class="font-bold text-slate-700 uppercase text-[10px]">Winner Directory URL <span class="text-rose-500">*</span></label>
                <a href="#" class="text-[10px] text-teal-700 font-semibold hover:underline">Verify Live ↗</a>
              </div>
              <input type="text" value="https://www.red-dot.org/project/auraring-2025-winner" class="mt-1 w-full p-2 bg-slate-50 border border-slate-300 rounded-lg font-medium text-slate-800">
            </div>
          </div>

          <div class="space-y-1 text-xs">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700 uppercase text-[10px]">Official Jury Citation / Evaluator Feedback</label>
              <span class="text-[10px] text-slate-400">Excerpt from Red Dot Yearbook</span>
            </div>
            <textarea rows="3" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 text-xs">"The jury recognized AuraRing for its subtle tactile guidance language and seamless inclusive integration for urban accessibility. Its ergonomic nuance and micro-haptic feedback demonstrate extraordinary user-centered discipline."</textarea>
          </div>
        </div>

        <!-- SECTION 02: Evidentiary Documentation & Certificate -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 02</span>
              <h2 class="text-base font-bold text-slate-900">Evidentiary Documentation & Certificate</h2>
            </div>
            <span class="text-[10px] bg-slate-100 text-slate-700 font-bold px-2 py-0.5 rounded">STAGE 2 OF 4</span>
          </div>

          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">OFFICIAL AWARD CERTIFICATE OR RESULT CONFIRMATION LETTER <span class="text-rose-500">*</span></label>
            <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between">
              <div class="flex items-center space-x-3">
                <span class="w-9 h-9 rounded-lg bg-rose-100 text-rose-700 font-bold flex items-center justify-center text-xs">PDF</span>
                <div>
                  <div class="font-bold text-slate-900 flex items-center gap-1.5">
                    <span>RedDot_2025_Winner_Certificate_AuraRing.pdf</span>
                    <span class="text-[9px] bg-emerald-100 text-emerald-800 font-bold px-1.5 py-0.5 rounded">✓ Validated PDF</span>
                  </div>
                  <div class="text-[10px] text-slate-500">3.4 MB • Uploaded July 21, 2025 at 14:32 • SHA-256 Checksum
                    Verified</div>
                </div>
              </div>
              <div class="flex space-x-2">
                <button class="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-700 hover:bg-slate-50 text-[11px]">View</button>
                <button class="px-2.5 py-1 bg-white border border-slate-200 rounded text-slate-700 hover:bg-slate-50 text-[11px]">Replace</button>
              </div>
            </div>
          </div>

          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">Secondary Verification (Official Yearbook Page / Acceptance Email)</label>
            <div class="p-3 bg-slate-50 border border-slate-200 rounded-xl flex items-center justify-between">
              <div class="flex items-center space-x-3">
                <span class="w-9 h-9 rounded-lg bg-sky-100 text-sky-700 font-bold flex items-center justify-center text-xs">IMG</span>
                <div>
                  <div class="font-bold text-slate-900">RedDot_OnlineExhibition_AuraRing_Page.pdf</div>
                  <div class="text-[10px] text-slate-500">1.8 MB • Online Catalog Screenshot & Metadata</div>
                </div>
              </div>
              <button class="text-[11px] text-rose-600 hover:underline">Remove</button>
            </div>
          </div>

          <div class="p-3 bg-teal-50/60 rounded-xl border border-teal-200 flex items-start space-x-3 text-xs">
            <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
            <div>
              <div class="flex items-center space-x-2">
                <strong class="text-teal-950">PolyU Affiliation Compliance Verified</strong>
                <span class="text-[9px] bg-teal-200 text-teal-900 font-bold px-1.5 py-0.2 rounded">CLAUSE 1 CERTIFIED</span>
              </div>
              <p class="text-[11px] text-teal-800 mt-0.5">I confirm that the submitted competition diploma, catalog
                listing, and media materials visibly attribute institution credit as
                <strong>"School of Design, The Hong Kong Polytechnic University"</strong> as mandated by the subsidy
                covenant.</p>
            </div>
          </div>
        </div>

        <!-- SECTION 03: Showcase Archive & PR Package -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 03</span>
              <h2 class="text-base font-bold text-slate-900">Showcase Archive & PR Package</h2>
            </div>
            <span class="text-[10px] bg-slate-100 text-slate-700 font-bold px-2 py-0.5 rounded">STAGE 3 OF 4</span>
          </div>

          <div class="flex justify-between items-center p-3 bg-slate-50 rounded-xl text-xs">
            <div>
              <div class="font-bold text-slate-800">Public Exhibition & Social PR Authorization</div>
              <div class="text-[10px] text-slate-500">Authorize School of Design Communications & PR to feature AuraRing
                in the PolyU Annual Showcase 2025 and university press releases.</div>
            </div>
            <label class="relative inline-flex items-center cursor-pointer">
              <input type="checkbox" checked class="sr-only peer">
              <div class="w-9 h-5 bg-slate-200 peer-focus:outline-none rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-slate-300 after:border after:rounded-full after:h-4 after:w-4 after:transition-all peer-checked:bg-teal-600"></div>
            </label>
          </div>

          <!-- Hero Render Upload -->
          <div class="space-y-2 text-xs">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700 uppercase text-[10px]">EXHIBITION HERO RENDER (PRINT READY 300 DPI) <span class="text-rose-500">*</span></label>
              <span class="text-[10px] text-slate-400">Min. 3000 x 2000px</span>
            </div>
            <div class="relative rounded-xl overflow-hidden border border-slate-200 bg-slate-900">
              <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?w=800&auto=format&fit=crop&q=80" alt="AuraRing Hero" class="w-full h-44 object-cover opacity-85">
              <div
                class="absolute bottom-0 inset-x-0 p-3 bg-gradient-to-t from-slate-950/90 to-transparent flex justify-between items-end text-white text-xs">
                <div>
                  <div class="font-bold">AuraRing_Exhibition_Hero_300dpi.png</div>
                  <div class="text-[10px] text-slate-300">4000 x 2500 px • 6.2 MB • CMYK Color Profile</div>
                </div>
                <span class="text-[10px] bg-teal-600 text-white font-bold px-2 py-0.5 rounded">HERO KEY VISUAL</span>
              </div>
            </div>
          </div>

          <!-- Prototype photos grid -->
          <div class="space-y-2 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">Supplementary Prototype & Process Photos (Max 5 Files)</label>
            <div class="grid grid-cols-3 gap-2">
              <div class="relative rounded-lg overflow-hidden border border-slate-200 bg-slate-100 h-20">
                <img src="https://images.unsplash.com/photo-1581092160607-ee22621dd758?w=300&auto=format&fit=crop&q=80" alt="PCB Macro" class="w-full h-full object-cover">
                <span class="absolute bottom-1 left-1 bg-slate-900/80 text-white text-[9px] px-1 rounded">PCB_Macro.jpg</span>
              </div>
              <div class="relative rounded-lg overflow-hidden border border-slate-200 bg-slate-100 h-20">
                <img src="https://images.unsplash.com/photo-1576091160399-112ba8d25d1d?w=300&auto=format&fit=crop&q=80" alt="Context" class="w-full h-full object-cover">
                <span class="absolute bottom-1 left-1 bg-slate-900/80 text-white text-[9px] px-1 rounded">Context_01.jpg</span>
              </div>
              <div
                class="rounded-lg border-2 border-dashed border-slate-300 hover:border-slate-400 h-20 flex flex-col items-center justify-center text-slate-500 cursor-pointer text-[10px]">
                <span>+ ADD IMAGE</span>
              </div>
            </div>
          </div>

          <div class="space-y-1 text-xs">
            <label class="font-bold text-slate-700 uppercase text-[10px]">Video Demonstration URL (Vimeo / YouTube / OneDrive)</label>
            <div class="flex items-center space-x-2">
              <input type="text" value="https://vimeo.com/polyudesign/auraring-spatial-concept-2025" class="w-full p-2 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 font-medium text-xs">
              <button class="px-2.5 py-2 bg-slate-200 rounded text-slate-700 hover:bg-slate-300 text-xs font-semibold shrink-0">
                <svg class="w-4 h-4 text-slate-700" fill="currentColor" viewBox="0 0 20 20"><path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd"/></svg>
              </button>
            </div>
          </div>

          <div class="space-y-1 text-xs">
            <div class="flex justify-between items-center">
              <label class="font-bold text-slate-700 uppercase text-[10px]">Exhibition Booklet Abstract (English, Max 120 Words) <span class="text-rose-500">*</span></label>
              <span class="text-[10px] text-teal-700 font-semibold">94 / 120 words</span>
            </div>
            <textarea rows="3" class="w-full p-2.5 bg-slate-50 border border-slate-300 rounded-lg text-slate-800 text-xs leading-relaxed">AuraRing reimagines micro-navigation for individuals navigating dense architectural transit hubs. By translating complex spatial vectors into continuous rotational haptic pulses, the ring eliminates phone-screen distraction and auditory fatigue. Engineered with lightweight biometric silicone and recycled grade-5 titanium, AuraRing delivers an unobtrusive user experience recognized by the Red Dot Jury for defining future inclusive product ergonomics.</textarea>
          </div>
        </div>

        <!-- SECTION 04: Audit Release Declaration -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <span class="text-[10px] font-bold text-teal-700 uppercase">SECTION 04</span>
              <h2 class="text-base font-bold text-slate-900">Audit Release Declaration</h2>
            </div>
            <span class="text-[10px] bg-slate-100 text-slate-700 font-bold px-2 py-0.5 rounded">FINAL STEP</span>
          </div>

          <label class="flex items-start space-x-3 p-3.5 rounded-xl bg-slate-50 border border-slate-200 cursor-pointer text-xs">
            <input type="checkbox" checked class="mt-0.5 rounded text-teal-600 focus:ring-teal-500">
            <div class="text-slate-700 leading-relaxed">
              I, <strong class="text-slate-900">Chloe Wong</strong>, hereby solemnly declare that all competition outcomes, credentials, and digital deliverables submitted are authentic, unaltered, and formally recognized by Red Dot Award. I understand that false or misleading submissions will result in immediate revocation of subsidy approval and referral to the PolyU Student Discipline Committee.
            </div>
          </label>

          <!-- Authenticated NetID Stamp -->
          <div
            class="p-4 bg-slate-50 rounded-xl border border-slate-200 flex flex-col sm:flex-row sm:items-center justify-between gap-3 text-xs">
            <div>
              <span class="text-[10px] font-bold text-slate-400 uppercase tracking-wider block">AUTHENTICATED APPLICANT NETID SIGNATURE</span>
              <div class="font-bold text-slate-900 text-sm mt-0.5">Chloe Wong (NetID: 22048192D)</div>
              <div class="text-[11px] text-slate-500 mt-0.5">PolyU Single Sign-On (SSO) Timestamp: July 21, 2025 •
                15:48:12 HKT</div>
            </div>
            <div
              class="inline-flex items-center space-x-1.5 px-3 py-1.5 bg-white border border-teal-200 rounded-lg shadow-2xs self-start sm:self-center">
              <svg class="w-4 h-4 text-teal-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                  d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z" />
              </svg>
              <span class="text-[11px] font-bold text-teal-900">Cryptographically Sealed</span>
            </div>
          </div>
        </div>

      </div>

      <!-- Right Guidance Rail (3 Cols) -->
      <div class="lg:col-span-3 space-y-4">

        <!-- Honors Unlocked -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="flex items-center space-x-1.5 text-slate-900 font-bold uppercase text-[11px]">
            <svg class="w-4 h-4 text-teal-600" fill="currentColor" viewBox="0 0 20 20">
              <path fill-rule="evenodd"
                d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                clip-rule="evenodd" />
            </svg>
            <span>Honors Unlocked</span>
          </div>
          <p class="text-slate-500 text-[11px]">Tier 1 International Winner recognition entitles your team to the
            following school honours:</p>
          <ul class="space-y-2 text-slate-700 text-[11px]">
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-900">Exhibition Booth</strong> at PolyU Annual Design Show 2025</div>
            </li>
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div><strong class="text-slate-900">Dean's Commendation Letter</strong> for Global Excellence</div>
            </li>
            <li class="flex items-start gap-1.5">
              <span class="text-teal-600 font-bold">✓</span>
              <div>Entry in the <strong class="text-slate-900">International Student Achievement Registry</strong></div>
            </li>
          </ul>
        </div>

        <!-- Reimbursement Pipeline Tracker -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-3 text-xs">
          <div class="flex justify-between items-center text-[11px]">
            <span class="font-bold text-slate-900 uppercase">Reimbursement Pipeline</span>
            <span class="font-bold text-teal-700">HK$ 1,500</span>
          </div>

          <div class="space-y-3 pt-1 border-t border-slate-100">
            <div class="flex items-start space-x-2">
              <span class="w-4 h-4 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center text-[9px] mt-0.5">✓</span>
              <div>
                <strong class="text-slate-900 block">Pre-Approval Claim Approved</strong>
                <span class="text-[10px] text-slate-400">June 12, 2025 • Capped at HK$1,500</span>
              </div>
            </div>

            <div class="flex items-start space-x-2">
              <span class="w-4 h-4 rounded-full bg-teal-600 text-white font-bold flex items-center justify-center text-[9px] mt-0.5">2</span>
              <div>
                <strong class="text-teal-900 block">Result & Archive Verification</strong>
                <span class="text-[10px] text-teal-700 font-medium">In Progress (This Form)</span>
              </div>
            </div>

            <div class="flex items-start space-x-2 text-slate-400">
              <span class="w-4 h-4 rounded-full border border-slate-300 font-bold flex items-center justify-center text-[9px] mt-0.5">3</span>
              <div>
                <strong class="text-slate-700 block">FO Financial Audit Release</strong>
                <span class="text-[10px]">Expected ~3 working days after signoff</span>
              </div>
            </div>

            <div class="flex items-start space-x-2 text-slate-400">
              <span class="w-4 h-4 rounded-full border border-slate-300 font-bold flex items-center justify-center text-[9px] mt-0.5">4</span>
              <div>
                <strong class="text-slate-700 block">Auto-Pay Direct Deposit</strong>
                <span class="text-[10px]">HSBC Account ending in •••• 833</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Need Clarification Support Box -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200 shadow-xs space-y-2 text-xs">
          <h3 class="font-bold text-slate-900 uppercase text-[11px]">Need Clarification?</h3>
          <p class="text-[11px] text-slate-500">For visual archive resolutions or subsidy inquiries, reach out to the
            administrative team directly:</p>
          <div class="pt-1 space-y-1 text-[11px]">
            <div>Annual Show PR: <a href="mailto:sd.showcase@polyu.edu.hk"
                class="text-teal-700 font-semibold hover:underline">sd.showcase@polyu.edu.hk</a></div>
            <div>Subsidy Finance: <a href="mailto:sd.subsidy@polyu.edu.hk"
                class="text-teal-700 font-semibold hover:underline">sd.subsidy@polyu.edu.hk</a></div>
          </div>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex items-center justify-between">
      <button onclick="showScreen('screen-2')" class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50 flex items-center space-x-1">
        <span>← Return to Subsidies Dashboard</span>
      </button>
      <div class="flex items-center space-x-3">
        <span class="text-xs text-slate-500 hidden sm:inline">READY FOR INSTITUTIONAL ARCHIVE • All 4 mandatory stages satisfied</span>
        <button class="px-4 py-2 bg-white border border-slate-200 rounded-xl text-xs font-semibold text-slate-700 hover:bg-slate-50">Save Draft</button>
        <!-- Per Prompt: press "Submit Result & Archive Dossier" to enter Screen 9 -->
        <button id="btnSubmitResultTo9" onclick="showScreen('screen-9')" class="px-6 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-bold flex items-center space-x-2 shadow-lg transition transform hover:-translate-y-0.5">
          <span>Submit Result & Archive Dossier</span>
          <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SCREEN 9: Application Submitted Successfully / Registration Confirmation -->
  <!-- ========================================================================= -->
  <main id="screen-9" class="screen-view hidden max-w-7xl w-full mx-auto p-6 lg:p-10 space-y-6">
    <!-- Breadcrumb & Top Confirmation Header -->
    <div class="border-b border-slate-200 pb-5">
      <div class="flex items-center space-x-2 text-xs text-slate-500 mb-2">
        <a href="#" onclick="showScreen('screen-2')" class="hover:underline">Dashboard</a>
        <span>/</span>
        <span>Subsidies</span>
        <span>/</span>
        <span>#SUB-2025-0892</span>
        <span>/</span>
        <span class="font-semibold text-slate-800">Submission Confirmation</span>
      </div>

      <div class="flex flex-col md:flex-row md:items-start justify-between gap-4">
        <div class="flex items-start space-x-3.5">
          <div
            class="w-10 h-10 rounded-2xl bg-teal-50 border border-teal-200 text-teal-700 flex items-center justify-center shrink-0 shadow-2xs">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
            </svg>
          </div>
          <div>
            <div class="flex items-center space-x-2">
              <span class="text-[10px] font-bold px-2 py-0.5 rounded bg-teal-100 text-teal-800 uppercase tracking-wide">● GRANT LODGED & STAMPED</span>
              <span class="text-xs text-slate-500">Tier 1 International Category</span>
            </div>
            <h1 class="text-2xl lg:text-3xl font-extrabold text-slate-900 mt-1">Application Successfully Submitted &
              Registered</h1>
            <p class="text-xs text-slate-500 mt-1">
              Reference No. <strong class="text-slate-800">#SUB-2025-0892</strong> • Submitted on July 21, 2025 at 16:42
              HKT via PolyU NetID SSO
            </p>
            <div
              class="mt-3 p-3 bg-teal-50/70 border border-teal-200/80 rounded-xl flex items-center space-x-2 text-xs text-teal-900">
              <svg class="w-4 h-4 text-teal-600 shrink-0" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd"
                  d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                  clip-rule="evenodd" />
              </svg>
              <span>A formal submission dossier has been cryptographically signed and archived. A confirmation digest has been dispatched to <strong>chloe.wong@connect.polyu.hk</strong> and co-authors.</span>
            </div>
          </div>
        </div>

        <!-- Quick Top Action Buttons -->
        <div class="flex flex-wrap md:flex-col items-end gap-2 shrink-0">
          <button class="px-4 py-2 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-semibold shadow-xs flex items-center space-x-1.5">
            <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4"/></svg>
            <span>Download Dossier (PDF)</span>
          </button>
          <div class="flex items-center space-x-2">
            <button class="px-3 py-1.5 bg-white border border-slate-200 hover:bg-slate-50 text-slate-700 rounded-lg text-xs font-medium">Print Audit Slip</button>
            <button onclick="showScreen('screen-2')" class="px-3 py-1.5 bg-white border border-slate-200 hover:bg-slate-50 text-slate-700 rounded-lg text-xs font-medium">Dashboard</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Main Grid Content -->
    <div class="grid grid-cols-1 lg:grid-cols-12 gap-6">

      <!-- Left Column (8 Cols) -->
      <div class="lg:col-span-8 space-y-6">

        <!-- Grant Allocation & Financial Reservation Card -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200/80 shadow-xs space-y-5">
          <div class="flex justify-between items-center border-b border-slate-100 pb-3">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-amber-50 text-amber-700 flex items-center justify-center text-sm font-bold">💳</span>
              <div>
                <h2 class="text-sm font-bold text-slate-900">Grant Allocation & Financial Reservation</h2>
                <div class="text-[10px] text-slate-500">PolyU School of Design Student Design Competition Subsidy Scheme
                </div>
              </div>
            </div>
            <span class="text-[10px] font-mono bg-slate-100 px-2 py-0.5 rounded text-slate-600">FIS CODE: SD-COMP-2425-T1</span>
          </div>

          <!-- Highlight Row -->
          <div
            class="grid grid-cols-1 md:grid-cols-12 gap-4 items-center bg-slate-50 p-4 rounded-xl border border-slate-100">
            <div class="md:col-span-7">
              <span class="text-[10px] font-bold text-slate-500 uppercase tracking-wider block">PRE-APPROVED GRANT RESERVATION</span>
              <div class="flex items-baseline space-x-2 mt-1">
                <span class="text-3xl font-black text-slate-900">HK$ 1,500.00</span>
                <span class="text-xs bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded">100% Capped Grant</span>
              </div>
              <p class="text-[11px] text-slate-500 mt-1">Maximum statutory allocation locked for Tier 1 entry fee.
                Encumbered until post-event result reconciliation.</p>
              <div class="flex items-center space-x-2 text-[11px] text-teal-700 font-semibold mt-2">
                <span>✓ Direct Credit SIS Verified</span>
                <span>•</span>
                <span>No upfront voucher required</span>
              </div>
            </div>

            <!-- Gauge Graphic (Right 5 cols) -->
            <div
              class="md:col-span-5 border-t md:border-t-0 md:border-l border-slate-200 pt-3 md:pt-0 md:pl-5 flex items-center space-x-3">
              <div class="relative w-16 h-16 flex items-center justify-center">
                <svg class="w-16 h-16 transform -rotate-90" viewBox="0 0 36 36">
                  <path class="text-slate-200" stroke-width="3.5" stroke="currentColor" fill="none"
                    d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
                  <path class="text-teal-600" stroke-dasharray="64, 100" stroke-width="3.5" stroke-linecap="round"
                    stroke="currentColor" fill="none"
                    d="M18 2.0845 a 15.9155 15.9155 0 0 1 0 31.831 a 15.9155 15.9155 0 0 1 0 -31.831" />
                </svg>
                <span class="absolute text-[11px] font-bold text-slate-800">64%</span>
              </div>
              <div class="text-xs">
                <span class="text-[10px] text-slate-400 uppercase font-semibold">AY 2024/25 ANNUAL BALANCE</span>
                <div class="font-bold text-slate-900 mt-0.5">HK$ 1,800.00 Remaining</div>
                <div class="text-[10px] text-slate-500">HK$ 3,200 committed of HK$ 5,000 cap</div>
              </div>
            </div>
          </div>

          <!-- Ledger Table -->
          <div class="space-y-2">
            <span class="text-[10px] font-bold text-slate-500 uppercase tracking-wider">COST PEGGING & CALCULATION LEDGER</span>
            <div class="overflow-x-auto">
              <table class="w-full text-left text-xs border border-slate-200 rounded-xl overflow-hidden">
                <thead class="bg-slate-100 text-slate-600 text-[10px] uppercase font-bold">
                  <tr>
                    <th class="p-2.5">Item / Ledger Description</th>
                    <th class="p-2.5">Base Currency</th>
                    <th class="p-2.5">PolyU Pegged Rate</th>
                    <th class="p-2.5 text-right">Amount (HKD)</th>
                  </tr>
                </thead>
                <tbody class="divide-y divide-slate-100 text-slate-700">
                  <tr>
                    <td class="p-2.5 font-medium">
                      Gross Entry Fee (Single Concept Entry)
                      <span class="block text-[10px] text-slate-400">Early-bird institutional student concession</span>
                    </td>
                    <td class="p-2.5 font-mono">EUR 450.00</td>
                    <td class="p-2.5 text-slate-500">1 EUR = HK$ 8.4200</td>
                    <td class="p-2.5 text-right font-bold text-slate-900">HK$ 3,789.00</td>
                  </tr>
                  <tr class="bg-teal-50/40 text-teal-900">
                    <td class="p-2.5 font-semibold flex items-center space-x-1">
                      <span>✓ School of Design Subsidy Coverage</span>
                    </td>
                    <td class="p-2.5 font-mono">—</td>
                    <td class="p-2.5 text-[10px]">Tier 1 Scheme Ceiling Applied</td>
                    <td class="p-2.5 text-right font-bold text-teal-800">- HK$ 1,500.00</td>
                  </tr>
                  <tr>
                    <td class="p-2.5 text-slate-600">
                      Student Team Self-Funded Out-of-Pocket Balance
                      <span class="block text-[10px] text-slate-400">Split among 3 registered team members (~HK$ 763.00/person)</span>
                    </td>
                    <td class="p-2.5 font-mono text-slate-500">EUR 271.85</td>
                    <td class="p-2.5 text-slate-400">—</td>
                    <td class="p-2.5 text-right font-bold text-slate-800">HK$ 2,289.00</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <!-- Designated Disbursement Channel -->
          <div
            class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 flex flex-col sm:flex-row sm:items-center justify-between gap-3 text-xs">
            <div class="flex items-center space-x-3">
              <span class="w-8 h-8 rounded-lg bg-white border border-slate-200 flex items-center justify-center font-bold text-slate-700 text-sm">🏛️</span>
              <div>
                <span class="text-[10px] font-bold text-slate-400 uppercase">DESIGNATED DISBURSEMENT CHANNEL</span>
                <div class="font-bold text-slate-900">HSBC Hong Kong ••••••••••• 833</div>
                <div class="text-[10px] text-slate-500">FPS ID: +852 9482•••• • SIS Auto-Pay Registry ID #CHL-92D</div>
              </div>
            </div>
            <span class="text-[10px] bg-emerald-50 text-emerald-800 font-bold px-2.5 py-1 rounded-md border border-emerald-200 self-start sm:self-center">✓ VERIFIED SIS LINK</span>
          </div>
        </div>

        <!-- Application Lifecycle & Pipeline Tracker -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200/80 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <div>
              <h2 class="text-sm font-bold text-slate-900">Application Lifecycle & What Happens Next</h2>
              <div class="text-[10px] text-slate-500">Active PolyU SD Grant Pipeline Status Tracker</div>
            </div>
            <span class="text-[10px] font-bold bg-teal-100 text-teal-800 px-2 py-0.5 rounded">● STEP 2 OF 5 IN PROGRESS</span>
          </div>

          <div class="space-y-4 text-xs pt-1">
            <!-- Stage 1 -->
            <div class="flex items-start space-x-3">
              <div
                class="w-6 h-6 rounded-full bg-emerald-500 text-white font-bold flex items-center justify-center shrink-0 mt-0.5 text-xs">
                ✓</div>
              <div class="flex-1">
                <div class="flex justify-between items-center">
                  <strong class="text-slate-900">Stage 1: Student Dossier Submission</strong>
                  <span class="text-[10px] bg-emerald-100 text-emerald-800 font-bold px-1.5 py-0.2 rounded">COMPLETED • JULY 21, 16:42 HKT</span>
                </div>
                <p class="text-[11px] text-slate-500 mt-0.5">Application successfully uploaded with all required entry
                  guides and quotation documents verified via PolyU NetID.</p>
              </div>
            </div>

            <!-- Stage 2 -->
            <div class="flex items-start space-x-3 bg-teal-50/40 p-3 rounded-xl border border-teal-200">
              <div
                class="w-6 h-6 rounded-full bg-teal-700 text-white font-bold flex items-center justify-center shrink-0 mt-0.5 text-xs">
                2</div>
              <div class="flex-1">
                <div class="flex justify-between items-center">
                  <strong class="text-teal-950 font-bold">Stage 2: Faculty Endorsement Review</strong>
                  <span class="text-[10px] bg-teal-200 text-teal-900 font-bold px-2 py-0.5 rounded">ACTIVE NOW • SLA: 5 Working Days (Due July 28, 2025)</span>
                </div>
                <p class="text-[11px] text-teal-900 mt-1">Assigned to Studio Tutor <strong>Prof. Marcus Lee</strong>.
                  The tutor validates international competition prestige and academic studio alignment.</p>
                <div class="flex items-center justify-between mt-2 pt-2 border-t border-teal-200/60 text-[11px]">
                  <span class="text-teal-800 flex items-center gap-1">
                    <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                    System Automated Chaser Ping: In 71 hours
                  </span>
                  <button class="text-teal-800 font-bold hover:underline">Send Polite Reminder ↗</button>
                </div>
              </div>
            </div>

            <!-- Stage 3 -->
            <div class="flex items-start space-x-3 text-slate-400">
              <div
                class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0 mt-0.5 text-xs">
                3</div>
              <div class="flex-1">
                <div class="flex justify-between items-center">
                  <strong class="text-slate-600">Stage 3: School of Design Finance Audit & Lock</strong>
                  <span class="text-[10px] font-semibold text-slate-400">PENDING STAGE 2</span>
                </div>
                <p class="text-[11px] text-slate-400 mt-0.5">Administrative validation and formal fiscal encumbrance in
                  the PolyU Bursar Central Ledger.</p>
              </div>
            </div>

            <!-- Stage 4 -->
            <div class="flex items-start space-x-3 text-slate-400">
              <div
                class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0 mt-0.5 text-xs">
                4</div>
              <div class="flex-1">
                <div class="flex justify-between items-center">
                  <strong class="text-slate-600">Stage 4: Competition Execution & Results</strong>
                  <span class="text-[10px]">Organizer Timeline: April – July 2025</span>
                </div>
                <p class="text-[11px] text-slate-400 mt-0.5">Organizer Entry Deadline: <strong>April 24, 2025</strong>.
                  Official Jury Announcement: <strong>July 09, 2025</strong>.</p>
              </div>
            </div>

            <!-- Stage 5 -->
            <div class="flex items-start space-x-3 text-slate-400">
              <div
                class="w-6 h-6 rounded-full bg-slate-100 font-bold flex items-center justify-center shrink-0 mt-0.5 text-xs">
                5</div>
              <div class="flex-1">
                <div class="flex justify-between items-center">
                  <strong class="text-slate-600">Stage 5: Post-Competition Claim & Auto-Disbursement</strong>
                  <span class="text-[10px]">30 Days Post Announcement</span>
                </div>
                <p class="text-[11px] text-slate-400 mt-0.5">Submit organizer proof of submission, payment invoice, and
                  award/participation certificate to trigger HK$ 1,500.00 bank direct transfer.</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Submitted Dossier Quick Summary -->
        <div class="bg-white p-6 rounded-2xl border border-slate-200/80 shadow-xs space-y-4">
          <div class="flex justify-between items-center border-b border-slate-100 pb-2">
            <h2 class="text-sm font-bold text-slate-900">Submitted Dossier Quick Summary</h2>
            <span class="text-[10px] font-mono text-slate-400">ARCHIVED METADATA</span>
          </div>

          <div
            class="p-3.5 bg-slate-50 rounded-xl border border-slate-200 flex flex-col sm:flex-row items-start sm:items-center space-y-3 sm:space-y-0 sm:space-x-3">
            <img src="https://images.unsplash.com/photo-1605100804763-247f67b3557e?w=120&auto=format&fit=crop&q=80" alt="AuraRing Thumbnail" class="w-16 h-16 object-cover rounded-lg border border-slate-300 shrink-0">
            <div class="text-xs space-y-0.5">
              <div class="flex items-center space-x-2">
                <span class="text-[9px] bg-slate-900 text-white font-bold px-1.5 py-0.2 rounded">DESIGN CONCEPT</span>
                <span class="text-[10px] text-slate-500">Wearable Tech / Assistive Spatial Interaction</span>
              </div>
              <h3 class="font-bold text-slate-900 text-sm">AuraRing: Haptic Spatial Guidance Ring</h3>
              <p class="text-[11px] text-slate-500">Micro-haptic directional pulse interface engineered for visually
                impaired navigation in dense indoor environments, created during SD3102 Studio.</p>
              <div class="flex items-center space-x-3 text-[10px] text-slate-500 pt-0.5">
                <span>🏆 Red Dot Award: Design Concept 2025 (Singapore/Essen)</span>
                <span>•</span>
                <span>📅 Closing: 24 Apr 2025</span>
              </div>
            </div>
          </div>

          <!-- Co-Authors & Split Cards -->
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 text-xs">
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <div class="flex items-center justify-between">
                <span class="font-bold text-slate-900">Chloe Wong</span>
                <span class="text-[10px] font-bold text-teal-800 bg-teal-50 px-1 rounded">HK$ 600</span>
              </div>
              <div class="text-[10px] text-slate-500">Lead Applicant (40%)</div>
            </div>
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <div class="flex items-center justify-between">
                <span class="font-bold text-slate-900">Ken Ka-Ho Leung</span>
                <span class="text-[10px] font-bold text-slate-700 bg-slate-100 px-1 rounded">HK$ 450</span>
              </div>
              <div class="text-[10px] text-slate-500">Co-Author (30%)</div>
            </div>
            <div class="p-2.5 bg-slate-50 rounded-xl border border-slate-200">
              <div class="flex items-center justify-between">
                <span class="font-bold text-slate-900">Anson Chun-Kit Chan</span>
                <span class="text-[10px] font-bold text-slate-700 bg-slate-100 px-1 rounded">HK$ 450</span>
              </div>
              <div class="text-[10px] text-slate-500">Co-Author (30%)</div>
            </div>
          </div>

          <!-- Attachments Row -->
          <div class="space-y-1.5 text-xs pt-1">
            <span class="text-[10px] font-bold text-slate-400 uppercase">ATTACHED VERIFICATION DOCUMENTS (3)</span>
            <div class="grid grid-cols-1 sm:grid-cols-3 gap-2 text-[11px]">
              <div class="p-2 bg-slate-50 rounded-lg border border-slate-200 flex items-center justify-between">
                <span class="truncate">📄 RedDot_EntryGuide.pdf</span>
                <span class="text-[9px] text-slate-400">2.4 MB</span>
              </div>
              <div class="p-2 bg-slate-50 rounded-lg border border-slate-200 flex items-center justify-between">
                <span class="truncate">📄 Invoice_Quote_2025.pdf</span>
                <span class="text-[9px] text-slate-400">1.2 MB</span>
              </div>
              <div class="p-2 bg-slate-50 rounded-lg border border-slate-200 flex items-center justify-between">
                <span class="truncate">🖼️ AuraRing_Render.png</span>
                <span class="text-[9px] text-slate-400">4.2 MB</span>
              </div>
            </div>
          </div>
        </div>

      </div>

      <!-- Right Column (4 Cols) -->
      <div class="lg:col-span-4 space-y-4">

        <!-- Required Student Actions -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-3 text-xs">
          <div class="flex justify-between items-center">
            <span class="font-bold text-slate-900 uppercase">Required Student Actions</span>
            <span class="text-[10px] bg-teal-50 text-teal-800 font-bold px-2 py-0.5 rounded">4 Items</span>
          </div>

          <div class="space-y-3 text-[11px] text-slate-600">
            <div class="p-3 bg-slate-50 rounded-xl space-y-1">
              <strong class="text-slate-900 flex items-center gap-1">🔔 Notify Academic Tutor</strong>
              <p>Please mention this application during your next studio consultation with Prof. Lee.</p>
              <a href="#" class="text-teal-700 font-semibold hover:underline block pt-0.5">Draft Email to Prof. Lee
                →</a>
            </div>

            <div class="p-3 bg-slate-50 rounded-xl space-y-1">
              <strong class="text-slate-900 flex items-center gap-1">🏷️ PolyU Affiliation Crediting Clause</strong>
              <p>Official entry credit must strictly state:
                <span class="font-bold text-slate-800">"School of Design, The Hong Kong Polytechnic University"</span>
                to qualify for reimbursement.</p>
            </div>

            <div class="p-3 bg-slate-50 rounded-xl space-y-1">
              <strong class="text-slate-900 flex items-center gap-1">🧾 Preserve Original Invoices</strong>
              <p>Keep credit card monthly statements showing the EUR charge & official organizer VAT receipt.</p>
            </div>

            <div class="p-3 bg-slate-50 rounded-xl space-y-1">
              <strong class="text-slate-900 flex items-center gap-1">📅 Calendar Critical Dates</strong>
              <p>Sync submission closing (24 Apr) and release notice (9 Jul) with your student calendar.</p>
              <a href="#" class="text-teal-700 font-semibold hover:underline block pt-0.5">+ Add .ics to
                Outlook/Apple</a>
            </div>
          </div>
        </div>

        <!-- Designated Endorser Card -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-3 text-xs">
          <div class="flex justify-between items-center text-[10px] font-bold text-slate-400 uppercase">
            <span>DESIGNATED ENDORSER</span>
            <span class="text-teal-700">Faculty Reviewer</span>
          </div>

          <div class="flex items-center space-x-3">
            <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=100&auto=format&fit=crop&q=80" alt="Prof Marcus Lee" class="w-10 h-10 rounded-xl object-cover border border-slate-300">
            <div>
              <div class="font-bold text-slate-900">Prof. Marcus Lee</div>
              <div class="text-[10px] text-slate-500">Associate Professor (IID)</div>
              <div class="text-[10px] text-slate-400">SD3102 Studio Director • V812 JCIT</div>
            </div>
          </div>

          <div class="pt-2 border-t border-slate-100 text-[11px] space-y-1">
            <div class="flex justify-between">
              <span class="text-slate-500">Endorsement Status:</span>
              <span class="text-teal-700 font-bold">● Email Dispatched</span>
            </div>
            <div class="flex justify-between">
              <span class="text-slate-500">Authentication Token:</span>
              <span class="font-mono text-slate-700">NETID-VERIF-9820-T1</span>
            </div>
            <div class="flex justify-between">
              <span class="text-slate-500">Expected Clearance:</span>
              <strong class="text-slate-800">By July 28, 2025</strong>
            </div>
          </div>
        </div>

        <!-- Need Clarification Support Box -->
        <div class="bg-white p-5 rounded-2xl border border-slate-200/80 shadow-xs space-y-2 text-xs">
          <h3 class="font-bold text-slate-900 uppercase text-[11px]">Need Clarification?</h3>
          <p class="text-[11px] text-slate-500">For financial pegging disputes, quota adjustments, or co-author
            authorisations, reach out to the General Office.</p>
          <div class="space-y-1 text-[11px] pt-1 text-slate-600">
            <div>✉️ <a href="mailto:sd.subsidy@polyu.edu.hk"
                class="text-teal-700 font-semibold hover:underline">sd.subsidy@polyu.edu.hk</a></div>
            <div>📞 +852 2766 5454 (Mon-Fri 09:00 - 17:30)</div>
            <div>🏢 V810, Jockey Club Innovation Tower</div>
          </div>
          <a href="#" class="text-[11px] text-teal-700 font-bold hover:underline block pt-1">📖 Read Subsidy Scheme
            Guidelines (Rev. 2024/25)</a>
        </div>

      </div>

    </div>

    <!-- Bottom Sticky Navigation Bar -->
    <div class="border-t border-slate-200 pt-4 flex flex-col sm:flex-row items-center justify-between gap-3">
      <div class="flex items-center space-x-2 text-xs text-slate-500">
        <span class="w-5 h-5 rounded-full bg-slate-100 text-slate-600 flex items-center justify-center font-bold text-[10px]">📋</span>
        <span>Managing Application <strong class="text-slate-800">#SUB-2025-0892</strong> • All changes are auditable via PolyU Central SIS</span>
      </div>

      <div class="flex items-center space-x-3 w-full sm:w-auto justify-end">
        <button class="px-3.5 py-2 bg-white border border-slate-200 hover:bg-slate-50 rounded-xl text-xs font-semibold text-slate-700 shadow-2xs flex items-center space-x-1.5">
          <svg class="w-4 h-4 text-slate-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8.684 13.342C8.886 12.938 9 12.482 9 12c0-.482-.114-.938-.316-1.342m0 2.684a3 3 0 110-2.684m0 2.684l6.632 3.316m-6.632-6l6.632-3.316m0 0a3 3 0 105.367-2.684 3 3 0 00-5.367 2.684zm0 9.316a3 3 0 105.368 2.684 3 3 0 00-5.368-2.684z"/></svg>
          <span>Share with Team</span>
        </button>
        <!-- Per Prompt: Screen 9 -> press "Back to Subsidy Dashboard" to return back to Screen 2 -->
        <button id="btnBackToDashboardFrom9" onclick="showScreen('screen-2')" class="px-5 py-2.5 bg-slate-900 hover:bg-slate-800 text-white rounded-xl text-xs font-bold shadow-md flex items-center space-x-2 transition">
          <span>Back to Subsidy Dashboard</span>
          <svg class="w-4 h-4 text-teal-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
        </button>
      </div>
    </div>
  </main>

  <!-- ========================================================================= -->
  <!-- SHARED APP FOOTER (Screens 2 through 9) -->
  <!-- ========================================================================= -->
  <footer id="app-global-footer"
    class="hidden bg-white border-t border-slate-200 py-6 px-6 lg:px-12 mt-12 text-xs text-slate-500">
    <div class="max-w-7xl mx-auto flex flex-col md:flex-row items-center justify-between gap-4">
      <div>
        <strong class="text-slate-800">School of Design</strong> • The Hong Kong Polytechnic University
        <div class="text-[11px] text-slate-400 mt-0.5">© 2025 PolyU School of Design. All rights reserved.</div>
      </div>
      <div class="flex items-center space-x-6 text-[11px]">
        <div>
          <span class="font-bold text-slate-700 uppercase">SCHEME TERMS & CAPS</span>
          <div class="text-slate-500">Max HK1,500perclaim•AnnualCap:HK3,000 / Academic Year</div>
        </div>
        <div>
          <span class="font-bold text-slate-700 uppercase">GENERAL ENQUIRY</span>
          <div><a href="mailto:sd.subsidy@polyu.edu.hk"
              class="text-teal-700 hover:underline">sd.subsidy@polyu.edu.hk</a></div>
        </div>
      </div>
    </div>
  </footer>

  <!-- ========================================================================= -->
  <!-- INTERACTIVE SPA ROUTER & NAVIGATION CONTROLLER SCRIPT -->
  <!-- ========================================================================= -->
  <script>
    /**
     * Primary Screen Transition Handler
     * Controls SPA views according to the specified navigation logic:
     * Screen 1: SSO Authentication
     * Screen 2: Dashboard
     * Screen 3: Step 1: Academic & Project Info
     * Screen 4: Step 2: Competition & Tier Verification
     * Screen 5: Step 3: Budget & Estimator
     * Screen 6: Step 4: Faculty Endorsement
     * Screen 7: Step 5: Review & Declaration
     * Screen 8: Competition Result Reporting & Showcase Archive
     * Screen 9: Application Successfully Submitted
     */
    function showScreen(screenId) {
      // 1. Hide all screen views and Screen 1
      const screens = [
        'screen-1', 'screen-2', 'screen-3', 'screen-4',
        'screen-5', 'screen-6', 'screen-7', 'screen-8', 'screen-9'
      ];
      
      screens.forEach(id => {
        const el = document.getElementById(id);
        if (el) {
          el.classList.add('hidden');
        }
      });

      // 2. Unhide target screen
      const target = document.getElementById(screenId);
      if (target) {
        target.classList.remove('hidden');
      }

      // 3. Toggle Global Header & Global Footer visibility
      const globalHeader = document.getElementById('app-global-header');
      const globalFooter = document.getElementById('app-global-footer');

      if (screenId === 'screen-1') {
        globalHeader.classList.add('hidden');
        globalFooter.classList.add('hidden');
      } else {
        globalHeader.classList.remove('hidden');
        globalFooter.classList.remove('hidden');
      }

      // 4. Synchronize Quick Navigation Dropdown
      const quickNavSelect = document.getElementById('quickNavSelect');
      if (quickNavSelect) {
        quickNavSelect.value = screenId;
      }

      // 5. Scroll smoothly to top
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    /**
     * Navigation Logic specified for Screen 7:
     * "Screen 7: press 'Submit Subsidy Application' to submit the application and return to Screen 1"
     */
    function submitApplicationToScreen1() {
      // Show confirmation toast / alert before returning
      const confirmed = confirm("Submit application dossier #SUB-2025-0892 and return to PolyU Institutional SSO Login?");
      if (confirmed) {
        showScreen('screen-1');
      }
    }

    // Initialize to Screen 1 on page load
    document.addEventListener('DOMContentLoaded', () => {
      showScreen('screen-1');

      // Update timestamp dynamically
      const stampEl = document.getElementById('currentTimestamp');
      if (stampEl) {
        const now = new Date();
        stampEl.textContent = now.toISOString().replace('T', ' ').substring(0, 19) + ' HKT';
      }
    });
  </script>
</body>

</html>
