<script lang="ts">
  import { page } from '$app/stores';

</script>

<header class="sticky top-0 z-40 w-full border-b bg-background/95 backdrop-blur supports-[backdrop-filter]:bg-background/60">

  <div class="container mx-auto flex h-16 items-center justify-between px-4">
    
    <a class="flex items-center gap-3" href="/" aria-label="Refúgio Pet - Início">
    
      <div class="w-9 h-9 rounded-full bg-success flex items-center justify-center shrink-0">
        <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5 text-white" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
          <circle cx="11" cy="4" r="2"></circle>
          <circle cx="18" cy="8" r="2"></circle>
          <circle cx="20" cy="16" r="2"></circle>
          <path d="M9 10a5 5 0 0 1 5 5v3.5a3.5 3.5 0 0 1-6.84 1.045Q6.52 17.48 4.46 16.84A3.5 3.5 0 0 1 5.5 10Z"></path>
        </svg>
      </div>

      <span class="text-success font-bold text-lg leading-none">Refúgio Pet</span>
    </a>

    <div class="hidden md:flex items-center gap-6">
      <nav class="flex items-center gap-6 text-sm">
        <a class="transition-colors hover:text-success {$page.url.pathname == '/' ? "text-success border-b-2 border-success pb-1" : "text-base-content/70"}" href="/">Início</a>
        <a class="transition-colors hover:text-success {$page.url.pathname == '/pets' ? "text-success border-b-2 border-success pb-1" : "text-base-content/70"}" href="/pets">Pets</a>
        <a class="transition-colors hover:text-success {$page.url.pathname == '/lost-pets' ? "text-success border-b-2 border-success pb-1" : "text-base-content/70"}" href="/lost-pets">Perdidos</a>
        <a class="transition-colors hover:text-success {$page.url.pathname == '/report-lost-pet' ? "text-success border-b-2 border-success pb-1" : "text-base-content/70"}" href="/report-lost-pet">Reportar Pet Perdido</a>
      </nav>

      <div class="flex items-center gap-2">
        <a class="inline-flex items-center gap-2 text-sm font-medium btn btn-ghost btn-sm" href="/sign-in">
          <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true" viewBox="0 0 24 24">
            <path d="M15 3h4a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2h-4"></path>
            <polyline points="10 17 15 12 10 7"></polyline>
            <line x1="15" x2="3" y1="12" y2="12"></line>
          </svg>
          Entrar
        </a>
        <a class="btn btn-success btn-sm text-sm" href="/sign-up">Cadastrar</a>
      </div>
    </div>

    <button id="mobile-menu-btn" class="md:hidden inline-flex items-center justify-center p-2 rounded-md btn btn-ghost btn-sm" aria-controls="mobile-menu" aria-expanded="false" type="button" aria-label="Abrir menu">
      <svg xmlns="http://www.w3.org/2000/svg" class="w-5 h-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
        <line x1="4" x2="20" y1="12" y2="12"></line>
        <line x1="4" x2="20" y1="6" y2="6"></line>
        <line x1="4" x2="20" y1="18" y2="18"></line>
      </svg>
    </button>
  </div>

  <div id="mobile-menu" class="md:hidden hidden border-t bg-base-100">
    <div class="container mx-auto px-4 py-3 flex flex-col gap-2">
      <a class="py-2 text-sm transition-colors hover:text-success text-success border-b-2 border-success pb-1" href="/" aria-current="page">Início</a>
      <a class="py-2 text-sm transition-colors hover:text-success text-base-content/70" href="/pets">Pets</a>
      <a class="py-2 text-sm transition-colors hover:text-success text-base-content/70" href="/lost-pets">Perdidos</a>
      <a class="py-2 text-sm transition-colors hover:text-success text-base-content/70" href="/report-lost-pet">Reportar Pet Perdido</a>

      <div class="pt-2 flex gap-2">
        <a class="flex-1 btn btn-ghost btn-sm" href="/sign-in">Entrar</a>
        <a class="flex-1 btn btn-success btn-sm" href="/sign-up">Cadastrar</a>
      </div>
    </div>
  </div>

  </header>
