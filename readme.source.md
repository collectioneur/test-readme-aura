# SMIL Animation Experiments

```aura width=860 height=280
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#06060e', borderRadius: 20, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <svg width="860" height="280" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <filter id="ab1" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="25">
          <animate attributeName="stdDeviation" values="20;50;30;45;20" dur="8s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <filter id="ab2" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="35">
          <animate attributeName="stdDeviation" values="35;18;50;22;35" dur="11s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <filter id="ab3" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="30">
          <animate attributeName="stdDeviation" values="28;55;20;40;28" dur="14s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
    </defs>
    <path fill="rgba(120,40,255,0.6)" filter="url(#ab1)">
      <animate attributeName="d"
        values="M100,200 C180,80 300,220 430,140 C530,80 650,200 760,140 L760,280 L100,280 Z;M100,140 C220,240 280,90 430,190 C550,250 700,90 760,180 L760,280 L100,280 Z;M100,180 C150,100 320,250 430,110 C520,200 700,70 760,160 L760,280 L100,280 Z;M100,200 C180,80 300,220 430,140 C530,80 650,200 760,140 L760,280 L100,280 Z"
        dur="12s" repeatCount="indefinite" />
    </path>
    <path fill="rgba(0,180,255,0.45)" filter="url(#ab2)">
      <animate attributeName="d"
        values="M50,220 C150,100 280,240 430,160 C560,100 680,220 810,150 L810,280 L50,280 Z;M50,160 C200,260 260,100 430,200 C540,110 720,240 810,170 L810,280 L50,280 Z;M50,190 C120,120 310,260 430,120 C580,220 660,90 810,190 L810,280 L50,280 Z;M50,220 C150,100 280,240 430,160 C560,100 680,220 810,150 L810,280 L50,280 Z"
        dur="16s" repeatCount="indefinite" />
    </path>
    <path fill="rgba(255,50,160,0.35)" filter="url(#ab3)">
      <animate attributeName="d"
        values="M0,240 C120,130 260,260 430,170 C580,110 700,250 860,150 L860,280 L0,280 Z;M0,170 C100,260 300,110 430,210 C560,270 720,110 860,200 L860,280 L0,280 Z;M0,200 C160,120 280,250 430,140 C530,240 680,100 860,170 L860,280 L0,280 Z;M0,240 C120,130 260,260 430,170 C580,110 700,250 860,150 L860,280 L0,280 Z"
        dur="20s" repeatCount="indefinite" />
    </path>
    <path fill="rgba(255,200,50,0.2)" filter="url(#ab1)">
      <animate attributeName="d"
        values="M200,250 C280,150 380,260 500,180 C600,120 720,230 830,170 L830,280 L200,280 Z;M200,190 C300,270 350,130 500,210 C610,150 740,250 830,190 L830,280 L200,280 Z;M200,220 C260,140 400,260 500,150 C580,230 700,110 830,180 L830,280 L200,280 Z;M200,250 C280,150 380,260 500,180 C600,120 720,230 830,170 L830,280 L200,280 Z"
        dur="14s" repeatCount="indefinite" begin="2s" />
    </path>
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{ fontSize: 30, fontWeight: 700, color: 'white', letterSpacing: '-0.5px' }}>Morphing Aurora</span>
    <span style={{ fontSize: 12, color: 'rgba(200,200,255,0.5)', marginTop: 6 }}>SMIL path morphing + animated Gaussian blur pulsation</span>
  </div>
</div>
```

```aura width=860 height=240
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#08080e', borderRadius: 18, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <svg width="860" height="240" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <filter id="np-glow" x="-100%" y="-100%" width="300%" height="300%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="5">
          <animate attributeName="stdDeviation" values="3;8;3" dur="3s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <filter id="np-glow-lg" x="-100%" y="-100%" width="300%" height="300%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="12">
          <animate attributeName="stdDeviation" values="8;18;8" dur="5s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
    </defs>
    <line x1="130" y1="70" x2="300" y2="120" stroke="rgba(100,180,255,0.25)" strokeWidth="1">
      <animate attributeName="opacity" values="0.08;0.5;0.08" dur="3s" repeatCount="indefinite" />
    </line>
    <line x1="300" y1="120" x2="430" y2="55" stroke="rgba(180,100,255,0.25)" strokeWidth="1">
      <animate attributeName="opacity" values="0.08;0.5;0.08" dur="4s" repeatCount="indefinite" begin="0.5s" />
    </line>
    <line x1="430" y1="55" x2="580" y2="140" stroke="rgba(100,255,200,0.25)" strokeWidth="1">
      <animate attributeName="opacity" values="0.08;0.5;0.08" dur="3.5s" repeatCount="indefinite" begin="1s" />
    </line>
    <line x1="580" y1="140" x2="730" y2="75" stroke="rgba(255,150,100,0.25)" strokeWidth="1">
      <animate attributeName="opacity" values="0.08;0.5;0.08" dur="4.5s" repeatCount="indefinite" begin="0.3s" />
    </line>
    <line x1="130" y1="70" x2="430" y2="55" stroke="rgba(200,100,255,0.12)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.03;0.25;0.03" dur="5s" repeatCount="indefinite" begin="0.7s" />
    </line>
    <line x1="300" y1="120" x2="580" y2="140" stroke="rgba(100,200,255,0.12)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.03;0.25;0.03" dur="6s" repeatCount="indefinite" begin="1.2s" />
    </line>
    <line x1="430" y1="55" x2="730" y2="75" stroke="rgba(255,200,100,0.12)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.03;0.25;0.03" dur="5.5s" repeatCount="indefinite" begin="0.9s" />
    </line>
    <line x1="200" y1="180" x2="300" y2="120" stroke="rgba(140,140,255,0.1)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.02;0.2;0.02" dur="5s" repeatCount="indefinite" begin="1.5s" />
    </line>
    <line x1="500" y1="185" x2="580" y2="140" stroke="rgba(200,140,255,0.1)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.02;0.2;0.02" dur="4.5s" repeatCount="indefinite" begin="0.8s" />
    </line>
    <line x1="650" y1="175" x2="730" y2="75" stroke="rgba(140,255,200,0.1)" strokeWidth="0.5">
      <animate attributeName="opacity" values="0.02;0.2;0.02" dur="5.5s" repeatCount="indefinite" begin="2s" />
    </line>
    <circle cx="130" cy="70" r="4" fill="rgba(100,180,255,0.9)" filter="url(#np-glow)">
      <animate attributeName="r" values="3;9;3" dur="2.5s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0.5;1;0.5" dur="2.5s" repeatCount="indefinite" />
    </circle>
    <circle cx="300" cy="120" r="4" fill="rgba(180,100,255,0.9)" filter="url(#np-glow)">
      <animate attributeName="r" values="3;10;3" dur="3s" repeatCount="indefinite" begin="0.4s" />
      <animate attributeName="opacity" values="0.5;1;0.5" dur="3s" repeatCount="indefinite" begin="0.4s" />
    </circle>
    <circle cx="430" cy="55" r="4" fill="rgba(100,255,200,0.9)" filter="url(#np-glow)">
      <animate attributeName="r" values="3;8;3" dur="2.8s" repeatCount="indefinite" begin="0.8s" />
      <animate attributeName="opacity" values="0.5;1;0.5" dur="2.8s" repeatCount="indefinite" begin="0.8s" />
    </circle>
    <circle cx="580" cy="140" r="4" fill="rgba(255,150,100,0.9)" filter="url(#np-glow)">
      <animate attributeName="r" values="3;9;3" dur="3.3s" repeatCount="indefinite" begin="1.2s" />
      <animate attributeName="opacity" values="0.5;1;0.5" dur="3.3s" repeatCount="indefinite" begin="1.2s" />
    </circle>
    <circle cx="730" cy="75" r="4" fill="rgba(255,200,100,0.9)" filter="url(#np-glow)">
      <animate attributeName="r" values="3;8;3" dur="2.6s" repeatCount="indefinite" begin="0.6s" />
      <animate attributeName="opacity" values="0.5;1;0.5" dur="2.6s" repeatCount="indefinite" begin="0.6s" />
    </circle>
    <circle cx="200" cy="180" r="2" fill="rgba(100,180,255,0.5)">
      <animate attributeName="r" values="1.5;5;1.5" dur="4s" repeatCount="indefinite" begin="0.2s" />
      <animate attributeName="opacity" values="0.2;0.7;0.2" dur="4s" repeatCount="indefinite" begin="0.2s" />
    </circle>
    <circle cx="500" cy="185" r="2" fill="rgba(180,100,255,0.5)">
      <animate attributeName="r" values="1.5;5;1.5" dur="3.7s" repeatCount="indefinite" begin="1s" />
      <animate attributeName="opacity" values="0.2;0.7;0.2" dur="3.7s" repeatCount="indefinite" begin="1s" />
    </circle>
    <circle cx="650" cy="175" r="2" fill="rgba(100,255,200,0.5)">
      <animate attributeName="r" values="1.5;4;1.5" dur="4.2s" repeatCount="indefinite" begin="0.5s" />
      <animate attributeName="opacity" values="0.2;0.7;0.2" dur="4.2s" repeatCount="indefinite" begin="0.5s" />
    </circle>
    <circle cx="130" cy="70" r="20" fill="rgba(100,180,255,0.15)" filter="url(#np-glow-lg)">
      <animate attributeName="r" values="15;30;15" dur="4s" repeatCount="indefinite" />
    </circle>
    <circle cx="430" cy="55" r="20" fill="rgba(100,255,200,0.12)" filter="url(#np-glow-lg)">
      <animate attributeName="r" values="15;28;15" dur="5s" repeatCount="indefinite" begin="1s" />
    </circle>
    <circle cx="730" cy="75" r="20" fill="rgba(255,200,100,0.12)" filter="url(#np-glow-lg)">
      <animate attributeName="r" values="15;25;15" dur="4.5s" repeatCount="indefinite" begin="0.5s" />
    </circle>
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10 }}>
    <span style={{ fontSize: 26, fontWeight: 700, color: 'white' }}>Neural Pulse Network</span>
    <span style={{ fontSize: 12, color: 'rgba(200,200,255,0.45)', marginTop: 4 }}>SMIL animated radius, opacity, and pulsating glow blur</span>
  </div>
</div>
```

```aura width=860 height=280
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#05050c', borderRadius: 18, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <svg width="860" height="280" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <filter id="td-warp" x="-30%" y="-30%" width="160%" height="160%">
        <feTurbulence type="turbulence" baseFrequency="0.015" numOctaves="4" seed="3" result="turb">
          <animate attributeName="baseFrequency" values="0.008;0.04;0.015;0.05;0.008" dur="12s" repeatCount="indefinite" />
        </feTurbulence>
        <feDisplacementMap in="SourceGraphic" in2="turb" scale="22" xChannelSelector="R" yChannelSelector="G">
          <animate attributeName="scale" values="12;40;18;35;12" dur="10s" repeatCount="indefinite" />
        </feDisplacementMap>
      </filter>
      <filter id="td-blur-core" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="4">
          <animate attributeName="stdDeviation" values="2;8;2" dur="4s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <filter id="td-blur-outer" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="18">
          <animate attributeName="stdDeviation" values="12;28;12" dur="6s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <radialGradient id="td-grad-core" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(180,100,255,0.9)" />
        <stop offset="35%" stopColor="rgba(100,50,220,0.5)" />
        <stop offset="100%" stopColor="rgba(30,10,80,0)" />
      </radialGradient>
      <radialGradient id="td-grad-outer" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(80,40,200,0.4)" />
        <stop offset="100%" stopColor="rgba(20,10,60,0)" />
      </radialGradient>
    </defs>
    <circle cx="430" cy="140" r="90" fill="url(#td-grad-outer)" filter="url(#td-blur-outer)">
      <animate attributeName="r" values="80;110;80" dur="7s" repeatCount="indefinite" />
    </circle>
    <g filter="url(#td-warp)">
      <circle cx="430" cy="140" r="120" fill="none" stroke="rgba(120,60,255,0.3)" strokeWidth="1" />
      <circle cx="430" cy="140" r="95" fill="none" stroke="rgba(80,180,255,0.25)" strokeWidth="1.5" />
      <circle cx="430" cy="140" r="70" fill="none" stroke="rgba(200,80,255,0.35)" strokeWidth="2" />
      <circle cx="430" cy="140" r="45" fill="none" stroke="rgba(255,100,200,0.45)" strokeWidth="2" />
      <circle cx="430" cy="140" r="22" fill="none" stroke="rgba(255,180,255,0.5)" strokeWidth="2.5" />
      <line x1="310" y1="20" x2="550" y2="260" stroke="rgba(100,80,255,0.12)" strokeWidth="0.8" />
      <line x1="550" y1="20" x2="310" y2="260" stroke="rgba(100,80,255,0.12)" strokeWidth="0.8" />
      <line x1="310" y1="140" x2="550" y2="140" stroke="rgba(100,80,255,0.12)" strokeWidth="0.8" />
      <line x1="430" y1="20" x2="430" y2="260" stroke="rgba(100,80,255,0.12)" strokeWidth="0.8" />
      <line x1="340" y1="50" x2="520" y2="230" stroke="rgba(140,80,255,0.08)" strokeWidth="0.5" />
      <line x1="520" y1="50" x2="340" y2="230" stroke="rgba(140,80,255,0.08)" strokeWidth="0.5" />
    </g>
    <circle cx="430" cy="140" r="50" fill="url(#td-grad-core)" filter="url(#td-blur-core)">
      <animate attributeName="r" values="40;60;40" dur="5s" repeatCount="indefinite" />
    </circle>
    <circle cx="430" cy="140" r="6" fill="rgba(255,220,255,0.8)">
      <animate attributeName="r" values="4;8;4" dur="2.5s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0.6;1;0.6" dur="2.5s" repeatCount="indefinite" />
    </circle>
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10, marginTop: 160 }}>
    <span style={{ fontSize: 26, fontWeight: 700, color: 'white' }}>Distortion Portal</span>
    <span style={{ fontSize: 12, color: 'rgba(200,200,255,0.45)', marginTop: 4 }}>feTurbulence + feDisplacementMap with animated frequency and scale</span>
  </div>
</div>
```

```aura width=860 height=320
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#07070d', borderRadius: 18, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <svg width="860" height="320" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <filter id="om-trail" x="-200%" y="-200%" width="500%" height="500%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="3" />
      </filter>
      <filter id="om-core" x="-200%" y="-200%" width="500%" height="500%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="10">
          <animate attributeName="stdDeviation" values="6;16;6" dur="5s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
      <radialGradient id="om-center-grad" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(200,170,255,0.5)" />
        <stop offset="100%" stopColor="rgba(100,60,200,0)" />
      </radialGradient>
    </defs>
    <ellipse cx="430" cy="160" rx="260" ry="120" fill="none" stroke="rgba(100,80,255,0.04)" strokeWidth="0.5" />
    <ellipse cx="430" cy="160" rx="190" ry="85" fill="none" stroke="rgba(100,80,255,0.06)" strokeWidth="0.5" />
    <ellipse cx="430" cy="160" rx="120" ry="50" fill="none" stroke="rgba(100,80,255,0.08)" strokeWidth="0.5" />
    <circle cx="430" cy="160" r="25" fill="url(#om-center-grad)" filter="url(#om-core)">
      <animate attributeName="r" values="18;35;18" dur="5s" repeatCount="indefinite" />
    </circle>
    <circle cx="430" cy="160" r="4" fill="rgba(255,255,255,0.9)">
      <animate attributeName="r" values="3;5;3" dur="2s" repeatCount="indefinite" />
    </circle>
    <circle r="5" fill="rgba(100,200,255,0.95)" filter="url(#om-trail)">
      <animateMotion dur="5s" repeatCount="indefinite"
        path="M310,160 C310,108 360,80 430,80 C500,80 550,108 550,160 C550,212 500,240 430,240 C360,240 310,212 310,160 Z" />
    </circle>
    <circle r="3.5" fill="rgba(255,100,200,0.9)" filter="url(#om-trail)">
      <animateMotion dur="7s" repeatCount="indefinite" begin="1s"
        path="M240,160 C240,87 320,40 430,40 C540,40 620,87 620,160 C620,233 540,280 430,280 C320,280 240,233 240,160 Z" />
    </circle>
    <circle r="6" fill="rgba(100,255,180,0.9)" filter="url(#om-trail)">
      <animateMotion dur="3.8s" repeatCount="indefinite" begin="0.5s"
        path="M310,160 C310,118 365,95 430,95 C495,95 550,118 550,160 C550,202 495,225 430,225 C365,225 310,202 310,160 Z" />
    </circle>
    <circle r="2.5" fill="rgba(255,200,80,0.85)" filter="url(#om-trail)">
      <animateMotion dur="9s" repeatCount="indefinite" begin="2s"
        path="M170,160 C170,68 280,5 430,5 C580,5 690,68 690,160 C690,252 580,315 430,315 C280,315 170,252 170,160 Z" />
    </circle>
    <circle r="4" fill="rgba(200,100,255,0.9)" filter="url(#om-trail)">
      <animateMotion dur="6s" repeatCount="indefinite" begin="3s"
        path="M280,160 C280,102 345,65 430,65 C515,65 580,102 580,160 C580,218 515,255 430,255 C345,255 280,218 280,160 Z" />
    </circle>
    <circle cx="430" cy="160" r="3" fill="rgba(100,200,255,0.3)">
      <animate attributeName="r" values="40;55;40" dur="6s" repeatCount="indefinite" />
      <animate attributeName="opacity" values="0.05;0.15;0.05" dur="6s" repeatCount="indefinite" />
    </circle>
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10, marginTop: 195 }}>
    <span style={{ fontSize: 26, fontWeight: 700, color: 'white' }}>Orbital Dance</span>
    <span style={{ fontSize: 12, color: 'rgba(200,200,255,0.45)', marginTop: 4 }}>SMIL animateMotion along bezier orbital paths</span>
  </div>
</div>
```

```aura width=860 height=300
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#06060c', borderRadius: 18, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <svg width="860" height="300" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <filter id="rp-soft" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="1.5" />
      </filter>
      <filter id="rp-bloom" x="-50%" y="-50%" width="200%" height="200%">
        <feGaussianBlur in="SourceGraphic" stdDeviation="20">
          <animate attributeName="stdDeviation" values="15;30;15" dur="6s" repeatCount="indefinite" />
        </feGaussianBlur>
      </filter>
    </defs>
    <circle cx="430" cy="130" r="25" fill="rgba(140,100,255,0.15)" filter="url(#rp-bloom)">
      <animate attributeName="r" values="20;45;20" dur="4s" repeatCount="indefinite" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(100,180,255,0.6)" strokeWidth="2.5" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" />
      <animate attributeName="opacity" from="0.9" to="0" dur="4s" repeatCount="indefinite" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(140,100,255,0.6)" strokeWidth="2.5" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" begin="0.7s" />
      <animate attributeName="opacity" from="0.9" to="0" dur="4s" repeatCount="indefinite" begin="0.7s" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(200,80,255,0.6)" strokeWidth="2.5" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" begin="1.4s" />
      <animate attributeName="opacity" from="0.9" to="0" dur="4s" repeatCount="indefinite" begin="1.4s" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(255,100,180,0.6)" strokeWidth="2.5" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" begin="2.1s" />
      <animate attributeName="opacity" from="0.9" to="0" dur="4s" repeatCount="indefinite" begin="2.1s" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(255,180,80,0.5)" strokeWidth="2" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" begin="2.8s" />
      <animate attributeName="opacity" from="0.85" to="0" dur="4s" repeatCount="indefinite" begin="2.8s" />
    </circle>
    <circle cx="430" cy="130" fill="none" stroke="rgba(80,255,200,0.4)" strokeWidth="1.5" r="10" filter="url(#rp-soft)">
      <animate attributeName="r" from="8" to="180" dur="4s" repeatCount="indefinite" begin="3.5s" />
      <animate attributeName="opacity" from="0.8" to="0" dur="4s" repeatCount="indefinite" begin="3.5s" />
    </circle>
    <path fill="none" stroke="rgba(180,140,255,0.25)" strokeWidth="1" strokeDasharray="4 8">
      <animate attributeName="d"
        values="M250,130 Q340,60 430,130 Q520,200 610,130;M250,130 Q340,200 430,130 Q520,60 610,130;M250,130 Q340,60 430,130 Q520,200 610,130"
        dur="6s" repeatCount="indefinite" />
    </path>
    <path fill="none" stroke="rgba(100,200,255,0.2)" strokeWidth="0.8" strokeDasharray="3 6">
      <animate attributeName="d"
        values="M300,130 Q365,80 430,130 Q495,180 560,130;M300,130 Q365,180 430,130 Q495,80 560,130;M300,130 Q365,80 430,130 Q495,180 560,130"
        dur="5s" repeatCount="indefinite" begin="1s" />
    </path>
    <circle cx="430" cy="130" r="4" fill="rgba(255,255,255,0.95)">
      <animate attributeName="r" values="3;6;3" dur="2s" repeatCount="indefinite" />
    </circle>
  </svg>
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', zIndex: 10, marginTop: 175 }}>
    <span style={{ fontSize: 26, fontWeight: 700, color: 'white' }}>Ripple Wavefront</span>
    <span style={{ fontSize: 12, color: 'rgba(200,200,255,0.45)', marginTop: 4 }}>Staggered SMIL radius cascade + morphing wave paths + bloom blur</span>
  </div>
</div>
```

```aura width=860 height=400
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#000000', borderRadius: 20, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/2c/Rotating_earth_%28large%29.gif" width={860} height={400} style={{ position: 'absolute', top: 0, left: 0, width: '100%', height: '100%', objectFit: 'cover', opacity: 0.7 }} />
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', zIndex: 10 }}>
    <span style={{ fontSize: 64, fontWeight: 800, color: 'white', letterSpacing: '-2px', textShadow: '0 0 40px rgba(100,180,255,0.5)' }}>hello world</span>
  </div>
</div>
```

```aura width=860 height=400
<div style={{ position: 'relative', width: '100%', height: '100%', background: '#000000', borderRadius: 20, overflow: 'hidden', display: 'flex', alignItems: 'center', justifyContent: 'center', fontFamily: 'Inter, sans-serif' }}>
  <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExZ2hpZnQxYjU0NHF0N3l6bHdzMHFkNGp5YTRpcWg5NmczNW83bWo2NyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/jRiUEeFanZ94UZEVoQ/giphy.gif" width={860} height={400} style={{ position: 'absolute', top: 0, left: 0, width: '100%', height: '100%', objectFit: 'cover', opacity: 0.7 }} />
  <div style={{ display: 'flex', flexDirection: 'column', alignItems: 'center', justifyContent: 'center', zIndex: 10 }}>
    <span style={{ fontSize: 64, fontWeight: 800, color: 'white', letterSpacing: '-2px', textShadow: '0 0 40px rgba(100,180,255,0.5)' }}>hello world</span>
  </div>
</div>
```

```aura width=860 height=22 link="https://collectioneur.github.io/readme-aura/"
  <div style={{ display: 'flex', justifyContent: 'center', alignItems: 'center', width: '100%', height: '100%', padding: 0, margin: 0 }}>
    <span style={{ fontSize: 12, lineHeight: 1, color: 'rgba(150,140,200,0.55)', fontWeight: 500, letterSpacing: '0.4px' }}>powered by readme-aura</span>
  </div>
```

```aura width=150 height=40 link="https://x.com/collectioneurr"
<div style={{ position: 'relative', display: 'flex', width: '100%', height: '100%', backgroundColor: '#111111', borderRadius: 20, boxSizing: 'border-box' }}>
  <svg width="150" height="40" viewBox="0 0 150 40" overflow="visible" xmlns="http://www.w3.org/2000/svg" style={{ position: 'absolute', top: 0, left: 0, pointerEvents: 'none', overflow: 'visible' }}>
    <defs>
      <linearGradient id="tw-holo" gradientUnits="objectBoundingBox" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%" stopColor="#ffffff" />
        <stop offset="10%" stopColor="#111111" />
        <stop offset="50%" stopColor="#eeeeee" />
        <stop offset="60%" stopColor="#ffbbaa" />
        <stop offset="80%" stopColor="#111111" />
        <stop offset="100%" stopColor="#555555" />
        <animateTransform
          attributeName="gradientTransform"
          type="rotate"
          from="0 0.5 0.5"
          to="360 0.5 0.5"
          dur="8s"
          repeatCount="indefinite"
        />
      </linearGradient>
    </defs>
    <rect x="1.25" y="1.25" width="147.5" height="37.5" rx="18.75" ry="18.75" fill="none" stroke="url(#tw-holo)" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round" />
    <rect x="0.25" y="0.25" width="149.5" height="39.5" rx="19.75" ry="19.75" fill="none" stroke="#AAAAAA" strokeWidth="0.5" strokeLinecap="round" strokeLinejoin="round" />
  </svg>
  <div style={{ position: 'relative', display: 'flex', flexDirection: 'row', alignItems: 'center', justifyContent: 'center', gap: '5px', flex: 1, width: '100%', height: '100%', paddingLeft: 12, paddingRight: 10, boxSizing: 'border-box' }}>
  <img src="x-icon.png" width={18} height={18} alt="" style={{ flexShrink: 0, display: 'block' }} />
    <span style={{ fontFamily: 'Inter, sans-serif', fontWeight: 700, fontSize: 13, color: '#f5f5f5', letterSpacing: '-0.2px' }}>@collectioneurr</span>
  </div>
</div>
```
