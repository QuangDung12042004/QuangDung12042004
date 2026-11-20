<svg width="1200" height="320" viewBox="0 0 1200 320" fill="none" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Deep Obsidian Background Gradient -->
    <linearGradient id="bgGrad" x1="0" y1="0" x2="1200" y2="320" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#070B14" />
      <stop offset="45%" stop-color="#0D1322" />
      <stop offset="100%" stop-color="#080C16" />
    </linearGradient>

    <!-- Bronze Gold & Cyber Cyan Glows -->
    <radialGradient id="drumGlow" cx="245" cy="160" r="185" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#EAB308" stop-opacity="0.22" />
      <stop offset="55%" stop-color="#38BDF8" stop-opacity="0.10" />
      <stop offset="100%" stop-color="#070B14" stop-opacity="0" />
    </radialGradient>

    <radialGradient id="sunStarGrad" cx="245" cy="160" r="44" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#FEF08A" />
      <stop offset="55%" stop-color="#EAB308" />
      <stop offset="100%" stop-color="#B45309" />
    </radialGradient>

    <linearGradient id="goldCyanLine" x1="455" y1="0" x2="1080" y2="0" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#EAB308" />
      <stop offset="50%" stop-color="#38BDF8" />
      <stop offset="100%" stop-color="#38BDF8" stop-opacity="0" />
    </linearGradient>

    <linearGradient id="borderAccent" x1="0" y1="0" x2="1200" y2="0" gradientUnits="userSpaceOnUse">
      <stop offset="0%" stop-color="#0D1117" />
      <stop offset="22%" stop-color="#EAB308" stop-opacity="0.6" />
      <stop offset="55%" stop-color="#38BDF8" stop-opacity="0.6" />
      <stop offset="100%" stop-color="#0D1117" />
    </linearGradient>

    <pattern id="techGrid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#1E293B" stroke-width="0.6" stroke-opacity="0.45" />
    </pattern>
  </defs>

  <!-- Base Canvas -->
  <rect width="1200" height="320" rx="14" fill="url(#bgGrad)" />
  <rect width="1200" height="320" rx="14" fill="url(#techGrid)" />
  <circle cx="245" cy="160" r="185" fill="url(#drumGlow)" />

  <!-- Subtle Circuit Traces -->
  <g stroke="#1E293B" stroke-width="1.2" fill="none">
    <path d="M 392 110 H 440 L 456 94 H 1140" />
    <path d="M 398 160 H 435" stroke="#38BDF8" stroke-opacity="0.35" />
    <path d="M 385 215 H 440 L 458 233 H 920" />
  </g>
  <circle cx="456" cy="94" r="2.5" fill="#EAB308" />
  <circle cx="435" cy="160" r="2.5" fill="#38BDF8" />
  <circle cx="458" cy="233" r="2.5" fill="#38BDF8" />

  <!-- ==================== DONG SON BRONZE DRUM (CYBER VECTOR) ==================== -->
  <g id="dong-son-drum">
    <!-- Outer Rotating Holographic Cyber Ring -->
    <g>
      <circle cx="245" cy="160" r="146" stroke="#38BDF8" stroke-width="1.2" stroke-opacity="0.45" stroke-dasharray="48 16 8 16" />
      <circle cx="245" cy="160" r="138" stroke="#EAB308" stroke-width="1" stroke-opacity="0.5" stroke-dasharray="6 10" />
      <animateTransform attributeName="transform" type="rotate" from="0 245 160" to="360 245 160" dur="90s" repeatCount="indefinite" />
    </g>

    <!-- Drum Disc Base -->
    <circle cx="245" cy="160" r="130" fill="#090D16" stroke="#EAB308" stroke-width="1.5" stroke-opacity="0.75" />

    <!-- Outer Geometric Sawtooth & Dot Ring -->
    <circle cx="245" cy="160" r="122" stroke="#EAB308" stroke-width="3.5" stroke-opacity="0.45" stroke-dasharray="2 6" />
    <circle cx="245" cy="160" r="114" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.4" />

    <!-- Chim Lac Flight Corridor (Slow Counter-Rotation) -->
    <g>
      <!-- Top Lac Bird -->
      <path d="M 222 65 C 234 61, 248 62, 264 66 L 278 63 L 263 69 C 254 72, 246 72, 238 69 L 226 75 L 233 68 Z" fill="#FACC15" opacity="0.9" />
      <path d="M 243 64 L 235 54 L 249 63 Z" fill="#38BDF8" opacity="0.85" />

      <!-- Bottom Lac Bird -->
      <path d="M 268 255 C 256 259, 242 258, 226 254 L 212 257 L 227 251 C 236 248, 244 248, 252 251 L 264 245 L 257 252 Z" fill="#FACC15" opacity="0.9" />
      <path d="M 247 256 L 255 266 L 241 257 Z" fill="#38BDF8" opacity="0.85" />

      <!-- Right Lac Bird -->
      <path d="M 340 137 C 344 149, 343 163, 339 179 L 342 193 L 336 178 C 333 169, 333 161, 336 153 L 330 141 L 337 148 Z" fill="#FACC15" opacity="0.9" />
      <path d="M 341 158 L 351 150 L 342 164 Z" fill="#38BDF8" opacity="0.85" />

      <!-- Left Lac Bird -->
      <path d="M 150 183 C 146 171, 147 157, 151 141 L 148 127 L 154 142 C 157 151, 157 159, 154 167 L 160 179 L 153 172 Z" fill="#FACC15" opacity="0.9" />
      <path d="M 149 162 L 139 170 L 148 156 Z" fill="#38BDF8" opacity="0.85" />

      <!-- Diagonal Geometric Totem Markers -->
      <circle cx="311" cy="94" r="2.5" fill="#38BDF8" />
      <circle cx="311" cy="226" r="2.5" fill="#38BDF8" />
      <circle cx="179" cy="226" r="2.5" fill="#38BDF8" />
      <circle cx="179" cy="94" r="2.5" fill="#38BDF8" />

      <animateTransform attributeName="transform" type="rotate" from="360 245 160" to="0 245 160" dur="120s" repeatCount="indefinite" />
    </g>

    <!-- Inner Concentric Rings -->
    <circle cx="245" cy="160" r="76" stroke="#EAB308" stroke-width="1.2" stroke-opacity="0.65" />
    <circle cx="245" cy="160" r="68" stroke="#EAB308" stroke-width="3" stroke-opacity="0.5" stroke-dasharray="1.5 5" />
    <circle cx="245" cy="160" r="54" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.5" />
    <circle cx="245" cy="160" r="47" stroke="#EAB308" stroke-width="1" stroke-opacity="0.6" />

    <!-- Central 14-Pointed Dong Son Sun Star -->
    <polygon
      points="287,160 259.6,163.3 282.8,178.2 256.7,169.4 271.2,192.8 251.5,173.5 254.3,200.9 245,175 235.7,200.9 238.5,173.5 218.8,192.8 233.3,169.4 207.2,178.2 230.4,163.3 203,160 230.4,156.7 207.2,141.8 233.3,150.6 218.8,127.2 238.5,146.5 235.7,119.1 245,145 254.3,119.1 251.5,146.5 271.2,127.2 256.7,150.6 282.8,141.8 259.6,156.7"
      fill="url(#sunStarGrad)"
    />
    <circle cx="245" cy="160" r="11" fill="#090D16" stroke="#FEF08A" stroke-width="1.5" />
    <circle cx="245" cy="160" r="4.5" fill="#38BDF8" />
  </g>

  <!-- ==================== IDENTITY & TYPOGRAPHY ==================== -->
  <g font-family="'Segoe UI', 'Inter', -apple-system, BlinkMacSystemFont, sans-serif">
    <!-- Top Heritage Status Tag -->
    <text x="456" y="78" fill="#38BDF8" font-family="'JetBrains Mono', 'Fira Code', monospace" font-size="12.5" font-weight="600" letter-spacing="2.2">
      ◈ VIETNAM DIGITAL HERITAGE  //  HO CHI MINH CITY
    </text>

    <!-- Main Name -->
    <text x="454" y="136" fill="#F8FAFC" font-size="44" font-weight="800" letter-spacing="2">
      LUONG QUANG DUNG
    </text>

    <!-- Gold-to-Cyan Accent Bar -->
    <rect x="456" y="151" width="620" height="2.5" rx="1.25" fill="url(#goldCyanLine)" />

    <!-- Role & Alias -->
    <text x="456" y="182" fill="#EAB308" font-family="'JetBrains Mono', 'Fira Code', monospace" font-size="16" font-weight="600" letter-spacing="2.5">
      GNUD  ·  BACKEND SOFTWARE DEVELOPER
    </text>

    <!-- Sleek Tech Pills -->
    <g font-family="'JetBrains Mono', 'Fira Code', monospace" font-size="11.5" font-weight="600" letter-spacing="1">
      <rect x="456" y="206" width="116" height="30" rx="6" fill="#0F172A" stroke="#1E293B" stroke-width="1" />
      <text x="514" y="225" fill="#38BDF8" text-anchor="middle">C# / .NET 8</text>

      <rect x="582" y="206" width="142" height="30" rx="6" fill="#0F172A" stroke="#1E293B" stroke-width="1" />
      <text x="653" y="225" fill="#E2E8F0" text-anchor="middle">MICROSERVICES</text>

      <rect x="734" y="206" width="178" height="30" rx="6" fill="#0F172A" stroke="#1E293B" stroke-width="1" />
      <text x="823" y="225" fill="#E2E8F0" text-anchor="middle">CLEAN ARCHITECTURE</text>

      <rect x="922" y="206" width="178" height="30" rx="6" fill="#0F172A" stroke="#1E293B" stroke-width="1" />
      <text x="1011" y="225" fill="#EAB308" text-anchor="middle">DISTRIBUTED SYSTEMS</text>
    </g>
  </g>

  <!-- Corner HUD Brackets -->
  <g stroke="#38BDF8" stroke-width="1.5" stroke-opacity="0.5" fill="none">
    <path d="M 20 36 V 20 H 36" />
    <path d="M 1164 20 H 1180 V 36" />
    <path d="M 20 284 V 300 H 36" />
    <path d="M 1164 300 H 1180 V 284" />
  </g>

  <!-- Bottom Edge Highlight -->
  <rect x="0" y="317" width="1200" height="3" fill="url(#borderAccent)" />
</svg>
