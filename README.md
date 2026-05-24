<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Karya Indah Furniture — Premium Solid Wood Tables</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            wood:    { DEFAULT: '#6B3A2A', light: '#8B5442', dark: '#3E1F12', pale: '#F5EDE6' },
            bark:    '#2C1A0E',
            sand:    '#D4B896',
            cream:   '#FAF7F2',
            charcoal:{ DEFAULT: '#2D2D2D', light: '#4A4A4A', pale: '#F0EFED' },
            grain:   '#E8D5C0',
          },
          fontFamily: {
            display: ['Cormorant Garamond', 'serif'],
            body:    ['Jost', 'sans-serif'],
          },
        }
      }
    }
  </script>
  <style>
    *, *::before, *::after { box-sizing: border-box; }
    html { scroll-behavior: smooth; }
    body { font-family: 'Jost', sans-serif; background: #FAF7F2; color: #2D2D2D; }

    /* ── Noise texture overlay ── */
    body::before {
      content: '';
      position: fixed; inset: 0; pointer-events: none; z-index: 9999;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.035'/%3E%3C/svg%3E");
      opacity: 0.4;
    }

    /* ── Nav ── */
    #navbar { transition: background .4s, box-shadow .4s; }
    #navbar.scrolled { background: rgba(250,247,242,0.97); box-shadow: 0 1px 0 #e8d5c0; }

    /* ── Hero ── */
    .hero-bg {
      background-image:
        linear-gradient(to right, rgba(44,26,14,0.82) 0%, rgba(44,26,14,0.35) 55%, rgba(44,26,14,0.10) 100%),
        url('https://images.unsplash.com/photo-0a68260b8a1e312bc1ca1d5cd142e12d?w=1800&q=85&auto=format&fit=crop');
      background-size: cover;
      background-position: center 40%;
    }

    /* ── Marquee ── */
    .marquee-track { display: flex; width: max-content; animation: marquee 28s linear infinite; }
    @keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

    /* ── Product cards ── */
    .product-card { transition: transform .4s cubic-bezier(.25,.8,.25,1), box-shadow .4s; }
    .product-card:hover { transform: translateY(-6px); box-shadow: 0 24px 48px rgba(62,31,18,.13); }
    .product-card .overlay { opacity: 0; transition: opacity .35s; }
    .product-card:hover .overlay { opacity: 1; }
    .product-img { transition: transform .6s cubic-bezier(.25,.8,.25,1); }
    .product-card:hover .product-img { transform: scale(1.06); }

    /* ── Section reveals ── */
    .reveal { opacity: 0; transform: translateY(32px); transition: opacity .7s ease, transform .7s ease; }
    .reveal.visible { opacity: 1; transform: none; }

    /* ── Underline link ── */
    .nav-link { position: relative; }
    .nav-link::after { content: ''; position: absolute; left: 0; bottom: -2px; width: 0; height: 1px; background: #6B3A2A; transition: width .3s; }
    .nav-link:hover::after { width: 100%; }

    /* ── Form focus ── */
    input:focus, textarea:focus, select:focus { outline: none; border-color: #6B3A2A !important; box-shadow: 0 0 0 3px rgba(107,58,42,.12); }

    /* ── Divider ornament ── */
    .ornament { display: flex; align-items: center; gap: 16px; }
    .ornament::before, .ornament::after { content: ''; flex: 1; height: 1px; background: #D4B896; }

    /* ── WA button pulse ── */
    .wa-pulse { animation: pulse-green 2s infinite; }
    @keyframes pulse-green {
      0%, 100% { box-shadow: 0 0 0 0 rgba(37,211,102,.4); }
      50%       { box-shadow: 0 0 0 10px rgba(37,211,102,0); }
    }

    /* ── Mobile menu ── */
    #mobile-menu { transition: max-height .35s ease, opacity .35s ease; max-height: 0; opacity: 0; overflow: hidden; }
    #mobile-menu.open { max-height: 320px; opacity: 1; }

    /* ── Scroll indicator ── */
    #scroll-progress { position: fixed; top: 0; left: 0; height: 2px; background: linear-gradient(90deg,#6B3A2A,#D4B896); z-index: 1000; transition: width .1s; }
  </style>
</head>
<body class="bg-cream">

  <!-- Scroll Progress -->
  <div id="scroll-progress" style="width:0%"></div>

  <!-- ══════════════════════════════════════════
       NAVBAR
  ══════════════════════════════════════════ -->
  <nav id="navbar" class="fixed top-0 inset-x-0 z-50 px-6 lg:px-16 py-4">
    <div class="max-w-7xl mx-auto flex items-center justify-between">

      <!-- Logo -->
      <a href="#home" class="flex items-center gap-3 group">
        <div class="w-9 h-9 bg-wood rounded-sm flex items-center justify-center shrink-0">
          <svg viewBox="0 0 32 32" class="w-5 h-5 fill-cream">
            <path d="M4 28V10l12-6 12 6v18H20v-8h-8v8H4z"/>
            <rect x="13" y="20" width="6" height="8" rx="1"/>
          </svg>
        </div>
        <div class="leading-tight">
          <div class="font-display text-lg font-semibold text-bark tracking-wide">Karya Indah</div>
          <div class="font-body text-[9px] uppercase tracking-[.2em] text-wood-light -mt-0.5">Furniture</div>
        </div>
      </a>

      <!-- Desktop links -->
      <ul class="hidden md:flex items-center gap-10">
        <li><a href="#home"     class="nav-link font-body text-sm font-medium text-charcoal hover:text-wood tracking-wide">Home</a></li>
        <li><a href="#products" class="nav-link font-body text-sm font-medium text-charcoal hover:text-wood tracking-wide">Products</a></li>
        <li><a href="#about"    class="nav-link font-body text-sm font-medium text-charcoal hover:text-wood tracking-wide">About Us</a></li>
        <li><a href="#contact"  class="nav-link font-body text-sm font-medium text-charcoal hover:text-wood tracking-wide">Contact</a></li>
      </ul>

      <!-- CTA + hamburger -->
      <div class="flex items-center gap-4">
        <a href="#contact" class="hidden md:inline-flex items-center gap-2 bg-wood hover:bg-wood-dark text-cream font-body text-sm font-medium px-5 py-2.5 rounded-sm transition-colors duration-300">
          Request Quote
          <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
        <button id="menu-toggle" class="md:hidden text-charcoal focus:outline-none" aria-label="Menu">
          <svg id="icon-menu" class="w-6 h-6" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M4 6h16M4 12h16M4 18h16"/></svg>
          <svg id="icon-close" class="w-6 h-6 hidden" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M6 18L18 6M6 6l12 12"/></svg>
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="md:hidden bg-cream/97 backdrop-blur border-t border-grain mt-3 mx-0">
      <ul class="flex flex-col px-6 py-4 gap-5">
        <li><a href="#home"     class="mobile-link font-body text-sm font-medium text-charcoal hover:text-wood">Home</a></li>
        <li><a href="#products" class="mobile-link font-body text-sm font-medium text-charcoal hover:text-wood">Products</a></li>
        <li><a href="#about"    class="mobile-link font-body text-sm font-medium text-charcoal hover:text-wood">About Us</a></li>
        <li><a href="#contact"  class="mobile-link font-body text-sm font-medium text-charcoal hover:text-wood">Contact</a></li>
        <li><a href="#contact"  class="block bg-wood text-cream text-sm font-medium text-center py-2.5 rounded-sm">Request Quote</a></li>
      </ul>
    </div>
  </nav>


  <!-- ══════════════════════════════════════════
       HERO
  ══════════════════════════════════════════ -->
  <section id="home" class="hero-bg min-h-screen flex flex-col justify-center relative overflow-hidden">

    <!-- Decorative vertical rule -->
    <div class="absolute left-16 top-0 bottom-0 w-px bg-sand/20 hidden xl:block"></div>

    <div class="max-w-7xl mx-auto px-6 lg:px-16 pt-28 pb-24 w-full">
      <div class="max-w-2xl">

        <!-- Eyebrow -->
        <div class="flex items-center gap-3 mb-8 reveal">
          <span class="w-8 h-px bg-sand"></span>
          <span class="font-body text-xs uppercase tracking-[.25em] text-sand font-medium">Suar & Trembesi Wood Specialists</span>
        </div>

        <!-- Headline -->
        <h1 class="font-display text-5xl sm:text-6xl lg:text-7xl xl:text-8xl font-light text-cream leading-[1.05] reveal" style="transition-delay:.1s">
          Crafted From<br/>
          <em class="font-semibold not-italic text-sand">Living</em><br/>
          <span class="font-light">Wood.</span>
        </h1>

        <!-- Sub -->
        <p class="font-body text-base sm:text-lg text-cream/75 font-light mt-7 max-w-lg leading-relaxed reveal" style="transition-delay:.2s">
          Each table carries the soul of Indonesian forest — live edges, natural grain, and decades of growth shaped into heirloom-quality furniture for export and local markets.
        </p>

        <!-- CTAs -->
        <div class="flex flex-wrap items-center gap-4 mt-10 reveal" style="transition-delay:.3s">
          <a href="#products" class="inline-flex items-center gap-2.5 bg-sand hover:bg-grain text-bark font-body font-medium text-sm px-8 py-4 transition-colors duration-300">
            View Catalog
            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
          </a>
          <a href="#contact" class="inline-flex items-center gap-2.5 border border-cream/40 hover:border-cream text-cream font-body font-medium text-sm px-8 py-4 transition-colors duration-300">
            Request Quote
          </a>
        </div>

        <!-- Stats row -->
        <div class="flex flex-wrap gap-10 mt-16 reveal" style="transition-delay:.4s">
          <div>
            <div class="font-display text-3xl font-semibold text-sand">15+</div>
            <div class="font-body text-xs text-cream/60 uppercase tracking-widest mt-0.5">Years Crafting</div>
          </div>
          <div class="w-px bg-sand/25"></div>
          <div>
            <div class="font-display text-3xl font-semibold text-sand">40+</div>
            <div class="font-body text-xs text-cream/60 uppercase tracking-widest mt-0.5">Export Countries</div>
          </div>
          <div class="w-px bg-sand/25"></div>
          <div>
            <div class="font-display text-3xl font-semibold text-sand">5k+</div>
            <div class="font-body text-xs text-cream/60 uppercase tracking-widest mt-0.5">Tables Delivered</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Scroll hint -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 reveal" style="transition-delay:.6s">
      <span class="font-body text-[10px] uppercase tracking-[.2em] text-cream/50">Scroll</span>
      <div class="w-px h-10 bg-sand/40 relative overflow-hidden">
        <div class="absolute top-0 w-full h-1/2 bg-sand animate-bounce"></div>
      </div>
    </div>
  </section>


  <!-- ══════════════════════════════════════════
       MARQUEE STRIP
  ══════════════════════════════════════════ -->
  <div class="bg-wood py-4 overflow-hidden select-none">
    <div class="marquee-track text-sand/80 font-body text-xs uppercase tracking-[.2em]">
      <span class="px-8">Solid Suar Wood</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Live Edge Tables</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Premium Export Quality</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Handcrafted in Indonesia</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Custom Dimensions</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Trembesi Specialists</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Solid Suar Wood</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Live Edge Tables</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Premium Export Quality</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Handcrafted in Indonesia</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Custom Dimensions</span><span class="px-2 text-sand/30">◆</span>
      <span class="px-8">Trembesi Specialists</span><span class="px-2 text-sand/30">◆</span>
    </div>
  </div>


  <!-- ══════════════════════════════════════════
       PRODUCTS
  ══════════════════════════════════════════ -->
  <section id="products" class="py-28 px-6 lg:px-16 bg-cream">
    <div class="max-w-7xl mx-auto">

      <!-- Section header -->
      <div class="mb-16 reveal">
        <div class="ornament mb-5">
          <span class="font-body text-xs uppercase tracking-[.25em] text-wood font-medium whitespace-nowrap">Our Collection</span>
        </div>
        <div class="text-center">
          <h2 class="font-display text-4xl sm:text-5xl lg:text-6xl font-light text-bark leading-tight">
            Signature <em class="font-semibold not-italic">Pieces</em>
          </h2>
          <p class="font-body text-charcoal-light font-light mt-4 max-w-xl mx-auto leading-relaxed">
            Each piece is shaped from a single slab — no veneers, no shortcuts. The grain, knots, and natural edges tell the story of the tree.
          </p>
        </div>
      </div>

      <!-- Product Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

        <!-- Card 1: Dining Table -->
        <div class="product-card bg-white rounded-sm overflow-hidden group reveal" style="transition-delay:.05s">
          <div class="relative overflow-hidden h-64 bg-charcoal-pale">
            <img
              src="https://images.unsplash.com/photo-1617806118233-18e1de247200?w=800&q=80&auto=format&fit=crop"
              alt="Solid Suar Dining Table"
              class="product-img w-full h-full object-cover"
            />
            <!-- Overlay -->
            <div class="overlay absolute inset-0 bg-bark/60 flex items-center justify-center">
              <a href="#contact" class="border border-cream text-cream font-body text-xs uppercase tracking-widest px-6 py-2.5 hover:bg-cream hover:text-bark transition-colors">
                Inquire Now
              </a>
            </div>
            <!-- Badges -->
            <div class="absolute top-4 left-4 flex flex-col gap-2">
              <span class="bg-wood text-cream font-body text-[10px] uppercase tracking-widest px-3 py-1">Premium Export Quality</span>
            </div>
            <div class="absolute top-4 right-4">
              <span class="bg-bark/80 text-sand font-body text-[10px] px-2.5 py-1">Bestseller</span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-start justify-between mb-3">
              <div>
                <h3 class="font-display text-xl font-semibold text-bark">Solid Suar Dining Table</h3>
                <p class="font-body text-xs text-wood mt-0.5 uppercase tracking-wider">Suar / Rain Tree Wood</p>
              </div>
              <div class="w-8 h-8 rounded-full border border-wood/30 flex items-center justify-center shrink-0 mt-1">
                <div class="w-4 h-4 rounded-full" style="background: radial-gradient(circle at 35% 35%, #a0724a, #3e1f12)"></div>
              </div>
            </div>
            <p class="font-body text-sm text-charcoal-light font-light leading-relaxed">
              A commanding centrepiece. Single-slab top with natural live edges, epoxy-filled natural voids, and a hand-rubbed oil finish.
            </p>
            <!-- Specs -->
            <div class="mt-5 pt-5 border-t border-grain grid grid-cols-3 gap-3 text-center">
              <div>
                <div class="font-display text-sm font-semibold text-bark">200 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Length</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">90 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Width</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">75 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Height</div>
              </div>
            </div>
            <a href="#contact" class="mt-5 flex items-center justify-between text-wood hover:text-wood-dark font-body text-sm font-medium group/link">
              <span>Get a Custom Quote</span>
              <svg class="w-4 h-4 group-hover/link:translate-x-1 transition-transform" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
            </a>
          </div>
        </div>

        <!-- Card 2: Coffee Table -->
        <div class="product-card bg-white rounded-sm overflow-hidden group reveal" style="transition-delay:.15s">
          <div class="relative overflow-hidden h-64 bg-charcoal-pale">
            <img
              src="https://images.unsplash.com/photo-1555041469-a586c61ea9bc?w=800&q=80&auto=format&fit=crop"
              alt="Live Edge Coffee Table"
              class="product-img w-full h-full object-cover"
            />
            <div class="overlay absolute inset-0 bg-bark/60 flex items-center justify-center">
              <a href="#contact" class="border border-cream text-cream font-body text-xs uppercase tracking-widest px-6 py-2.5 hover:bg-cream hover:text-bark transition-colors">
                Inquire Now
              </a>
            </div>
            <div class="absolute top-4 left-4 flex flex-col gap-2">
              <span class="bg-wood text-cream font-body text-[10px] uppercase tracking-widest px-3 py-1">Premium Export Quality</span>
              <span class="bg-sand text-bark font-body text-[10px] uppercase tracking-widest px-3 py-1">New Arrival</span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-start justify-between mb-3">
              <div>
                <h3 class="font-display text-xl font-semibold text-bark">Live Edge Coffee Table</h3>
                <p class="font-body text-xs text-wood mt-0.5 uppercase tracking-wider">Trembesi / Samanea Wood</p>
              </div>
              <div class="w-8 h-8 rounded-full border border-wood/30 flex items-center justify-center shrink-0 mt-1">
                <div class="w-4 h-4 rounded-full" style="background: radial-gradient(circle at 35% 35%, #c4956a, #5c3218)"></div>
              </div>
            </div>
            <p class="font-body text-sm text-charcoal-light font-light leading-relaxed">
              Wide natural edges preserved in full. Paired with hand-forged black iron hairpin legs for a refined industrial warmth.
            </p>
            <div class="mt-5 pt-5 border-t border-grain grid grid-cols-3 gap-3 text-center">
              <div>
                <div class="font-display text-sm font-semibold text-bark">110 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Length</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">60 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Width</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">45 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Height</div>
              </div>
            </div>
            <a href="#contact" class="mt-5 flex items-center justify-between text-wood hover:text-wood-dark font-body text-sm font-medium group/link">
              <span>Get a Custom Quote</span>
              <svg class="w-4 h-4 group-hover/link:translate-x-1 transition-transform" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
            </a>
          </div>
        </div>

        <!-- Card 3: Executive Desk -->
        <div class="product-card bg-white rounded-sm overflow-hidden group reveal" style="transition-delay:.25s">
          <div class="relative overflow-hidden h-64 bg-charcoal-pale">
            <img
              src="https://images.unsplash.com/photo-1593085512500-5d55148d6f0d?w=800&q=80&auto=format&fit=crop"
              alt="Executive Desk"
              class="product-img w-full h-full object-cover"
            />
            <div class="overlay absolute inset-0 bg-bark/60 flex items-center justify-center">
              <a href="#contact" class="border border-cream text-cream font-body text-xs uppercase tracking-widest px-6 py-2.5 hover:bg-cream hover:text-bark transition-colors">
                Inquire Now
              </a>
            </div>
            <div class="absolute top-4 left-4 flex flex-col gap-2">
              <span class="bg-wood text-cream font-body text-[10px] uppercase tracking-widest px-3 py-1">Premium Export Quality</span>
              <span class="bg-charcoal text-cream font-body text-[10px] uppercase tracking-widest px-3 py-1">Custom Order</span>
            </div>
          </div>
          <div class="p-6">
            <div class="flex items-start justify-between mb-3">
              <div>
                <h3 class="font-display text-xl font-semibold text-bark">Executive Solid Desk</h3>
                <p class="font-body text-xs text-wood mt-0.5 uppercase tracking-wider">Suar / Rain Tree Wood</p>
              </div>
              <div class="w-8 h-8 rounded-full border border-wood/30 flex items-center justify-center shrink-0 mt-1">
                <div class="w-4 h-4 rounded-full" style="background: radial-gradient(circle at 35% 35%, #8b5442, #2c1a0e)"></div>
              </div>
            </div>
            <p class="font-body text-sm text-charcoal-light font-light leading-relaxed">
              A desk that commands presence. Book-matched slab top, dovetail-jointed solid drawers, and a satin matte lacquer finish built for decades.
            </p>
            <div class="mt-5 pt-5 border-t border-grain grid grid-cols-3 gap-3 text-center">
              <div>
                <div class="font-display text-sm font-semibold text-bark">300 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Length</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">75 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Width</div>
              </div>
              <div>
                <div class="font-display text-sm font-semibold text-bark">75 cm</div>
                <div class="font-body text-[10px] text-charcoal-light uppercase tracking-wide">Height</div>
              </div>
            </div>
            <a href="#contact" class="mt-5 flex items-center justify-between text-wood hover:text-wood-dark font-body text-sm font-medium group/link">
              <span>Get a Custom Quote</span>
              <svg class="w-4 h-4 group-hover/link:translate-x-1 transition-transform" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
            </a>
          </div>
        </div>

      </div>

      <!-- Bottom note -->
      <p class="text-center font-body text-sm text-charcoal-light font-light mt-12 reveal">
        All dimensions are standard. <span class="text-wood font-medium">Custom sizes available</span> — contact us with your specifications.
      </p>
    </div>
  </section>


  <!-- ══════════════════════════════════════════
       ABOUT
  ══════════════════════════════════════════ -->
  <section id="about" class="py-28 px-6 lg:px-16 bg-bark overflow-hidden">
    <div class="max-w-7xl mx-auto grid lg:grid-cols-2 gap-16 items-center">

      <!-- Image collage -->
      <div class="relative reveal">
        <div class="aspect-[4/5] rounded-sm overflow-hidden">
          <img
            src="https://images.unsplash.com/photo-1504148455328-c376907d081c?w=900&q=85&auto=format&fit=crop"
            alt="Workshop"
            class="w-full h-full object-cover"
          />
        </div>
        <!-- Floating card -->
        <div class="absolute -bottom-6 -right-6 lg:-right-10 bg-wood p-6 w-48 shadow-2xl">
          <div class="font-display text-4xl font-semibold text-cream">15+</div>
          <div class="font-body text-xs uppercase tracking-[.15em] text-sand mt-1">Years of Mastery</div>
          <div class="w-8 h-px bg-sand/50 mt-3"></div>
          <div class="font-body text-xs text-cream/70 mt-2 font-light leading-relaxed">Jepara, Central Java</div>
        </div>
        <!-- Grain texture overlay on image -->
        <div class="absolute inset-0 rounded-sm pointer-events-none" style="background:url('data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 width=%22100%22 height=%22100%22><filter id=%22n%22><feTurbulence baseFrequency=%220.65%22 numOctaves=%222%22/></filter><rect width=%22100%25%22 height=%22100%25%22 filter=%22url(%23n)%22 opacity=%220.04%22/></svg>');"></div>
      </div>

      <!-- Text -->
      <div class="reveal" style="transition-delay:.1s">
        <div class="flex items-center gap-3 mb-8">
          <span class="w-8 h-px bg-sand"></span>
          <span class="font-body text-xs uppercase tracking-[.25em] text-sand font-medium">Our Story</span>
        </div>
        <h2 class="font-display text-4xl sm:text-5xl font-light text-cream leading-tight mb-6">
          Shaped by Hands,<br/><em class="font-semibold not-italic text-sand">Rooted in Forest</em>
        </h2>
        <p class="font-body text-cream/70 font-light text-base leading-relaxed mb-5">
          Karya Indah Furniture was founded in Jepara with a single belief: the most beautiful furniture is the kind that shows where it came from. We work exclusively with sustainably sourced Suar (Rain Tree) and Trembesi wood from Indonesian forests.
        </p>
        <p class="font-body text-cream/70 font-light text-base leading-relaxed mb-8">
          Every slab is hand-selected, air-dried for a minimum of two years, and shaped by craftsmen who have spent their lives learning the language of wood. The result is furniture that ages — and improves — with the decades.
        </p>

        <!-- Values -->
        <div class="grid grid-cols-2 gap-5">
          <div class="border border-sand/20 p-4">
            <div class="w-8 h-8 bg-wood rounded-sm flex items-center justify-center mb-3">
              <svg class="w-4 h-4 text-sand" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87L18.18 21 12 17.77 5.82 21 7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
            </div>
            <div class="font-display text-base font-semibold text-cream mb-1">Sustainably Sourced</div>
            <div class="font-body text-xs text-cream/55 font-light leading-relaxed">FSC-certified supply chains, replanting partnerships</div>
          </div>
          <div class="border border-sand/20 p-4">
            <div class="w-8 h-8 bg-wood rounded-sm flex items-center justify-center mb-3">
              <svg class="w-4 h-4 text-sand" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
            </div>
            <div class="font-display text-base font-semibold text-cream mb-1">Export Ready</div>
            <div class="font-body text-xs text-cream/55 font-light leading-relaxed">ISPM-15 heat treatment, full phytosanitary docs</div>
          </div>
          <div class="border border-sand/20 p-4">
            <div class="w-8 h-8 bg-wood rounded-sm flex items-center justify-center mb-3">
              <svg class="w-4 h-4 text-sand" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M3 7l9-5 9 5v10l-9 5-9-5V7z"/></svg>
            </div>
            <div class="font-display text-base font-semibold text-cream mb-1">Custom Dimensions</div>
            <div class="font-body text-xs text-cream/55 font-light leading-relaxed">Any size, any finish — designed to your blueprint</div>
          </div>
          <div class="border border-sand/20 p-4">
            <div class="w-8 h-8 bg-wood rounded-sm flex items-center justify-center mb-3">
              <svg class="w-4 h-4 text-sand" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2M12 11a4 4 0 100-8 4 4 0 000 8z"/></svg>
            </div>
            <div class="font-display text-base font-semibold text-cream mb-1">Master Craftsmen</div>
            <div class="font-body text-xs text-cream/55 font-light leading-relaxed">Multi-generational woodworkers, hand-finishing only</div>
          </div>
        </div>
      </div>
    </div>
  </section>


  <!-- ══════════════════════════════════════════
       CONTACT
  ══════════════════════════════════════════ -->
  <section id="contact" class="py-28 px-6 lg:px-16 bg-cream">
    <div class="max-w-6xl mx-auto">

      <!-- Header -->
      <div class="text-center mb-16 reveal">
        <div class="ornament mb-5">
          <span class="font-body text-xs uppercase tracking-[.25em] text-wood font-medium whitespace-nowrap">Get In Touch</span>
        </div>
        <h2 class="font-display text-4xl sm:text-5xl lg:text-6xl font-light text-bark leading-tight">
          Let's Build<br/><em class="font-semibold not-italic">Something Lasting</em>
        </h2>
        <p class="font-body text-charcoal-light font-light mt-4 max-w-lg mx-auto">
          Whether you're a retailer, interior designer, or end buyer — we're here to help you find (or build) the perfect piece.
        </p>
      </div>

      <div class="grid lg:grid-cols-5 gap-12">

        <!-- Left: Info -->
        <div class="lg:col-span-2 reveal">
          <!-- WA button -->
          <a
            href="https://wa.me/6282314962511?text=Hello%2C%20I%20am%20interested%20in%20your%20furniture%20products."
            target="_blank"
            class="wa-pulse flex items-center gap-4 bg-[#25D366] hover:bg-[#1fbe5a] text-white rounded-sm px-6 py-4 mb-8 transition-colors duration-300"
          >
            <svg class="w-7 h-7 shrink-0" viewBox="0 0 24 24" fill="currentColor">
              <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
            </svg>
            <div>
              <div class="font-body font-semibold text-base">Chat via WhatsApp</div>
              <div class="font-body text-xs opacity-85 font-light">Quick response — usually within 1 hour</div>
            </div>
          </a>

          <!-- Contact details -->
          <div class="space-y-5">
            <div class="flex items-start gap-4">
              <div class="w-9 h-9 bg-wood/10 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                <svg class="w-4 h-4 text-wood" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/></svg>
              </div>
              <div>
                <div class="font-body text-xs uppercase tracking-widest text-charcoal-light mb-0.5">Phone / WA</div>
                <div class="font-body text-sm text-charcoal font-medium">+62 823-1496-2511</div>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <div class="w-9 h-9 bg-wood/10 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                <svg class="w-4 h-4 text-wood" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
              </div>
              <div>
                <div class="font-body text-xs uppercase tracking-widest text-charcoal-light mb-0.5">Email</div>
                <div class="font-body text-sm text-charcoal font-medium">karyaindahfurniture93@gmail.com</div>
              </div>
            </div>
            <div class="flex items-start gap-4">
              <div class="w-9 h-9 bg-wood/10 rounded-sm flex items-center justify-center shrink-0 mt-0.5">
                <svg class="w-4 h-4 text-wood" fill="none" stroke="currentColor" stroke-width="1.8" viewBox="0 0 24 24"><path d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/><circle cx="12" cy="11" r="3"/></svg>
              </div>
              <div>
                <div class="font-body text-xs uppercase tracking-widest text-charcoal-light mb-0.5">Workshop</div>
                <div class="font-body text-sm text-charcoal font-medium">Jl. Shima, Mulyoharjo, Kec. Jepara,<br/>Jepara 59431</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Right: Form -->
        <div class="lg:col-span-3 reveal" style="transition-delay:.1s">
          <div class="bg-white p-8 lg:p-10 shadow-sm">
            <h3 class="font-display text-2xl font-semibold text-bark mb-6">Send an Inquiry</h3>

            <div id="form-success" class="hidden bg-wood/10 border border-wood/30 text-wood font-body text-sm px-5 py-4 mb-6 rounded-sm">
              ✓ Thank you! We'll get back to you within 24 hours.
            </div>

            <form id="inquiry-form" class="space-y-5" novalidate>
              <div class="grid sm:grid-cols-2 gap-5">
                <div>
                  <label class="font-body text-xs uppercase tracking-widest text-charcoal-light block mb-2">Full Name *</label>
                  <input type="text" name="name" placeholder="Your name"
                    class="w-full border border-grain bg-cream font-body text-sm text-charcoal px-4 py-3 placeholder:text-charcoal-light/50 transition-all" required>
                </div>
                <div>
                  <label class="font-body text-xs uppercase tracking-widest text-charcoal-light block mb-2">Email Address *</label>
                  <input type="email" name="email" placeholder="you@company.com"
                    class="w-full border border-grain bg-cream font-body text-sm text-charcoal px-4 py-3 placeholder:text-charcoal-light/50 transition-all" required>
                </div>
              </div>
              <div class="grid sm:grid-cols-2 gap-5">
                <div>
                  <label class="font-body text-xs uppercase tracking-widest text-charcoal-light block mb-2">Phone / WhatsApp</label>
                  <input type="tel" name="phone" placeholder="+62 ..."
                    class="w-full border border-grain bg-cream font-body text-sm text-charcoal px-4 py-3 placeholder:text-charcoal-light/50 transition-all">
                </div>
                <div>
                  <label class="font-body text-xs uppercase tracking-widest text-charcoal-light block mb-2">Product Interest</label>
                  <select name="product" class="w-full border border-grain bg-cream font-body text-sm text-charcoal px-4 py-3 transition-all">
                    <option value="">Select a product...</option>
                    <option>Solid Suar Dining Table</option>
                    <option>Live Edge Coffee Table</option>
                    <option>Executive Solid Desk</option>
                    <option>Custom Order</option>
                    <option>Wholesale / Export</option>
                  </select>
                </div>
              </div>
              <div>
                <label class="font-body text-xs uppercase tracking-widest text-charcoal-light block mb-2">Message / Specifications *</label>
                <textarea name="message" rows="4" placeholder="Describe your requirements — dimensions, quantity, finish, destination country..."
                  class="w-full border border-grain bg-cream font-body text-sm text-charcoal px-4 py-3 placeholder:text-charcoal-light/50 transition-all resize-none" required></textarea>
              </div>
              <button
                type="submit"
                id="submit-btn"
                class="w-full bg-wood hover:bg-wood-dark text-cream font-body font-medium text-sm py-4 transition-colors duration-300 flex items-center justify-center gap-2"
              >
                <span id="btn-text">Send Inquiry</span>
                <svg id="btn-arrow" class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
                <svg id="btn-spinner" class="w-4 h-4 animate-spin hidden" fill="none" viewBox="0 0 24 24"><circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"/><path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8v8H4z"/></svg>
              </button>
            </form>
          </div>
        </div>

      </div>
    </div>
  </section>


  <!-- ══════════════════════════════════════════
       FOOTER
  ══════════════════════════════════════════ -->
  <footer class="bg-bark text-cream/70 font-body">

    <!-- Main footer -->
    <div class="max-w-7xl mx-auto px-6 lg:px-16 py-16 grid sm:grid-cols-2 lg:grid-cols-4 gap-10">

      <!-- Brand -->
      <div class="lg:col-span-2">
        <div class="flex items-center gap-3 mb-4">
          <div class="w-9 h-9 bg-wood rounded-sm flex items-center justify-center shrink-0">
            <svg viewBox="0 0 32 32" class="w-5 h-5 fill-cream">
              <path d="M4 28V10l12-6 12 6v18H20v-8h-8v8H4z"/>
            </svg>
          </div>
          <div>
            <div class="font-display text-lg font-semibold text-cream">Karya Indah Furniture</div>
            <div class="font-body text-[9px] uppercase tracking-[.2em] text-sand -mt-0.5">Premium Solid Wood</div>
          </div>
        </div>
        <p class="text-sm font-light leading-relaxed max-w-xs text-cream/55 mt-4">
          Crafting heirloom-quality solid Suar and Trembesi wood furniture since 2009. Export-ready, sustainably sourced, masterfully built.
        </p>
        <!-- Socials -->
        <div class="flex gap-3 mt-6">
          <a href="#" class="w-9 h-9 border border-cream/20 hover:border-sand hover:text-sand flex items-center justify-center transition-colors" aria-label="Instagram">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          </a>
          <a href="#" class="w-9 h-9 border border-cream/20 hover:border-sand hover:text-sand flex items-center justify-center transition-colors" aria-label="Facebook">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
          </a>
          <a href="https://wa.me/6282314962511" class="w-9 h-9 border border-cream/20 hover:border-[#25D366] hover:text-[#25D366] flex items-center justify-center transition-colors" aria-label="WhatsApp">
            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
          </a>
        </div>
      </div>

      <!-- Quick Links -->
      <div>
        <h4 class="font-body text-xs uppercase tracking-[.2em] text-sand mb-5">Quick Links</h4>
        <ul class="space-y-3 text-sm">
          <li><a href="#home"     class="hover:text-sand transition-colors">Home</a></li>
          <li><a href="#products" class="hover:text-sand transition-colors">Products</a></li>
          <li><a href="#about"    class="hover:text-sand transition-colors">About Us</a></li>
          <li><a href="#contact"  class="hover:text-sand transition-colors">Contact</a></li>
          <li><a href="#contact"  class="hover:text-sand transition-colors">Request Quote</a></li>
        </ul>
      </div>

      <!-- Products -->
      <div>
        <h4 class="font-body text-xs uppercase tracking-[.2em] text-sand mb-5">Products</h4>
        <ul class="space-y-3 text-sm">
          <li><a href="#products" class="hover:text-sand transition-colors">Suar Dining Tables</a></li>
          <li><a href="#products" class="hover:text-sand transition-colors">Live Edge Coffee Tables</a></li>
          <li><a href="#products" class="hover:text-sand transition-colors">Executive Desks</a></li>
          <li><a href="#contact"  class="hover:text-sand transition-colors">Custom Orders</a></li>
          <li><a href="#contact"  class="hover:text-sand transition-colors">Wholesale / Export</a></li>
        </ul>
      </div>
    </div>

    <!-- Bottom bar -->
    <div class="border-t border-cream/10 px-6 lg:px-16 py-5">
      <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-3 text-xs text-cream/35">
        <span>© 2024 Karya Indah Furniture. All rights reserved.</span>
        <span>Jepara, Central Java, Indonesia</span>
      </div>
    </div>
  </footer>


  <!-- ══════════════════════════════════════════
       JAVASCRIPT
  ══════════════════════════════════════════ -->
  <script>
    // ── Navbar scroll ──
    const navbar = document.getElementById('navbar');
    const scrollProgress = document.getElementById('scroll-progress');
    window.addEventListener('scroll', () => {
      const scrolled = window.scrollY;
      const total = document.documentElement.scrollHeight - window.innerHeight;
      scrollProgress.style.width = (scrolled / total * 100) + '%';
      navbar.classList.toggle('scrolled', scrolled > 60);
    });

    // ── Mobile menu ──
    const toggle = document.getElementById('menu-toggle');
    const menu   = document.getElementById('mobile-menu');
    const iconMenu  = document.getElementById('icon-menu');
    const iconClose = document.getElementById('icon-close');
    toggle.addEventListener('click', () => {
      const open = menu.classList.toggle('open');
      iconMenu.classList.toggle('hidden', open);
      iconClose.classList.toggle('hidden', !open);
    });
    document.querySelectorAll('.mobile-link, #mobile-menu a').forEach(a => {
      a.addEventListener('click', () => {
        menu.classList.remove('open');
        iconMenu.classList.remove('hidden');
        iconClose.classList.add('hidden');
      });
    });

    // ── Scroll reveal ──
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); } });
    }, { threshold: 0.12 });
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    // ── Form submit ──
    document.getElementById('inquiry-form').addEventListener('submit', function(e) {
      e.preventDefault();
      const btn     = document.getElementById('submit-btn');
      const text    = document.getElementById('btn-text');
      const arrow   = document.getElementById('btn-arrow');
      const spinner = document.getElementById('btn-spinner');
      btn.disabled = true;
      text.textContent = 'Sending…';
      arrow.classList.add('hidden');
      spinner.classList.remove('hidden');
      setTimeout(() => {
        btn.disabled = false;
        text.textContent = 'Send Inquiry';
        arrow.classList.remove('hidden');
        spinner.classList.add('hidden');
        document.getElementById('form-success').classList.remove('hidden');
        this.reset();
        setTimeout(() => document.getElementById('form-success').classList.add('hidden'), 5000);
      }, 1800);
    });

    // ── Nav active state on scroll ──
    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('.nav-link');
    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(s => {
        if (window.scrollY >= s.offsetTop - 120) current = s.id;
      });
      navLinks.forEach(link => {
        link.style.color = link.getAttribute('href') === '#' + current ? '#6B3A2A' : '';
      });
    });
  </script>

</body>
</html>
