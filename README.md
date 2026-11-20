import math

def generate_dong_son_banner():
    width, height = 1200, 320
    cx, cy = 235, 160  # Center of the Dong Son drum on the left
    
    svg_parts = []
    svg_parts.append(f'''<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 {width} {height}" width="100%" height="100%">
  <defs>
    <!-- Aurora Deep Space Background Gradient -->
    <linearGradient id="bgGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#070A12"/>
      <stop offset="45%" stop-color="#0F172A"/>
      <stop offset="78%" stop-color="#1E1B4B"/>
      <stop offset="100%" stop-color="#082F49"/>
    </linearGradient>

    <!-- Border Gradient -->
    <linearGradient id="borderGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#F59E0B" stop-opacity="0.7"/>
      <stop offset="50%" stop-color="#38BDF8" stop-opacity="0.8"/>
      <stop offset="100%" stop-color="#818CF8" stop-opacity="0.6"/>
    </linearGradient>

    <!-- Dong Son Gold Gradient -->
    <linearGradient id="goldGrad" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" stop-color="#FEF08A"/>
      <stop offset="45%" stop-color="#F59E0B"/>
      <stop offset="100%" stop-color="#B45309"/>
    </linearGradient>

    <!-- Cyber Cyan Gradient -->
    <linearGradient id="cyanGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#38BDF8"/>
      <stop offset="100%" stop-color="#818CF8"/>
    </linearGradient>

    <!-- Radial Aura Behind Drum -->
    <radialGradient id="drumAura" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#F59E0B" stop-opacity="0.28"/>
      <stop offset="45%" stop-color="#38BDF8" stop-opacity="0.14"/>
      <stop offset="100%" stop-color="#070A12" stop-opacity="0"/>
    </radialGradient>

    <!-- Radial Aura Behind Title -->
    <radialGradient id="textAura" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#38BDF8" stop-opacity="0.16"/>
      <stop offset="60%" stop-color="#818CF8" stop-opacity="0.06"/>
      <stop offset="100%" stop-color="#070A12" stop-opacity="0"/>
    </radialGradient>

    <!-- Soft Glow Filter -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="2.5" result="blur"/>
      <feMerge>
        <feMergeNode in="blur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Subtle Cyber Grid Pattern -->
    <pattern id="cyberGrid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#38BDF8" stroke-width="0.5" stroke-opacity="0.07"/>
    </pattern>

    <clipPath id="cardClip">
      <rect x="1" y="1" width="{width-2}" height="{height-2}" rx="16"/>
    </clipPath>

    <style>
      .spin-cw {{
        transform-origin: {cx}px {cy}px;
        animation: spinCW 75s linear infinite;
      }}
      .spin-ccw {{
        transform-origin: {cx}px {cy}px;
        animation: spinCCW 110s linear infinite;
      }}
      .pulse-core {{
        transform-origin: {cx}px {cy}px;
        animation: pulseCore 4s ease-in-out infinite;
      }}
      @keyframes spinCW {{
        from {{ transform: rotate(0deg); }}
        to   {{ transform: rotate(360deg); }}
      }}
      @keyframes spinCCW {{
        from {{ transform: rotate(360deg); }}
        to   {{ transform: rotate(0deg); }}
      }}
      @keyframes pulseCore {{
        0%, 100% {{ opacity: 0.88; }}
        50%      {{ opacity: 1; }}
      }}
      .title-text {{
        font-family: 'Segoe UI', -apple-system, BlinkMacSystemFont, Roboto, Helvetica, Arial, sans-serif;
        font-weight: 800;
        letter-spacing: 3.5px;
      }}
      .mono-text {{
        font-family: 'JetBrains Mono', 'Fira Code', 'SFMono-Regular', Consolas, monospace;
      }}
    </style>
  </defs>

  <!-- Base Card -->
  <g clip-path="url(#cardClip)">
    <rect width="{width}" height="{height}" fill="url(#bgGrad)"/>
    <rect width="{width}" height="{height}" fill="url(#cyberGrid)"/>

    <!-- Ambient Glows -->
    <circle cx="{cx}" cy="{cy}" r="230" fill="url(#drumAura)"/>
    <ellipse cx="780" cy="150" rx="340" ry="140" fill="url(#textAura)"/>

    <!-- Futuristic Circuit Traces Connecting Drum to Right Panel -->
    <g stroke="#38BDF8" stroke-opacity="0.22" stroke-width="1.2" fill="none">
      <path d="M 395 95 L 455 95 L 480 70 L 1140 70"/>
      <path d="M 412 135 L 465 135 L 485 115 L 530 115"/>
      <path d="M 412 185 L 465 185 L 485 205 L 530 205"/>
      <path d="M 395 225 L 455 225 L 480 250 L 1140 250"/>
    </g>
    <!-- Circuit Nodes -->
    <g fill="#38BDF8" fill-opacity="0.6">
      <circle cx="480" cy="70" r="2.5"/>
      <circle cx="530" cy="115" r="2.5"/>
      <circle cx="530" cy="205" r="2.5"/>
      <circle cx="480" cy="250" r="2.5"/>
    </g>
    <g fill="#F59E0B" fill-opacity="0.75">
      <circle cx="1140" cy="70" r="2.5"/>
      <circle cx="1140" cy="250" r="2.5"/>
    </g>
''')

    # --- DONG SON BRONZE DRUM VECTOR ARTWORK ---
    # 1. Outer Static Cyber HUD Frame around Drum
    svg_parts.append(f'''
    <!-- Outer Cyber HUD Ring -->
    <circle cx="{cx}" cy="{cy}" r="186" fill="none" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.25" stroke-dasharray="6 6"/>
    <circle cx="{cx}" cy="{cy}" r="176" fill="none" stroke="url(#goldGrad)" stroke-width="1.5" stroke-opacity="0.65"/>
    <circle cx="{cx}" cy="{cy}" r="168" fill="none" stroke="#38BDF8" stroke-width="0.8" stroke-opacity="0.35"/>
''')

    # HUD Degree Ticks on outer ring
    ticks = []
    for deg in range(0, 360, 15):
        rad = math.radians(deg)
        r1 = 176
        r2 = 183 if deg % 45 == 0 else 180
        x1, y1 = cx + r1 * math.cos(rad), cy + r1 * math.sin(rad)
        x2, y2 = cx + r2 * math.cos(rad), cy + r2 * math.sin(rad)
        col = "#F59E0B" if deg % 45 == 0 else "#38BDF8"
        op = "0.8" if deg % 45 == 0 else "0.35"
        ticks.append(f'<line x1="{x1:.1f}" y1="{y1:.1f}" x2="{x2:.1f}" y2="{y2:.1f}" stroke="{col}" stroke-width="1.2" stroke-opacity="{op}"/>')
    svg_parts.append("    " + "\n    ".join(ticks))

    # 2. Rotating Band 1: Lac Birds (Chim Lac) + Geometric Ring (r=118 to r=164)
    svg_parts.append(f'''
    <g class="spin-ccw">
      <circle cx="{cx}" cy="{cy}" r="162" fill="none" stroke="#F59E0B" stroke-width="1" stroke-opacity="0.5"/>
      <circle cx="{cx}" cy="{cy}" r="120" fill="none" stroke="#F59E0B" stroke-width="1.2" stroke-opacity="0.6"/>
''')
    # Sawtooth band between r=154 and r=162
    saw_outer = []
    n_teeth_outer = 72
    for i in range(n_teeth_outer):
        a1 = 2 * math.pi * i / n_teeth_outer
        a2 = 2 * math.pi * (i + 0.5) / n_teeth_outer
        a3 = 2 * math.pi * (i + 1) / n_teeth_outer
        x1, y1 = cx + 154 * math.cos(a1), cy + 154 * math.sin(a1)
        x2, y2 = cx + 161 * math.cos(a2), cy + 161 * math.sin(a2)
        x3, y3 = cx + 154 * math.cos(a3), cy + 154 * math.sin(a3)
        saw_outer.append(f"M {x1:.1f} {y1:.1f} L {x2:.1f} {y2:.1f} L {x3:.1f} {y3:.1f}")
    svg_parts.append(f'      <path d="{" ".join(saw_outer)}" fill="none" stroke="#F59E0B" stroke-width="0.9" stroke-opacity="0.55"/>')

    # 6 Stylized Lac Birds flying counter-clockwise at r=137
    for b in range(6):
        angle_deg = b * 60
        # Place bird at radius 137 along angle_deg, oriented tangentially
        rad = math.radians(angle_deg)
        bx = cx + 137 * math.cos(rad)
        by = cy + 137 * math.sin(rad)
        rot = angle_deg - 90
        svg_parts.append(f'''      <g transform="translate({bx:.1f},{by:.1f}) rotate({rot:.1f})" filter="url(#glow)">
        <!-- Stylized Lac Bird: long beak, crest, sweeping wings, forked tail -->
        <path d="M 18 0 L 6 -2.5 L 2 -1.5 L -4 -12 L -7 -10 L -3 -1 L -14 -4 L -11 0 L -15 4 L -3 1 L -6 11 L -3 12 L 2 1.5 L 6 2.5 Z" fill="url(#goldGrad)" fill-opacity="0.9"/>
        <path d="M 3 -2 C 0 -6, -4 -6, -6 -4" fill="none" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.85"/>
      </g>''')

    # Small tangent dotted circles between birds
    for b in range(6):
        angle_deg = b * 60 + 30
        rad = math.radians(angle_deg)
        dx = cx + 137 * math.cos(rad)
        dy = cy + 137 * math.sin(rad)
        svg_parts.append(f'      <circle cx="{dx:.1f}" cy="{dy:.1f}" r="5.5" fill="none" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.65"/>')
        svg_parts.append(f'      <circle cx="{dx:.1f}" cy="{dy:.1f}" r="1.8" fill="#FDE047"/>')

    svg_parts.append("    </g>")

    # 3. Rotating Band 2: Inner Geometric Sawtooth & Dot Ring (r=66 to r=114)
    svg_parts.append(f'''
    <g class="spin-cw">
      <circle cx="{cx}" cy="{cy}" r="113" fill="none" stroke="#38BDF8" stroke-width="1" stroke-opacity="0.55"/>
      <circle cx="{cx}" cy="{cy}" r="96" fill="none" stroke="#F59E0B" stroke-width="1" stroke-opacity="0.55"/>
      <circle cx="{cx}" cy="{cy}" r="74" fill="none" stroke="#F59E0B" stroke-width="1.3" stroke-opacity="0.75"/>
''')
    # Concentric circle motifs in r=96..113
    n_circles = 24
    for i in range(n_circles):
        a = 2 * math.pi * i / n_circles
        rx = cx + 104.5 * math.cos(a)
        ry = cy + 104.5 * math.sin(a)
        svg_parts.append(f'      <circle cx="{rx:.1f}" cy="{ry:.1f}" r="4.2" fill="none" stroke="#38BDF8" stroke-width="0.9" stroke-opacity="0.65"/>')
        svg_parts.append(f'      <circle cx="{rx:.1f}" cy="{ry:.1f}" r="1.2" fill="#FDE047" fill-opacity="0.85"/>')

    # Inner comb-teeth / sawtooth band in r=76..94
    saw_inner = []
    n_teeth_inner = 48
    for i in range(n_teeth_inner):
        a1 = 2 * math.pi * i / n_teeth_inner
        a2 = 2 * math.pi * (i + 0.5) / n_teeth_inner
        a3 = 2 * math.pi * (i + 1) / n_teeth_inner
        x1, y1 = cx + 76 * math.cos(a1), cy + 76 * math.sin(a1)
        x2, y2 = cx + 93 * math.cos(a2), cy + 93 * math.sin(a2)
        x3, y3 = cx + 76 * math.cos(a3), cy + 76 * math.sin(a3)
        saw_inner.append(f"M {x1:.1f} {y1:.1f} L {x2:.1f} {y2:.1f} L {x3:.1f} {y3:.1f}")
    svg_parts.append(f'      <path d="{" ".join(saw_inner)}" fill="none" stroke="#F59E0B" stroke-width="1" stroke-opacity="0.65"/>')
    svg_parts.append("    </g>")

    # 4. Central 14-Ray Dong Son Sun Star (Ngôi sao 14 cánh)
    svg_parts.append('    <g class="pulse-core" filter="url(#glow)">')
    n_rays = 14
    star_pts = []
    for i in range(n_rays * 2):
        r = 66 if i % 2 == 0 else 25
        a = 2 * math.pi * i / (n_rays * 2) - math.pi / 2
        px = cx + r * math.cos(a)
        py = cy + r * math.sin(a)
        star_pts.append(f"{px:.1f},{py:.1f}")
    svg_parts.append(f'      <polygon points="{" ".join(star_pts)}" fill="url(#goldGrad)" fill-opacity="0.92" stroke="#FEF08A" stroke-width="0.8"/>')

    # Inter-ray geometric peacock-feather triangles (hoa văn lông công xen giữa cánh sao)
    for i in range(n_rays):
        a_mid = 2 * math.pi * (i + 0.5) / n_rays - math.pi / 2
        a_left = 2 * math.pi * (i + 0.22) / n_rays - math.pi / 2
        a_right = 2 * math.pi * (i + 0.78) / n_rays - math.pi / 2
        tx1, ty1 = cx + 63 * math.cos(a_left), cy + 63 * math.sin(a_left)
        tx2, ty2 = cx + 63 * math.cos(a_right), cy + 63 * math.sin(a_right)
        tx3, ty3 = cx + 36 * math.cos(a_mid), cy + 36 * math.sin(a_mid)
        svg_parts.append(f'      <polygon points="{tx1:.1f},{ty1:.1f} {tx2:.1f},{ty2:.1f} {tx3:.1f},{ty3:.1f}" fill="none" stroke="#38BDF8" stroke-width="0.9" stroke-opacity="0.75"/>')

    # Sun Center Core
    svg_parts.append(f'      <circle cx="{cx}" cy="{cy}" r="18" fill="#0B0F19" stroke="#FDE047" stroke-width="2"/>')
    svg_parts.append(f'      <circle cx="{cx}" cy="{cy}" r="9" fill="url(#goldGrad)"/>')
    svg_parts.append('    </g>')

    # --- RIGHT SIDE: ENGINEER IDENTITY & TECH HUD ---
    tx = 495
    svg_parts.append(f'''
    <!-- Status Pill -->
    <g transform="translate({tx}, 86)">
      <rect x="0" y="0" width="338" height="24" rx="12" fill="#0F172A" stroke="#F59E0B" stroke-width="1" stroke-opacity="0.55"/>
      <circle cx="14" cy="12" r="4" fill="#38BDF8" filter="url(#glow)"/>
      <text x="26" y="16" fill="#FDE047" font-size="11" font-weight="600" letter-spacing="1.5" class="mono-text">VIETNAM HERITAGE // SYSTEM ONLINE</text>
    </g>

    <!-- Main Name -->
    <text x="{tx}" y="156" fill="#F8FAFC" font-size="40" class="title-text" filter="url(#glow)">LUONG QUANG DUNG</text>

    <!-- Subtitle -->
    <text x="{tx}" y="186" fill="#38BDF8" font-size="15" font-weight="600" letter-spacing="2.2" class="mono-text">GNUD  ·  BACKEND SOFTWARE DEVELOPER</text>

    <!-- Accent Line -->
    <rect x="{tx}" y="202" width="180" height="2" rx="1" fill="url(#cyanGrad)"/>
    <rect x="{tx + 188}" y="202" width="48" height="2" rx="1" fill="#F59E0B"/>

    <!-- Tech Stack Tags inside Banner -->
    <g transform="translate({tx}, 216)" class="mono-text" font-size="11" font-weight="600">
      <rect x="0" y="0" width="68" height="22" rx="6" fill="#0F172A" stroke="#38BDF8" stroke-opacity="0.45"/>
      <text x="34" y="15" fill="#E2E8F0" text-anchor="middle">.NET 8</text>

      <rect x="76" y="0" width="44" height="22" rx="6" fill="#0F172A" stroke="#38BDF8" stroke-opacity="0.45"/>
      <text x="98" y="15" fill="#E2E8F0" text-anchor="middle">C#</text>

      <rect x="128" y="0" width="158" height="22" rx="6" fill="#0F172A" stroke="#818CF8" stroke-opacity="0.45"/>
      <text x="207" y="15" fill="#E2E8F0" text-anchor="middle">CLEAN ARCHITECTURE</text>

      <rect x="294" y="0" width="122" height="22" rx="6" fill="#0F172A" stroke="#F59E0B" stroke-opacity="0.5"/>
      <text x="355" y="15" fill="#FDE047" text-anchor="middle">MICROSERVICES</text>

      <rect x="424" y="0" width="152" height="22" rx="6" fill="#0F172A" stroke="#38BDF8" stroke-opacity="0.45"/>
      <text x="500" y="15" fill="#94A3B8" text-anchor="middle">HO CHI MINH, VN</text>
    </g>
  </g>

  <!-- Outer Glowing Card Border -->
  <rect x="1" y="1" width="{width-2}" height="{height-2}" rx="16" fill="none" stroke="url(#borderGrad)" stroke-width="1.5"/>
</svg>''')

    return "\n".join(svg_parts)

svg_content = generate_dong_son_banner()
with open("banner.svg", "w", encoding="utf-8") as f:
    f.write(svg_content)

print("Generated banner.svg, length:", len(svg_content))
