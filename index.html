<!DOCTYPE html>
<html lang="es" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Rappi MX · Portal de Adquisición & AI</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/3.9.1/chart.min.js"></script>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.1/jszip.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.5/FileSaver.min.js"></script>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">
<script>
  const savedTheme = localStorage.getItem('rappi_theme') || 'dark';
  if(savedTheme === 'light') document.documentElement.setAttribute('data-theme', 'light');
</script>
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --r:#FF441F;--r2:#FF6B4A;--bg:#09090B;--bg2:#131316;--bg3:#1D1D21;
  --white:#000000;--ink:#FAFAFA;--ink2:#E4E4E7;--ink3:#A1A1AA;--ink4:#71717A;--ink5:#3F3F46;
  --green:#22C55E;--gbg:rgba(34, 197, 94, 0.15);--gtext:#4ADE80;
  --blue:#3B82F6;--bbg:rgba(59, 130, 246, 0.15);--btext:#60A5FA;
  --amber:#F59E0B;--abg:rgba(245, 158, 11, 0.15);--atext:#FBBF24;
  --purple:#8B5CF6;--pbg:rgba(139, 92, 246, 0.15);--ptext:#A78BFA;
  --red:#EF4444;--rbg:rgba(239, 68, 68, 0.15);--rtext:#F87171;
  --teal:#14B8A6;--tbg:rgba(20, 184, 166, 0.15);--ttext:#2DD4BF;
  --shadow:0 4px 20px rgba(0,0,0,0.4);--shadow-glow:0 0 15px rgba(255,68,31,0.25);
  --glass-border:1px solid rgba(255,255,255,0.08);
  --r-sm:6px;--r-md:10px;--r-lg:14px;--r-xl:20px;
}
[data-theme="light"] {
  --bg:#F4F4F5;--bg2:#FFFFFF;--bg3:#E4E4E7;
  --white:#FFFFFF;--ink:#09090B;--ink2:#18181B;--ink3:#52525B;--ink4:#71717A;--ink5:#D4D4D8;
  --glass-border:1px solid rgba(0,0,0,0.08);
  --shadow:0 4px 15px rgba(0,0,0,0.05);
  --shadow-glow:0 0 15px rgba(255,68,31,0.15);
}
html,body{height:100%;font-family:'Space Grotesk',sans-serif;background:var(--bg);color:var(--ink);font-size:14px;line-height:1.5;-webkit-font-smoothing:antialiased}

#loader{position:fixed;inset:0;background:var(--bg);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:24px;z-index:9999;transition:opacity .5s .1s}
#loader.out{opacity:0;pointer-events:none}
.loader-icon{width:72px;height:72px;background:var(--bg2);border:var(--glass-border);border-radius:20px;display:flex;align-items:center;justify-content:center;animation:pulse 1.4s ease-in-out infinite;box-shadow:var(--shadow-glow)}
.loader-icon svg{width:40px;height:40px;fill:var(--r)}
@keyframes pulse{0%,100%{transform:scale(1);box-shadow:0 0 15px rgba(255,68,31,0.2)}50%{transform:scale(1.05);box-shadow:0 0 30px rgba(255,68,31,0.5)}}
.loader-bar{width:240px;height:3px;background:var(--ink5);border-radius:3px;overflow:hidden}
.loader-bar-fill{height:100%;background:linear-gradient(90deg,var(--r),var(--r2));border-radius:3px;width:0;animation:load 1.8s ease forwards}
@keyframes load{to{width:100%}}
.loader-text{color:var(--ink3);font-size:12px;letter-spacing:.15em;text-transform:uppercase;font-weight:600}
.loader-error{color:var(--red);font-size:13px;text-align:center;max-width:320px;display:none;white-space:pre-wrap}

#app{display:grid;grid-template-columns:1fr;grid-template-rows:60px 1fr 72px;height:100vh;overflow:hidden}
header{grid-row:1;grid-column:1;background:rgba(9, 9, 11, 0.8);backdrop-filter:blur(12px);display:flex;align-items:center;padding:0 24px 0 0;border-bottom:var(--glass-border);z-index:50}
.hd-brand{width:72px;height:60px;display:flex;align-items:center;justify-content:center;flex-shrink:0;border-right:var(--glass-border);background:var(--bg2);cursor:pointer}
.hd-logo{width:36px;height:36px;background:var(--r);border-radius:10px;display:flex;align-items:center;justify-content:center;box-shadow:var(--shadow-glow)}
.hd-logo svg{width:20px;height:20px;fill:#fff}
.hd-btn-back{display:none;background:var(--bg2);border:1px solid var(--ink5);color:var(--ink);cursor:pointer;width:36px;height:36px;border-radius:var(--r-sm);align-items:center;justify-content:center;transition:all .2s;margin-left:16px;}
.hd-btn-back:hover{background:var(--bg3);border-color:var(--r);color:var(--r);box-shadow:0 0 10px rgba(255,68,31,0.2)}
.hd-btn-back svg{width:20px;height:20px}
.hd-title{padding:0 24px;display:flex;align-items:baseline;gap:12px}
.hd-title h1{font-size:16px;font-weight:700;color:var(--ink);letter-spacing:-.3px}
.hd-title span{font-size:12px;color:var(--ink4);letter-spacing:0.05em}
.hd-right{margin-left:auto;display:flex;align-items:center;gap:16px;flex-wrap:wrap}
.hd-kpi{display:flex;align-items:center;gap:10px;padding:6px 16px;background:var(--bg2);border:var(--glass-border);border-radius:var(--r-md)}
.hd-kpi-click{cursor:pointer; transition:all .2s;}
.hd-kpi-click:hover{border-color:var(--r);box-shadow:0 0 10px rgba(255,68,31,0.2)}
.hd-kpi-label{font-size:10px;color:var(--ink3);text-transform:uppercase;letter-spacing:.1em;font-weight:600}
.hd-kpi-val{font-size:15px;font-weight:700;color:var(--ink);font-family:'JetBrains Mono',monospace}
.hd-kpi-val.orange{color:var(--r)}
.hd-btn-theme{background:var(--bg2);border:1px solid var(--ink5);color:var(--ink);cursor:pointer;width:36px;height:36px;border-radius:var(--r-sm);display:flex;align-items:center;justify-content:center;transition:all .2s;}
.hd-btn-theme:hover{background:var(--bg3);border-color:var(--r);color:var(--r);box-shadow:0 0 10px rgba(255,68,31,0.2)}
.hd-btn-theme svg{width:18px;height:18px}
.hd-btn{padding:8px 16px;background:linear-gradient(135deg, var(--r) 0%, var(--r2) 100%);color:#fff;border:none;border-radius:var(--r-sm);font-family:inherit;font-size:12px;font-weight:600;cursor:pointer;display:flex;align-items:center;gap:6px;transition:all .2s;box-shadow:var(--shadow-glow)}
.hd-btn:hover{transform:translateY(-1px);box-shadow:0 4px 20px rgba(255,68,31,0.4)}
.hd-btn svg{width:14px;height:14px}
.hd-conn{display:flex;align-items:center;gap:8px;padding:6px 12px;background:var(--bg2);border-radius:20px;border:var(--glass-border)}
.hd-dot{width:8px;height:8px;border-radius:50%;background:var(--ink5);transition:all .3s}
.hd-dot.ok{background:var(--green);box-shadow:0 0 8px var(--green)}
.hd-dot.err{background:var(--red);box-shadow:0 0 8px var(--red)}
.hd-conn-text{font-size:11px;color:var(--ink3);font-weight:600;letter-spacing:.05em}
.hd-hamburger{display:none;background:transparent;border:none;cursor:pointer;padding:8px;color:var(--ink)}
.hd-hamburger svg{width:24px;height:24px;stroke:var(--ink)}

/* BOTTOM NAVIGATION */
nav{grid-row:3;grid-column:1;background:var(--bg2);border-top:var(--glass-border);display:flex;flex-direction:row;align-items:center;justify-content:flex-start;padding:0 16px;gap:8px;z-index:40;transition:transform .3s ease;overflow-x:auto}
nav::-webkit-scrollbar{display:none}
.nav-btn{flex-shrink:0;width:48px;height:48px;border-radius:12px;border:1px solid transparent;background:transparent;cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--ink4);transition:all .2s;position:relative}
.nav-btn svg{width:22px;height:22px}
.nav-btn:hover{background:var(--bg3);color:var(--ink)}
.nav-btn.active{background:rgba(255,68,31,.1);color:var(--r);border-color:rgba(255,68,31,.2);box-shadow:inset 0 0 10px rgba(255,68,31,.05)}
.nav-tip{position:absolute;bottom:calc(100% + 12px);left:50%;background:var(--ink);color:var(--bg);font-weight:600;font-size:11px;white-space:nowrap;padding:6px 12px;border-radius:6px;pointer-events:none;opacity:0;transition:all .2s;z-index:100;transform:translateX(-50%) translateY(10px);box-shadow:var(--shadow)}
.nav-btn:hover .nav-tip{opacity:1;transform:translateX(-50%) translateY(0)}
.nav-sep{width:1px;height:24px;background:var(--ink5);margin:0 8px;flex-shrink:0}
.nav-badge{position:absolute;top:4px;right:4px;min-width:18px;height:18px;background:var(--r);border-radius:9px;font-size:9px;font-weight:700;color:#fff;display:flex;align-items:center;justify-content:center;padding:0 4px;box-shadow:0 0 8px rgba(255,68,31,.5)}

main{grid-row:2;grid-column:1;overflow-y:auto;overflow-x:hidden;padding:32px 40px;background:var(--bg)}
.page{display:none;animation:fadeUp .3s cubic-bezier(0.16, 1, 0.3, 1)}
.page.on{display:block}
@keyframes fadeUp{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:translateY(0)}}
.ph{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:32px;gap:20px;flex-wrap:wrap}
.ph-left h2{font-size:28px;font-weight:700;letter-spacing:-.5px;color:var(--ink)}
.ph-left p{font-size:14px;color:var(--ink3);margin-top:6px}
.ph-right{display:flex;gap:12px;flex-shrink:0}

/* CARDS & METRICS */
.metrics{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:16px;margin-bottom:32px}
.mc{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);padding:20px 24px;position:relative;overflow:hidden;transition:all .3s;cursor:pointer;box-shadow:0 4px 6px rgba(0,0,0,0.05)}
.mc:hover{border-color:var(--ink4);transform:translateY(-3px);box-shadow:0 8px 24px rgba(0,0,0,0.1)}
.mc-accent{position:absolute;top:0;left:0;right:0;height:2px;}
.mc-label{font-size:11px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--ink3);margin-bottom:12px}
.mc-val{font-size:36px;font-weight:700;font-family:'Space Grotesk',sans-serif;color:var(--ink);line-height:1;letter-spacing:-1px}
.mc-sub{font-size:12px;color:var(--ink4);margin-top:8px}
.mc-change{display:inline-flex;align-items:center;gap:4px;font-size:11px;font-weight:600;padding:4px 8px;border-radius:20px;margin-top:8px}
.mc-change.up{background:var(--gbg);color:var(--gtext)}
.mc-change.warn{background:var(--abg);color:var(--atext)}

/* UI ELEMENTS */
.sec-title{font-size:14px;font-weight:600;letter-spacing:.05em;text-transform:uppercase;color:var(--ink2);margin-bottom:16px;display:flex;align-items:center;justify-content:space-between}
.sec-title a{font-size:12px;font-weight:500;color:var(--r);cursor:pointer;text-decoration:none;text-transform:none;letter-spacing:normal}
.sec-title a:hover{color:var(--r2);text-shadow:0 0 8px rgba(255,68,31,0.4)}
.chip{display:inline-flex;align-items:center;gap:6px;padding:4px 10px;border-radius:20px;font-size:11px;font-weight:600;white-space:nowrap;border:1px solid transparent}
.chip::before{content:'';width:6px;height:6px;border-radius:50%;background:currentColor;flex-shrink:0;box-shadow:0 0 5px currentColor}
.chip-base{background:var(--bbg);color:var(--btext);border-color:rgba(59,130,246,0.3)}
.chip-prospecto{background:var(--bbg);color:var(--btext);border-color:rgba(59,130,246,0.3)}
.chip-r2s{background:var(--abg);color:var(--atext);border-color:rgba(245,158,11,0.3)}
.chip-wp{background:var(--tbg);color:var(--ttext);border-color:rgba(20,184,166,0.3)}
.chip-firma{background:rgba(180,83,9,0.2);color:#FCD34D;border-color:rgba(180,83,9,0.4)}
.chip-handoff{background:var(--pbg);color:var(--ptext);border-color:rgba(139,92,246,0.3)}
.chip-sob{background:var(--rbg);color:var(--rtext);border-color:rgba(239,68,68,0.3)}
.chip-rts{background:var(--gbg);color:var(--gtext);border-color:rgba(34,197,94,0.3)}
.chip-nc{background:var(--bg3);color:var(--ink3);border-color:var(--ink5)}
.chip-int{background:var(--gbg);color:var(--gtext);border-color:rgba(34,197,94,0.3)}
.chip-err{background:var(--rbg);color:var(--rtext);border-color:rgba(239,68,68,0.3)}
.chip-buz{background:var(--bg3);color:var(--ink3);border-color:var(--ink5)}

/* TOOLBARS & INPUTS */
.toolbar{display:flex;gap:12px;margin-bottom:20px;flex-wrap:wrap;align-items:center;background:var(--white);padding:16px;border-radius:var(--r-lg);border:var(--glass-border)}
.search{flex:1;min-width:240px;position:relative}
.search svg{position:absolute;left:14px;top:50%;transform:translateY(-50%);width:16px;height:16px;color:var(--ink4);pointer-events:none}
.search input{width:100%;padding:10px 14px 10px 40px;border:1px solid var(--ink5);border-radius:var(--r-sm);font-family:inherit;font-size:13px;background:var(--bg);color:var(--ink);outline:none;transition:all .2s}
.search input:focus, .fsel:focus{border-color:var(--r);box-shadow:0 0 0 2px rgba(255,68,31,0.1)}
.search input::placeholder{color:var(--ink4)}
.fsel{padding:10px 14px;border:1px solid var(--ink5);border-radius:var(--r-sm);font-family:inherit;font-size:13px;background:var(--bg);color:var(--ink);outline:none;cursor:pointer;min-width:140px;appearance:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23A1A1AA' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 10px center;padding-right:32px;}
.fsel:disabled{background:var(--bg2);cursor:not-allowed;opacity:0.5}
.btn{display:inline-flex;align-items:center;justify-content:center;gap:8px;padding:10px 18px;border-radius:var(--r-sm);font-family:inherit;font-size:13px;font-weight:600;cursor:pointer;transition:all .2s;border:1px solid transparent;white-space:nowrap}
.btn svg{width:16px;height:16px;flex-shrink:0}
.btn-primary{background:var(--r);color:#fff;box-shadow:var(--shadow-glow)}.btn-primary:hover{background:var(--r2);transform:translateY(-1px);box-shadow:0 4px 15px rgba(255,68,31,0.4)}
.btn-outline{background:transparent;color:var(--ink);border-color:var(--ink4)}.btn-outline:hover{background:var(--bg3);border-color:var(--ink2)}
.btn-ghost{background:transparent;color:var(--ink3)}.btn-ghost:hover{background:var(--bg3);color:var(--ink)}
.btn-sm{padding:6px 12px;font-size:12px}

/* TABLAS */
.tbl-wrap{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);overflow:hidden;box-shadow:var(--shadow)}
.tbl-scroll{overflow-x:auto;-webkit-overflow-scrolling:touch}
table{width:100%;border-collapse:collapse;min-width:900px}
thead{background:var(--bg2);border-bottom:1px solid var(--ink5)}
th{padding:14px 16px;text-align:left;font-size:11px;font-weight:600;letter-spacing:.05em;text-transform:uppercase;color:var(--ink3);cursor:pointer;user-select:none;white-space:nowrap;transition:color .2s}
th:hover{color:var(--ink)}
th.asc::after{content:' ↑';color:var(--r)}
th.desc::after{content:' ↓';color:var(--r)}
tbody tr{border-bottom:1px solid var(--ink5);cursor:pointer;transition:background .2s}
tbody tr:last-child{border-bottom:none}
tbody tr:hover{background:var(--bg3)}
td{padding:14px 16px;font-size:13px;color:var(--ink);vertical-align:middle}
td.muted{color:var(--ink3);font-size:12px}
td.mono{font-family:'JetBrains Mono',monospace;font-size:12px;color:var(--ink2)}
td.name{font-weight:600;color:var(--ink);max-width:220px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.tbl-footer{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;border-top:1px solid var(--ink5);background:var(--bg2);flex-wrap:wrap;gap:12px}
.tbl-count{font-size:12px;color:var(--ink4);font-weight:500}
.pager{display:flex;gap:4px;flex-wrap:wrap}
.pg-btn{width:32px;height:32px;border-radius:var(--r-sm);border:1px solid var(--ink5);background:var(--bg);font-weight:600;font-size:12px;color:var(--ink3);cursor:pointer;display:flex;align-items:center;justify-content:center;transition:all .2s}
.pg-btn:hover{background:var(--bg3);color:var(--ink);border-color:var(--ink4)}
.pg-btn.on{background:var(--r);color:#fff;border-color:var(--r);box-shadow:0 0 10px rgba(255,68,31,0.3)}
.elegant-table{min-width:1000px;background:transparent}
.elegant-table thead{background:transparent;border-bottom:none}
.elegant-table th{background:transparent;color:var(--ink4);border-bottom:2px solid var(--ink5);padding:18px 16px;text-transform:uppercase;font-size:10px;letter-spacing:0.1em;font-weight:600;cursor:default}
.elegant-table td{border-bottom:1px solid var(--ink5);padding:16px;transition:all 0.2s ease}
.elegant-table tbody tr{transition:transform 0.2s ease,box-shadow 0.2s ease;cursor:pointer;background:var(--white)}
.elegant-table tbody tr:hover{transform:translateY(-2px);box-shadow:0 10px 20px rgba(0,0,0,0.1);position:relative;z-index:10;border-radius:10px;border:var(--glass-border)}
.elegant-table tbody tr:hover td{background:var(--bg2);border-bottom-color:transparent}
.val-zero{color:var(--ink5);font-weight:400;opacity:0.5}
.val-num{color:var(--ink);font-weight:700;font-family:'JetBrains Mono',monospace}
.badge-pill{display:inline-flex;align-items:center;justify-content:center;padding:6px 14px;border-radius:20px;font-weight:700;font-size:12px;min-width:60px;font-family:'JetBrains Mono',monospace;border:1px solid rgba(255,255,255,0.1)}

/* PIPELINE & FUNNEL */
.pipeline{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:16px;margin-bottom:32px}
.pl-head{padding:12px 16px;border-radius:var(--r-md) var(--r-md) 0 0;display:flex;align-items:center;justify-content:space-between;border:var(--glass-border);border-bottom:none}
.pl-head-label{font-size:10px;font-weight:700;letter-spacing:.05em;text-transform:uppercase}
.pl-head-num{font-size:20px;font-weight:700;font-family:'JetBrains Mono',monospace}
.pl-body{background:var(--bg2);border:var(--glass-border);border-radius:0 0 var(--r-md) var(--r-md);min-height:220px;max-height:380px;overflow-y:auto;padding:10px}
.pl-card{background:var(--bg);border-radius:var(--r-sm);padding:12px;margin-bottom:8px;cursor:pointer;transition:all .2s;border:1px solid var(--ink5);font-size:12px;box-shadow:0 2px 4px rgba(0,0,0,0.2)}
.pl-card:hover{border-color:var(--ink3);transform:translateY(-2px);box-shadow:0 4px 8px rgba(0,0,0,0.4)}
.pl-card-name{font-weight:600;color:var(--ink);overflow:hidden;text-overflow:ellipsis;white-space:nowrap;margin-bottom:4px;font-size:13px}
.pl-card-agent{color:var(--ink4);font-size:11px;font-family:'JetBrains Mono',monospace}
.pl-empty{text-align:center;padding:32px 16px;color:var(--ink5);font-size:12px;font-weight:500;text-transform:uppercase;letter-spacing:.05em}
.funnel-row{display:flex;align-items:center;gap:0;margin-bottom:32px;background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);overflow:hidden;overflow-x:auto;-webkit-overflow-scrolling:touch;box-shadow:var(--shadow)}
.funnel-step{flex:1;min-width:120px;padding:20px 16px;text-align:center;border-right:1px solid var(--ink5);position:relative;background:var(--bg2)}
.funnel-step:last-child{border-right:none}
.funnel-step::after{content:'›';position:absolute;right:-7px;top:50%;transform:translateY(-50%);color:var(--ink4);font-size:24px;font-weight:300;z-index:1}
.funnel-step:last-child::after{display:none}
.fs-num{font-size:32px;font-weight:700;letter-spacing:-1px;color:var(--ink);font-family:'Space Grotesk',sans-serif}
.fs-label{font-size:10px;font-weight:600;letter-spacing:.05em;text-transform:uppercase;color:var(--ink4);margin-top:4px}
.fs-pct{font-size:12px;color:var(--ink3);margin-top:6px;font-family:'JetBrains Mono',monospace}

/* BAR CHARTS & OTHERS */
.bar-chart{display:flex;flex-direction:column;gap:12px}
.bar-row{display:flex;align-items:center;gap:12px}
.bar-label{font-size:12px;font-weight:500;color:var(--ink2);width:140px;flex-shrink:0;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;text-align:right}
.bar-track{flex:1;height:24px;background:var(--bg3);border-radius:12px;overflow:hidden;position:relative;box-shadow:inset 0 1px 3px rgba(0,0,0,0.5)}
.bar-fill{height:100%;border-radius:12px;transition:width 1s cubic-bezier(.22,.61,.36,1);box-shadow:inset 0 -2px 4px rgba(0,0,0,0.2)}
.bar-val{position:absolute;right:10px;top:50%;transform:translateY(-50%);font-size:11px;font-weight:700;color:#fff;font-family:'JetBrains Mono',monospace;text-shadow:0 1px 2px rgba(0,0,0,0.8)}

/* DRAWER, TOASTS & ALERTS */
.overlay{position:fixed;inset:0;background:rgba(0,0,0,.7);z-index:200;display:none;justify-content:flex-end;backdrop-filter:blur(5px)}
.overlay.on{display:flex}
.drawer{width:560px;max-width:100vw;background:var(--bg2);height:100vh;overflow-y:auto;display:flex;flex-direction:column;animation:drIn .3s cubic-bezier(0.16, 1, 0.3, 1);border-left:var(--glass-border);box-shadow:-10px 0 30px rgba(0,0,0,0.5)}
@keyframes drIn{from{transform:translateX(100%)}to{transform:translateX(0)}}
.dr-head{padding:24px;border-bottom:1px solid var(--ink5);display:flex;align-items:flex-start;gap:16px;position:sticky;top:0;background:rgba(19,19,22,0.95);backdrop-filter:blur(8px);z-index:5}
.dr-head-main{flex:1;min-width:0}
.dr-title{font-size:20px;font-weight:700;letter-spacing:-.4px;color:var(--ink);overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.dr-sub{font-size:13px;color:var(--ink3);margin-top:6px;display:flex;align-items:center;gap:8px}
.dr-close{width:36px;height:36px;border-radius:var(--r-sm);border:1px solid var(--ink5);background:var(--bg);cursor:pointer;display:flex;align-items:center;justify-content:center;color:var(--ink3);font-size:18px;transition:all .2s;flex-shrink:0}
.dr-close:hover{background:var(--bg3);color:var(--ink);border-color:var(--ink4)}
.dr-body{padding:24px;flex:1}
.dr-sec{margin-bottom:28px}
.dr-sec-title{font-size:11px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--ink4);margin-bottom:12px;padding-bottom:8px;border-bottom:1px solid var(--ink5)}
.dr-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px}
.dr-field{background:var(--bg);padding:12px;border-radius:var(--r-sm);border:1px solid var(--ink5)}
.dr-field .dk{font-size:10px;text-transform:uppercase;letter-spacing:.05em;color:var(--ink4);margin-bottom:6px;font-weight:600}
.dr-field .dv{font-size:14px;color:var(--ink);font-weight:500}
.dr-field .dv.mono{font-family:'JetBrains Mono',monospace;font-size:13px}
.dr-full{grid-column:1/-1}
.dr-comment{background:var(--bg3);border-radius:var(--r-sm);padding:14px;font-size:14px;color:var(--ink2);line-height:1.6;border-left:3px solid var(--r);font-style:italic}
.dr-foot{padding:20px 24px;border-top:1px solid var(--ink5);background:var(--bg2);display:flex;gap:12px;position:sticky;bottom:0}
.field-g{margin-bottom:16px}
.field-g label{display:block;font-size:11px;font-weight:600;color:var(--ink3);margin-bottom:6px;text-transform:uppercase;letter-spacing:.05em}
.field-g input,.field-g select,.field-g textarea{width:100%;padding:12px;border:1px solid var(--ink5);border-radius:var(--r-sm);font-family:inherit;font-size:14px;color:var(--ink);background:var(--bg);outline:none;transition:all .2s}
.field-g input:focus,.field-g select:focus,.field-g textarea:focus{border-color:var(--r);box-shadow:0 0 0 2px rgba(255,68,31,0.15)}
.field-g textarea{min-height:90px;resize:vertical;line-height:1.5}
.alert{display:flex;gap:12px;padding:14px 16px;border-radius:var(--r-sm);font-size:13px;margin-bottom:20px;line-height:1.5;font-weight:500}
.alert svg{width:18px;height:18px;flex-shrink:0;margin-top:2px}
.a-warn{background:var(--abg);color:var(--atext);border:1px solid rgba(245,158,11,0.4)}
.a-err{background:var(--rbg);color:var(--rtext);border:1px solid rgba(239,68,68,0.4)}
.a-ok{background:var(--gbg);color:var(--gtext);border:1px solid rgba(34,197,94,0.4)}
.a-info{background:var(--bbg);color:var(--btext);border:1px solid rgba(59,130,246,0.4)}
#toasts{position:fixed;bottom:24px;right:24px;z-index:9999;display:flex;flex-direction:column;gap:10px;pointer-events:none}
.toast{display:flex;align-items:center;gap:12px;padding:14px 20px;border-radius:var(--r-md);font-size:14px;font-weight:500;pointer-events:all;box-shadow:0 10px 30px rgba(0,0,0,0.5);border:var(--glass-border);animation:tin .3s cubic-bezier(0.16, 1, 0.3, 1);max-width:320px}
.toast.ok{background:#064E3B;color:#D1FAE5;border-color:rgba(52,211,153,0.3)}
.toast.er{background:#7F1D1D;color:#FEE2E2;border-color:rgba(248,113,113,0.3)}
.toast.inf{background:var(--bg3);color:var(--ink);border-color:var(--ink5)}
.toast svg{width:18px;height:18px;flex-shrink:0}
.toast.hide{animation:tout .2s ease forwards}
@keyframes tin{from{opacity:0;transform:translateY(15px) scale(0.95)}to{opacity:1;transform:translateY(0) scale(1)}}
@keyframes tout{to{opacity:0;transform:translateY(15px) scale(0.95)}}

/* MORE COMPONENTS */
.empty{text-align:center;padding:60px 24px}
.empty svg{width:48px;height:48px;color:var(--ink5);margin-bottom:16px}
.empty h3{font-size:16px;font-weight:600;color:var(--ink2);margin-bottom:8px}
.empty p{font-size:14px;color:var(--ink4)}
.form-wrap{max-width:680px}
.form-card{background:var(--white);border:var(--glass-border);border-radius:var(--r-xl);padding:32px;margin-bottom:24px;box-shadow:var(--shadow)}
.form-card-title{font-size:12px;font-weight:600;letter-spacing:.1em;text-transform:uppercase;color:var(--r);margin-bottom:24px;padding-bottom:12px;border-bottom:1px solid var(--ink5)}
.two-col{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-bottom:32px}
.card{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);padding:24px;overflow:hidden;box-shadow:var(--shadow)}
.card.full{grid-column:1/-1}
.f2{display:grid;grid-template-columns:1fr 1fr;gap:16px}
::-webkit-scrollbar{width:8px;height:8px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--ink5);border-radius:4px;border:2px solid var(--bg)}
::-webkit-scrollbar-thumb:hover{background:var(--ink4)}

/* CALCULADORA & EXTRAS */
.calc-wrap{max-width:840px;display:grid;grid-template-columns:1fr 1.2fr;gap:32px}
.tier-list{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);overflow:hidden;box-shadow:var(--shadow)}
.tier-row{display:grid;grid-template-columns:1fr 1fr 1fr 1fr;padding:12px 16px;font-size:13px;border-bottom:1px solid var(--ink5);align-items:center;text-align:center;font-family:'JetBrains Mono',monospace}
.tier-row>div:first-child{text-align:left;font-family:'Space Grotesk',sans-serif;font-weight:600}
.tier-row>div:last-child{text-align:right;color:var(--ink4)}
.tier-row.active{background:rgba(255, 215, 0, 0.1);border-left:4px solid #FBBF24}
.tier-row.active>div{color:var(--ink);font-weight:700!important}
.tier-row.active .t-val{color:#FBBF24!important;text-shadow:0 0 10px rgba(251,191,36,0.3)}
.tier-header{background:var(--bg2);color:var(--ink3);font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:11px;text-transform:uppercase;letter-spacing:.05em}
.calc-result{background:linear-gradient(135deg, #18181B 0%, #09090B 100%);color:var(--ink);border:1px solid rgba(255,68,31,0.3);border-radius:var(--r-lg);padding:32px;text-align:center;box-shadow:var(--shadow-glow);position:relative;overflow:hidden}
.calc-result::before{content:'position:absolute;top:0;left:0;right:0;height:4px;background:linear-gradient(90deg,var(--r),var(--purple))}
.cr-label{font-size:11px;text-transform:uppercase;letter-spacing:.1em;color:var(--ink4);margin-bottom:10px;font-weight:600}
.cr-val{font-size:48px;font-weight:700;letter-spacing:-1px;line-height:1;margin-bottom:16px;font-family:'Space Grotesk',sans-serif}
.cr-sub{font-size:14px;color:var(--ink3);background:var(--bg);display:inline-block;padding:6px 16px;border-radius:20px;border:1px solid var(--ink5);font-family:'JetBrains Mono',monospace}
.ind-meta-input{width:70px;padding:6px 10px;border:1px solid var(--ink5);border-radius:var(--r-sm);font-family:'JetBrains Mono',monospace;font-size:14px;text-align:center;background:var(--bg);color:var(--ink);outline:none;transition:border-color .2s}

/* LLEGADAS TARDE - CALENDARIO & CORAZONES */
.hearts-container{display:flex;gap:16px;justify-content:center;margin:32px 0}
.mario-heart{width:56px;height:56px;shape-rendering:crispEdges;transition:all 0.4s;filter:drop-shadow(0 0 10px rgba(229,37,33,0.5))}
.mario-heart.empty{opacity:0.2;filter:grayscale(1) drop-shadow(0 0 0 transparent)}
.status-box{text-align:center;padding:16px;border-radius:var(--r-sm);font-weight:700;font-size:16px;margin-top:16px;border:var(--glass-border);letter-spacing:.05em}
.cal-grid{display:grid;grid-template-columns:repeat(7,1fr);gap:8px;margin-top:20px}
.cal-head{text-align:center;font-size:11px;font-weight:700;color:var(--ink4);text-transform:uppercase;padding-bottom:12px}
.cal-day{aspect-ratio:1;border:1px solid var(--ink5);border-radius:var(--r-sm);display:flex;align-items:center;justify-content:center;font-size:14px;font-weight:600;font-family:'JetBrains Mono',monospace;color:var(--ink);cursor:pointer;transition:all 0.2s;background:var(--bg)}
.cal-day:hover{border-color:var(--r);background:rgba(255,68,31,0.1);transform:scale(1.05)}
.cal-day.empty{background:transparent;border-color:transparent;cursor:default}
.cal-day.empty:hover{transform:none;background:transparent}
.cal-day.late{background:var(--rbg);color:var(--red);border-color:rgba(239,68,68,0.5);box-shadow:inset 0 0 15px rgba(239,68,68,0.2)}
.cal-day.on-time{background:var(--gbg);color:var(--green);border-color:rgba(34,197,94,0.3)}

.doc-list{display:flex;flex-direction:column;gap:10px;margin-top:16px}
.doc-item{display:flex;align-items:center;justify-content:space-between;padding:12px 16px;background:var(--bg);border:1px solid var(--ink5);border-radius:var(--r-sm);font-size:13px;font-family:'JetBrains Mono',monospace}
.doc-item.done{background:var(--gbg);color:var(--gtext);border-color:var(--green)}
.doc-item.error{background:var(--rbg);color:var(--rtext);border-color:var(--red)}

.seg-list{display:flex;flex-direction:column;gap:12px}
.seg-card{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);padding:16px 20px;display:grid;grid-template-columns:48px 1fr auto;gap:16px;align-items:center;cursor:pointer;transition:all .2s;box-shadow:var(--shadow)}
.seg-card:hover{border-color:var(--ink4);transform:translateY(-2px);box-shadow:0 8px 20px rgba(0,0,0,0.3)}
.seg-urg{width:48px;height:48px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:10px;font-weight:700;text-transform:uppercase;letter-spacing:.05em;flex-shrink:0;flex-direction:column;gap:2px}
.seg-urg.venc{background:var(--rbg);color:var(--red);border:1px solid rgba(239,68,68,0.3);box-shadow:0 0 10px rgba(239,68,68,0.2)}
.seg-urg.hoy{background:var(--abg);color:var(--amber);border:1px solid rgba(245,158,11,0.3)}
.seg-urg.ok{background:var(--bg3);color:var(--ink3);border:1px solid var(--ink5)}
.seg-name{font-size:15px;font-weight:600;color:var(--ink);margin-bottom:6px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap}
.seg-detail{font-size:13px;color:var(--ink3)}
.seg-right{text-align:right;flex-shrink:0}
.seg-hora{font-size:14px;font-weight:700;color:var(--ink);font-family:'JetBrains Mono',monospace}

.agents-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:16px}
.ag-card{background:var(--white);border:var(--glass-border);border-radius:var(--r-lg);padding:20px;cursor:pointer;transition:all .2s;box-shadow:var(--shadow)}
.ag-card:hover{border-color:var(--ink4);transform:translateY(-3px);box-shadow:0 8px 24px rgba(0,0,0,0.4)}
.ag-top{display:flex;align-items:center;gap:14px;margin-bottom:16px}
.ag-av{width:46px;height:46px;border-radius:12px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:16px;color:#fff;flex-shrink:0;box-shadow:inset 0 -2px 5px rgba(0,0,0,0.2)}
.ag-name{font-size:14px;font-weight:600;color:var(--ink)}
.ag-email{font-size:11px;color:var(--ink4);font-family:'JetBrains Mono',monospace;margin-top:4px}
.ag-stats{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;padding-top:16px;border-top:1px solid var(--ink5)}
.ag-stat{text-align:center;background:var(--bg);padding:8px;border-radius:var(--r-sm);border:1px solid var(--ink5)}
.ag-stat-v{font-size:20px;font-weight:700;font-family:'Space Grotesk',sans-serif;color:var(--ink);line-height:1}
.ag-stat-l{font-size:9px;color:var(--ink4);text-transform:uppercase;letter-spacing:.05em;margin-top:6px;font-weight:600}

.nav-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.8);backdrop-filter:blur(4px);z-index:39}
.nav-overlay.on{display:block}

/* Estilos Popups Mapa */
.leaflet-popup-content-wrapper, .leaflet-popup-tip { background: var(--bg2); color: var(--ink); border: 1px solid var(--ink5); box-shadow: var(--shadow-glow); }
.leaflet-popup-content { font-family: 'Space Grotesk', sans-serif; margin: 12px; }
.leaflet-container a.leaflet-popup-close-button { color: var(--ink4); }

/* Menu AI Dropzone */
#ai-drop-zone.drag-over { border-color: var(--r) !important; background-color: var(--rbg); transform: scale(1.02); }

@media(max-width:860px){
  #app{grid-template-rows:60px 1fr}
  nav{position:fixed;left:0;top:60px;bottom:0;width:260px;flex-direction:column;align-items:flex-start;padding:24px 16px;transform:translateX(-100%);z-index:40;background:rgba(19,19,22,0.95);backdrop-filter:blur(10px);border-top:none;border-right:var(--glass-border);overflow-x:visible;}
  nav.open{transform:translateX(0);box-shadow:10px 0 30px rgba(0,0,0,0.5)}
  nav .nav-btn{width:100%;justify-content:flex-start;gap:16px;padding:0 16px;border-radius:var(--r-sm);height:50px;flex-shrink:0}
  nav .nav-tip{position:static;opacity:1;background:transparent;color:var(--ink2);font-size:14px;font-weight:500;padding:0;pointer-events:auto;transform:none;box-shadow:none}
  nav .nav-btn:hover .nav-tip{transform:none}
  nav .nav-sep{width:100%;height:1px;margin:8px 0}
  .hd-brand,.hd-kpi,.hd-conn{display:none} .hd-hamburger{display:flex}
  main{grid-row:2;grid-column:1;padding:20px} .pipeline,.two-col,.calc-wrap,.f2,.dr-grid{grid-template-columns:1fr}
  .metrics{grid-template-columns:1fr 1fr} .ph{flex-direction:column;gap:16px}
  .toolbar{gap:10px} .toolbar .fsel,.toolbar .search{min-width:100%;width:100%}
}
@media(max-width:480px){ .metrics{grid-template-columns:1fr} .fs-num{font-size:24px} main{padding:16px} }
</style>
</head>
<body>

<!-- CAPA DE LOGIN (AUTENTICACIÓN) -->
<div id="login-overlay" style="position:fixed;inset:0;background:var(--bg);z-index:10000;display:flex;align-items:center;justify-content:center;flex-direction:column;transition:opacity 0.4s ease;">
  <div class="form-card" style="width:100%;max-width:400px;text-align:center;box-shadow:var(--shadow-glow);background:var(--bg2);">
    <div style="margin-bottom:32px;">
       <div class="hd-logo" style="margin:0 auto 16px auto;width:64px;height:64px;border-radius:18px;"><svg viewBox="0 0 24 24" style="width:36px;height:36px;"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg></div>
       <h2 style="font-size:24px;font-weight:700;color:var(--ink);letter-spacing:-0.5px;">THE TEAM</h2>
       <p style="color:var(--ink4);font-size:13px;margin-top:4px;">Acceso exclusivo para THE TEAM</p>
    </div>
    <div class="field-g" style="text-align:left;margin-bottom:20px;">
       <label style="color:var(--ink3)">Correo Electrónico</label>
       <input type="email" id="login-email" placeholder="usuario@rappi.com" style="font-family:'JetBrains Mono';background:var(--bg);border-color:var(--ink5);">
    </div>
    <div class="field-g" style="text-align:left;margin-bottom:24px;">
       <label style="color:var(--ink3)">Contraseña</label>
       <input type="password" id="login-pass" placeholder="••••••••" style="font-family:'JetBrains Mono';background:var(--bg);border-color:var(--ink5);">
    </div>
    <div id="login-error" style="color:var(--red);font-size:13px;margin-bottom:20px;display:none;font-weight:600;padding:10px;background:var(--rbg);border-radius:var(--r-sm);"></div>
    <button class="btn btn-primary" id="btn-login-submit" style="width:100%;justify-content:center;padding:16px;font-size:15px;letter-spacing:0.05em;text-transform:uppercase;">Iniciar Sesión</button>
  </div>
</div>

<div id="loader">
  <div class="loader-icon"><svg viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg></div>
  <div class="loader-bar"><div class="loader-bar-fill"></div></div>
  <div class="loader-text" id="loader-text">Iniciando Sistema Core...</div>
  <div class="loader-error" id="loader-error" style="margin-top:12px;"></div>
</div>

<div class="nav-overlay" id="nav-overlay"></div>

<div id="app">
  <header>
    <button class="hd-hamburger" id="hd-hamburger" aria-label="Menu"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><line x1="3" y1="6" x2="21" y2="6"/><line x1="3" y1="12" x2="21" y2="12"/><line x1="3" y1="18" x2="21" y2="18"/></svg></button>
    <div class="hd-brand" id="hd-logo-btn" style="cursor:pointer" title="Ir al Inicio"><div class="hd-logo"><svg viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg></div></div>
    <button class="hd-btn-back" id="btn-global-back" title="Volver al Dashboard"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="15 18 9 12 15 6"/></svg></button>
    <div class="hd-title"><h1>THE TEAM</h1><span>Portal de Adquisición · MX</span></div>
    <div class="hd-right">
      <div class="hd-kpi"><span class="hd-kpi-label">Gestiones</span><span class="hd-kpi-val" id="hkpi-total">—</span></div>
      <div class="hd-kpi"><span class="hd-kpi-label">RTS Global</span><span class="hd-kpi-val orange" id="hkpi-ho">—</span></div>
      <div class="hd-kpi hd-kpi-click" id="btn-kpi-activos" title="Ver Directorio Roster"><span class="hd-kpi-label">Activos</span><span class="hd-kpi-val" id="hkpi-ag">—</span></div>
      <button class="hd-btn-theme" id="btn-theme-toggle" title="Cambiar Tema (Dark/Light)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 2a10 10 0 0 0 0 20z" fill="currentColor"/></svg></button>
      <button class="hd-btn" id="btn-refresh"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="1 4 1 10 7 10"/><path d="M3.51 15a9 9 0 102.13-9.36L1 10"/></svg>Sincronizar</button>
      <div class="hd-conn"><div class="hd-dot" id="hd-dot"></div><span class="hd-conn-text" id="hd-conn-text">—</span></div>
    </div>
  </header>

  <nav id="sidebar">
    <button class="nav-btn active" data-page="dashboard"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="7" height="7" rx="1.5"/><rect x="14" y="3" width="7" height="7" rx="1.5"/><rect x="3" y="14" width="7" height="7" rx="1.5"/><rect x="14" y="14" width="7" height="7" rx="1.5"/></svg><span class="nav-tip">Dashboard</span></button>
    <button class="nav-btn" data-page="registros"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/><line x1="16" y1="13" x2="8" y2="13"/><line x1="16" y1="17" x2="8" y2="17"/><line x1="10" y1="9" x2="8" y2="9"/></svg><span class="nav-tip">Base de Datos</span><span class="nav-badge" id="nb-total">—</span></button>
    <button class="nav-btn" data-page="roster"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg><span class="nav-tip">Directorio Roster</span></button>
    <button class="nav-btn" data-page="pipeline"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg><span class="nav-tip">Pipeline Kanban</span></button>
    <button class="nav-btn" data-page="desglose"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="18" height="18" rx="2" ry="2"/><line x1="3" y1="9" x2="21" y2="9"/><line x1="9" y1="21" x2="9" y2="9"/></svg><span class="nav-tip">Desglose de Etapas</span></button>
    <button class="nav-btn" data-page="llamadas"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg><span class="nav-tip">Analítica de Llamadas</span></button>
    <button class="nav-btn" data-page="zonas"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><polygon points="1 6 1 22 8 18 16 22 23 18 23 2 16 6 8 2 1 6"/><line x1="8" y1="2" x2="8" y2="18"/><line x1="16" y1="6" x2="16" y2="22"/></svg><span class="nav-tip">Heatmap & Zonas</span></button>
    <button class="nav-btn" data-page="seguimientos"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="4" width="18" height="18" rx="2"/><line x1="16" y1="2" x2="16" y2="6"/><line x1="8" y1="2" x2="8" y2="6"/><line x1="3" y1="10" x2="21" y2="10"/><circle cx="8" cy="15" r="1" fill="currentColor"/><circle cx="12" cy="15" r="1" fill="currentColor"/><circle cx="16" cy="15" r="1" fill="currentColor"/></svg><span class="nav-tip">Callbacks & Tareas</span><span class="nav-badge" id="nb-seg" style="display:none"></span></button>
    <div class="nav-sep"></div>
    <button class="nav-btn" data-page="indicadores"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M3 3v18h18"/><rect x="7" y="14" width="4" height="7"/><rect x="15" y="9" width="4" height="12"/><path d="M11 6l4 4"/></svg><span class="nav-tip">KPIs & Comisiones</span></button>
    <button class="nav-btn" data-page="calculadora"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="4" y="2" width="16" height="20" rx="2"/><line x1="8" y1="6" x2="16" y2="6"/><line x1="16" y1="14" x2="16.01" y2="14"/><line x1="12" y1="14" x2="12.01" y2="14"/><line x1="8" y1="14" x2="8.01" y2="14"/><line x1="16" y1="18" x2="16.01" y2="18"/><line x1="12" y1="18" x2="12.01" y2="18"/><line x1="8" y1="18" x2="8.01" y2="18"/><line x1="16" y1="10" x2="16.01" y2="10"/><line x1="12" y1="10" x2="12.01" y2="10"/><line x1="8" y1="10" x2="8.01" y2="10"/></svg><span class="nav-tip">Simulador de Payout</span></button>
    <button class="nav-btn" data-page="tardanzas"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg><span class="nav-tip">Control de Asistencia</span></button>
    <button class="nav-btn" data-page="documentos"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M21.44 11.05l-9.19 9.19a6 6 0 0 1-8.49-8.49l9.19-9.19a4 4 0 0 1 5.66 5.66l-9.2 9.19a2 2 0 0 1-2.83-2.83l8.49-8.48"/></svg><span class="nav-tip">Sync con Google Drive</span></button>
    <button class="nav-btn" data-page="nuevo"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="16"/><line x1="8" y1="12" x2="16" y2="12"/></svg><span class="nav-tip">Carga Rápida (Form)</span></button>
    <div class="nav-sep"></div>
    <button class="nav-btn" data-page="menuai"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M12 2a10 10 0 1 0 10 10H12V2z"/><path d="M12 12L2.5 7.5"/></svg><span class="nav-tip">Rappi Menu AI Pro</span></button>
  </nav>

  <main id="main-content">
    <!-- DASHBOARD -->
    <div class="page on" id="p-dashboard">
      <div class="ph">
        <div class="ph-left"><h2>Vista General</h2><p id="dash-updated" style="font-family:'JetBrains Mono',monospace;font-size:12px;">Cargando streams de datos...</p></div>
      </div>
      <div class="metrics" id="dash-metrics"></div>
      <div class="sec-title">Embudo de Conversión <a id="link-pipeline" style="cursor:pointer;">Analizar Pipeline ›</a></div>
      <div class="funnel-row" id="dash-funnel"></div>
      <div class="two-col" style="margin-top:32px">
        <div class="card"><div class="sec-title" style="margin-bottom:20px">Top Performers</div><div id="dash-ranking"></div></div>
        <div class="card"><div class="sec-title" style="margin-bottom:20px">Distribución de Estados</div><div id="dash-resultados"></div></div>
      </div>
      <div class="sec-title" style="margin-top:16px">Gestiones Recientes <a id="link-registros" style="cursor:pointer;">Acceder BBDD ›</a></div>
      <div class="tbl-wrap"><div class="tbl-scroll"><table>
        <thead><tr><th>Entity / Merchant</th><th>Contacto</th><th>Stage</th><th>Status</th><th>Agente</th><th>Timestamp</th></tr></thead>
        <tbody id="dash-tbody"></tbody>
      </table></div></div>
    </div>

    <!-- ANÁLISIS BBDD -->
    <div class="page" id="p-analisis-bbdd">
      <div class="ph" style="margin-bottom:24px;">
        <div class="ph-left">
          <button class="btn btn-ghost btn-sm" style="margin-bottom:16px;padding:0;color:var(--ink4)" onclick="go('dashboard')">‹ Retornar</button>
          <h2>Data Warehouse Analytics</h2><p>Desglose analítico global del pipeline.</p>
        </div>
      </div>
      <div class="toolbar" style="margin-bottom:24px;">
        <select class="fsel" id="f-analisis-agente"><option value="">Todos los agentes</option></select>
        <select class="fsel" id="f-analisis-mes"><option value="">Todos los Meses</option></select>
        <select class="fsel" id="f-analisis-dia" disabled><option value="">Todos los Días</option></select>
        <button class="btn btn-ghost btn-sm" id="btn-reset-analisis">Resetear Filtros</button>
      </div>
      <div style="display:flex; gap:16px; margin-bottom:32px; flex-wrap:wrap;">
        <div class="mc" style="flex:1; min-width:140px; border-top:2px solid var(--ink2); cursor:default; transform:none;">
          <div class="mc-label">Volumen Gestiones</div><div class="mc-val" id="analisis-tot-text">0</div></div>
        <div class="mc" style="flex:1; min-width:140px; border-top:2px solid var(--purple); cursor:default; transform:none;">
          <div class="mc-label">Volumen Cierres</div><div class="mc-val" id="analisis-rts-text" style="color:var(--purple);text-shadow:0 0 10px rgba(139,92,246,0.3)">0</div></div>
        <div class="mc" style="flex:1; min-width:140px; border-top:2px solid var(--green); cursor:default; transform:none;">
          <div class="mc-label">Ratio de Conversión</div><div class="mc-val" id="analisis-conv-text" style="color:var(--green);text-shadow:0 0 10px rgba(34,197,94,0.3)">0%</div></div>
      </div>
      <div class="two-col">
        <div class="card full" style="height:360px;display:flex;flex-direction:column"><div class="sec-title">Evolución Histórica (Trendline)</div><div style="flex:1;position:relative"><canvas id="chart-total-hist"></canvas></div></div>
        <div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title">Distribución Geográfica</div><div style="flex:1;position:relative"><canvas id="chart-total-zonas"></canvas></div></div>
        <div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title">Peak Hours (Productividad)</div><div style="flex:1;position:relative"><canvas id="chart-total-horas"></canvas></div></div>
      </div>
    </div>

    <!-- REGISTROS -->
    <div class="page" id="p-registros">
      <div class="ph"><div class="ph-left"><h2>Base de Datos Maestra</h2><p>Acceso estructurado a los registros de prospección</p></div><div class="ph-right"><button class="btn btn-primary" id="btn-nueva-reg">Insertar Row</button></div></div>
      <div class="toolbar">
        <div class="search"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg><input type="text" id="q" placeholder="Query: restaurante, tel, keyword…"></div>
        <select class="fsel" id="f-etapa"><option value="">Filtro: Stage</option><option>PROSPECTO</option><option>ED</option><option>DM</option><option>FIRMA CONTRATO</option><option>DC</option><option>DATA COLECCTION / SOB</option><option>RTS</option></select>
        <select class="fsel" id="f-res"><option value="">Filtro: Status</option><option>Contactado - Interesado</option><option>Contactado - No interesado</option><option>No contesta</option><option>Buzón de voz</option><option>Número errado / no existe</option><option>WhatsApp enviado</option><option>Cuelga</option></select>
        <select class="fsel" id="f-agente"><option value="">Filtro: Agente</option></select>
        <button class="btn btn-ghost btn-sm" id="btn-reset-filters">Clear</button>
        <div style="width:100%;height:1px;background:var(--ink5);margin:6px 0"></div>
        <select class="fsel" id="f-mes"><option value="">Todo el Histórico</option></select>
        <select class="fsel" id="f-dia"><option value="">Día</option></select>
        <div style="display:flex;align-items:center;gap:8px"><span style="font-size:12px;color:var(--ink4);font-family:'JetBrains Mono'">[MIN]:</span><select class="fsel" id="f-hora-ini" style="min-width:100px"><option value="">--:--</option></select><span style="font-size:12px;color:var(--ink4);font-family:'JetBrains Mono'">[MAX]:</span><select class="fsel" id="f-hora-fin" style="min-width:100px"><option value="">--:--</option></select></div>
        <div style="margin-left:auto;display:flex;gap:6px;background:var(--bg3);padding:6px;border-radius:10px;border:var(--glass-border)"><button class="btn btn-sm btn-primary" id="btn-v-table">Datagrid</button><button class="btn btn-sm btn-ghost" id="btn-v-charts">Dashboard</button></div>
      </div>
      <div id="reg-view-table"><div class="tbl-wrap"><div class="tbl-scroll"><table><thead><tr><th id="th-fecha">Timestamp</th><th id="th-restaurante">Entity Name</th><th>Phone</th><th id="th-proceso">Pipeline Stage</th><th>Call Status</th><th id="th-email">Assigned User</th><th>Log / Comments</th><th>Merchant ID</th></tr></thead><tbody id="reg-tbody"></tbody></table></div><div class="tbl-footer"><span class="tbl-count" id="reg-count">—</span><div class="pager" id="reg-pager"></div></div></div></div>
      <div id="reg-view-charts" style="display:none;margin-top:24px">
        <div class="card full" style="height:340px;display:flex;flex-direction:column;margin-bottom:24px"><div class="sec-title" style="font-size:16px">Volumen de Prospección</div><div style="flex:1;position:relative"><canvas id="chart-reg-tendencia"></canvas></div></div>
        <div class="two-col">
          <div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title">Distribución por Nodos</div><div style="flex:1;position:relative"><canvas id="chart-reg-etapa"></canvas></div></div>
          <div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title">Call Status Breakdown</div><div style="flex:1;position:relative"><canvas id="chart-reg-res"></canvas></div></div>
          <div class="card full" style="height:320px;display:flex;flex-direction:column"><div class="sec-title">Output por Agente <span style="font-weight:normal;color:var(--ink4);font-size:12px;font-family:'JetBrains Mono'">(Select to drill-down)</span></div><div style="flex:1;position:relative"><canvas id="chart-reg-agente"></canvas></div></div>
          <div class="card full" id="card-agente-detalle" style="display:none;background:var(--bg2);border:2px solid var(--r);box-shadow:var(--shadow-glow)"><div class="sec-title" id="title-agente-detalle" style="font-size:18px;color:var(--ink)">Análisis de Conversión</div><div style="margin-top:20px;margin-bottom:20px;padding:20px;background:var(--bg3);border-radius:var(--r-md);border:var(--glass-border)"><div class="sec-title" style="font-size:11px;color:var(--ink3);margin-bottom:16px">Métricas (T-7)</div><div id="agente-weekly-kpis" style="display:flex;gap:20px;flex-wrap:wrap"></div></div><div style="display:grid;grid-template-columns:2fr 1fr;gap:28px"><div style="height:240px;position:relative"><canvas id="chart-funnel"></canvas></div><div id="agente-kpis" style="display:flex;flex-direction:column;gap:16px;justify-content:center"></div></div></div>
        </div>
      </div>
    </div>

    <!-- PIPELINE -->
    <div class="page" id="p-pipeline"><div class="ph"><div class="ph-left"><h2>Pipeline Kanban</h2><p>Visualización del flujo de adquisición de merchants</p></div></div><div class="funnel-row" id="pl-funnel" style="margin-bottom:32px"></div><div class="pipeline" id="pipeline-grid"></div></div>

    <!-- ROSTER -->
    <div class="page" id="p-roster">
      <div class="ph"><div class="ph-left"><h2>Directorio Roster</h2><p>Listado centralizado de todos los agentes activos en el sistema</p></div></div>
      <div style="overflow-x:auto;-webkit-overflow-scrolling:touch;background:var(--bg2);border:var(--glass-border);border-radius:var(--r-lg);padding:16px;">
        <table class="elegant-table" style="min-width: 800px;">
          <thead><tr>
            <th>Usuario / Agente</th>
            <th style="text-align:center">ID (Email)</th>
            <th style="text-align:center">Teléfono</th>
            <th style="text-align:center">Status de Red</th>
          </tr></thead>
          <tbody id="roster-tbody"></tbody>
        </table>
      </div>
    </div>

    <!-- DESGLOSE -->
    <div class="page" id="p-desglose">
      <div class="ph">
        <div class="ph-left"><h2>Node Analytics</h2><p>Matrix operativa de agentes en el pipeline de ventas</p></div>
        <div class="ph-right" style="flex-wrap:wrap; align-items:center;">
          <div style="display:flex;gap:6px;background:var(--bg3);padding:6px;border-radius:10px;border:var(--glass-border)">
            <button class="btn btn-sm btn-primary" id="btn-desglose-table">Datagrid</button>
            <button class="btn btn-sm btn-ghost" id="btn-desglose-charts">Métricas Visuales</button>
          </div>
          <button class="btn btn-primary" id="btn-global-funnel" style="background:var(--bg3); border:1px solid var(--r); color:var(--r);"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="width:16px;height:16px"><polygon points="22 3 2 3 10 12.46 10 19 14 21 14 12.46 22 3"/></svg>Conversión Global</button>
        </div>
      </div>
      <div id="desglose-view-table">
        <div style="overflow-x:auto;-webkit-overflow-scrolling:touch;background:var(--bg2);border:var(--glass-border);border-radius:var(--r-lg);padding:16px;">
          <table class="elegant-table"><thead><tr><th style="min-width:240px">Usuario</th><th style="text-align:center;color:var(--ink3)">Total<br>Logs</th><th style="text-align:center">Prospect</th><th style="text-align:center">ED</th><th style="text-align:center">DM</th><th style="text-align:center">Contract</th><th style="text-align:center">DC</th><th style="text-align:center">Collection</th><th style="text-align:center;color:var(--green);font-weight:800;font-size:12px;text-shadow:0 0 5px rgba(34,197,94,0.5)">RTS</th><th style="text-align:center">Target</th><th style="text-align:center">Attainment</th><th style="text-align:center">Acción</th></tr></thead><tbody id="desglose-tbody"></tbody></table>
        </div>
      </div>
      <div id="desglose-view-charts" style="display:none;margin-top:24px">
        <div class="card full" style="height:340px;display:flex;flex-direction:column;margin-bottom:24px">
           <div class="sec-title">RTS vs Meta de Adquisición (Top Agents)</div>
           <div style="flex:1;position:relative"><canvas id="chart-desglose-attainment"></canvas></div>
        </div>
        <div class="two-col">
           <div class="card" style="height:340px;display:flex;flex-direction:column">
              <div class="sec-title">Carga Operativa (Toques/Logs Totales)</div>
              <div style="flex:1;position:relative"><canvas id="chart-desglose-workload"></canvas></div>
           </div>
           <div class="card" style="height:340px;display:flex;flex-direction:column">
              <div class="sec-title">Distribución General (Pipeline)</div>
              <div style="flex:1;position:relative"><canvas id="chart-desglose-pipeline"></canvas></div>
           </div>
        </div>
      </div>
    </div>

    <!-- DETALLE LLAMADAS -->
    <div class="page" id="p-llamadas">
      <div class="ph" style="margin-bottom:24px;"><div class="ph-left"><h2>Telecom Analytics</h2><p>Extracción de registros de llamadas (Telephony Logs)</p></div></div>
      <div class="toolbar" style="margin-bottom:24px;"><select class="fsel" id="f-llamadas-agente" style="min-width:280px;"><option value="">Vista General (Cross-Agent)</option></select><button class="btn btn-primary btn-sm" id="btn-refresh-llamadas" style="margin-left:auto;">Fetch Sync</button></div>
      <div class="two-col" style="margin-bottom:32px;"><div class="mc" style="border-top:2px solid var(--blue); cursor:default; transform:none;"><div class="mc-label">Call Count Total</div><div class="mc-val" id="ll-kpi-total" style="color:var(--blue)">0</div></div><div class="mc" style="border-top:2px solid var(--teal); cursor:default; transform:none;"><div class="mc-label">Agentes Enrutados</div><div class="mc-val" id="ll-kpi-agentes" style="color:var(--teal)">0</div></div></div>
      <div class="two-col" style="margin-bottom:32px;"><div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title">Tendencia de Trafico</div><div style="flex:1;position:relative"><canvas id="chart-ll-tendencia"></canvas></div></div><div class="card" style="height:340px;display:flex;flex-direction:column"><div class="sec-title" id="title-ll-comp">Disposition Breakdown</div><div style="flex:1;position:relative"><canvas id="chart-ll-comparativa"></canvas></div></div></div>
      <div class="sec-title">Raw Logs Extract</div>
      <div class="toolbar" style="margin-bottom:20px;padding:12px 16px;"><div class="search"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg><input type="text" id="q-llamadas" placeholder="Search hash, phone, agent..."></div></div>
      <div class="tbl-wrap"><div class="tbl-scroll"><table class="elegant-table" style="min-width: 1000px;"><thead><tr id="llamadas-thead-tr"></tr></thead><tbody id="llamadas-tbody"></tbody></table></div><div class="tbl-footer"><span class="tbl-count" id="ll-count" style="font-family:'JetBrains Mono'">—</span></div></div>
    </div>

    <!-- ZONAS -->
    <div class="page" id="p-zonas">
      <div class="ph"><div class="ph-left"><h2>Geo-Heatmaps & Zonas Hunteables</h2><p>Mapeo de densidad y directorio de zonas habilitadas para prospección</p></div></div>
      <div class="two-col">
        <div class="card full" style="padding:0;overflow:hidden;position:relative;min-height:450px;background:var(--bg3);">
          <div id="map-container" style="width:100%;height:100%;min-height:450px;z-index:1;"></div>
        </div>
      </div>
      <div class="sec-title" style="margin-top:32px">Directorio de Zonas (Targets & Orgánicas)</div><div class="agents-grid" id="zonas-grid"></div>
    </div>

    <!-- SEGUIMIENTOS -->
    <div class="page" id="p-seguimientos"><div class="ph"><div class="ph-left"><h2>Callbacks & Alertas</h2><p>Queue de tareas pendientes derivadas del NLP en comentarios</p></div></div><div class="seg-list" id="seg-list"></div></div>

    <!-- INDICADORES -->
    <div class="page" id="p-indicadores">
      <div class="ph"><div class="ph-left"><h2>KPIs de Negocio</h2><p>Proyección de Payouts y cumplimiento de cuotas</p></div><div class="ph-right"><div style="display:flex;align-items:center;gap:12px;background:var(--bg3);padding:8px 16px;border-radius:var(--r-sm);border:var(--glass-border)"><label style="font-size:12px;font-weight:600;color:var(--ink3)">Target Base:</label><input type="number" id="global-meta" class="ind-meta-input" value="20" min="1" max="999"></div></div></div>
      <div class="tbl-wrap"><div class="tbl-scroll"><table><thead><tr><th>Usuario</th><th style="text-align:center">Leads Handled</th><th style="text-align:center">Conv. Interés</th><th style="text-align:center;color:var(--purple)">Handoffs (RTS)</th><th style="text-align:center">Attainment (C/M)</th><th style="text-align:right">Payout Calc. (Est)</th></tr></thead><tbody id="ind-tbody"></tbody></table></div></div>
    </div>

    <!-- CALCULADORA -->
    <div class="page" id="p-calculadora">
      <div class="ph"><div class="ph-left"><h2>Payout Simulator</h2><p>Simulador algorítmico de esquema comisional por Tiers</p></div></div>
      <div class="calc-wrap" id="calc-container">
        <div style="display:flex;flex-direction:column;gap:24px">
          <div class="form-card" style="margin:0">
            <div class="form-card-title">Data Binding</div>
            <div class="field-g" style="margin-bottom:20px"><label>1. Enlazar Perfil Operativo</label><select id="calc-agent-sel" style="border-color:var(--r);background-color:var(--bg3);color:var(--ink);box-shadow:0 0 10px rgba(255,68,31,0.1)"><option value="">Selecciona tu ID...</option></select></div>
            <div class="f2"><div class="field-g"><label>Target (C/M)</label><input type="number" id="calc-meta" value="0" readonly style="background-color:var(--bg2);cursor:not-allowed;font-weight:bold;color:var(--ink4);font-family:'JetBrains Mono'"></div><div class="field-g"><label>RTS Vol.</label><input type="number" id="calc-handoffs" value="0" readonly style="background-color:var(--bg2);cursor:not-allowed;font-weight:bold;color:var(--ink4);font-family:'JetBrains Mono'"></div></div>
          </div>
          <div class="calc-result" style="display:flex;justify-content:space-between;align-items:center;text-align:left">
            <div><div class="cr-label">Attainment</div><div class="cr-val" id="calc-att" style="font-size:42px;margin-bottom:8px">0%</div><div class="cr-sub" id="calc-sub" style="background:rgba(0,0,0,0.4);border:1px solid rgba(255,255,255,0.1)">Payout: 0%</div></div>
            <div style="text-align:right"><div class="cr-label">Forecasted Payout</div><div class="cr-val" id="calc-pago" style="color:var(--rtext);font-size:42px;margin-bottom:0;text-shadow:0 0 15px rgba(248,113,113,0.5)">$0</div></div>
          </div>
        </div>
        <div class="tier-list"><div class="tier-row tier-header"><div>Att%</div><div>Payout%</div><div>Base</div><div style="text-align:right">Delta</div></div><div id="tier-body"></div></div>
      </div>
    </div>

    <!-- TARDANZAS -->
    <div class="page" id="p-tardanzas">
      <div class="ph">
         <div class="ph-left"><h2>Retardos</h2><p>Control general de asistencias y penalizaciones (Automático).</p></div>
      </div>
      <div class="tbl-wrap">
         <div class="tbl-scroll">
            <table class="elegant-table">
               <thead>
                  <tr>
                     <th>Agente / Usuario</th>
                     <th style="text-align:center" title="Ingresos después de las 09:00">Llegadas Tarde</th>
                     <th style="text-align:center" title="Salidas antes de las 18:00">Salidas Temprano</th>
                     <th style="text-align:center" title="Faltas u omisiones de marca">Otras Faltas</th>
                     <th style="text-align:center">Vidas Restantes</th>
                     <th style="text-align:center">Estado de Cuenta</th>
                     <th style="text-align:center">Acción</th>
                  </tr>
               </thead>
               <tbody id="tar-tbody"></tbody>
            </table>
         </div>
      </div>
    </div>

    <!-- DOCUMENTOS DRIVE -->
    <div class="page" id="p-documentos">
      <div class="ph"><div class="ph-left"><h2>Drive Storage Sync</h2><p>Módulo de carga de documentos ED/Contratos directos a G-Drive.</p></div></div>
      <div class="form-wrap" style="max-width:840px;">
        <div class="form-card">
          <div class="form-card-title">Routing Path</div>
          <div class="f2">
            <div class="field-g"><label>1. Root Node (User) *</label><select id="doc-agent-sel" style="font-family:'JetBrains Mono'"><option value="">Awaiting Input...</option></select></div>
            <div class="field-g"><label>2. Entity Node (Merchant) *</label><input type="text" id="doc-restaurante" placeholder="Ej: Tacos El Güero" style="font-family:'JetBrains Mono'"></div>
          </div>
          <div style="margin-top:24px; border-top:1px solid var(--ink5); padding-top:24px;">
            <div class="form-card-title">Payload (Max 10MB/Unit)</div>
            <div style="display:flex; gap:16px; margin-bottom:20px;">
               <button class="btn btn-outline" style="flex:1; justify-content:center; padding:14px; border-color:rgba(59,130,246,0.5); color:var(--btext); background:var(--bbg);" id="btn-select-files" onclick="document.getElementById('doc-files-input').click()">Select Files</button>
               <button class="btn btn-outline" style="flex:1; justify-content:center; padding:14px; border-color:rgba(245,158,11,0.5); color:var(--atext); background:var(--abg);" id="btn-select-folder" onclick="document.getElementById('doc-folder-input').click()">Select Directory</button>
            </div>
            <input type="file" id="doc-files-input" multiple style="display:none;">
            <input type="file" id="doc-folder-input" webkitdirectory directory multiple style="display:none;">
            <div class="doc-list" id="doc-queue"><div style="text-align:center; padding:24px; color:var(--ink4); font-size:13px; border:1px dashed var(--ink5); border-radius:var(--r-sm); background:var(--bg3);">No hay archivos en la cola.</div></div>
          </div>
          <button class="btn btn-primary" id="btn-upload-doc" style="width:100%;justify-content:center;padding:16px;margin-top:32px; font-size:15px; letter-spacing:0.05em">Ejecutar Upload (Drive API)</button>
        </div>
      </div>
    </div>

    <!-- NUEVA GESTIÓN -->
    <div class="page" id="p-nuevo">
      <div class="ph"><div class="ph-left"><h2>Data Entry Form</h2><p>Inserción manual de registros al Data Warehouse</p></div></div>
      <div class="form-wrap">
        <div class="alert a-info" style="margin-bottom:24px">[!] Required fields marked with *. Email syntax forces @rappi.com. Merchant ID forces MX prefix.</div>
        <div class="form-card">
          <div class="form-card-title">Entity Core Info</div>
          <div class="f2"><div class="field-g"><label>Entity Name *</label><input id="n-nom" placeholder="e.g. Tacos El Güero" maxlength="200"></div><div class="field-g"><label>Tel / Cel</label><input id="n-tel" placeholder="+52..." maxlength="20" style="font-family:'JetBrains Mono'"></div></div>
          <div class="f2"><div class="field-g"><label>Country</label><select id="n-pais"><option>MX</option><option>CO</option><option>BR</option><option>AR</option></select></div><div class="field-g"><label>Zone Cluster</label><input id="n-zona" placeholder="CDMX, Monterrey…" maxlength="100"></div></div>
          <div class="field-g"><label>Merchant ID (MX######)</label><input id="n-id" placeholder="MX491983" maxlength="20" style="font-family:'JetBrains Mono'"></div>
        </div>
        <div class="form-card">
          <div class="form-card-title">Operation Details</div>
          <div class="f2">
            <div class="field-g"><label>Pipeline Stage *</label><select id="n-etapa"><option>PROSPECTO</option><option>ED</option><option>DM</option><option>FIRMA CONTRATO</option><option>DC</option><option>DATA COLECCTION / SOB</option><option>RTS</option></select></div>
            <div class="field-g"><label>Call Status *</label><select id="n-res"><option value="">Awaiting Input...</option><option>Contactado - Interesado</option><option>Contactado - No interesado</option><option>No contesta</option><option>Buzón de voz</option><option>Número errado / no existe</option><option>WhatsApp enviado</option><option>Cuelga</option><option>Ya tiene cuenta Rappi</option><option>Llamar después</option><option>Renegociación</option></select></div>
          </div>
          <div class="field-g"><label>Auth Email * (@rappi.com)</label><input id="n-ag" type="email" placeholder="user@rappi.com" maxlength="100" style="font-family:'JetBrains Mono'"></div>
          <div class="f2"><div class="field-g"><label>Callback Date</label><input id="n-fseg" type="date" style="font-family:'JetBrains Mono'"></div><div class="field-g"><label>Callback Time</label><input id="n-hseg" type="time" style="font-family:'JetBrains Mono'"></div></div>
          <div class="field-g"><label>Operation Log</label><textarea id="n-com" placeholder="Añade contexto, acuerdos, tags…" maxlength="1000"></textarea></div>
          <div class="field-g"><label>Source URL (Maps/Web)</label><input id="n-link" placeholder="https://…" maxlength="500" type="url" style="font-family:'JetBrains Mono'"></div>
        </div>
        <div id="n-alert" style="display:none"></div>
        <div style="display:flex;gap:12px;margin-bottom:40px"><button class="btn btn-primary" id="n-btn" style="flex:1;justify-content:center;padding:14px;font-size:14px">Commit Record</button><button class="btn btn-outline" id="n-clear-btn" style="padding:14px">Flush Form</button></div>
      </div>
    </div>

    <!-- RAPPI MENU AI (INTEGRADO) -->
    <div class="page" id="p-menuai">
      <div class="ph">
        <div class="ph-left">
            <h2>Rappi Menu AI Pro</h2>
            <p>Digitalización 1:1 con motor Gemini 2.5 Flash + Imagen 4</p>
        </div>
      </div>
      
      <!-- Upload section -->
      <div id="ai-upload-sec" class="form-card" style="max-width: 800px; margin: 0 auto; box-shadow: var(--shadow-glow);">
          <div class="form-card-title" style="font-size: 16px; margin-bottom: 12px;"><span style="color:var(--r); font-weight:800; font-style:italic">Misión:</span> Escaneo Perfecto</div>
          <p style="color:var(--ink4); font-size:12px; margin-bottom: 24px; text-transform:uppercase; letter-spacing:0.1em">Protocolo Margen 0% · Transcripción Literal de Datos</p>
          
          <div class="field-g">
              <label>Nombre del Comercio *</label>
              <input type="text" id="ai-rest-name" placeholder="EJ: TAQUERÍA EL FOGÓN" style="font-size: 18px; font-weight: 800; text-transform: uppercase; text-align: center; padding: 16px;">
          </div>
          
          <div id="ai-drop-zone" style="border: 2px dashed var(--ink5); border-radius: var(--r-xl); padding: 80px 20px; text-align: center; cursor: pointer; transition: all 0.3s; margin-top: 24px; background: var(--bg2);">
              <div style="font-size: 64px; margin-bottom: 16px; transition: transform 0.3s;" id="ai-drop-icon">📸</div>
              <h3 style="font-size: 24px; font-weight: 800; color: var(--ink); text-transform: uppercase;">Sube el Menú</h3>
              <p style="color: var(--ink4); font-size: 12px; margin-top: 8px;">Arrastra la imagen/PDF o haz clic aquí</p>
              <input type="file" id="ai-file-input" accept="image/*,application/pdf" style="display: none;">
          </div>
      </div>

      <!-- Loading section -->
      <div id="ai-loading-sec" style="display: none; text-align: center; padding: 80px 20px;">
           <div style="font-size: 12px; color: var(--r); font-weight: 800; margin-bottom: 16px; font-family: 'JetBrains Mono'; letter-spacing: 0.2em; text-transform: uppercase;">CRONÓMETRO DE MISIÓN <br> <span id="ai-timer" style="font-size:20px; color:var(--ink);">00:00:00</span></div>
           
           <div style="font-size: 120px; font-weight: 900; color: var(--ink); line-height: 1; font-style:italic; text-shadow: 0 0 40px rgba(255,68,31,0.3);" id="ai-perc">0%</div>
           
           <div class="bar-track" style="max-width: 500px; margin: 32px auto; height: 12px; background: rgba(255,255,255,0.05); border: 1px solid var(--ink5);">
               <div class="bar-fill" id="ai-bar" style="width: 0%; background: linear-gradient(90deg, var(--r), var(--amber)); box-shadow: 0 0 20px var(--r);"></div>
           </div>
           
           <div style="color: var(--r); font-size: 24px; font-weight: 800; text-transform: uppercase; font-style:italic;" id="ai-status">Sincronizando IA...</div>
           <div style="color: var(--ink4); font-size: 11px; margin-top: 8px; text-transform: uppercase; letter-spacing: 0.2em;" id="ai-substatus">Escaneando cada carácter sin errores</div>
      </div>

      <!-- Results Section -->
      <div id="ai-results-sec" style="display: none;">
           <div style="display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; margin-bottom: 32px; gap: 20px; border-bottom: 1px solid var(--ink5); padding-bottom: 24px;">
               <div>
                   <h3 id="ai-final-name" style="font-size: 36px; font-weight: 900; color: var(--ink); font-style:italic; text-transform:uppercase;">RESTAURANTE</h3>
                   <p style="color: var(--ink4); font-size: 12px; text-transform: uppercase; letter-spacing: 0.1em; margin-top:4px;">Extracción Literal Finalizada (100%)</p>
                   <div style="margin-top: 12px; display: inline-flex; align-items: center; gap: 8px; background: var(--bg2); padding: 6px 12px; border-radius: 20px; border: var(--glass-border);">
                       <span style="font-size: 10px; color: var(--ink4); font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em;">Tiempo de Sync:</span>
                       <span id="ai-final-time" style="font-family: 'JetBrains Mono'; font-weight: 800; color: var(--r);">00:00:00</span>
                   </div>
               </div>
               <div style="display: flex; gap: 12px; flex-wrap: wrap;">
                   <button id="ai-btn-zip" class="btn" style="background: var(--blue); color: #fff; padding: 12px 24px; font-size: 13px;"><span>📦</span> ZIP Fotos Sony Pro</button>
                   <button id="ai-btn-reset" class="btn btn-outline" style="padding: 12px 24px;">Nuevo Escaneo</button>
               </div>
           </div>
           
           <div class="tbl-wrap">
               <div class="tbl-scroll">
                   <table class="elegant-table" style="min-width: 1200px;">
                       <thead>
                           <tr>
                               <th style="text-align:center">Corredor<br><span style="font-size:9px; color:var(--ink5);">(max. 3 pal)</span></th>
                               <th style="text-align:center">Nombre Plato<br><span style="font-size:9px; color:var(--ink5);">(max. 5 pal)</span></th>
                               <th style="width:25%; text-align:center">Descripción<br><span style="font-size:9px; color:var(--ink5);">(max. 40 pal)</span></th>
                               <th style="text-align:center">Precio</th>
                               <th style="text-align:center">Elecciones<br><span style="font-size:9px; color:var(--ink5);">(Opcional)</span></th>
                               <th style="text-align:center">Agregar<br><span style="font-size:9px; color:var(--ink5);">(Opcional)</span></th>
                               <th style="text-align:center">Quitar<br><span style="font-size:9px; color:var(--ink5);">(Opcional)</span></th>
                           </tr>
                       </thead>
                       <tbody id="ai-table-body"></tbody>
                   </table>
               </div>
           </div>
           
           <div style="margin-top: 32px; display:flex; justify-content:center; gap:16px; flex-wrap:wrap;">
               <button id="ai-btn-copy" class="btn btn-primary" style="padding: 16px 40px; font-size: 14px; text-transform: uppercase; letter-spacing: 0.1em; border-radius:30px;">Copiar para Sheets (Celda B2)</button>
               <a href="https://docs.google.com/spreadsheets/d/1YYu6rhgiBzlItp5JGty5yIfw6fQ3k7XUwgvg2yZQSvA/copy" target="_blank" class="btn btn-outline" style="padding: 16px 40px; font-size: 14px; text-transform: uppercase; letter-spacing: 0.1em; border-radius:30px; text-decoration: none;">Abrir Hoja de Registro</a>
           </div>
      </div>
    </div>
  </main>
</div>

<!-- DRAWER -->
<div class="overlay" id="overlay">
  <div class="drawer" id="drawer">
    <div class="dr-head"><div class="dr-head-main"><div class="dr-title" id="dr-title">—</div><div class="dr-sub" id="dr-sub">—</div></div><button class="dr-close" id="dr-close-btn">✕</button></div>
    <div class="dr-body" id="dr-body"></div>
    <div class="dr-foot" id="dr-foot"></div>
  </div>
</div>
<div id="toasts"></div>

<script>
const CONFIG = Object.freeze({
  SID: '1fdlxZLChYsownCkzmdEDafXXn7sChXjj6HiUxksQl5o', 
  SCRIPT_URL: 'https://script.google.com/macros/s/AKfycbwrkqTtTe8QNJS1kCk0xp0AyfM95LqurFFBrqP_s-Tzs6Af9VeYNFegTIdwdJXqm1eAqg/exec',
  FETCH_TIMEOUT_MS: 12000,
  DEBOUNCE_MS: 280,
  PAGE_SIZE: 35
});

// GLOBALS CRM
let CURRENT_USER_EMAIL = sessionStorage.getItem('rappi_auth_user') || '';
const ADMIN_EMAIL = "santiago.saenz@rappi.com";
const IS_ADMIN = () => CURRENT_USER_EMAIL === ADMIN_EMAIL;

let DATA = [], FILTERED = [], sortCol = 'fecha', sortDir = 1, currentPage = 1, AGENT_STATS = {};
let INDICADORES_TOTALS = { prospectos:0, ed:0, dm:0, firma:0, dc:0, datacol:0, rts:0 };
let INDICADORES_COL_FOUND = { prospectos:false, ed:false, dm:false, firma:false, dc:false, datacol:false, rts:false, meta:false };
let TARDANZAS_DATA = {}, DOCS_QUEUE = [], LLAMADAS_DATA = [], LLAMADAS_COLS = [], ZONAS_DATA = {}, ROSTER_DATA = {};
const CHARTS = {};
const AV_COLORS = ['#FF441F','#3B82F6','#22C55E','#8B5CF6','#F59E0B','#14B8A6','#EF4444','#10B981','#9333EA','#D97706','#0F766E','#D946EF','#EA580C','#6366F1'];

// GLOBALS MENU AI
const apiKey = ""; // Inyectado por el entorno Canvas
let menuData = { platos: [], bebidas: [] };
let missionStart, timerInterval;

const $ = id => typeof id === 'string' ? document.getElementById(id) : id;
const esc = s => String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;').replace(/'/g,'&#39;');

const fetchWithTimeout = async (url, ms) => { 
  const c = new AbortController(), tId = setTimeout(() => c.abort(), ms); 
  try { const r = await fetch(url, { signal: c.signal }); clearTimeout(tId); return r; } catch (e) { clearTimeout(tId); throw e; }
};

const parseDateStr = s => { 
  if(!s) return null; const g = String(s).match(/Date\((\d+),(\d+),(\d+)\)/); if(g) return new Date(+g[1], +g[2], +g[3]); 
  const str = String(s).trim(); 
  if(str.includes('-')) { const [y,m,d] = str.split('-'); if(y&&m&&d) return new Date(+y, +m-1, +d); } 
  if(str.includes('/')) { const p = str.split('/'); let d=p[0], m=p[1], y=p[2]||''; if(y.length===2) y='20'+y; return new Date(+y, +m-1, +d); } 
  const f = new Date(str); return isNaN(f) ? null : f; 
};

const normalizeTime = s => { 
  if(!s) return null; const m = String(s).match(/(\d{1,2}):(\d{2})/); if(!m) return null; 
  let h = parseInt(m[1], 10); const low = String(s).toLowerCase();
  if(low.includes('p') && h < 12) h += 12; if(low.includes('a') && h === 12) h = 0; 
  return String(h).padStart(2, '0') + ':' + m[2]; 
};

const debounce = (fn, ms) => { let t; return (...args) => { clearTimeout(t); t = setTimeout(() => fn(...args), ms); }; };
const destroyChart = k => { if(CHARTS[k]) { CHARTS[k].destroy(); delete CHARTS[k]; } };
const aName = email => !email ? '—' : email.split('@')[0].replace(/[._]/g, ' ').replace(/\b\w/g, c => c.toUpperCase());

const getCleanId = str => str ? String(str).split('@')[0].toLowerCase().replace(/[^a-z0-9]/g, '') : '';

const getAgentStats = email => { 
  if(!email) return null; 
  const cleanId = getCleanId(email);
  if(AGENT_STATS[cleanId]) return AGENT_STATS[cleanId]; 
  
  const keys = Object.keys(AGENT_STATS);
  for(let i=0; i<keys.length; i++) {
     if(keys[i].length > 5 && (cleanId.includes(keys[i]) || keys[i].includes(cleanId))) return AGENT_STATS[keys[i]];
  }
  return null; 
};

const hasSeg = r => {
  const c = String(r.comentario || '').toLowerCase();
  return ((c.includes('llamar') && (c.includes('mañana') || c.includes('semana') || c.includes('lunes') || c.includes('martes') || c.includes('miércoles') || c.includes('jueves') || c.includes('viernes') || /\d{1,2}\//.test(c))) || (c.includes('pendiente') && c.includes('llamar')));
};

function getUnifiedAgentList() {
  const map = new Map();
  const EXCLUDED_AGENTS = ['tatiana herrera', 'deicy laiton', 'angie cruz', 'gonzalo carrillo', 'sebastian ibanez', 'sebastián ibáñez'];
  
  // Escudo Anti-Error Humano: Valida si el nombre del Sheet tiene coincidencia lógica con el Email
  const isPlausibleMatch = (name, email) => {
      if (!name || name.toLowerCase() === 'agent' || name.toLowerCase() === 'agente') return false;
      if (!email) return true;
      const c1 = name.toLowerCase().split(/[\s._-]/).filter(x => x.length > 2);
      const c2 = email.split('@')[0].toLowerCase().split(/[\s._-]/).filter(x => x.length > 2);
      if (c1.length === 0 || c2.length === 0) return true; 
      return c1.some(p1 => c2.some(p2 => p1.includes(p2) || p2.includes(p1) || p1.substring(0,4) === p2.substring(0,4)));
  };

  // 1. Mapear DATA (BBDD)
  DATA.forEach(r => {
    if (!r.email) return;
    const cleanId = getCleanId(r.email);
    if (!cleanId) return;
    if (!map.has(cleanId)) map.set(cleanId, { val: r.email.toLowerCase(), label: aName(r.email), cleanId: cleanId });
  });

  // 2. Cruzar INDICADORES (AGENT_STATS)
  Object.values(AGENT_STATS).forEach(s => {
    if (!s.originalName) return;
    const cleanId = getCleanId(s.originalName);
    if (!cleanId) return;
    
    if (!map.has(cleanId)) {
      map.set(cleanId, { val: cleanId + '@rappi.com', label: isPlausibleMatch(s.originalName, cleanId) ? aName(s.originalName) : aName(cleanId), cleanId: cleanId });
    } else if (isPlausibleMatch(s.originalName, map.get(cleanId).val)) {
      map.get(cleanId).label = aName(s.originalName);
    }
  });

  // 3. Cruzar ROSTER 
  Object.values(ROSTER_DATA).forEach(r => {
    if (!r.cleanId) return;
    if (!map.has(r.cleanId)) {
      map.set(r.cleanId, { val: r.email || r.cleanId + '@rappi.com', label: isPlausibleMatch(r.nombre, r.email || r.cleanId) ? r.nombre : aName(r.email || r.cleanId), cleanId: r.cleanId });
    } else {
      if (r.email) map.get(r.cleanId).val = r.email.toLowerCase();
      if (isPlausibleMatch(r.nombre, map.get(r.cleanId).val)) {
          map.get(r.cleanId).label = r.nombre;
      }
    }
  });

  // 4. Formatear y Aplicar Lista de Exclusión
  return Array.from(map.values())
    .map(a => {
        if (!a.label || a.label.toLowerCase() === 'agent' || a.label.toLowerCase() === 'agente') a.label = aName(a.val);
        // Capitalización limpia tipo "Título"
        a.label = a.label.split(' ').filter(Boolean).map(w => w.charAt(0).toUpperCase() + w.slice(1).toLowerCase()).join(' ');
        return a;
    })
    .filter(a => {
        const lbl = a.label.toLowerCase();
        const eml = a.val.toLowerCase();
        return !EXCLUDED_AGENTS.some(ex => lbl.includes(ex) || eml.includes(ex.replace(' ', '.')) || eml.includes(ex.replace(' ', '')));
    })
    .sort((a, b) => a.label.localeCompare(b.label));
}

const normalizeEtapa = e => { 
  const str = String(e).toUpperCase().trim();
  if (str.includes('DATA COL') || str.includes('COLEC') || str.includes('COLLEC') || str === 'SOB') return 'DATA COLECCTION / SOB';
  const m = {'BASE':'BASE','PROSPECTO':'PROSPECTO','R2S':'ED','ED':'ED','DM':'DM','FIRMA':'FIRMA CONTRATO','FIRMA CONTRATO':'FIRMA CONTRATO','HANDOFF':'DC','HO':'DC','DC':'DC','RTS':'RTS'}; 
  return m[str] || str || 'BASE'; 
};

const inferRes = c => { 
  const s = String(c).toLowerCase(); 
  if(s.includes('no interesado')) return 'Contactado - No interesado'; if(s.includes('interesado')) return 'Contactado - Interesado'; 
  if(s.includes('no contesta') || s.includes('no contest')) return 'No contesta'; if(s.includes('buz\u00f3n') || s.includes('buzon')) return 'Buz\u00f3n de voz'; 
  if(s.includes('errado') || s.includes('no existe') || s.includes('equivocado') || s.includes('suspendido') || s.includes('cambiado')) return 'N\u00famero errado'; 
  if(s.includes('cuelga') || s.includes('corta')) return 'Cuelga'; if(s.includes('whatsapp') || s.includes(' wa ') || s.includes(' wp ') || s.includes('wapp')) return 'WhatsApp enviado'; 
  if(s.includes('handoff') || s.includes('realizado') || s.includes('subido') || s.includes('rts')) return 'Contactado - Interesado'; 
  if(s.includes('ocupado')) return 'No contesta'; 
  return !c.trim() ? '\u2014' : 'Contactado'; 
};

const stageColor = s => ({'BASE':'var(--ink4)','PROSPECTO':'var(--blue)','ED':'var(--amber)','DM':'var(--teal)','FIRMA CONTRATO':'#F59E0B','DC':'var(--purple)','DATA COLECCTION / SOB':'var(--rtext)','RTS':'var(--green)'}[s] || 'var(--ink3)');
const etapaChip = e => { const m = {'BASE':'chip-base','PROSPECTO':'chip-base','ED':'chip-r2s','DM':'chip-wp','FIRMA CONTRATO':'chip-firma','DC':'chip-handoff','DATA COLECCTION / SOB':'chip-sob','RTS':'chip-rts'}; return `<span class="chip ${m[e] || 'chip-base'}">${esc(e) || '\u2014'}</span>`; };
const resChip = r => { if(!r || r === '—') return `<span style="color:var(--ink4);font-size:12px">\u2014</span>`; const m = {'Contactado - Interesado':'chip-int','Contactado':'chip-int','No contesta':'chip-nc','Buz\u00f3n de voz':'chip-buz','N\u00famero errado':'chip-err','Cuelga':'chip-err','WhatsApp enviado':'chip-wp','Contactado - No interesado':'chip-nc'}; return `<span class="chip ${m[r] || 'chip-nc'}">${esc(r.replace('Contactado - ', '').replace(' / no existe', ''))}</span>`; };

function setConn(s) { 
  const d = $('hd-dot'), t = $('hd-conn-text'); if(!d || !t) return; 
  if(s === 'ok') { d.className = 'hd-dot ok'; t.textContent = 'Data Stream Activo'; } else if(s === 'err') { d.className = 'hd-dot err'; t.textContent = 'Offline'; } else { d.className = 'hd-dot'; t.textContent = 'Syncing...'; } 
}

function hideLoader() { const l = $('loader'); if(l) l.classList.add('out'); }

function showLoaderError(msg) { 
  const textEl = $('loader-text');
  const errEl = $('loader-error');
  if(textEl) textEl.textContent = 'Fallo de Conexión'; 
  if(errEl) { errEl.style.display = 'block'; errEl.textContent = msg + '\n\nVerifica los permisos del nodo o reintenta conexión.'; } 
}

function toast(msg, type='inf') { 
  const t = document.createElement('div'); t.className = `toast ${type}`; 
  const i = {
    ok: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>',
    er: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="15" y1="9" x2="9" y2="15"/><line x1="9" y1="9" x2="15" y2="15"/></svg>',
    inf: '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>'
  }; 
  t.innerHTML = (i[type] || i.inf) + esc(msg); 
  const c = $('toasts'); if(c) { c.appendChild(t); setTimeout(() => { t.classList.add('hide'); setTimeout(() => t.remove(), 200); }, 4000); }
}

function go(id) { 
  document.querySelectorAll('.page').forEach(p => p.classList.remove('on')); document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active')); 
  const el = $('p-' + id); if(el) el.classList.add('on'); 
  const btn = document.querySelector(`.nav-btn[data-page="${id}"]`); if(btn) btn.classList.add('active'); 
  const bBtn = $('btn-global-back'); if(bBtn) bBtn.style.display = (id === 'dashboard') ? 'none' : 'flex';
  closeMobileNav(); 
  if(id === 'zonas' && window.geoMap) { setTimeout(() => window.geoMap.invalidateSize(), 150); }
}

function filterAgent(e) { go('registros'); const s = $('f-agente'); if(s) s.value = e; doFilter(); }
function openMobileNav() { if($('sidebar')) $('sidebar').classList.add('open'); if($('nav-overlay')) $('nav-overlay').classList.add('on'); }
function closeMobileNav() { if($('sidebar')) $('sidebar').classList.remove('open'); if($('nav-overlay')) $('nav-overlay').classList.remove('on'); }

// ... [Carga de datos CRM mantenida intacta] ...
async function loadMetasFromTabs() {
  AGENT_STATS = {};
  try {
    const r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=INDICADORES`, CONFIG.FETCH_TIMEOUT_MS);
    if(!r.ok) return; const t = await r.text(); const js = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1); if(!js) return; 
    const j = JSON.parse(js); if(!j.table) return;
    
    let nIdx = -1, rIdx = -1, cIdx = -1, mIdx = -1, telIdx = -1, iMap = { prospectos:-1, ed:-1, dm:-1, firma:-1, dc:-1, datacol:-1 };
    const scan = [{c: j.table.cols}, ...(j.table.rows || []).slice(0, 3)];
    for(const row of scan) {
      (row.c || []).forEach((c, i) => {
        if(!c || (c.label == null && c.v == null)) return; const l = String(c.label || c.v || '').toLowerCase().trim(); if(!l) return;
        if(l.includes('nombre') || l.includes('agente')) nIdx = i; 
        if(l === 'rts' || l.includes('rts')) { rIdx = i; INDICADORES_COL_FOUND.rts = true; }
        if(l === 'c/m' || l.startsWith('c/m')) cIdx = i; 
        if(l.includes('meta mensual') || l === 'meta') { mIdx = i; INDICADORES_COL_FOUND.meta = true; }
        if(l.includes('prospecto') && iMap.prospectos === -1) { iMap.prospectos = i; INDICADORES_COL_FOUND.prospectos = true; } 
        if(l === 'ed' && iMap.ed === -1) { iMap.ed = i; INDICADORES_COL_FOUND.ed = true; }
        if((l === 'dm' || l === 'd') && iMap.dm === -1) { iMap.dm = i; INDICADORES_COL_FOUND.dm = true; } 
        if(l.includes('firma') && iMap.firma === -1) { iMap.firma = i; INDICADORES_COL_FOUND.firma = true; }
        if(l === 'dc' && iMap.dc === -1) { iMap.dc = i; INDICADORES_COL_FOUND.dc = true; } 
        if((l.includes('data col') || l.includes('datac') || l.includes('colec') || l.includes('collec') || l.includes('sob')) && iMap.datacol === -1) { iMap.datacol = i; INDICADORES_COL_FOUND.datacol = true; }
        if(l.includes('tel') || l.includes('cel') || l.includes('phone') || l.includes('movil') || l.includes('móvil') || l.includes('contacto') || l.includes('número') || l.includes('numero') || l.includes('wa') || l.includes('whatsapp')) telIdx = i;
      }); 
      if(nIdx !== -1 && rIdx !== -1) break;
    }
    if(nIdx === -1) return;
    
    INDICADORES_TOTALS = { prospectos:0, ed:0, dm:0, firma:0, dc:0, datacol:0, rts:0 };
    const gVal = (row, idx) => (idx === -1 || !row.c || !row.c[idx]) ? 0 : parseFloat(String(row.c[idx].v || 0).replace(/,/g, '')) || 0;
    
    (j.table.rows || []).forEach(row => {
      if(!row.c || !row.c[nIdx] || row.c[nIdx].v == null) return; const raw = String(row.c[nIdx].v).trim(); if(!raw || raw.toLowerCase().includes('total')) return;
      
      const cleanCurr = getCleanId(CURRENT_USER_EMAIL);
      const ek = raw.toLowerCase().trim(), nk = ek.replace(/[^a-z0-9]/g, '');
      
      // Filtro RBAC: Bloqueo de info de otros agentes
      if (!IS_ADMIN() && getCleanId(ek) !== cleanCurr && getCleanId(nk) !== cleanCurr) return;

      const p = gVal(row, iMap.prospectos), e = gVal(row, iMap.ed), d = gVal(row, iMap.dm), f = gVal(row, iMap.firma), dc = gVal(row, iMap.dc), dat = gVal(row, iMap.datacol), rts = gVal(row, rIdx), meta = gVal(row, mIdx);
      
      const cellT = telIdx !== -1 ? row.c[telIdx] : null;
      const telefono = cellT ? String(cellT.f !== undefined ? cellT.f : (cellT.v !== null && cellT.v !== undefined ? cellT.v : '')).trim() : '';

      INDICADORES_TOTALS.prospectos += p; INDICADORES_TOTALS.ed += e; INDICADORES_TOTALS.dm += d; INDICADORES_TOTALS.firma += f; INDICADORES_TOTALS.dc += dc; INDICADORES_TOTALS.datacol += dat; INDICADORES_TOTALS.rts += rts;
      
      let cm = 0; if(cIdx !== -1 && row.c[cIdx]) { const cs = row.c[cIdx].f || String(row.c[cIdx].v || 0); cm = parseFloat(cs.replace(/,/g, '.').replace(/%/g, '')) || 0; if(!cs.includes('%') && cm > 0 && cm <= 10) cm *= 100; }
      if(meta > 0 && cm === 0) cm = (rts / meta) * 100;
      
      const st = { originalName: raw, rts: rts, cm: Math.round(cm), meta: meta, telefono: telefono, etapas: { prospectos: p, ed: e, dm: d, firma: f, dc: dc, datacol: dat } };
      AGENT_STATS[ek] = st; if(nk) AGENT_STATS[nk] = st;
    });
  } catch(e) { console.warn('INDICADORES load failed:', e.message); }
}

async function loadLlamadas() {
  LLAMADAS_DATA = []; LLAMADAS_COLS = [];
  try {
    const r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=LLAMADAS`, CONFIG.FETCH_TIMEOUT_MS);
    if(!r.ok) return; const t = await r.text(); const jStr = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1); if(!jStr) return; 
    const j = JSON.parse(jStr); if(!j.table || !j.table.cols) return;
    LLAMADAS_COLS = j.table.cols.map((c, i) => c.label ? c.label.trim() : `Columna_${i+1}`).filter(c => c !== '');
    LLAMADAS_DATA = (j.table.rows || []).map((row, rIdx) => {
      let obj = { _id: rIdx }; LLAMADAS_COLS.forEach((col, i) => { const cell = row.c && row.c[i]; obj[col] = cell ? (cell.f !== undefined ? String(cell.f) : String(cell.v !== null ? cell.v : '')) : ''; }); return obj;
    }).filter(r => Object.values(r).some(v => v !== '' && v !== r._id));

    // Filtro RBAC: Restringir llamadas a propias si no es Admin
    if (!IS_ADMIN()) {
        const aCol = LLAMADAS_COLS.find(c => /agente|nombre|email/i.test(c));
        const cleanCurr = getCleanId(CURRENT_USER_EMAIL);
        if (aCol) {
            LLAMADAS_DATA = LLAMADAS_DATA.filter(r => {
                const val = getCleanId(r[aCol]);
                return val.includes(cleanCurr) || cleanCurr.includes(val);
            });
        } else {
            LLAMADAS_DATA = []; // Fallback de seguridad
        }
    }
  } catch(e) { console.warn('Error LLAMADAS:', e.message); }
}

async function loadZonas() {
  ZONAS_DATA = {};
  try {
    const r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=ZONAS`, CONFIG.FETCH_TIMEOUT_MS);
    if(!r.ok) return; const t = await r.text(); const js = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1); if(!js) return;
    const j = JSON.parse(js); if(!j.table) return;
    
    const cols = j.table.cols;
    let idIdx = -1, latIdx = -1, lngIdx = -1, nameIdx = -1;
    
    cols.forEach((c, i) => {
      if(!c || !c.label) return;
      const l = c.label.toLowerCase();
      if(l.includes('ops zone') || l === 'zona' || l === 'id') idIdx = i;
      if(l.includes('lat')) latIdx = i;
      if(l.includes('lon') || l.includes('lng')) lngIdx = i;
      if(l.includes('nombre') || l.includes('desc')) nameIdx = i;
    });

    if(idIdx === -1) idIdx = 0;
    if(latIdx === -1) latIdx = 1;
    if(lngIdx === -1) lngIdx = 2;

    (j.table.rows || []).forEach(row => {
      if(!row.c || !row.c[idIdx] || row.c[idIdx].v == null) return;
      const zId = String(row.c[idIdx].v).trim();
      const lat = row.c[latIdx] && row.c[latIdx].v != null ? parseFloat(row.c[latIdx].v) : null;
      const lng = row.c[lngIdx] && row.c[lngIdx].v != null ? parseFloat(row.c[lngIdx].v) : null;
      const zName = nameIdx !== -1 && row.c[nameIdx] && row.c[nameIdx].v != null ? String(row.c[nameIdx].v).trim() : zId;

      if (lat && lng) ZONAS_DATA[zId.toLowerCase()] = { id: zId, lat: lat, lng: lng, name: zName };
    });
  } catch(e) { console.warn('ZONAS load failed:', e.message); }
}

async function loadRosterTab() {
  ROSTER_DATA = {};
  try {
    let r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=ROSTER`, CONFIG.FETCH_TIMEOUT_MS);
    if (!r.ok) r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=Roster`, CONFIG.FETCH_TIMEOUT_MS);
    if (!r.ok) return; 
    
    const t = await r.text(); const js = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1); if(!js) return;
    const j = JSON.parse(js); if(!j.table) return;

    let eIdx = -1, tIdx = -1, nIdx = -1;
    const scan = [{c: j.table.cols}, ...(j.table.rows || []).slice(0, 3)];
    for(const row of scan) {
      (row.c || []).forEach((c, i) => {
        if(!c || (c.label == null && c.v == null)) return; 
        const l = String(c.label || c.v || '').toLowerCase().trim(); 
        if(!l) return;
        if(l === 'email' || l === 'correo' || l.includes('mail') || l.includes('id')) eIdx = i;
        if(l.includes('tel') || l.includes('cel') || l.includes('phone') || l.includes('movil') || l.includes('móvil') || l.includes('numero') || l.includes('número')) tIdx = i;
        if(l === 'nombre' || l === 'nombre completo' || l.includes('agente') || l.includes('usuario')) {
             if (nIdx === -1) nIdx = i; 
        }
      });
      if(eIdx !== -1 || tIdx !== -1 || nIdx !== -1) break;
    }

    (j.table.rows || []).forEach(row => {
      let email = eIdx !== -1 && row.c[eIdx] ? String(row.c[eIdx].v).trim().toLowerCase() : '';
      let name = nIdx !== -1 && row.c[nIdx] ? String(row.c[nIdx].v).trim() : '';
      
      if (name.toLowerCase() === 'agent' || name.toLowerCase() === 'agente') name = '';
      if(!email && name) email = name.replace(/[^a-zA-Z0-9]/g, '').toLowerCase() + '@rappi.com';
      if(!email && !name) return;
      
      let tel = '';
      if(tIdx !== -1 && row.c[tIdx]) {
          tel = String(row.c[tIdx].f !== undefined ? row.c[tIdx].f : (row.c[tIdx].v !== null ? row.c[tIdx].v : '')).trim();
      }

      const cleanId = getCleanId(email || name);

      // Filtro RBAC
      if (!IS_ADMIN() && cleanId !== getCleanId(CURRENT_USER_EMAIL)) return;

      ROSTER_DATA[cleanId] = { email: email, nombre: name, telefono: tel, cleanId: cleanId };
    });
  } catch(e) { console.warn('ROSTER tab load failed:', e.message); }
}

async function loadRetardos() {
  TARDANZAS_DATA = {};
  try {
    const r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=RETARDOS`, CONFIG.FETCH_TIMEOUT_MS);
    if(!r.ok) return;
    const t = await r.text();
    const js = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1);
    if(!js) return;
    const j = JSON.parse(js);
    if(!j.table) return;

    const cols = j.table.cols;
    let dIdx = -1, aIdx = -1, inIdx = -1, outIdx = -1;

    cols.forEach((c, i) => {
      if(!c || !c.label) return;
      const l = c.label.toLowerCase();
      if(l.includes('fecha') || l.includes('date')) dIdx = i;
      if(l.includes('agente') || l.includes('email') || l.includes('nombre') || l.includes('usuario')) aIdx = i;
      if(l.includes('entrada') || l.includes('ingreso') || l.includes('in')) inIdx = i;
      if(l.includes('salida') || l.includes('egreso') || l.includes('out')) outIdx = i;
    });

    if(dIdx === -1 || aIdx === -1) return;

    (j.table.rows || []).forEach(row => {
      if(!row.c || !row.c[aIdx] || row.c[aIdx].v == null) return;
      const agentRaw = String(row.c[aIdx].v).trim();
      const cleanId = getCleanId(agentRaw);
      
      // Filtro RBAC
      if (!IS_ADMIN() && cleanId !== getCleanId(CURRENT_USER_EMAIL)) return;
      if(!cleanId) return;

      let dateStr = '';
      const cellD = row.c[dIdx];
      if(cellD) {
          const d = parseDateStr(cellD.f || cellD.v);
          if(d) dateStr = `${d.getFullYear()}-${String(d.getMonth()+1).padStart(2,'0')}-${String(d.getDate()).padStart(2,'0')}`;
      }
      if(!dateStr) return;

      const cellIn = inIdx !== -1 && row.c[inIdx] ? (row.c[inIdx].f || row.c[inIdx].v) : '';
      const cellOut = outIdx !== -1 && row.c[outIdx] ? (row.c[outIdx].f || row.c[outIdx].v) : '';

      const timeIn = normalizeTime(cellIn) || '';
      const timeOut = normalizeTime(cellOut) || '';

      let penalize = false;
      let pData = { lateIn: false, earlyOut: false, other: false, reasons: [] };

      // Validaciones estrictas de horarios y asistencia segmentadas
      if (!timeIn && !timeOut) {
          penalize = true;
          pData.other = true;
          pData.reasons.push(`Falta / No Asistió`);
      } else {
          if (timeIn && timeIn > "09:00") {
              penalize = true;
              pData.lateIn = true;
              pData.reasons.push(`Ingreso Tarde: ${timeIn}`);
          } else if (!timeIn) {
              penalize = true;
              pData.other = true;
              pData.reasons.push(`Omisión de Ingreso`);
          }

          if (timeOut && timeOut < "18:00") {
              penalize = true;
              pData.earlyOut = true;
              pData.reasons.push(`Salida Temprano: ${timeOut}`);
          } else if (!timeOut) {
              penalize = true;
              pData.other = true;
              pData.reasons.push(`Omisión de Salida`);
          }
      }

      if (penalize) {
          if(!TARDANZAS_DATA[cleanId]) TARDANZAS_DATA[cleanId] = {};
          TARDANZAS_DATA[cleanId][dateStr] = pData;
      }
    });
  } catch(e) { console.warn('RETARDOS tab load failed:', e.message); }
}

async function loadData(silent = false) {
  if (!silent) {
    setConn('loading');
    const l = $('loader'); if(l) l.classList.remove('out');
  } else { 
    const d = $('hd-dot'), t = $('hd-conn-text'); if (d && t) { d.className = 'hd-dot'; t.textContent = 'Auto-Syncing...'; } 
  }
  try {
    // Sincronización en paralelo para máxima velocidad y fiabilidad
    await Promise.all([
        loadMetasFromTabs(),
        loadLlamadas(),
        loadZonas(),
        loadRosterTab(),
        loadRetardos()
    ]);
    
    const r = await fetchWithTimeout(`https://docs.google.com/spreadsheets/d/${CONFIG.SID}/gviz/tq?tqx=out:json&sheet=BBDD`, CONFIG.FETCH_TIMEOUT_MS);
    if(!r.ok) throw new Error(`HTTP ${r.status}`); 
    const t = await r.text(); const jStr = t.substring(t.indexOf('{'), t.lastIndexOf('}') + 1); 
    if(!jStr) throw new Error("Asegúrate de que tu Google Sheet tenga el permiso 'Cualquier persona con el enlace puede leer'."); 
    const j = JSON.parse(jStr); if(j.status === 'error') throw new Error(j.errors[0].message);
    
    const parsedData = (j.table.rows || []).map(row => Array.from({length:11}, (_, i) => { const c = row.c && row.c[i]; return !c || c.v == null ? '' : (c.f !== undefined ? String(c.f) : String(c.v)); }))
      .filter(r => r[1] && r[1].trim() && r[1].trim().toLowerCase() !== 'x' && r[1].trim().toLowerCase() !== 'nombre restaurante')
      .map((r, i) => ({ id: i, ts: (r[0] || '').trim(), restaurante: (r[1] || '').trim(), tel: (r[2] || '').trim(), proceso: normalizeEtapa((r[3] || '').trim()), email: (r[4] || '').trim().toLowerCase(), comentario: (r[5] || '').trim(), brand: (r[6] || '').trim(), fecha: (r[7] || r[0] || '').trim(), hora: (r[8] || '').trim(), zona: (r[9] || 'Sin Zona').trim(), agent: (r[10] || '').trim(), resultado: inferRes(r[5] || '') }));
    
    // Filtro RBAC Core
    if (IS_ADMIN()) {
        DATA = parsedData;
    } else {
        const cleanCurr = getCleanId(CURRENT_USER_EMAIL);
        DATA = parsedData.filter(r => getCleanId(r.email) === cleanCurr);
    }

    setConn('ok'); if (!silent) toast('Data Stream completado — ' + DATA.length + ' logs', 'ok'); 
  } catch(e) { 
    setConn('err'); 
    if (!silent) toast('Fallo de conexión: ' + e.message, 'er'); 
  } finally {
    renderAll(); 
    if (!silent) hideLoader();
  }
}

function renderAll() { 
  const cf = {
    q: $('q') ? $('q').value : '',
    agente: $('f-agente') ? $('f-agente').value : '', mes: $('f-mes') ? $('f-mes').value : '', dia: $('f-dia') ? $('f-dia').value : '',
    hi: $('f-hora-ini') ? $('f-hora-ini').value : '', hf: $('f-hora-fin') ? $('f-hora-fin').value : '', a_agente: $('f-analisis-agente') ? $('f-analisis-agente').value : '',
    a_mes: $('f-analisis-mes') ? $('f-analisis-mes').value : '', a_dia: $('f-analisis-dia') ? $('f-analisis-dia').value : '',
    ll_agente: $('f-llamadas-agente') ? $('f-llamadas-agente').value : '', calc_agente: $('calc-agent-sel') ? $('calc-agent-sel').value : ''
  };
  
  renderTopbar(); renderMetrics(); renderDash(); fillMonthFilter(); fillHourFilter(); fillAgentFilter(); fillCalcAgents(); fillAnalisisFilters(); fillDocAgents(); 
  
  if($('q') && cf.q) $('q').value = cf.q;
  if($('f-agente') && cf.agente) $('f-agente').value = cf.agente; if($('f-mes') && cf.mes) $('f-mes').value = cf.mes; if($('f-dia') && cf.dia) $('f-dia').value = cf.dia;
  if($('f-hora-ini') && cf.hi) $('f-hora-ini').value = cf.hi; if($('f-hora-fin') && cf.hf) $('f-hora-fin').value = cf.hf; if($('f-analisis-agente') && cf.a_agente) $('f-analisis-agente').value = cf.a_agente;
  if($('f-llamadas-agente') && cf.ll_agente) $('f-llamadas-agente').value = cf.ll_agente;
  if($('calc-agent-sel') && cf.calc_agente) $('calc-agent-sel').value = cf.calc_agente;
  
  doFilter(); renderPipeline(); renderSeguimientos(); renderRoster(); renderDesglose(); renderIndicadores(); renderZonas(); renderAnalisisBBDD(); renderLlamadas(); initCalc(); initTardanzas(); 
}

function renderTopbar() { 
  if($('hkpi-total')) $('hkpi-total').textContent = DATA.length; 
  if($('hkpi-ho')) $('hkpi-ho').textContent = INDICADORES_COL_FOUND.rts ? INDICADORES_TOTALS.rts : DATA.filter(r => r.proceso === 'RTS').length; 
  
  if (!IS_ADMIN()) {
      const labels = document.querySelectorAll('.hd-kpi-label');
      if (labels.length >= 3) {
          labels[0].textContent = "Mis Gestiones";
          labels[1].textContent = "Mis RTS";
          labels[2].textContent = "Status Red";
      }
      if($('hkpi-ag')) {
          $('hkpi-ag').textContent = "Online";
          $('hkpi-ag').parentElement.classList.remove('hd-kpi-click');
          $('hkpi-ag').parentElement.title = "Conectado al Servidor";
      }
  } else {
      if($('hkpi-ag')) $('hkpi-ag').textContent = getUnifiedAgentList().length; 
  }
  
  if($('nb-total')) $('nb-total').textContent = DATA.length; 
}

function renderMetrics() {
  const t = DATA.length;
  const getStage = (key, stage) => INDICADORES_COL_FOUND[key] ? INDICADORES_TOTALS[key] : DATA.filter(r => r.proceso === stage).length;
  const upd = $('dash-updated'); if(upd) upd.textContent = `Última actualización: ${new Date().toLocaleString('es-MX', {day:'2-digit', month:'short', hour:'2-digit', minute:'2-digit'})} · Total de registros: ${t}`;
  const bc = (l, v, s, a, c, ct, p) => `<div class="mc" data-target="${p}" title="Drill-down Analytics"><div class="mc-accent" style="background:${a};box-shadow:0 0 10px ${a}"></div><div class="mc-label">${l}</div><div class="mc-val">${Number(v).toLocaleString()}</div><div class="mc-sub">${s}</div>${c ? `<div class="mc-change ${ct}">${c}</div>` : ''}</div>`;
  
  const activeAgents = getUnifiedAgentList().length;
  let retardosCount = 0; Object.values(TARDANZAS_DATA).forEach(obj => { retardosCount += Object.keys(obj).length; });

  const me = $('dash-metrics');
  if(me) {
    me.innerHTML = [ 
      bc('Logs Totales', t, 'Lifetime Records', '#71717A', '', '', 'analisis-bbdd'), 
      bc('Roster', activeAgents, 'Agentes Activos', 'var(--teal)', '', '', 'roster'), 
      bc('Retardos', retardosCount, 'Faltas registradas', 'var(--red)', '', '', 'tardanzas'), 
      bc('Prospectos', getStage('prospectos','PROSPECTO'), 'Detecciones Base', 'var(--blue)', '', '', 'desglose'), 
      bc('ED (Espera Doc)', getStage('ed','ED'), 'Hold: Documentación', 'var(--amber)', '', '', 'desglose'), 
      bc('DM (Migración)', getStage('dm','DM'), 'Proceso Migratorio', 'var(--teal)', '', '', 'desglose'), 
      bc('Firma Contrato', getStage('firma','FIRMA CONTRATO'), 'Legal Pending', '#F59E0B', '', '', 'desglose'), 
      bc('DC', getStage('dc','DC'), 'Data Validation', 'var(--purple)', '', '', 'desglose'), 
      bc('Data Collection', getStage('datacol','DATA COLECCTION / SOB'), 'SOB Processing', 'var(--rtext)', '', '', 'desglose'), 
      bc('RTS Consolidados', getStage('rts','RTS'), 'Market-Ready (RTS)', 'var(--green)', '+ ' + Math.round(getStage('rts','RTS') / Math.max(t, 1) * 100) + '%', 'up', 'desglose') 
    ].join('');
    me.querySelectorAll('.mc').forEach(el => el.addEventListener('click', () => go(el.dataset.target)));
  }
  const nb = $('nb-seg'); if(nb) { const segs = DATA.filter(hasSeg).length; if(segs > 0) { nb.textContent = segs; nb.style.display = 'flex'; } else { nb.style.display = 'none'; } }
}

function renderDash() {
  const ST = ['PROSPECTO','ED','DM','FIRMA CONTRATO','DC','DATA COLECCTION / SOB','RTS'], SL = ['PROSPECTO','ED (DOC)','DM (MIGR)','CONTRATO','DC','COLLECTION','RTS'], t = DATA.length;
  const fun = $('dash-funnel');
  if(fun) {
    fun.innerHTML = ST.map((s, i) => {
      const mapKey = { 'PROSPECTO':'prospectos', 'ED':'ed', 'DM':'dm', 'FIRMA CONTRATO':'firma', 'DC':'dc', 'DATA COLECCTION / SOB':'datacol', 'RTS':'rts' };
      const k = mapKey[s], n = (k && INDICADORES_COL_FOUND[k]) ? INDICADORES_TOTALS[k] : DATA.filter(r => r.proceso === s).length;
      return `<div class="funnel-step"><div class="fs-num" style="color:${stageColor(s)};text-shadow:0 0 10px ${stageColor(s)}">${n}</div><div class="fs-label">${SL[i]}</div><div class="fs-pct">${Math.round(n / Math.max(t, 1) * 100)}%</div></div>`;
    }).join('');
  }

  // Tweak Text for Non-Admins
  if (!IS_ADMIN()) {
      const trTitles = document.querySelectorAll('.sec-title');
      trTitles.forEach(el => {
          if(el.textContent.includes('Top Performers')) el.childNodes[0].textContent = "Mi Rendimiento ";
          if(el.textContent.includes('Distribución de Estados')) el.childNodes[0].textContent = "Mis Estados ";
      });
  }

  const agMap = {}; DATA.forEach(r => { if(r.email) agMap[r.email] = (agMap[r.email] || 0) + 1; }); 
  const topAgents = Object.entries(agMap).sort((a, b) => b[1] - a[1]).slice(0, 8), mxAgent = topAgents[0]?.[1] || 1;
  if($('dash-ranking')) $('dash-ranking').innerHTML = `<div class="bar-chart">${topAgents.map(([e, n]) => `<div class="bar-row"><div class="bar-label">${esc(aName(e).split(' ')[0])}</div><div class="bar-track"><div class="bar-fill" style="width:${Math.round(n / mxAgent * 100)}%"></div><div class="bar-val">${n}</div></div></div>`).join('')}</div>`;
  const rsMap = {}; DATA.forEach(r => { rsMap[r.resultado] = (rsMap[r.resultado] || 0) + 1; }); 
  const rTop = Object.entries(rsMap).sort((a, b) => b[1] - a[1]).slice(0, 8), rMx = rTop[0]?.[1] || 1;
  const resColors = { 'Contactado - Interesado':'var(--green)', 'No contesta':'var(--amber)', 'Buz\u00f3n de voz':'var(--ink5)', 'N\u00famero errado':'var(--red)', 'Cuelga':'var(--red)', 'WhatsApp enviado':'var(--teal)', 'Contactado - No interesado':'var(--amber)', 'Contactado':'var(--green)' };
  if($('dash-resultados')) $('dash-resultados').innerHTML = `<div class="bar-chart">${rTop.map(([r, n]) => `<div class="bar-row"><div class="bar-label">${esc(r.replace('Contactado - ', '').substring(0, 18))}</div><div class="bar-track"><div class="bar-fill" style="width:${Math.round(n / rMx * 100)}%;background:${resColors[r] || 'var(--blue)'};box-shadow:inset 0 -2px 4px rgba(0,0,0,0.5)"></div><div class="bar-val">${n}</div></div></div>`).join('')}</div>`;
  if($('dash-tbody')) {
    $('dash-tbody').innerHTML = [...DATA].reverse().slice(0, 15).map(r => `<tr data-id="${r.id}"><td class="name">${esc(r.restaurante)}</td><td class="mono">${esc(r.tel)}</td><td>${etapaChip(r.proceso)}</td><td>${resChip(r.resultado)}</td><td class="muted">${esc(aName(r.email))}</td><td class="muted" style="font-family:'JetBrains Mono'">${esc(r.fecha)}</td></tr>`).join('');
    $('dash-tbody').querySelectorAll('tr').forEach(tr => tr.addEventListener('click', () => openDrawer(+tr.dataset.id)));
  }
}

function renderLlamadas() {
  const tb = $('llamadas-tbody'), th = $('llamadas-thead-tr'); if(!tb || !th) return;
  const aCol = LLAMADAS_COLS.find(c => /agente|nombre|email/i.test(c)), fCol = LLAMADAS_COLS.find(c => /fecha|date|tiempo|dia/i.test(c)), eCol = LLAMADAS_COLS.find(c => /estado|resultado|status|proceso|disposicion/i.test(c));
  const selAgente = $('f-llamadas-agente');
  if(selAgente && aCol && LLAMADAS_DATA.length > 0 && !selAgente.dataset.loaded) { 
    selAgente.innerHTML = `<option value="">Vista General (Cross-Agent)</option>` + [...new Set(LLAMADAS_DATA.map(r => r[aCol]).filter(Boolean))].sort().map(a => `<option value="${esc(a)}">${esc(a)}</option>`).join('');
    selAgente.dataset.loaded = 'true'; 
    if(!IS_ADMIN() && selAgente.options.length === 2) { selAgente.value = selAgente.options[1].value; selAgente.disabled = true; }
  }
  const sVal = selAgente ? selAgente.value : ''; 
  let chartData = LLAMADAS_DATA; if(sVal && aCol) chartData = LLAMADAS_DATA.filter(r => r[aCol] === sVal);
  if($('ll-kpi-total')) $('ll-kpi-total').textContent = chartData.length.toLocaleString(); 
  if($('ll-kpi-agentes')) $('ll-kpi-agentes').textContent = (aCol && chartData.length > 0) ? new Set(chartData.map(r => r[aCol]).filter(Boolean)).size : '—';
  
  let fData = {}; 
  if(fCol) { chartData.forEach(r => { let val = r[fCol]; if(val && val.length > 10) val = val.substring(0, 10); if(val) fData[val] = (fData[val] || 0) + 1; }); }
  destroyChart('ll_tendencia'); const sortedFechas = Object.keys(fData).sort(); Chart.defaults.color = '#A1A1AA'; Chart.defaults.borderColor = 'rgba(255,255,255,0.05)';
  if($('chart-ll-tendencia')) {
    CHARTS['ll_tendencia'] = new Chart($('chart-ll-tendencia'), { type: 'line', data: { labels: sortedFechas.length ? sortedFechas : ['Sin Fechas Registradas'], datasets: [{ label: 'Calls', data: sortedFechas.length ? sortedFechas.map(d => fData[d]) : [0], borderColor: '#3B82F6', backgroundColor: 'rgba(59,130,246,0.1)', fill: true, tension: 0.4, pointRadius: 3, pointBackgroundColor: '#3B82F6' }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true } } } });
  }
  
  destroyChart('ll_comparativa'); if($('title-ll-comp')) $('title-ll-comp').textContent = sVal ? 'Desglose Resultados' : 'Top Callers Volume';
  if($('chart-ll-comparativa')) {
    if(sVal && eCol) {
      let eData = {}; chartData.forEach(r => { let v = r[eCol] || 'Unknown'; eData[v] = (eData[v] || 0) + 1; }); const labels = Object.keys(eData).sort((a,b) => eData[b] - eData[a]);
      CHARTS['ll_comparativa'] = new Chart($('chart-ll-comparativa'), { type: 'doughnut', data: { labels: labels, datasets: [{ data: labels.map(x => eData[x]), backgroundColor: ['#22C55E','#F59E0B','#EF4444','#3B82F6','#8B5CF6','#71717A'], borderWidth: 1, borderColor: '#18181B' }] }, options: { maintainAspectRatio: false, cutout: '70%', plugins: { legend: { position: 'right', labels: { font: { size: 11 } } } } } });
    } else if(!sVal && aCol) {
      let aData = {}; chartData.forEach(r => { let v = r[aCol] || 'Unassigned'; aData[v] = (aData[v] || 0) + 1; }); const sortedAg = Object.entries(aData).sort((a,b) => b[1] - a[1]).slice(0, 10);
      CHARTS['ll_comparativa'] = new Chart($('chart-ll-comparativa'), { type: 'bar', data: { labels: sortedAg.map(x => x[0].split(' ')[0] || x[0]), datasets: [{ label: 'Llamadas', data: sortedAg.map(x => x[1]), backgroundColor: '#FF441F', borderRadius: 4 }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true, display: false }, x: { grid: { display: false } } } } });
    } else { 
      CHARTS['ll_comparativa'] = new Chart($('chart-ll-comparativa'), { type: 'bar', data: { labels: ['Awaiting Data'], datasets: [{ data: [0] }] }, options: { maintainAspectRatio: false } }); 
    }
  }
  
  if(LLAMADAS_COLS.length === 0) { th.innerHTML = `<th>Aviso</th>`; tb.innerHTML = `<tr><td>Verifique integración de nodo LLAMADAS.</td></tr>`; if($('ll-count')) $('ll-count').textContent = '0 records'; return; }
  th.innerHTML = LLAMADAS_COLS.map(c => `<th>${esc(c)}</th>`).join(''); 
  const qStr = $('q-llamadas') ? ($('q-llamadas').value || '').toLowerCase() : ''; 
  let finalTable = chartData; if(qStr) finalTable = finalTable.filter(r => Object.values(r).some(v => String(v).toLowerCase().includes(qStr)));
  const maxRows = 200, sliceRows = finalTable.slice(0, maxRows); 
  if($('ll-count')) $('ll-count').textContent = finalTable.length > maxRows ? `Showing [${maxRows}] of ${finalTable.length.toLocaleString()} records` : `${finalTable.length.toLocaleString()} records`;
  
  if(sliceRows.length === 0) { tb.innerHTML = `<tr><td colspan="${LLAMADAS_COLS.length}"><div class="empty"><h3>Query Not Found</h3></div></td></tr>`; } 
  else { tb.innerHTML = sliceRows.map(r => `<tr>${LLAMADAS_COLS.map(c => `<td style="max-width:200px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis" title="${esc(r[c]||'')}">${esc(r[c]) || '<span class="muted" style="opacity:0.3">NULL</span>'}</td>`).join('')}</tr>`).join(''); }
}

function fillAnalisisFilters() {
  const agList = getUnifiedAgentList(); const sA = $('f-analisis-agente'); 
  if(sA) sA.innerHTML = `<option value="">Cross-Agent (Todos)</option>` + agList.map(a => `<option value="${a.val}">${esc(a.label)}</option>`).join('');
  const monthSet = new Set(); DATA.forEach(r => { const d = parseDateStr(r.fecha); if(d) monthSet.add(d.getMonth()); }); 
  const mNames = ["Enero","Febrero","Marzo","Abril","Mayo","Junio","Julio","Agosto","Septiembre","Octubre","Noviembre","Diciembre"];
  const selMes = $('f-analisis-mes'); if(selMes) selMes.innerHTML = `<option value="">Timeline Completo</option>` + [...monthSet].sort((a,b) => b-a).map(m => `<option value="${m}">${mNames[m]}</option>`).join(''); 
  updateAnalisisDayFilter();
}

function updateAnalisisDayFilter() { 
  const fM = $('f-analisis-mes') ? $('f-analisis-mes').value : ''; const sel = $('f-analisis-dia'); if(!sel) return; 
  if(!fM) { sel.innerHTML = `<option value="">Día específico</option>`; sel.disabled = true; return; } 
  sel.disabled = false; const dSet = new Set(); DATA.forEach(r => { const d = parseDateStr(r.fecha); if(d && d.getMonth() === +fM) dSet.add(d.getDate()); }); 
  sel.innerHTML = `<option value="">Todo el mes</option>` + [...dSet].sort((a,b) => a-b).map(d => `<option value="${d}">${d}</option>`).join(''); 
}

function renderAnalisisBBDD() {
  const fa = $('f-analisis-agente') ? $('f-analisis-agente').value : '', fm = $('f-analisis-mes') ? $('f-analisis-mes').value : '', fd = $('f-analisis-dia') ? $('f-analisis-dia').value : '';
  const fData = DATA.filter(r => { 
    if(fa && r.email !== fa) return false; 
    if(fm !== '' || fd !== '') { const d = parseDateStr(r.fecha); if(!d) return false; if(fm !== '' && d.getMonth() !== +fm) return false; if(fd !== '' && d.getDate() !== +fd) return false; } 
    return true; 
  });
  
  const tGest = fData.length, tRts = fData.filter(r => r.proceso === 'RTS').length, conv = tGest > 0 ? Math.round((tRts / tGest) * 100) : 0;
  if($('analisis-tot-text')) $('analisis-tot-text').textContent = tGest; 
  if($('analisis-rts-text')) $('analisis-rts-text').textContent = tRts; 
  if($('analisis-conv-text')) $('analisis-conv-text').textContent = conv + '%';
  
  const histMap = {}, zMap = {}, hMap = {}; 
  fData.forEach(r => { 
    const d = parseDateStr(r.fecha); if(d) { const key = String(d.getDate()).padStart(2, '0') + '/' + String(d.getMonth() + 1).padStart(2, '0'); histMap[key] = (histMap[key] || 0) + 1; }
    const z = r.zona && r.zona.trim() !== '' ? r.zona.trim() : 'Sin Asignar'; zMap[z] = (zMap[z] || 0) + 1; 
    const t = normalizeTime(r.hora); if(t) { const hr = t.split(':')[0] + ':00'; hMap[hr] = (hMap[hr] || 0) + 1; }
  });
  
  destroyChart('total_hist'); const sortedDates = Object.keys(histMap).sort((a,b) => { const [da, ma] = a.split('/'), [db, mb] = b.split('/'); return new Date(2000, +ma - 1, +da) - new Date(2000, +mb - 1, +db); });
  if($('chart-total-hist')) CHARTS['total_hist'] = new Chart($('chart-total-hist'), { type: 'line', data: { labels: sortedDates, datasets: [{ label: 'Inputs Diarios', data: sortedDates.map(d => histMap[d]), borderColor: '#A1A1AA', backgroundColor: 'rgba(161,161,170,0.1)', fill: true, tension: 0.4, pointRadius: 2, pointBackgroundColor: '#A1A1AA' }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true } } } });
  
  destroyChart('total_zonas'); const sZonas = Object.entries(zMap).sort((a,b) => b[1] - a[1]), tZonas = sZonas.slice(0, 5), oZonas = sZonas.slice(5).reduce((acc, v) => acc + v[1], 0); 
  if(oZonas > 0) tZonas.push(['Otros Nodes', oZonas]); 
  const totalZ = tZonas.reduce((s, i) => s + i[1], 0);
  if($('chart-total-zonas')) CHARTS['total_zonas'] = new Chart($('chart-total-zonas'), { type: 'doughnut', data: { labels: tZonas.map(z => `${z[0]}: ${z[1]} (${totalZ > 0 ? Math.round((z[1]/totalZ)*100) : 0}%)`), datasets: [{ data: tZonas.map(z => z[1]), backgroundColor: ['#FF441F','#3B82F6','#22C55E','#F59E0B','#8B5CF6','#3F3F46'], borderWidth: 1, borderColor: '#18181B' }] }, options: { maintainAspectRatio: false, plugins: { legend: { position: 'right', labels: { font: { size: 10 } } } }, cutout: '75%' } });
  
  destroyChart('total_horas'); const sHoras = Object.keys(hMap).sort((a,b) => parseInt(a) - parseInt(b)), tHoras = sHoras.reduce((s, h) => s + hMap[h], 0);
  if($('chart-total-horas')) CHARTS['total_horas'] = new Chart($('chart-total-horas'), { type: 'bar', data: { labels: sHoras.map(h => `${h} | ${hMap[h]} (${tHoras > 0 ? Math.round((hMap[h]/tHoras)*100) : 0}%)`), datasets: [{ label: 'Workload', data: sHoras.map(h => hMap[h]), backgroundColor: '#3B82F6', borderRadius: 4 }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true, grid: { display: false } }, x: { grid: { display: false }, ticks: { font: { size: 9 }, maxRotation: 45, minRotation: 45 } } } } });
}

const debouncedFilter = debounce(doFilter, CONFIG.DEBOUNCE_MS);
function doFilter() {
  const sq = $('q') ? ($('q').value || '').toLowerCase() : '', fe = $('f-etapa') ? $('f-etapa').value : '', fr = $('f-res') ? $('f-res').value : '', fa = $('f-agente') ? $('f-agente').value : '', fM = $('f-mes') ? $('f-mes').value : '', fD = $('f-dia') ? $('f-dia').value : '', fHI = $('f-hora-ini') ? $('f-hora-ini').value : '', fHF = $('f-hora-fin') ? $('f-hora-fin').value : '';
  FILTERED = DATA.filter(r => { 
    if(sq && !r.restaurante.toLowerCase().includes(sq) && !r.tel.includes(sq) && !r.email.includes(sq) && !r.comentario.toLowerCase().includes(sq) && !r.brand.toLowerCase().includes(sq)) return false; 
    if(fe && r.proceso !== fe) return false; if(fr && r.resultado !== fr) return false; if(fa && r.email !== fa) return false;
    if(fM !== '' || fD !== '') { const d = parseDateStr(r.fecha); if(!d) return false; if(fM !== '' && d.getMonth() !== +fM) return false; if(fD !== '' && d.getDate() !== +fD) return false; }
    if(fHI || fHF) { const rT = normalizeTime(r.hora); if(!rT) return false; if(fHI && rT < fHI) return false; if(fHF && rT > fHF.replace(':00', ':59')) return false; } 
    return true;
  });
  FILTERED.sort((a,b) => { const av = a[sortCol] || '', bv = b[sortCol] || ''; return av < bv ? -sortDir : av > bv ? sortDir : 0; }); 
  currentPage = 1; renderTable(); if($('reg-view-charts') && $('reg-view-charts').style.display === 'block') renderRegCharts();
}

function srt(col) { if(sortCol === col) sortDir *= -1; else { sortCol = col; sortDir = 1; } ['fecha','restaurante','proceso','email'].forEach(c => { const th = $(`th-${c}`); if(th) th.className = c === col ? (sortDir === 1 ? 'asc' : 'desc') : ''; }); doFilter(); }

function renderTable() {
  const start = (currentPage - 1) * CONFIG.PAGE_SIZE, slice = FILTERED.slice(start, start + CONFIG.PAGE_SIZE); 
  if($('reg-count')) $('reg-count').textContent = 'Records: ' + FILTERED.length.toLocaleString();
  const tbody = $('reg-tbody');
  if(!slice.length) { if(tbody) tbody.innerHTML = `<tr><td colspan="8"><div class="empty"><h3>Query Not Found</h3></div></td></tr>`; } 
  else { 
    if(tbody) { 
      tbody.innerHTML = slice.map(r => `<tr data-id="${r.id}"><td class="muted" style="font-family:'JetBrains Mono'">${esc(r.fecha)}</td><td class="name">${esc(r.restaurante)}</td><td class="mono">${esc(r.tel)}</td><td>${etapaChip(r.proceso)}</td><td>${resChip(r.resultado)}</td><td class="muted" style="font-size:11px">${esc(aName(r.email))}</td><td class="muted" style="max-width:160px;overflow:hidden;text-overflow:ellipsis;white-space:nowrap">${esc(r.comentario).substring(0, 55)}${r.comentario.length > 55 ? '\u2026' : ''}</td><td class="mono" style="color:var(--ink4);font-size:11px">${esc(r.brand) || '\u2014'}</td></tr>`).join(''); 
      tbody.querySelectorAll('tr').forEach(tr => tr.addEventListener('click', () => openDrawer(+tr.dataset.id))); 
    } 
  }
  renderPager();
}

function renderPager() {
  const totalP = Math.ceil(FILTERED.length / CONFIG.PAGE_SIZE), pagerEl = $('reg-pager');
  if(totalP <= 1) { if(pagerEl) pagerEl.innerHTML = ''; return; } 
  const pages = []; for(let i = 1; i <= totalP; i++) { if(i === 1 || i === totalP || Math.abs(i - currentPage) <= 1) pages.push(i); else if(pages[pages.length - 1] !== '…') pages.push('…'); }
  if(pagerEl) { 
    pagerEl.innerHTML = pages.map(x => x === '…' ? `<span style="color:var(--ink5);font-size:12px;padding:0 8px">\u2026</span>` : `<button class="pg-btn${x === currentPage ? ' on' : ''}" data-p="${x}">${x}</button>`).join(''); 
    pagerEl.querySelectorAll('.pg-btn').forEach(b => b.addEventListener('click', () => { currentPage = +b.dataset.p; renderTable(); })); 
  }
}

function resetFilters() { if($('q')) $('q').value = ''; ['f-etapa','f-res','f-agente','f-mes','f-hora-ini','f-hora-fin'].forEach(id => { if($(id)) $(id).value = ''; }); updateDayFilter(); doFilter(); }
function fillMonthFilter() { const ms = new Set(); DATA.forEach(r => { const d = parseDateStr(r.fecha); if(d) ms.add(d.getMonth()); }); const names = ["Enero","Febrero","Marzo","Abril","Mayo","Junio","Julio","Agosto","Septiembre","Octubre","Noviembre","Diciembre"]; if($('f-mes')) $('f-mes').innerHTML = `<option value="">Todo el Histórico</option>` + [...ms].sort((a,b) => b-a).map(m => `<option value="${m}">${names[m]}</option>`).join(''); updateDayFilter(); }
function updateDayFilter() { const fM = $('f-mes') ? $('f-mes').value : '', s = $('f-dia'); if(!s) return; if(fM === '') { s.innerHTML = `<option value="">Día</option>`; s.disabled = true; return; } s.disabled = false; const ds = new Set(); DATA.forEach(r => { const d = parseDateStr(r.fecha); if(d && d.getMonth() === +fM) ds.add(d.getDate()); }); s.innerHTML = `<option value="">Todos los Días</option>` + [...ds].sort((a,b) => a-b).map(d => `<option value="${d}">${d}</option>`).join(''); }
function fillHourFilter() { const hs = new Set(); DATA.forEach(r => { const t = normalizeTime(r.hora); if(t) hs.add(t.split(':')[0]); }); const opts = `<option value="">--:--</option>` + [...hs].sort((a,b) => +a - +b).map(h => `<option value="${h}:00">${h}:00</option>`).join(''); if($('f-hora-ini')) $('f-hora-ini').innerHTML = opts; if($('f-hora-fin')) $('f-hora-fin').innerHTML = opts; }
function fillAgentFilter() { 
  const ag = getUnifiedAgentList(); const s = $('f-agente');
  if(s) { 
      s.innerHTML = `<option value="">Filtro: Agente</option>` + ag.map(a => `<option value="${a.val}">${esc(a.label)}</option>`).join(''); 
      if(!IS_ADMIN() && ag.length===1) { s.value = ag[0].val; s.disabled = true; }
  } 
}
function setRegView(v) { const i = v === 'table'; if($('btn-v-table')) $('btn-v-table').className = i ? 'btn btn-sm btn-primary' : 'btn btn-sm btn-ghost'; if($('btn-v-charts')) $('btn-v-charts').className = i ? 'btn btn-sm btn-ghost' : 'btn btn-sm btn-primary'; if($('reg-view-table')) $('reg-view-table').style.display = i ? 'block' : 'none'; if($('reg-view-charts')) $('reg-view-charts').style.display = i ? 'none' : 'block'; if(!i) renderRegCharts(); }

function renderRegCharts() {
  const aE = {}, aR = {}, aA = {}, aF = {}; 
  FILTERED.forEach(r => { aE[r.proceso] = (aE[r.proceso] || 0) + 1; aR[r.resultado] = (aR[r.resultado] || 0) + 1; if(r.email) aA[r.email] = (aA[r.email] || 0) + 1; if(r.fecha) { const d = parseDateStr(r.fecha); if(d) aF[String(d.getDate()).padStart(2,'0')+'/'+String(d.getMonth()+1).padStart(2,'0')] = (aF[String(d.getDate()).padStart(2,'0')+'/'+String(d.getMonth()+1).padStart(2,'0')] || 0) + 1; } });
  const T = { r:'#FF441F', blue:'#3B82F6', green:'#22C55E', amber:'#F59E0B', purple:'#8B5CF6' };
  destroyChart('tendencia'); const sD = Object.keys(aF).sort((a,b) => { const [da,ma] = a.split('/'), [db,mb] = b.split('/'); return new Date(2000, +ma-1, +da) - new Date(2000, +mb-1, +db); });
  if($('chart-reg-tendencia')) CHARTS['tendencia'] = new Chart($('chart-reg-tendencia'), { type: 'line', data: { labels: sD, datasets: [{ label: 'Volumen', data: sD.map(d => aF[d]), borderColor: T.blue, backgroundColor: 'rgba(59,130,246,0.15)', fill: true, tension: 0.4, pointRadius: 3, pointBackgroundColor: T.blue }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { y: { beginAtZero: true } } } });
  destroyChart('etapa'); const tE = Object.values(aE).reduce((a,b) => a+b, 0);
  if($('chart-reg-etapa')) CHARTS['etapa'] = new Chart($('chart-reg-etapa'), { type: 'doughnut', data: { labels: Object.keys(aE).map(k => `${k}: ${aE[k]} (${tE>0 ? Math.round((aE[k]/tE)*100) : 0}%)`), datasets: [{ data: Object.values(aE), backgroundColor: [T.blue, T.green, T.amber, T.r, T.purple, '#EF4444', '#F59E0B'], borderWidth: 1, borderColor: '#18181B' }] }, options: { maintainAspectRatio: false, plugins: { legend: { position: 'right', labels: { font: { size: 10 } } } }, cutout: '70%' } });
  destroyChart('res'); const rS = Object.entries(aR).sort((a,b) => b[1]-a[1]).slice(0, 6), tR = rS.reduce((s,i) => s+i[1], 0);
  if($('chart-reg-res')) CHARTS['res'] = new Chart($('chart-reg-res'), { type: 'bar', data: { labels: rS.map(x => `${x[0].replace('Contactado - ','')}: ${x[1]} (${tR>0 ? Math.round((x[1]/tR)*100) : 0}%)`), datasets: [{ data: rS.map(x => x[1]), backgroundColor: T.amber, borderRadius: 4 }] }, options: { indexAxis: 'y', maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { display: false, grid: { display: false } }, y: { grid: { display: false }, ticks: { font: { size: 10 } } } } } });
  destroyChart('agentes'); const aS = Object.entries(aA).sort((a,b) => b[1]-a[1]).slice(0, 25), aEms = aS.map(x => x[0]);
  if($('chart-reg-agente')) CHARTS['agentes'] = new Chart($('chart-reg-agente'), { type: 'bar', data: { labels: aS.map(x => `${esc(aName(x[0]).split(' ')[0])} (${x[1]})`), datasets: [{ label: 'Gestiones', data: aS.map(x => x[1]), backgroundColor: T.r, hoverBackgroundColor: T.purple, borderRadius: 4 }] }, options: { maintainAspectRatio: false, plugins: { legend: { display: false }, tooltip: { callbacks: { label: c => c.raw + ' Logs' } } }, scales: { y: { display: false, grid: { display: false } }, x: { grid: { display: false }, ticks: { font: { size: 9 }, maxRotation: 45, minRotation: 45 } } }, onClick: (e, el) => { if(el.length) renderAgentDetail(aEms[el[0].index]); }, onHover: (ev, el) => { ev.native.target.style.cursor = el.length ? 'pointer' : 'default'; } } });
  if($('card-agente-detalle')) $('card-agente-detalle').style.display = 'none';
}

function fillAnalisisFilters() {
  const agList = getUnifiedAgentList(); const sA = $('f-analisis-agente'); 
  if(sA) {
      sA.innerHTML = `<option value="">Cross-Agent (Todos)</option>` + agList.map(a => `<option value="${a.val}">${esc(a.label)}</option>`).join('');
      if(!IS_ADMIN() && agList.length===1) { sA.value = agList[0].val; sA.disabled = true; }
  }
  const monthSet = new Set(); DATA.forEach(r => { const d = parseDateStr(r.fecha); if(d) monthSet.add(d.getMonth()); }); 
  const mNames = ["Enero","Febrero","Marzo","Abril","Mayo","Junio","Julio","Agosto","Septiembre","Octubre","Noviembre","Diciembre"];
  const selMes = $('f-analisis-mes'); if(selMes) selMes.innerHTML = `<option value="">Timeline Completo</option>` + [...monthSet].sort((a,b) => b-a).map(m => `<option value="${m}">${mNames[m]}</option>`).join(''); 
  updateAnalisisDayFilter();
}

function renderAgentDetail(email) {
  if(!$('card-agente-detalle')) return; $('card-agente-detalle').style.display = 'block'; $('title-agente-detalle').innerHTML = `Analíticas de Usuario: <span style="color:var(--r);font-weight:700">${esc(aName(email))}</span>`;
  const aR = FILTERED.filter(r => r.email === email), ST = ['PROSPECTO','ED','DM','FIRMA CONTRATO','DC','DATA COLECCTION / SOB','RTS'], SL = ['PROSPECTO','ED','DM','CONTRATO','DC','COLLECTION','RTS'], fD = ST.map(s => aR.filter(r => r.proceso === s).length), fT = Math.max(aR.length, 1);
  destroyChart('funnel'); CHARTS['funnel'] = new Chart($('chart-funnel'), { type: 'bar', data: { labels: SL.map((l, i) => `${l}: ${fD[i]} (${Math.round((fD[i]/fT)*100)}%)`), datasets: [{ label: 'Entidades', data: fD, backgroundColor: ['#3B82F6','#F59E0B','#14B8A6','#F59E0B','#8B5CF6','#EF4444','#22C55E'], borderRadius: 4, barPercentage: 0.6 }] }, options: { indexAxis: 'y', maintainAspectRatio: false, plugins: { legend: { display: false }, tooltip: { callbacks: { label: c => c.raw + ' Logs' } } }, scales: { x: { display: false }, y: { grid: { display: false }, ticks: { font: { weight: 'bold', size: 10 } } } } } });
  const t = aR.length, h = aR.filter(r => r.proceso === 'RTS').length, i = aR.filter(r => r.resultado === 'Contactado - Interesado').length;
  $('agente-kpis').innerHTML = `<div class="mc" style="padding:16px;border-top:2px solid var(--ink4)"><div class="mc-label">Net Output</div><div class="mc-val">${t}</div></div><div class="mc" style="padding:16px;border-top:2px solid var(--green)"><div class="mc-label">Positive Leads</div><div class="mc-val" style="color:var(--green)">${i}</div><div class="mc-sub">${t ? Math.round(i/t*100) : 0}% conversion rate</div></div><div class="mc" style="padding:16px;border-top:2px solid var(--purple)"><div class="mc-label">RTS Closed</div><div class="mc-val" style="color:var(--purple)">${h}</div><div class="mc-sub">${t ? Math.round(h/t*100) : 0}% pipeline ratio</div></div>`;
  const vD = DATA.map(r => parseDateStr(r.fecha)).filter(d => d && !isNaN(d)), mD = vD.length ? new Date(Math.max(...vD)) : new Date(), wR = aR.filter(r => { const d = parseDateStr(r.fecha); return d && ((mD - d) / 86400000 <= 7); });
  $('agente-weekly-kpis').innerHTML = `<div style="flex:1;display:flex;align-items:center;gap:12px;background:var(--bg2);padding:14px;border-radius:var(--r-sm);border:var(--glass-border)"><div style="width:40px;height:40px;background:var(--bg3);border-radius:10px;display:flex;align-items:center;justify-content:center"><svg viewBox="0 0 24 24" fill="none" stroke="var(--ink)" stroke-width="2" style="width:20px;height:20px"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg></div><div><div style="font-size:10px;color:var(--ink4);font-weight:600;text-transform:uppercase;letter-spacing:.05em">Volumen (T-7)</div><div style="font-size:20px;font-weight:700;color:var(--ink);font-family:'Space Grotesk'">${wR.length}</div></div></div><div style="flex:1;display:flex;align-items:center;gap:12px;background:var(--bg2);padding:14px;border-radius:var(--r-sm);border:var(--glass-border)"><div style="width:40px;height:40px;background:var(--pbg);border-radius:10px;display:flex;align-items:center;justify-content:center"><svg viewBox="0 0 24 24" fill="none" stroke="var(--purple)" stroke-width="2" style="width:20px;height:20px"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg></div><div><div style="font-size:10px;color:var(--ink4);font-weight:600;text-transform:uppercase;letter-spacing:.05em">RTS Creados (T-7)</div><div style="font-size:20px;font-weight:700;color:var(--purple);font-family:'Space Grotesk'">${wR.filter(r => r.proceso === 'RTS').length}</div></div></div>`;
  $('card-agente-detalle').scrollIntoView({behavior:'smooth', block:'nearest'});
}

function renderPipeline() {
  const ST = ['PROSPECTO','ED','DM','FIRMA CONTRATO','DC','DATA COLECCTION / SOB','RTS'], SL = ['PROSPECTO','ED (DOC)','DM (MIGR)','CONTRATO','DC','COLLECTION','RTS'], bM = {'FIRMA CONTRATO':'rgba(245,158,11,0.1)', 'DATA COLECCTION / SOB':'rgba(239,68,68,0.1)', 'RTS':'rgba(34,197,94,0.1)'};
  if($('pl-funnel')) $('pl-funnel').innerHTML = ST.map((s, i) => `<div class="funnel-step"><div class="fs-num" style="color:${stageColor(s)};text-shadow:0 0 10px ${stageColor(s)}">${DATA.filter(r => r.proceso === s).length}</div><div class="fs-label">${SL[i]}</div><div class="fs-pct">${Math.round(DATA.filter(r => r.proceso === s).length / Math.max(DATA.length, 1) * 100)}%</div></div>`).join('');
  if($('pipeline-grid')) {
    $('pipeline-grid').innerHTML = ST.map((s, i) => {
      const rs = DATA.filter(r => r.proceso === s), cs = rs.slice().reverse().slice(0, 15).map(r => `<div class="pl-card" data-id="${r.id}"><div class="pl-card-name">${esc(r.restaurante)}</div><div class="pl-card-agent">${esc(aName(r.email))} · ${esc(r.fecha)}</div></div>`).join('');
      return `<div class="pl-col"><div class="pl-head" style="background:${bM[s] || 'var(--bg3)'}"><span class="pl-head-label" style="color:${stageColor(s)}">${s}</span><span class="pl-head-num" style="color:${stageColor(s)}">${rs.length}</span></div><div class="pl-body">${cs || '<div class="pl-empty">No entities found</div>'}</div></div>`;
    }).join('');
    $('pipeline-grid').querySelectorAll('.pl-card').forEach(c => c.addEventListener('click', () => openDrawer(+c.dataset.id)));
  }
}

function renderRoster() {
  const tbody = $('roster-tbody');
  if(!tbody) return;
  const agents = getUnifiedAgentList();
  
  if(agents.length === 0) {
    tbody.innerHTML = `<tr><td colspan="4"><div class="empty"><h3>Directorio Vacío</h3><p>Añade agentes a tu pestaña ROSTER o INDICADORES en Sheets.</p></div></td></tr>`;
    return;
  }

  tbody.innerHTML = agents.map((a, i) => {
    const initials = a.label.split(' ').map(w => w[0] || '').join('').substring(0,2).toUpperCase();
    const avatarBg = AV_COLORS[i % AV_COLORS.length];
    
    // Cruzar mediante CleanId garantizado
    const rosterInfo = ROSTER_DATA[a.cleanId];
    const st = getAgentStats(a.val);
    
    const tel = rosterInfo && rosterInfo.telefono ? rosterInfo.telefono : (st && st.telefono ? st.telefono : '—');
    
    let telHtml = `<span style="color:var(--ink5)">—</span>`;
    if (tel && tel !== '—') {
        let cleanTel = tel.replace(/[^\d]/g, '');
        if (cleanTel.length === 10) {
            if (cleanTel.startsWith('3')) cleanTel = '57' + cleanTel;
            else cleanTel = '52' + cleanTel; 
        }
        
        telHtml = `<a href="https://wa.me/${cleanTel}" target="_blank" onclick="event.stopPropagation();" title="Abrir chat en WhatsApp" style="color:var(--green); text-decoration:none; display:inline-flex; align-items:center; gap:6px; font-weight:700; transition:all 0.2s; padding:4px 10px; background:rgba(34,197,94,0.1); border-radius:20px; border:1px solid rgba(34,197,94,0.2);" onmouseover="this.style.background='rgba(34,197,94,0.2)'; this.style.boxShadow='0 0 10px rgba(34,197,94,0.3)'" onmouseout="this.style.background='rgba(34,197,94,0.1)'; this.style.boxShadow='none'">
            <svg viewBox="0 0 24 24" width="14" height="14" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.305-.885-.653-1.482-1.46-1.656-1.758-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51a12.8 12.8 0 00-.57-.012c-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg>
            ${esc(tel)}
        </a>`;
    }
    
    return `<tr data-email="${esc(a.val)}" title="Ver Log de Actividad">
      <td>
        <div style="display:flex;align-items:center;gap:14px">
          <div style="width:38px;height:38px;border-radius:10px;background:${avatarBg};color:#fff;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:12px;flex-shrink:0;box-shadow:inset 0 -2px 5px rgba(0,0,0,0.3)">${initials}</div>
          <div>
            <div style="font-weight:600;color:var(--ink);font-size:14px">${esc(a.label)}</div>
          </div>
        </div>
      </td>
      <td style="text-align:center;font-family:'JetBrains Mono';font-size:13px;color:var(--ink3)">${esc(a.val)}</td>
      <td style="text-align:center;">${telHtml}</td>
      <td style="text-align:center"><span class="chip chip-rts" style="box-shadow:0 0 10px rgba(34,197,94,0.2)">Activo</span></td>
    </tr>`;
  }).join('');
  
  tbody.querySelectorAll('tr').forEach(tr => tr.addEventListener('click', () => {
    openAgentHistory(tr.dataset.email);
  }));
}

function renderSeguimientos() {
  const ss = DATA.filter(hasSeg), listEl = $('seg-list');
  if(!ss.length) { if(listEl) listEl.innerHTML = `<div class="empty"><h3>Queue is Empty</h3></div>`; return; }
  if(listEl) {
    listEl.innerHTML = ss.slice(0, 50).map((r, i) => {
      const cl = i % 5 === 0 ? 'venc' : i % 3 === 0 ? 'hoy' : 'ok', lb = cl === 'venc' ? 'Venc' : cl === 'hoy' ? 'T-0' : 'T+1', em = cl === 'venc' ? '⚠' : '⚡';
      return `<div class="seg-card" data-id="${r.id}"><div class="seg-urg ${cl}"><span>${em}</span><span>${lb}</span></div><div><div class="seg-name">${esc(r.restaurante)}</div><div class="seg-detail">${esc(aName(r.email))} · ${etapaChip(r.proceso)} · <em style="color:var(--ink4)">${esc(r.comentario).substring(0, 80)}...</em></div></div><div class="seg-right"><div class="seg-hora">${esc(r.hora) || '--:--'}</div><div class="seg-date" style="font-family:'JetBrains Mono'">${esc(r.fecha)}</div></div></div>`;
    }).join('');
    listEl.querySelectorAll('.seg-card').forEach(c => c.addEventListener('click', () => openDrawer(+c.dataset.id)));
  }
}

function setDesgloseView(v) {
    const isTable = v === 'table';
    if($('btn-desglose-table')) $('btn-desglose-table').className = isTable ? 'btn btn-sm btn-primary' : 'btn btn-sm btn-ghost';
    if($('btn-desglose-charts')) $('btn-desglose-charts').className = isTable ? 'btn btn-sm btn-ghost' : 'btn btn-sm btn-primary';
    if($('desglose-view-table')) $('desglose-view-table').style.display = isTable ? 'block' : 'none';
    if($('desglose-view-charts')) $('desglose-view-charts').style.display = isTable ? 'none' : 'block';
    if(!isTable) renderDesglose(); // Re-trigger chart rendering
}

function renderDesgloseCharts(agentsData) {
    if (!$('desglose-view-charts') || $('desglose-view-charts').style.display === 'none') return;
    
    // Filtrar a los top 15 agentes para evitar saturar la gráfica si son muchos
    const topAgents = agentsData.slice(0, 15);
    const labels = topAgents.map(a => esc(a.label.split(' ')[0] + ' ' + (a.label.split(' ')[1] ? a.label.split(' ')[1][0] + '.' : '')));
    
    Chart.defaults.color = '#A1A1AA';
    Chart.defaults.borderColor = 'rgba(255,255,255,0.05)';

    destroyChart('desglose_attainment');
    if($('chart-desglose-attainment')) {
        CHARTS['desglose_attainment'] = new Chart($('chart-desglose-attainment'), {
            type: 'bar',
            data: {
                labels: labels,
                datasets: [
                    {
                        label: 'RTS Logrados',
                        data: topAgents.map(a => a.rts),
                        backgroundColor: '#4ADE80',
                        borderRadius: 4,
                        order: 2
                    },
                    {
                        label: 'Meta Target',
                        data: topAgents.map(a => a.meta),
                        type: 'line',
                        borderColor: '#F59E0B',
                        backgroundColor: 'transparent',
                        borderDash: [5, 5],
                        pointRadius: 0,
                        borderWidth: 2,
                        order: 1
                    }
                ]
            },
            options: { maintainAspectRatio: false, plugins: { legend: { position: 'top', labels: {font: {size:11}} } }, scales: { y: { beginAtZero: true }, x: { grid: { display: false }, ticks: {maxRotation: 45, minRotation: 45} } } }
        });
    }

    destroyChart('desglose_workload');
    if($('chart-desglose-workload')) {
        CHARTS['desglose_workload'] = new Chart($('chart-desglose-workload'), {
            type: 'bar',
            data: {
                labels: labels,
                datasets: [{
                    label: 'Total Logs',
                    data: topAgents.map(a => a.total),
                    backgroundColor: '#3B82F6',
                    borderRadius: 4
                }]
            },
            options: { indexAxis: 'y', maintainAspectRatio: false, plugins: { legend: { display: false } }, scales: { x: { beginAtZero: true }, y: { grid: { display: false } } } }
        });
    }

    destroyChart('desglose_pipeline');
    if($('chart-desglose-pipeline')) {
        const pipeSums = {
            Prospecto: agentsData.reduce((s,a)=>s+a.prospecto, 0),
            ED: agentsData.reduce((s,a)=>s+a.ed, 0),
            DM: agentsData.reduce((s,a)=>s+a.dm, 0),
            Firma: agentsData.reduce((s,a)=>s+a.firma, 0),
            DC: agentsData.reduce((s,a)=>s+a.dc, 0),
            SOB: agentsData.reduce((s,a)=>s+a.datacol, 0)
        };
        CHARTS['desglose_pipeline'] = new Chart($('chart-desglose-pipeline'), {
            type: 'doughnut',
            data: {
                labels: Object.keys(pipeSums),
                datasets: [{
                    data: Object.values(pipeSums),
                    backgroundColor: ['#3B82F6', '#F59E0B', '#14B8A6', '#F59E0B', '#8B5CF6', '#EF4444'],
                    borderWidth: 1,
                    borderColor: '#18181B'
                }]
            },
            options: { maintainAspectRatio: false, cutout: '70%', plugins: { legend: { position: 'right', labels: { font: { size: 10 } } } } }
        });
    }
}

function renderDesglose() {
  const mG = $('global-meta') ? (parseInt($('global-meta').value) || 20) : 20, aD = {};
  getUnifiedAgentList().forEach(a => { aD[a.val] = { email: a.val, label: a.label, prospecto: 0, ed: 0, dm: 0, firma: 0, dc: 0, datacol: 0, rts: 0, total: 0, meta: mG }; });
  DATA.forEach(r => { const k = r.email; if(!k || !aD[k]) return; aD[k].total++; const m = { 'PROSPECTO':'prospecto', 'ED':'ed', 'DM':'dm', 'FIRMA CONTRATO':'firma', 'DC':'dc', 'DATA COLECCTION / SOB':'datacol', 'RTS':'rts' }; if(m[r.proceso]) aD[k][m[r.proceso]]++; });
  Object.values(aD).forEach(ag => { const s = getAgentStats(ag.email); if(!s) return; if(s.meta > 0) ag.meta = s.meta; if(s.etapas) { if(INDICADORES_COL_FOUND.prospectos) ag.prospecto = s.etapas.prospectos; if(INDICADORES_COL_FOUND.ed) ag.ed = s.etapas.ed; if(INDICADORES_COL_FOUND.dm) ag.dm = s.etapas.dm; if(INDICADORES_COL_FOUND.firma) ag.firma = s.etapas.firma; if(INDICADORES_COL_FOUND.dc) ag.dc = s.etapas.dc; if(INDICADORES_COL_FOUND.datacol) ag.datacol = s.etapas.datacol; if(INDICADORES_COL_FOUND.rts) ag.rts = s.rts; } });
  
  const sortedAgents = Object.values(aD).sort((a, b) => b.rts - a.rts);
  
  if($('desglose-tbody')) {
    $('desglose-tbody').innerHTML = sortedAgents.map((a, i) => {
      const t = Math.max(a.total, a.prospecto + a.ed + a.dm + a.firma + a.dc + a.datacol + a.rts), cp = a.meta > 0 ? Math.round(a.rts / a.meta * 100) : 0, bg = cp >= 100 ? 'rgba(34,197,94,0.15)' : cp >= 80 ? 'rgba(245,158,11,0.15)' : 'rgba(239,68,68,0.15)', tx = cp >= 100 ? '#4ADE80' : cp >= 80 ? '#FBBF24' : '#F87171', bd = cp >= 100 ? '#22C55E' : cp >= 80 ? '#F59E0B' : '#EF4444';
      
      const rtsColor = a.rts > 0 ? '#4ADE80' : '#F87171';
      const rtsGlow = a.rts > 0 ? '0 0 15px rgba(74,222,128,0.6)' : '0 0 15px rgba(248,113,113,0.8)';

      return `<tr><td><div style="display:flex;align-items:center;gap:14px"><div style="width:38px;height:38px;border-radius:10px;background:${AV_COLORS[i % AV_COLORS.length]};color:#fff;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:12px;flex-shrink:0">${a.label.split(' ').map(w => w[0] || '').join('').substring(0,2).toUpperCase()}</div><div><div style="font-weight:600;color:var(--ink);font-size:14px">${esc(a.label)}</div><div style="font-size:10px;color:var(--ink4);font-family:'JetBrains Mono'">${esc(a.email)}</div></div></div></td><td style="text-align:center;font-weight:700;font-size:16px;color:var(--ink);font-family:'JetBrains Mono'">${t}</td><td style="text-align:center"><span class="${a.prospecto > 0 ? 'val-num' : 'val-zero'}">${a.prospecto}</span></td><td style="text-align:center"><span class="${a.ed > 0 ? 'val-num' : 'val-zero'}">${a.ed}</span></td><td style="text-align:center"><span class="${a.dm > 0 ? 'val-num' : 'val-zero'}">${a.dm}</span></td><td style="text-align:center"><span class="${a.firma > 0 ? 'val-num' : 'val-zero'}">${a.firma}</span></td><td style="text-align:center"><span class="${a.dc > 0 ? 'val-num' : 'val-zero'}">${a.dc}</span></td><td style="text-align:center"><span class="${a.datacol > 0 ? 'val-num' : 'val-zero'}">${a.datacol}</span></td><td style="text-align:center;font-weight:800;font-size:18px;color:${rtsColor};text-shadow:${rtsGlow};font-family:'JetBrains Mono'">${a.rts}</td><td style="text-align:center;color:var(--ink3);font-size:12px;font-family:'JetBrains Mono'">${a.meta}</td><td style="text-align:center;border-left:1px dashed var(--ink5)"><div class="badge-pill" style="background:${bg};color:${tx};border-color:${bd};box-shadow:0 0 10px ${bg}">${cp}%</div></td><td style="text-align:center;"><button class="btn btn-sm btn-outline btn-funnel-agent" data-email="${esc(a.email)}" style="font-size:10px; padding:6px 10px; border-radius:20px;">Ver Funnel</button></td></tr>`;
    }).join('');
    
    $('desglose-tbody').querySelectorAll('.btn-funnel-agent').forEach(btn => btn.addEventListener('click', (e) => {
        e.stopPropagation();
        openFunnelDrawer(btn.dataset.email);
    }));
  }

  renderDesgloseCharts(sortedAgents);
}

function openFunnelDrawer(email) {
   let fData = DATA;
   let title = "Conversión Global del Equipo";
   let sub = "Promedios de pipeline del área";

   if (email !== 'ALL') {
      const cleanEmail = getCleanId(email);
      fData = DATA.filter(r => getCleanId(r.email) === cleanEmail || getCleanId(r.agent) === cleanEmail);
      const agentObj = getUnifiedAgentList().find(a => getCleanId(a.val) === cleanEmail);
      title = "Conversión: " + (agentObj ? esc(agentObj.label) : esc(email));
      sub = "Gestiones de: " + esc(email);
   }

   const stages = ['PROSPECTO','ED','DM','FIRMA CONTRATO','DC','DATA COLECCTION / SOB','RTS'];
   const sNames = ['Prospecto','ED (Documentos)','DM (Migración)','Firma de Contrato','DC (Data)','Collection / SOB','RTS (Cierre)'];
   const counts = stages.map(s => fData.filter(r => r.proceso === s).length);
   const total = Math.max(fData.length, 1);
   const rtsCount = fData.filter(r => r.proceso === 'RTS').length;
   const overallConv = Math.round(rtsCount / total * 100);

   let html = `<div class="dr-sec"><div class="dr-grid">
       <div class="dr-field"><div class="dk">Total Gestiones (Universo)</div><div class="dv" style="font-size:24px;font-weight:800;font-family:'JetBrains Mono'">${fData.length}</div></div>
       <div class="dr-field"><div class="dk">Tasa de Conversión a RTS</div><div class="dv" style="font-size:24px;font-weight:800;color:var(--green);font-family:'JetBrains Mono';text-shadow:0 0 10px rgba(34,197,94,0.3)">${overallConv}%</div></div>
   </div></div>`;

   html += `<div class="dr-sec"><div class="dr-sec-title">Análisis de Drop-off (Etapa por Etapa)</div>`;
   
   let funnelHtml = `<div style="display:flex;flex-direction:column;gap:8px;">`;
   for(let i=0; i<stages.length; i++) {
       let c = counts[i];
       let pct = Math.round((c / total) * 100);
       let barW = Math.max(pct, 1); // Minimum width to be visible
       let color = i === stages.length - 1 ? 'var(--green)' : 'var(--blue)';
       if(c === 0) color = 'var(--ink5)';
       
       funnelHtml += `
       <div style="background:var(--bg); border:1px solid var(--ink5); border-radius:var(--r-sm); padding:12px; position:relative; overflow:hidden;">
           <div style="position:absolute; left:0; top:0; bottom:0; width:${barW}%; background:${color}; opacity:0.15; z-index:0; transition:width 1s cubic-bezier(0.16, 1, 0.3, 1);"></div>
           <div style="position:relative; z-index:1; display:flex; justify-content:space-between; align-items:center;">
               <div>
                  <div style="font-size:10px; color:var(--ink4); font-weight:700; text-transform:uppercase; letter-spacing:0.05em">Paso ${i+1}</div>
                  <div style="font-size:14px; font-weight:700; color:var(--ink);">${sNames[i]}</div>
               </div>
               <div style="text-align:right;">
                  <div style="font-size:18px; font-weight:800; font-family:'JetBrains Mono'; color:${c===0?'var(--ink4)':'var(--ink)'}">${c}</div>
                  <div style="font-size:11px; color:${color}; font-weight:700;">${pct}% del total</div>
               </div>
           </div>
       </div>`;
   }
   funnelHtml += `</div></div>`;

   html += funnelHtml;

   if($('dr-title')) $('dr-title').textContent = title;
   if($('dr-sub')) $('dr-sub').textContent = sub;
   if($('dr-body')) $('dr-body').innerHTML = html;
   if($('dr-foot')) {
       $('dr-foot').innerHTML = `<button class="btn btn-outline" style="width:100%;justify-content:center" id="btn-close-funnel">Cerrar Detalle</button>`;
       $('btn-close-funnel').addEventListener('click', closeDrawer);
   }
   if($('overlay')) $('overlay').classList.add('on');
}

function renderZonas() {
  const TARGET_ZONES = [
    { city: 'Atlixco', name: 'ATL Valle Sur', opsId: '1266' }, { city: 'Atlixco', name: 'ATL Centro', opsId: '1265' },
    { city: 'Cuautla', name: 'Cuautla', opsId: '1212' }, { city: 'Cuernavaca', name: 'CVA-Temixco', opsId: '884' },
    { city: 'Cuernavaca', name: 'CVA-Norte', opsId: '1436' }, { city: 'Cuernavaca', name: 'CVA-Centro', opsId: '880' },
    { city: 'Dolores Hidalgo', name: 'DLH Dolores Hidalgo', opsId: '1271' }, { city: 'Guanajuato', name: 'GUA_SUR', opsId: '1490' },
    { city: 'Guanajuato', name: 'GUA_NORTE', opsId: '1188' }, { city: 'Salamanca', name: 'Salamanca', opsId: '739' },
    { city: 'San Luis Rio Colorado', name: 'San Luis Río Colorado', opsId: '664' }, { city: 'Silao', name: 'SIL Centro', opsId: '1185' },
    { city: 'Texcoco', name: 'Texcoco', opsId: '1312' }, { city: 'Tula De Allende', name: 'TDA San Marcos', opsId: '1239' },
    { city: 'Tula De Allende', name: 'TDA El Llano', opsId: '1238' }, { city: 'Tula De Allende', name: 'TDA Centro', opsId: '1237' },
    { city: 'Tulancingo', name: 'TGO La Rayuela', opsId: '1273' }, { city: 'Tulancingo', name: 'TGO Jaltepec', opsId: '1272' },
    { city: 'Tulancingo', name: 'TGO Centro', opsId: '1274' }
  ];

  const zM = {};
  TARGET_ZONES.forEach(tz => { zM[tz.opsId] = { isTarget: true, city: tz.city, nombre: tz.opsId, nombreDesc: tz.name, total: 0, handoff: 0, interesados: 0, zKey: tz.opsId }; });

  DATA.forEach(r => { 
    let rawZ = r.zona ? r.zona.trim() : 'Unassigned';
    let match = rawZ.match(/\d+/);
    let zKey = match ? match[0] : rawZ; 
    
    if(!zM[zKey]) { zM[zKey] = { isTarget: false, nombre: rawZ, nombreDesc: null, total: 0, handoff: 0, interesados: 0, zKey: zKey }; }
    zM[zKey].total++; 
    if(r.proceso === 'RTS') zM[zKey].handoff++; 
    if(r.resultado === 'Contactado - Interesado') zM[zKey].interesados++; 
  });
  
  Object.keys(zM).forEach(zKey => {
     const zKeyLower = zKey.toLowerCase();
     let zData = ZONAS_DATA[zKeyLower] || ZONAS_DATA['mx'+zKeyLower]; 
     if (zData) { zM[zKey].realLat = zData.lat; zM[zKey].realLng = zData.lng; if(!zM[zKey].nombreDesc) zM[zKey].nombreDesc = zData.name !== zData.id ? zData.name : null; }
  });

  const zs = Object.values(zM).filter(z => z.isTarget || (z.total > 0 && z.nombre !== 'Unassigned')).sort((a, b) => {
     if (a.isTarget && !b.isTarget) return -1;
     if (!a.isTarget && b.isTarget) return 1;
     if (a.isTarget && b.isTarget) return a.city.localeCompare(b.city) || String(a.nombreDesc).localeCompare(String(b.nombreDesc));
     return b.total - a.total;
  });

  if(!zs.length) { if($('zonas-grid')) $('zonas-grid').innerHTML = `<div class="pl-empty" style="grid-column:1/-1">Sin clusters detectados</div>`; return; }
  
  if($('zonas-grid')) {
    $('zonas-grid').innerHTML = zs.map(z => {
      const displayTitle = z.nombreDesc ? `${esc(z.nombreDesc)} (Ops: ${esc(z.nombre)})` : `Ops Zone: ${esc(z.nombre)}`;
      const badge = z.isTarget 
          ? `<span class="chip chip-rts" style="font-size:9px;padding:2px 6px;margin-bottom:6px;background:rgba(34,197,94,0.2);color:var(--green)">Target: ${esc(z.city)}</span>` 
          : `<span class="chip chip-base" style="font-size:9px;padding:2px 6px;margin-bottom:6px;">Zona Orgánica</span>`;
      const opacityStyle = z.isTarget && z.total === 0 ? 'opacity: 0.6;' : '';

      return `<div class="ag-card zona-card" data-zona="${esc(z.zKey)}" style="cursor:pointer; transition: transform 0.2s, box-shadow 0.2s; ${opacityStyle}"><div class="ag-top" style="margin-bottom:12px;align-items:flex-start;"><div class="ag-av" style="background:var(--bg3);border:1px solid var(--ink5);margin-top:4px;"><svg viewBox="0 0 24 24" fill="none" stroke="${z.isTarget ? 'var(--green)' : 'var(--ink2)'}" stroke-width="2" style="width:20px;height:20px"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg></div><div style="min-width:0;display:flex;flex-direction:column;">${badge}<div class="ag-name" style="font-size:15px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis" title="${displayTitle}">${displayTitle}</div><div class="ag-email">${z.total} Gestiones</div></div></div><div class="ag-stats"><div class="ag-stat"><div class="ag-stat-v">${z.interesados}</div><div class="ag-stat-l">Warm Leads</div></div><div class="ag-stat"><div class="ag-stat-v" style="color:var(--purple)">${z.handoff}</div><div class="ag-stat-l">Cierres</div></div><div class="ag-stat"><div class="ag-stat-v" style="color:var(--green)">${z.total > 0 ? Math.round(z.handoff / z.total * 100) : 0}%</div><div class="ag-stat-l">Conv. Rate</div></div></div></div>`;
    }).join('');

    $('zonas-grid').querySelectorAll('.zona-card').forEach(c => {
      c.addEventListener('click', () => openZoneHistory(c.dataset.zona));
    });
  }

  if($('map-container')) {
    if(!window.geoMap) {
      window.geoMap = L.map('map-container').setView([23.6345, -102.5528], 5);
      const isLight = document.documentElement.getAttribute('data-theme') === 'light';
      const tileUrl = isLight ? 'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png' : 'https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png';
      
      window.geoTile = L.tileLayer(tileUrl, {
        attribution: '&copy; OSM contributors &copy; CARTO',
        subdomains: 'abcd',
        maxZoom: 20
      }).addTo(window.geoMap);
      window.geoMarkers = L.layerGroup().addTo(window.geoMap);
    }
    
    const isLight = document.documentElement.getAttribute('data-theme') === 'light';
    const tileUrl = isLight ? 'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png' : 'https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png';
    window.geoTile.setUrl(tileUrl);
    window.geoMarkers.clearLayers();

    const mxCenter = [23.6345, -102.5528];
    let validPoints = [];

    zs.forEach((z) => {
       let lat = mxCenter[0], lng = mxCenter[1];
       if (z.realLat && z.realLng) { lat = z.realLat; lng = z.realLng; validPoints.push([lat, lng]); } 
       else { let hash = 0; for (let j = 0; j < z.nombre.length; j++) { hash = z.nombre.charCodeAt(j) + ((hash << 5) - hash); } lat = mxCenter[0] + ((hash % 100) / 100 - 0.5) * 4; lng = mxCenter[1] + (((hash >> 4) % 100) / 100 - 0.5) * 6; }
       if(z.total === 0 && (!z.realLat || !z.isTarget)) return;

       const rtsPct = z.total > 0 ? Math.round(z.handoff / z.total * 100) : 0;
       const circleColor = z.total === 0 ? '#71717A' : (rtsPct > 15 ? '#22C55E' : rtsPct > 0 ? '#F59E0B' : '#FF441F');
       const displayTitle = z.nombreDesc ? `${esc(z.nombreDesc)} (${esc(z.nombre)})` : `Ops Zone: ${esc(z.nombre)}`;

       L.circleMarker([lat, lng], {
         radius: z.total === 0 ? 8 : Math.min(Math.max(z.total * 0.8, 10), 35),
         fillColor: circleColor, color: circleColor, weight: z.isTarget ? 2 : 1, opacity: 0.9, fillOpacity: z.total === 0 ? 0.2 : 0.35
       }).bindPopup(`<div style="min-width:140px"><strong style="font-size:14px;color:var(--ink)">${displayTitle}</strong><div style="width:100%;height:1px;background:var(--ink5);margin:6px 0"></div><span style="color:var(--ink4)">Gestiones:</span> <strong style="color:var(--ink)">${z.total}</strong><br><span style="color:var(--ink4)">Cierres (RTS):</span> <strong style="color:var(--purple)">${z.handoff}</strong><br><span style="color:var(--ink4)">Conversión:</span> <strong style="color:var(--green)">${rtsPct}%</strong></div>`)
         .addTo(window.geoMarkers);
    });

    if (validPoints.length > 0) { window.geoMap.fitBounds(L.latLngBounds(validPoints).pad(0.1)); }
  }
}

function openZoneHistory(zKey) {
  const zR = DATA.filter(r => {
     let rawZ = r.zona ? r.zona.trim() : 'Unassigned';
     let match = rawZ.match(/\d+/);
     return (match ? match[0] : rawZ) === zKey;
  });
  
  const zNameDesc = ZONAS_DATA[zKey.toLowerCase()] ? ZONAS_DATA[zKey.toLowerCase()].name : `Ops Zone ${zKey}`;
  if($('dr-title')) $('dr-title').textContent = 'Cluster Analytics: ' + zNameDesc; 
  if($('dr-sub')) $('dr-sub').textContent = 'Ops Zone ID: ' + zKey;

  const agMap = {}; let rts = 0, int = 0;
  zR.forEach(r => { if(r.email) agMap[r.email] = (agMap[r.email] || 0) + 1; if(r.proceso === 'RTS') rts++; if(r.resultado === 'Contactado - Interesado') int++; });
  const topAg = Object.entries(agMap).sort((a,b)=>b[1]-a[1]).slice(0,5);

  let html = `<div class="dr-sec"><div class="dr-sec-title">Performance del Cluster</div><div class="dr-grid"><div class="dr-field"><div class="dk">Gestiones Totales</div><div class="dv" style="font-size:18px;font-weight:700">${zR.length}</div></div><div class="dr-field"><div class="dk">Warm Leads</div><div class="dv" style="font-size:18px;font-weight:700;color:var(--amber)">${int}</div></div><div class="dr-field"><div class="dk">Cierres (RTS)</div><div class="dv" style="font-size:18px;font-weight:700;color:var(--purple)">${rts}</div></div><div class="dr-field"><div class="dk">Conv. Rate</div><div class="dv" style="font-size:18px;font-weight:700;color:var(--green)">${zR.length > 0 ? Math.round(rts/zR.length*100) : 0}%</div></div></div></div><div class="dr-sec"><div class="dr-sec-title">Top Agentes en la Zona</div><div style="display:flex;flex-direction:column;gap:8px">${topAg.map(x => `<div style="display:flex;justify-content:space-between;padding:10px;background:var(--bg);border:1px solid var(--ink5);border-radius:var(--r-sm)"><span>${esc(aName(x[0]))}</span><strong style="font-family:'JetBrains Mono'">${x[1]} logs</strong></div>`).join('') || '<div class="muted" style="font-size:13px;padding:12px;background:var(--bg2);border-radius:var(--r-sm);text-align:center;">Sin agentes asignados aún</div>'}</div></div><div class="dr-sec"><div class="dr-sec-title">Últimas Interacciones (LIFO)</div><div class="tbl-wrap" style="box-shadow:none;border:var(--glass-border);background:var(--bg3)"><table style="min-width:100%"><thead><tr><th>Timestamp</th><th>Entity</th><th>Stage</th></tr></thead><tbody>${zR.length ? zR.slice(-10).reverse().map(r => `<tr class="zona-hist-row" data-id="${r.id}" style="cursor:pointer"><td class="muted" style="font-family:'JetBrains Mono'">${esc(r.fecha)}</td><td class="name" style="font-size:12px">${esc(r.restaurante)}<br><span style="font-size:10px;color:var(--ink4);font-weight:normal">${esc(aName(r.email))}</span></td><td>${etapaChip(r.proceso)}</td></tr>`).join('') : '<tr><td colspan="3" style="text-align:center;padding:24px;color:var(--ink4)">No hay registros en esta zona.</td></tr>'}</tbody></table></div></div>`;

  if($('dr-body')) { $('dr-body').innerHTML = html; $('dr-body').querySelectorAll('.zona-hist-row').forEach(tr => { tr.addEventListener('click', () => openDrawer(+tr.dataset.id)); }); }
  if($('dr-foot')) { $('dr-foot').innerHTML = `<button class="btn btn-outline" style="width:100%;justify-content:center" id="btn-close-hist">Cerrar Analytics</button>`; const btn = $('dr-foot').querySelector('#btn-close-hist'); if(btn) btn.addEventListener('click', closeDrawer); }
  if($('overlay')) $('overlay').classList.add('on');
}

let aHistChart = null;
function openAgentHistory(e) {
  const aR = DATA.filter(r => r.email === e); if(!aR.length) return;
  if($('dr-title')) $('dr-title').textContent = 'Entity Log: ' + aName(e); if($('dr-sub')) $('dr-sub').textContent = 'UID: ' + e;
  const hM = {}; aR.forEach(r => { const d = parseDateStr(r.fecha); if(d) { const k = String(d.getDate()).padStart(2, '0') + '/' + String(d.getMonth() + 1).padStart(2, '0'); if(!hM[k]) hM[k] = { g: 0, rts: 0 }; hM[k].g++; if(r.proceso === 'RTS') hM[k].rts++; } });
  const sd = Object.keys(hM).sort((a, b) => { const [da, ma] = a.split('/'), [db, mb] = b.split('/'); return new Date(2000, +ma - 1, +da) - new Date(2000, +mb - 1, +db); });
  
  if($('dr-body')) $('dr-body').innerHTML = `<div class="dr-sec"><div class="dr-sec-title">Rendimiento Temporal</div><div style="height:260px;position:relative;width:100%;background:var(--bg3);border-radius:var(--r-md);padding:16px;border:var(--glass-border)"><canvas id="agentHistoryChart"></canvas></div></div><div class="dr-sec"><div class="dr-sec-title">Últimas Interacciones (LIFO)</div><div class="tbl-wrap" style="box-shadow:none;border:var(--glass-border);background:var(--bg3)"><table style="min-width:100%"><thead><tr><th>Timestamp</th><th>Entity</th><th>Stage</th></tr></thead><tbody>${aR.slice(-5).reverse().map(r => `<tr data-id="${r.id}"><td class="muted" style="font-family:'JetBrains Mono'">${esc(r.fecha)}</td><td class="name" style="font-size:12px">${esc(r.restaurante)}</td><td>${etapaChip(r.proceso)}</td></tr>`).join('')}</tbody></table></div></div><div class="dr-sec"><button class="btn btn-primary" id="btn-ver-all-agent" data-email="${esc(e)}" style="width:100%;justify-content:center;background:var(--ink);color:var(--bg)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" style="width:16px;height:16px"><path d="M14 2H6a2 2 0 00-2 2v16a2 2 0 002 2h12a2 2 0 002-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>Extrapolar toda la Data</button></div>`;
  if($('dr-foot')) { $('dr-foot').innerHTML = `<button class="btn btn-outline" style="width:100%;justify-content:center" id="btn-close-hist">Terminar Sesión</button>`; const btn = $('dr-foot').querySelector('#btn-close-hist'); if(btn) btn.addEventListener('click', closeDrawer); }
  const btnVA = $('dr-body') ? $('dr-body').querySelector('#btn-ver-all-agent') : null; if(btnVA) btnVA.addEventListener('click', () => { closeDrawer(); filterAgent(btnVA.dataset.email); });
  if($('dr-body')) $('dr-body').querySelectorAll('tr[data-id]').forEach(tr => tr.addEventListener('click', () => openDrawer(+tr.dataset.id)));
  if($('overlay')) $('overlay').classList.add('on');
  
  setTimeout(() => {
    if(aHistChart) { aHistChart.destroy(); aHistChart = null; } const cv = $('agentHistoryChart'); if(!cv) return; Chart.defaults.color = '#A1A1AA';
    aHistChart = new Chart(cv, { type: 'line', data: { labels: sd, datasets: [ { label: 'Volumen Output', data: sd.map(d => hM[d].g), borderColor: '#3B82F6', backgroundColor: 'rgba(59,130,246,0.1)', fill: true, tension: 0.4, pointRadius: 2 }, { label: 'RTS (Cierres)', data: sd.map(d => hM[d].rts), borderColor: '#22C55E', backgroundColor: 'rgba(34,197,94,0.1)', fill: true, tension: 0.4, pointRadius: 3 } ] }, options: { maintainAspectRatio: false, plugins: { legend: { position: 'bottom', labels: { boxWidth: 12, font: { size: 10 } } }, tooltip: { mode: 'index', intersect: false } }, scales: { y: { beginAtZero: true, ticks: { stepSize: 1, precision: 0 } }, x: { grid: { display: false } } } } });
  }, 50);
}

function openDrawer(id) {
  const r = DATA.find(x => x.id === id); if(!r) return;
  if($('dr-title')) $('dr-title').textContent = r.restaurante; if($('dr-sub')) $('dr-sub').innerHTML = etapaChip(r.proceso) + '&nbsp;&nbsp;' + resChip(r.resultado);
  if($('dr-body')) $('dr-body').innerHTML = `<div class="dr-sec"><div class="dr-sec-title">Core Entity Data</div><div class="dr-grid"><div class="dr-field"><div class="dk">Telecom</div><div class="dv mono">${esc(r.tel)||'NULL'}</div></div><div class="dr-field"><div class="dk">Merchant ID</div><div class="dv mono">${esc(r.brand)||'NULL'}</div></div><div class="dr-field dr-full"><div class="dk">Designación</div><div class="dv" style="font-size:18px;font-weight:700">${esc(r.restaurante)}</div></div></div></div><div class="dr-sec"><div class="dr-sec-title">Log de Operación</div><div class="dr-grid"><div class="dr-field"><div class="dk">Timestamp (Date)</div><div class="dv mono">${esc(r.fecha)||'NULL'}</div></div><div class="dr-field"><div class="dk">Timestamp (Time)</div><div class="dv mono">${esc(r.hora)||'NULL'}</div></div><div class="dr-field"><div class="dk">Stage Actual</div><div class="dv">${etapaChip(r.proceso)}</div></div><div class="dr-field"><div class="dk">Disposition</div><div class="dv">${resChip(r.resultado)}</div></div><div class="dr-field dr-full"><div class="dk">Notas y Comentarios</div><div class="dr-comment">${esc(r.comentario)||'System: No comments provided.'}</div></div></div></div><div class="dr-sec"><div class="dr-sec-title">Autorización / Asignación</div><div class="dr-grid"><div class="dr-field"><div class="dk">Alias User</div><div class="dv">${esc(aName(r.email))}</div></div><div class="dr-field"><div class="dk">Key (Email)</div><div class="dv mono" style="font-size:11px">${esc(r.email)||'NULL'}</div></div><div class="dr-field"><div class="dk">Agent ID</div><div class="dv mono">${esc(r.agent)||'NULL'}</div></div></div></div><div class="dr-sec"><div class="dr-sec-title">State Mutation</div><div class="field-g"><label>Update Pipeline Stage</label><select id="edit-etapa" style="font-family:'Space Grotesk'">${['PROSPECTO','ED','DM','FIRMA CONTRATO','DC','DATA COLECCTION / SOB','RTS'].map(e=>`<option${r.proceso===e?' selected':''}>${e}</option>`).join('')}</select></div><div class="field-g"><label>Append al Log</label><textarea id="edit-com" placeholder="Ingrese información a concatenar en el historial..." maxlength="500"></textarea></div></div>`;
  if($('dr-foot')) { $('dr-foot').innerHTML = `<button class="btn btn-primary" id="btn-save-edit" data-id="${id}" style="flex:1;justify-content:center;box-shadow:0 0 15px rgba(255,68,31,0.3)"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="20 6 9 17 4 12"/></svg>Push to Database</button><button class="btn btn-outline" id="btn-close-drawer">Abort</button>`; const btnS=$('btn-save-edit'), btnC=$('btn-close-drawer'); if(btnS) btnS.addEventListener('click', () => saveEdit(+btnS.dataset.id)); if(btnC) btnC.addEventListener('click', closeDrawer); }
  if($('overlay')) $('overlay').classList.add('on');
}

function saveEdit(id) {
  const r = DATA.find(x => x.id === id); if(!r) return;
  const ne = $('edit-etapa') ? $('edit-etapa').value : null, nc = $('edit-com') ? $('edit-com').value.trim() : null;
  let nC = r.comentario; if (nc) nC = nc + ' [' + new Date().toLocaleDateString('es-MX') + '] — ' + r.comentario;
  const b = $('btn-save-edit'); if(!b) return;
  const oH = b.innerHTML; b.innerHTML = `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" style="animation:spin 1s linear infinite"><path d="M21 12a9 9 0 1 1-6.219-8.56"/></svg>Uploading...`; b.disabled = true;
  fetch(CONFIG.SCRIPT_URL, {method:'POST',body:JSON.stringify({action:'update',ts_match:r.ts,restaurante_match:r.restaurante,proceso:ne||r.proceso,comentario:nC})}).then(res=>res.json()).then(d=>{b.innerHTML=oH; b.disabled=false; if(d.status==='success'){if(ne)r.proceso=ne; if(nc)r.comentario=nC; closeDrawer(); renderAll(); toast('Payload consolidado', 'ok');} else toast(`Sync Error: ${d.message}`, 'er');}).catch(e=>{b.innerHTML=oH; b.disabled=false; toast('Endpoint Connection Failed', 'er');});
}

function closeDrawer() { if($('overlay')) $('overlay').classList.remove('on'); }

function submitForm() {
  const n=$('n-nom')?$('n-nom').value.trim():'', a=$('n-ag')?$('n-ag').value.trim():'', rs=$('n-res')?$('n-res').value:'', na=$('n-alert');
  const sE = m => {if(na){na.style.display='flex';na.className='alert a-err';na.innerHTML=`<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg><span>${esc(m)}</span>`;}};
  if(!n||!a||!rs) return sE('Validation failed: Missing fields.'); if(!a.endsWith('@rappi.com')) return sE('Security Policy: Only @rappi.com allowed.');
  const idR=$('n-id')?$('n-id').value.trim():''; if(idR&&!idR.startsWith('MX')) return sE('Syntax warning: ID must start with MX');
  const nw=new Date(), fS=nw.toLocaleDateString('es-MX'), hS=nw.toLocaleTimeString('es-MX',{hour:'2-digit',minute:'2-digit'}), tS=nw.toLocaleString('es-MX');
  const rC=$('n-com')?$('n-com').value.trim():'', fC=rC?`${rC} | Res: ${rs}`:`System Status: ${rs}`;
  const pl={action:"insert",ts:tS,restaurante:n,tel:$('n-tel')?$('n-tel').value.trim():'',proceso:$('n-etapa')?$('n-etapa').value:'',email:a,comentario:fC,brand:idR,fecha:fS,hora:hS,zona:$('n-zona')?$('n-zona').value.trim()||'Sin Zona':'Sin Zona',agent:''};
  const b=$('n-btn'); if(!b) return; const oH=b.innerHTML; b.innerHTML=`<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" style="animation:spin 1s linear infinite"><path d="M21 12a9 9 0 1 1-6.219-8.56"/></svg>Committing...`; b.disabled=true;
  fetch(CONFIG.SCRIPT_URL,{method:'POST',body:JSON.stringify(pl)}).then(r=>r.json()).then(d=>{b.innerHTML=oH; b.disabled=false; if(d.status==="success"){if(na){na.style.display='flex';na.className='alert a-ok';na.innerHTML=`<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="20 6 9 17 4 12"/></svg><span>Entity added!</span>`;} DATA.push({...pl,id:DATA.length,resultado:rs}); renderAll(); toast('Registro sincronizado', 'ok'); setTimeout(()=>{clearForm();if(na)na.style.display='none';go('registros');},2000);}else sE("Database Reject: "+d.message);}).catch(e=>{b.innerHTML=oH;b.disabled=false;sE("Network Error.");});
}

function clearForm() { ['n-nom','n-tel','n-zona','n-id','n-ag','n-com','n-link','n-fseg','n-hseg'].forEach(id=>{const e=$(id);if(e)e.value='';}); if($('n-etapa')) $('n-etapa').value='PROSPECTO'; if($('n-res')) $('n-res').value=''; if($('n-alert')) $('n-alert').style.display='none'; }

const TIERS = [ {l:'< 80%',min:0,max:79,po:0,pc:0,in:0}, {l:'80%-85%',min:80,max:85,po:447413,pc:73,in:447413}, {l:'86% - 89%',min:86,max:89,po:475376,pc:78,in:27963}, {l:'90% - 94%',min:90,max:94,po:521982,pc:86,in:46606}, {l:'95%-99%',min:95,max:99,po:559266,pc:92,in:37284}, {l:'100%',min:100,max:104,po:610000,pc:100,in:50734}, {l:'105%',min:105,max:109,po:697618,pc:114,in:87618}, {l:'110%',min:110,max:114,po:785237,pc:129,in:87618}, {l:'115%',min:115,max:119,po:872855,pc:143,in:87618}, {l:'120%',min:120,max:124,po:960473,pc:157,in:87618}, {l:'125%',min:125,max:129,po:1048092,pc:172,in:87618}, {l:'130%',min:130,max:134,po:1099358,pc:180,in:51266}, {l:'135%',min:135,max:139,po:1150624,pc:189,in:51266}, {l:'140%',min:140,max:144,po:1192569,pc:196,in:41945}, {l:'>=145%',min:145,max:9999,po:1220000,pc:200,in:27431} ];
const fmtDinero=n=>'$'+n.toLocaleString('en-US');
function calcComisionObj(h,m){ if(m<=0) return {...TIERS[0],cAtt:0}; const a=Math.floor((h/m)*100), t=TIERS.find(x=>a>=x.min&&a<=x.max)||TIERS[0]; return {...t,cAtt:a}; }
function initCalc(){ if($('tier-body')) $('tier-body').innerHTML=TIERS.map((t,i)=>`<div class="tier-row" id="tr-${i}"><div>${t.l}</div><div>${t.pc}%</div><div class="t-val" style="font-weight:700">${fmtDinero(t.po)}</div><div>${t.in===0?'':'+'+fmtDinero(t.in)}</div></div>`).join(''); runCalc(); }
function runCalc(){ const m=$('calc-meta')?(parseInt($('calc-meta').value)||20):20, hf=$('calc-handoffs')?(parseInt($('calc-handoffs').value)||0):0, rs=calcComisionObj(hf,m); if($('calc-pago')) $('calc-pago').textContent=fmtDinero(rs.po); if($('calc-att')) $('calc-att').textContent=rs.cAtt+'%'; if($('calc-sub')) $('calc-sub').textContent='Algorithm Payout: '+rs.pc+'%'; document.querySelectorAll('.tier-row').forEach(e=>e.classList.remove('active')); const idx=TIERS.findIndex(t=>rs.cAtt>=t.min&&rs.cAtt<=t.max); if(idx!==-1&&$('tr-'+idx)) $('tr-'+idx).classList.add('active'); }

function renderIndicadores(){ 
  const mG=$('global-meta')?(parseInt($('global-meta').value)||20):20, mp={}; 
  getUnifiedAgentList().forEach(a => { mp[a.val] = { e: a.val, label: a.label, a: 0, i: 0, h: 0 }; });
  DATA.forEach(r=>{const k=r.email; if(!k || !mp[k]) return; mp[k].a++; if(r.resultado==='Contactado - Interesado') mp[k].i++; if(r.proceso==='RTS') mp[k].h++;}); 
  const ar=Object.values(mp).sort((a,b)=>b.h-a.h); 
  if($('ind-tbody')){ 
    $('ind-tbody').innerHTML=ar.map(a=>{const st=getAgentStats(a.e)||{}, mA=st.meta||mG, aR=st.rts!==undefined?st.rts:a.h, c=calcComisionObj(aR,mA), at=st.cm!==undefined?st.cm:c.cAtt, col=at>=100?'var(--green)':at>=80?'var(--amber)':'var(--red)'; return `<tr data-email="${esc(a.e)}"><td class="name">${esc(a.label)}</td><td style="text-align:center;font-family:'JetBrains Mono'">${a.a}</td><td style="text-align:center;font-family:'JetBrains Mono'">${a.i}</td><td style="text-align:center;font-weight:700;color:var(--purple);font-family:'JetBrains Mono';font-size:16px">${aR}</td><td style="text-align:center"><span style="color:${col};font-weight:700;font-family:'Space Grotesk';font-size:16px">${at}%</span><br><span style="font-size:10px;color:var(--ink4);font-family:'JetBrains Mono'">(Target: ${mA})</span></td><td style="text-align:right;font-weight:700;color:var(--ink);font-family:'JetBrains Mono'">${fmtDinero(c.po)}</td></tr>`;}).join(''); 
    $('ind-tbody').querySelectorAll('tr').forEach(tr=>tr.addEventListener('click',()=>{go('calculadora'); setTimeout(()=>{if($('calc-agent-sel')) $('calc-agent-sel').value=tr.dataset.email; applyAgentToCalc();},50);})); 
  } 
}

function fillCalcAgents(){ 
  const ag=getUnifiedAgentList(); const s=$('calc-agent-sel'); 
  if(s) {
     s.innerHTML=`<option value="">Awaiting Profile ID...</option>`+ag.map(a=>`<option value="${a.val}">${esc(a.label)}</option>`).join(''); 
     if(!IS_ADMIN() && ag.length===1) { s.value = ag[0].val; s.disabled = true; applyAgentToCalc(); }
  }
}
function applyAgentToCalc(){ const e=$('calc-agent-sel')?$('calc-agent-sel').value:''; if(!e){ if($('calc-meta')) $('calc-meta').value=0; if($('calc-handoffs')) $('calc-handoffs').value=0; runCalc(); return; } const st=getAgentStats(e)||{}, mG=$('global-meta')?(parseInt($('global-meta').value)||20):20; if($('calc-meta')) $('calc-meta').value=st.meta||mG; let rts=st.rts!==undefined?st.rts:DATA.filter(r=>r.email===e&&r.proceso==='RTS').length; if($('calc-handoffs')) $('calc-handoffs').value=rts; runCalc(); toast('Configuración inyectada', 'ok'); }

function initTardanzas(){ renderTardanzas(); }
function getMarioHeartSVG(iE){ const c=iE?"mario-heart empty":"mario-heart"; return `<svg class="${c}" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg"><path fill="#0A0A0A" d="M3,2h2v1h-2z M11,2h2v1h-2z M2,3h1v1h-1z M5,3h1v1h-1z M10,3h1v1h-1z M13,3h1v1h-1z M1,4h1v2h-1z M14,4h1v2h-1z M1,6h1v2h-1z M14,6h1v2h-1z M2,8h1v2h-1z M13,8h1v2h-1z M3,10h1v2h-1z M12,10h1v2h-1z M4,12h1v1h-1z M11,12h1v1h-1z M5,13h1v1h-1z M10,13h1v1h-1z M6,14h4v1h-4z"/><path fill="#E52521" d="M3,3h2v1h-2z M11,3h2v1h-2z M2,4h3v1h-3z M11,4h3v1h-3z M2,5h12v1h-12z M2,6h12v1h-12z M2,7h12v1h-12z M3,8h10v1h-10z M3,9h10v1h-10z M4,10h8v1h-8z M4,11h8v1h-8z M5,12h6v1h-6z M6,13h4v1h-4z"/><path fill="#FFFFFF" d="M3,3h1v1h-1z M3,4h1v1h-1z M4,4h1v1h-1z"/></svg>`; }

function renderTardanzas(){
    const tbody = $('tar-tbody');
    if(!tbody) return;

    const nw = new Date(), yr = nw.getFullYear(), m = nw.getMonth();
    const prefixMonth = `${yr}-${String(m+1).padStart(2,'0')}`;

    const agents = getUnifiedAgentList();
    
    if (agents.length === 0) {
        tbody.innerHTML = `<tr><td colspan="7"><div class="empty"><h3>Directorio Vacío</h3></div></td></tr>`;
        return;
    }

    tbody.innerHTML = agents.map((a, i) => {
        const cleanId = a.cleanId;
        const allPenalties = TARDANZAS_DATA[cleanId] || {};
        const monthPenalties = Object.keys(allPenalties).filter(d => d.startsWith(prefixMonth));
        
        let cLate = 0, cEarly = 0, cOther = 0;
        monthPenalties.forEach(d => {
            if(allPenalties[d].lateIn) cLate++;
            if(allPenalties[d].earlyOut) cEarly++;
            if(allPenalties[d].other) cOther++;
        });

        const pCount = monthPenalties.length; // Días totales con alguna penalización
        const lives = Math.max(0, 3 - pCount);

        let statusHtml = '';
        if(lives === 3) statusHtml = `<span class="chip chip-rts" style="box-shadow:0 0 10px rgba(34,197,94,0.2)">Optimum</span>`;
        else if(lives === 2) statusHtml = `<span class="chip chip-r2s" style="box-shadow:0 0 10px rgba(245,158,11,0.2)">Warning</span>`;
        else if(lives === 1) statusHtml = `<span class="chip" style="background:rgba(194,65,12,0.15);color:#FB923C;border-color:rgba(194,65,12,0.3);box-shadow:0 0 10px rgba(194,65,12,0.2)">Critical</span>`;
        else statusHtml = `<span class="chip chip-err" style="box-shadow:0 0 10px rgba(239,68,68,0.2)">Terminated</span>`;

        let heartsHtml = '';
        for(let k=0; k<3; k++) {
            heartsHtml += `<svg style="width:16px;height:16px;margin:0 2px;filter:${k>=lives?'grayscale(1) opacity(0.3)':'drop-shadow(0 0 4px rgba(229,37,33,0.5))'}" viewBox="0 0 16 16"><path fill="#0A0A0A" d="M3,2h2v1h-2z M11,2h2v1h-2z M2,3h1v1h-1z M5,3h1v1h-1z M10,3h1v1h-1z M13,3h1v1h-1z M1,4h1v2h-1z M14,4h1v2h-1z M1,6h1v2h-1z M14,6h1v2h-1z M2,8h1v2h-1z M13,8h1v2h-1z M3,10h1v2h-1z M12,10h1v2h-1z M4,12h1v1h-1z M11,12h1v1h-1z M5,13h1v1h-1z M10,13h1v1h-1z M6,14h4v1h-4z"/><path fill="#E52521" d="M3,3h2v1h-2z M11,3h2v1h-2z M2,4h3v1h-3z M11,4h3v1h-3z M2,5h12v1h-12z M2,6h12v1h-12z M2,7h12v1h-12z M3,8h10v1h-10z M3,9h10v1h-10z M4,10h8v1h-8z M4,11h8v1h-8z M5,12h6v1h-6z M6,13h4v1h-4z"/><path fill="#FFFFFF" d="M3,3h1v1h-1z M3,4h1v1h-1z M4,4h1v1h-1z"/></svg>`;
        }

        const avatarBg = AV_COLORS[i % AV_COLORS.length];
        const initials = a.label.split(' ').map(w => w[0] || '').join('').substring(0,2).toUpperCase();

        return `<tr data-cleanid="${cleanId}">
            <td>
                <div style="display:flex;align-items:center;gap:14px">
                    <div style="width:32px;height:32px;border-radius:8px;background:${avatarBg};color:#fff;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:11px;flex-shrink:0">${initials}</div>
                    <div>
                        <div style="font-weight:600;color:var(--ink);font-size:14px">${esc(a.label)}</div>
                        <div style="font-size:10px;color:var(--ink4);font-family:'JetBrains Mono'">${esc(a.val)}</div>
                    </div>
                </div>
            </td>
            <td style="text-align:center;font-family:'JetBrains Mono';font-weight:800;font-size:16px;color:${cLate>0?'var(--amber)':'var(--ink)'}">${cLate}</td>
            <td style="text-align:center;font-family:'JetBrains Mono';font-weight:800;font-size:16px;color:${cEarly>0?'var(--amber)':'var(--ink)'}">${cEarly}</td>
            <td style="text-align:center;font-family:'JetBrains Mono';font-weight:800;font-size:16px;color:${cOther>0?'var(--red)':'var(--ink)'}">${cOther}</td>
            <td style="text-align:center;">${heartsHtml}</td>
            <td style="text-align:center;">${statusHtml}</td>
            <td style="text-align:center;"><button class="btn btn-sm btn-outline btn-tar-detail" data-id="${cleanId}" style="font-size:10px; padding:6px 12px; border-radius:20px;">Ver Detalle</button></td>
        </tr>`;
    }).join('');

    tbody.querySelectorAll('.btn-tar-detail').forEach(btn => {
        btn.addEventListener('click', (e) => {
            e.stopPropagation();
            openTardanzaDrawer(btn.dataset.id);
        });
    });
}

function openTardanzaDrawer(cleanId) {
    const agent = getUnifiedAgentList().find(a => a.cleanId === cleanId);
    if(!agent) return;

    const allPenalties = TARDANZAS_DATA[cleanId] || {};
    const nw = new Date(), yr = nw.getFullYear(), m = nw.getMonth();
    const prefixMonth = `${yr}-${String(m+1).padStart(2,'0')}`;
    const monthPenalties = Object.keys(allPenalties).filter(d => d.startsWith(prefixMonth));
    
    const pCount = monthPenalties.length;
    const lives = Math.max(0, 3 - pCount);

    let hH = '';
    for(let i=0; i<3; i++) hH += getMarioHeartSVG(i >= lives);

    const ms=["Enero","Febrero","Marzo","Abril","Mayo","Junio","Julio","Agosto","Septiembre","Octubre","Noviembre","Diciembre"];

    let html = `
    <div class="dr-sec">
        <div class="dr-sec-title">Estado de Vidas (${ms[m]} ${yr})</div>
        <div style="display:flex; flex-direction:column; align-items:center; background:var(--bg3); padding:24px; border-radius:var(--r-md); border:var(--glass-border);">
            <div class="hearts-container" style="margin:0 0 16px 0;">${hH}</div>
            <div style="font-weight:700; font-size:16px; color:${lives>0?'var(--ink)':'var(--red)'}">${lives} Vidas Restantes</div>
        </div>
    </div>
    <div class="dr-sec">
        <div class="dr-sec-title">Historial Detallado de Faltas y Retardos</div>
        <div class="tbl-wrap" style="box-shadow:none;border:var(--glass-border);background:var(--bg3)">
            <table style="min-width:100%">
                <thead><tr><th>Fecha / Tracker</th><th>Motivo y Hora</th></tr></thead>
                <tbody>
    `;

    const sortedDates = Object.keys(allPenalties).sort((a,b) => new Date(b) - new Date(a));

    if(sortedDates.length === 0) {
        html += `<tr><td colspan="2" style="text-align:center;padding:32px;color:var(--ink4)">Asistencia perfecta.<br>No hay registros de penalización.</td></tr>`;
    } else {
        html += sortedDates.map(d => {
            const isCurrentMonth = d.startsWith(prefixMonth);
            const badge = isCurrentMonth ? `<span class="chip chip-err" style="font-size:9px;padding:2px 6px;margin-left:8px;">Mes Actual</span>` : '';
            return `<tr>
                <td class="mono" style="color:var(--ink2); font-size:13px;">${esc(d)}${badge}</td>
                <td style="color:var(--red);font-weight:700;font-size:13px;">${esc(allPenalties[d].reasons.join(' | '))}</td>
            </tr>`;
        }).join('');
    }

    html += `</tbody></table></div></div>`;

    if($('dr-title')) $('dr-title').textContent = "Asistencia: " + agent.label;
    if($('dr-sub')) $('dr-sub').textContent = agent.val;
    if($('dr-body')) $('dr-body').innerHTML = html;
    if($('dr-foot')) {
        $('dr-foot').innerHTML = `<button class="btn btn-outline" style="width:100%;justify-content:center" id="btn-close-tar">Cerrar Detalle</button>`;
        $('btn-close-tar').addEventListener('click', closeDrawer);
    }
    if($('overlay')) $('overlay').classList.add('on');
}

// DOCS UPLOAD
function fillDocAgents() { 
  const ag=getUnifiedAgentList(); const s=$('doc-agent-sel'); 
  if(s) {
     s.innerHTML=`<option value="">Awaiting Input...</option>`+ag.map(a=>`<option value="${a.val}">${esc(a.label)}</option>`).join(''); 
     if(!IS_ADMIN() && ag.length===1) { s.value = ag[0].val; s.disabled = true; }
  }
}
function handleFilesSelection(e) { const nf=Array.from(e.target.files); if(!nf.length) return; DOCS_QUEUE=DOCS_QUEUE.concat(nf); renderDocsQueue(); if($('doc-files-input')) $('doc-files-input').value=""; if($('doc-folder-input')) $('doc-folder-input').value=""; }
function renderDocsQueue() { const q=$('doc-queue'); if(!q) return; if(DOCS_QUEUE.length===0){ q.innerHTML=`<div style="text-align:center;padding:24px;color:var(--ink4);border:1px dashed var(--ink5);border-radius:var(--r-sm);background:var(--bg3);">No hay archivos en la cola.</div>`; return; } q.innerHTML=DOCS_QUEUE.map((f,i)=>`<div class="doc-item" id="doc-item-${i}"><div style="display:flex;align-items:center;gap:12px;overflow:hidden"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M13 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V9z"/><polyline points="13 2 13 9 20 9"/></svg><span style="white-space:nowrap;overflow:hidden;text-overflow:ellipsis" title="${esc(f.webkitRelativePath||f.name)}">${esc(f.webkitRelativePath||f.name)}</span></div><div style="color:var(--ink4);font-size:11px">${(f.size/1024/1024).toFixed(2)} MB</div></div>`).join(''); }
function fileToBase64(f) { return new Promise((rs,rj)=>{const r=new FileReader(); r.onload=()=>rs(r.result.split(',')[1]); r.onerror=e=>rj(e); r.readAsDataURL(f);}); }

// RAPPI MENU AI FUNCTIONS
function runTimer() {
    const diff = Date.now() - missionStart;
    const h = Math.floor(diff / 3600000).toString().padStart(2, '0');
    const m = Math.floor((diff % 3600000) / 60000).toString().padStart(2, '0');
    const s = Math.floor((diff % 60000) / 1000).toString().padStart(2, '0');
    const formatted = `${h}:${m}:${s}`;
    const tEl = $('ai-timer'); if(tEl) tEl.innerText = formatted;
    return formatted;
}

async function fetchWithRetry(url, options, retries = 5, delay = 1000) {
    for (let i = 0; i < retries; i++) {
        try {
            const response = await fetch(url, options);
            if (response.ok) return await response.json();
            if (response.status !== 429 && response.status !== 503) break;
        } catch (e) { if (i === retries - 1) throw e; }
        await new Promise(res => setTimeout(res, delay));
        delay *= 2;
    }
    return null;
}

async function handleAIFiles(files) {
    const restName = $('ai-rest-name')?.value; 
    if(!restName) { toast("Escribe el nombre del restaurante", "er"); return; } 
    if(!files[0]) return;

    $('ai-upload-sec').style.display = 'none'; 
    $('ai-loading-sec').style.display = 'block'; 
    
    missionStart = Date.now();
    timerInterval = setInterval(runTimer, 1000);

    const reader = new FileReader();
    reader.onload = async (evt) => {
        const base64Data = evt.target.result.split(',')[1];
        try {
            updateAIProgress(10, "Auditoría de datos iniciada...");
            const data = await analyzeIA(base64Data, files[0].type);
            if (data) {
                menuData = data; 
                const items = [...(menuData.platos || []), ...(menuData.bebidas || [])];
                for (let i = 0; i < items.length; i++) {
                    const name = items[i].nombre || 'Producto';
                    updateAIProgress(15 + (i/items.length * 85), `Texturizando Sony A7R V: ${name}...`);
                    items[i].proImg = await generateSonyPhoto(items[i]);
                }
                const finalTime = runTimer();
                updateAIProgress(100, "Misión Completada.");
                clearInterval(timerInterval);
                
                $('ai-final-name').innerText = restName.toUpperCase();
                $('ai-final-time').innerText = finalTime;

                setTimeout(() => { 
                    renderAITable(); 
                    $('ai-loading-sec').style.display = 'none'; 
                    $('ai-results-sec').style.display = 'block'; 
                }, 1000);
            }
        } catch (err) {
            clearInterval(timerInterval);
            $('ai-loading-sec').style.display = 'none';
            $('ai-upload-sec').style.display = 'block';
            toast("FALLO EN ESCANEO: " + err.message, "er");
        }
    };
    reader.readAsDataURL(files[0]);
}

function updateAIProgress(val, text) { 
    const b = $('ai-bar'); 
    const p = $('ai-perc'); 
    const s = $('ai-status'); 
    if(b) b.style.width = val + "%"; 
    if(p) p.innerText = Math.round(val) + "%"; 
    if(s) s.innerText = text; 
}

async function analyzeIA(base64, mime) {
    const url = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
    const systemPrompt = `Actúa como un experto en digitalización de menús de Rappi Pro. 
    OBJETIVO: Transcripción literal 1:1 con MARGEN DE ERROR 0%.
    REGLAS DE ORO:
    1. FIDELIDAD: Transcribe nombres y precios LETRA POR LETRA y NÚMERO POR NÚMERO.
    2. NO HALLUCINATIONS: No inventes ingredientes, no cambies precios, no añadidas adjetivos.
    3. LONGITUD: 
       - Corredor: max 3 palabras.
       - Nombre: max 5 palabras.
       - Descripción: max 40 palabras.
    4. CAMPOS VACÍOS: Si algo no es visible o no existe, usa "N/A".
    JSON SCHEMA: { "platos": [{"nombre": "", "nombre_en": "", "desc": "", "desc_en": "", "precio": 0, "corredor": "", "elecciones": "N/A", "agregar": "N/A", "quitar": "N/A"}], "bebidas": [...] }`;
    
    const payload = {
        contents: [{ parts: [{ text: "Extraer menú como JSON literal siguiendo reglas de fidelidad absoluta." }, { inlineData: { mimeType: mime || "image/png", data: base64 } }] }],
        systemInstruction: { parts: [{ text: systemPrompt }] },
        generationConfig: { responseMimeType: "application/json" }
    };
    
    const json = await fetchWithRetry(url, { method: 'POST', headers: { 'Content-Type': 'application/json' }, body: JSON.stringify(payload) });
    if (json && json.candidates?.[0]?.content?.parts?.[0]?.text) {
        return JSON.parse(json.candidates[0].content.parts[0].text);
    }
    throw new Error("Respuesta inválida del motor.");
}

async function generateSonyPhoto(item) {
    const prodEN = item.nombre_en || item.nombre || "Gourmet dish";
    const isDrink = item.tipo === "BEBIDA" || item.corredor === "BEBIDAS";
    const url = `https://generativelanguage.googleapis.com/v1beta/models/imagen-4.0-generate-001:predict?key=${apiKey}`;
    let promptText = isDrink ? `Packshot of ${prodEN}. Sony A7R V.` : `Realistic gourmet ${prodEN}. Sony A7R V.`;
    try {
        const res = await fetch(url, { method: 'POST', body: JSON.stringify({ instances: [{ prompt: promptText }], parameters: { sampleCount: 1 } }) });
        const json = await res.json(); return json?.predictions?.[0]?.bytesBase64Encoded || null;
    } catch (e) { return null; }
}

function renderAITable() {
    let h = "";
    const b = (it, isB = false) => it.forEach(i => {
        const description = i.desc || i.descripcion || "N/A";
        const cat = isB ? 'BEBIDAS' : (i.corredor || 'GENERAL');
        h += `<tr>
            <td style="text-align:center;font-weight:700;color:var(--ink4);text-transform:uppercase;">${cat}</td>
            <td style="text-align:center;font-weight:700;color:var(--r);font-style:italic;">${i.nombre || "Sin nombre"}</td>
            <td style="text-align:center;font-size:12px;color:var(--ink3);font-style:italic;">${description}</td>
            <td style="text-align:center;font-weight:700;color:var(--ink);font-family:'JetBrains Mono';">$${(i.precio||0).toLocaleString()}</td>
            <td style="text-align:center;font-size:10px;color:var(--ink4);text-transform:uppercase;">${i.elecciones||'N/A'}</td>
            <td style="text-align:center;font-size:10px;color:var(--ink4);text-transform:uppercase;">${i.agregar||'N/A'}</td>
            <td style="text-align:center;font-size:10px;color:var(--ink4);text-transform:uppercase;">${i.quitar||'N/A'}</td>
        </tr>`;
    });
    b(menuData.platos||[]); b(menuData.bebidas||[], true);
    $('ai-table-body').innerHTML = h;
}

// DICCIONARIO DE CREDENCIALES
const AUTH_USERS = {
  "santiago.saenz@rappi.com": "1013685546",
  "luz.torres@rappi.com": "38070266",
  "claudia.casallas@rappi.com": "1077144465",
  "sorangine.giron@rappi.com": "1022975060",
  "leonardo.h@rappi.com": "1019101528",
  "fernanda.sanchez@rappi.com": "1014283478",
  "nicoll.ruiz@rappi.com": "1233497697",
  "jose.colorado@rappi.com": "1000077110",
  "julian.sarmiento@rappi.com": "1000518136",
  "karen.duarte@rappi.com": "1001217284",
  "michael.palacios@rappi.com": "1000124818",
  "valentina.leon@rappi.com": "1001092794",
  "leslie.garcia@rappi.com": "1030695604",
  "yeimi.vargas@rappi.com": "1000377427",
  "hector.nino@rappi.com": "1070953363",
  "jessica.marin@rappi.com": "1031179802",
  "jairo.castillo@rappi.com": "1076220222",
  "jarley.jamaica@rappi.com": "1015481834",
  "karen.zamora@rappi.com": "1010154373",
  "julian.orobio@rappi.com": "1000225274",
  "fabio.barragan@rappi.com": "1012360707"
};

function performLogin() {
  const email = $('login-email').value.trim().toLowerCase();
  const pass = $('login-pass').value.trim();
  const err = $('login-error');
  
  if (!email || !pass) {
      err.textContent = "Ingresa tu correo y contraseña.";
      err.style.display = 'block';
      return;
  }

  if (AUTH_USERS[email] && AUTH_USERS[email] === pass) {
      sessionStorage.setItem('rappi_auth_user', email);
      CURRENT_USER_EMAIL = email;
      $('login-overlay').style.opacity = '0';
      
      if($('n-ag')) $('n-ag').value = email;

      setTimeout(() => {
          $('login-overlay').style.display = 'none';
          loadData(); 
      }, 400);
  } else {
      err.textContent = "Credenciales incorrectas o usuario no autorizado.";
      err.style.display = 'block';
  }
}

document.addEventListener('DOMContentLoaded', () => {
  if($('btn-theme-toggle')) {
    $('btn-theme-toggle').addEventListener('click', () => {
      const isLight = document.documentElement.getAttribute('data-theme') === 'light';
      document.documentElement.setAttribute('data-theme', isLight ? 'dark' : 'light');
      localStorage.setItem('rappi_theme', isLight ? 'dark' : 'light');
      if (window.geoMap && window.geoTile) {
        const tileUrl = !isLight ? 'https://{s}.basemaps.cartocdn.com/light_all/{z}/{x}/{y}{r}.png' : 'https://{s}.basemaps.cartocdn.com/dark_all/{z}/{x}/{y}{r}.png';
        window.geoTile.setUrl(tileUrl);
      }
    });
  }
  if($('btn-global-back')) $('btn-global-back').addEventListener('click', () => go('dashboard'));
  if($('hd-logo-btn')) $('hd-logo-btn').addEventListener('click', () => go('dashboard'));
  if($('btn-kpi-activos')) $('btn-kpi-activos').addEventListener('click', () => go('roster'));

  if($('btn-global-funnel')) {
      $('btn-global-funnel').addEventListener('click', () => openFunnelDrawer('ALL'));
  }

  document.querySelectorAll('.nav-btn[data-page]').forEach(b=>b.addEventListener('click',()=>go(b.dataset.page)));
  ['hd-hamburger','nav-overlay','btn-refresh','btn-reset-filters','btn-v-table','btn-v-charts','btn-nueva-reg','link-pipeline','link-registros','n-btn','n-clear-btn','btn-reset-analisis','btn-refresh-llamadas'].forEach(id => {
    const el = $(id); if(!el) return;
    if(id==='hd-hamburger') el.addEventListener('click', openMobileNav);
    if(id==='nav-overlay') el.addEventListener('click', closeMobileNav);
    if(id==='btn-refresh') el.addEventListener('click', () => loadData(false));
    if(id==='btn-reset-filters') el.addEventListener('click', resetFilters);
    if(id==='btn-v-table') el.addEventListener('click', ()=>setRegView('table'));
    if(id==='btn-v-charts') el.addEventListener('click', ()=>setRegView('charts'));
    if(id==='btn-nueva-reg') el.addEventListener('click', ()=>go('nuevo'));
    if(id==='link-pipeline') el.addEventListener('click', ()=>go('pipeline'));
    if(id==='link-registros') el.addEventListener('click', ()=>go('registros'));
    if(id==='n-btn') el.addEventListener('click', submitForm);
    if(id==='n-clear-btn') el.addEventListener('click', clearForm);
    if(id==='btn-reset-analisis') el.addEventListener('click', ()=>{ if($('f-analisis-agente'))$('f-analisis-agente').value=''; if($('f-analisis-mes'))$('f-analisis-mes').value=''; updateAnalisisDayFilter(); renderAnalisisBBDD(); });
    if(id==='btn-refresh-llamadas') el.addEventListener('click', ()=>{ toast('Actualizando...', 'inf'); if($('f-llamadas-agente'))$('f-llamadas-agente').dataset.loaded=''; loadLlamadas().then(renderLlamadas); });
  });

  if($('overlay')) $('overlay').addEventListener('click', e=>{if(e.target===$('overlay')) closeDrawer();});
  if($('dr-close-btn')) $('dr-close-btn').addEventListener('click', closeDrawer);
  if($('q')) $('q').addEventListener('input', debouncedFilter);
  if($('q-llamadas')) $('q-llamadas').addEventListener('input', debounce(renderLlamadas, 280));

  ['f-etapa','f-res','f-agente','f-hora-ini','f-hora-fin','f-dia','f-analisis-agente','f-analisis-dia','f-llamadas-agente'].forEach(id=>{if($(id))$(id).addEventListener('change',id.includes('analisis')?renderAnalisisBBDD:(id==='f-llamadas-agente'?renderLlamadas:doFilter));});
  if($('f-mes')) $('f-mes').addEventListener('change', ()=>{updateDayFilter(); doFilter();});
  if($('f-analisis-mes')) $('f-analisis-mes').addEventListener('change', ()=>{updateAnalisisDayFilter(); renderAnalisisBBDD();});
  if($('global-meta')) $('global-meta').addEventListener('input', ()=>{renderDesglose(); renderIndicadores(); renderRoster();});
  if($('calc-agent-sel')) $('calc-agent-sel').addEventListener('change', applyAgentToCalc);

  [['th-fecha','fecha'],['th-restaurante','restaurante'],['th-proceso','proceso'],['th-email','email']].forEach(([id,col])=>{if($(id))$(id).addEventListener('click',()=>srt(col));});

  if($('doc-files-input')) $('doc-files-input').addEventListener('change', handleFilesSelection);
  if($('doc-folder-input')) $('doc-folder-input').addEventListener('change', handleFilesSelection);

  if($('btn-upload-doc')){
    $('btn-upload-doc').addEventListener('click', async function(){
      const aN=$('doc-agent-sel')?$('doc-agent-sel').value:'', rN=$('doc-restaurante')?$('doc-restaurante').value.trim():'', b=this;
      if(!aN) return toast("Root Node (Agent) missing.","er"); if(!rN) return toast("Entity Node (Merchant) missing.","er"); if(DOCS_QUEUE.length===0) return toast("Payload Queue is empty.","er");
      const oH=b.innerHTML; b.innerHTML=`<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" style="animation:spin 1s linear infinite"><path d="M21 12a9 9 0 1 1-6.219-8.56"/></svg>Uploading Payload...`; b.disabled=true; if($('doc-files-input')) $('doc-files-input').disabled=true; if($('doc-folder-input')) $('doc-folder-input').disabled=true;
      let sC=0;
      for(let i=0;i<DOCS_QUEUE.length;i++){
        let f=DOCS_QUEUE[i], it=$(`doc-item-${i}`);
        if(f.size>10*1024*1024){ if(it){it.classList.add('error'); it.innerHTML+=`<div style="font-size:10px;margin-top:4px">File Size Overflow (>10MB)</div>`;} continue; }
        try{
          if(it) it.style.borderLeft="3px solid var(--r)"; const b64=await fileToBase64(f);
          const res=await fetch(CONFIG.SCRIPT_URL,{method:'POST',body:JSON.stringify({action:'upload_document',agentFolder:aN,restaurantFolder:rN,fileName:f.name,mimeType:f.type||'application/octet-stream',fileBase64:b64})});
          const d=await res.json();
          if(d.status==='success'){ if(it){it.classList.add('done');it.style.borderLeft="none";} sC++; } else if(it) it.classList.add('error');
        }catch(e){ if(it) it.classList.add('error'); }
      }
      b.innerHTML=oH; b.disabled=false; if($('doc-files-input')) $('doc-files-input').disabled=false; if($('doc-folder-input')) $('doc-folder-input').disabled=false;
      if(sC===DOCS_QUEUE.length){ toast("Success! Transmisión completa.","ok"); DOCS_QUEUE=[]; setTimeout(renderDocsQueue,1500); if($('doc-restaurante')) $('doc-restaurante').value=""; }
      else if(sC>0){ toast(`Transfer partial: ${sC} files uploaded.`,"inf"); DOCS_QUEUE=[]; } else toast("API Reject: Fallo.","er");
    });
  }

  // AI Menu Event Listeners
  const dropZone = $('ai-drop-zone');
  if(dropZone) {
      ['dragenter', 'dragover', 'dragleave', 'drop'].forEach(e => dropZone.addEventListener(e, ev => { ev.preventDefault(); ev.stopPropagation(); }));
      dropZone.addEventListener('dragover', () => dropZone.classList.add('drag-over'));
      dropZone.addEventListener('dragleave', () => dropZone.classList.remove('drag-over'));
      dropZone.addEventListener('drop', e => { dropZone.classList.remove('drag-over'); handleAIFiles(e.dataTransfer.files); });
      dropZone.addEventListener('click', () => $('ai-file-input').click());
  }
  if($('ai-file-input')) $('ai-file-input').addEventListener('change', e => handleAIFiles(e.target.files));
  
  if($('ai-btn-reset')) $('ai-btn-reset').addEventListener('click', () => {
      $('ai-results-sec').style.display = 'none';
      $('ai-upload-sec').style.display = 'block';
      $('ai-rest-name').value = '';
      if($('ai-file-input')) $('ai-file-input').value = '';
  });

  if($('ai-btn-zip')) $('ai-btn-zip').addEventListener('click', () => {
      const zip = new JSZip(); const rest = $('ai-rest-name')?.value || "Rest";
      [...(menuData.platos||[]), ...(menuData.bebidas||[])].forEach(i => { if(i.proImg) zip.file(`${(i.nombre || 'item').replace(/[^a-z0-9]/gi, '_')}.png`, i.proImg, {base64:true}); });
      zip.generateAsync({type:"blob"}).then(c => { saveAs(c, `FOTOS_PRO_${rest.toUpperCase()}.zip`); toast("ZIP DESCARGADO", "ok"); });
  });

  if($('ai-btn-copy')) $('ai-btn-copy').addEventListener('click', () => {
      const rest = $('ai-rest-name')?.value || "Restaurante";
      let t = `RESTAURANTE: ${rest}\n\n`;
      const a = (it, isB = false) => it.forEach(p => t += `${isB?'BEBIDAS':(p.corredor||'GENERAL')}\t${p.nombre}\t${p.desc||'N/A'}\t${p.precio}\t${p.elecciones||'N/A'}\t${p.agregar||'N/A'}\t${p.quitar||'N/A'}\n`);
      a(menuData.platos||[]); a(menuData.bebidas||[], true);
      const el = document.createElement('textarea'); el.value = t; document.body.appendChild(el); el.select(); document.execCommand('copy'); document.body.removeChild(el); toast("COPIADO PARA SHEETS", "ok");
  });

  if($('btn-desglose-table')) $('btn-desglose-table').addEventListener('click', ()=>setDesgloseView('table'));
  if($('btn-desglose-charts')) $('btn-desglose-charts').addEventListener('click', ()=>setDesgloseView('charts'));

  setTimeout(()=>{if($('loader')&&!$('loader').classList.contains('out') && $('login-overlay').style.display === 'none'){showLoaderError("Tiempo agotado."); const e=$('loader-error'); if(e)e.innerHTML+=`<br><br><button class="btn btn-primary" onclick="hideLoader()" style="width:100%;justify-content:center">Forzar Entrada al Dashboard</button>`;}}, 15000);
  
  // VERIFICACIÓN DE SESIÓN (LOGIN GATE)
  if ($('btn-login-submit')) $('btn-login-submit').addEventListener('click', performLogin);
  if ($('login-pass')) {
      $('login-pass').addEventListener('keypress', function (e) {
          if (e.key === 'Enter') performLogin();
      });
  }

  const savedUser = sessionStorage.getItem('rappi_auth_user');
  if (savedUser && AUTH_USERS[savedUser]) {
      $('login-overlay').style.display = 'none';
      if($('n-ag')) $('n-ag').value = savedUser;
      loadData();
  } else {
      $('login-overlay').style.display = 'flex';
  }

  setInterval(() => {
    const isDrawerOpen = $('overlay') && $('overlay').classList.contains('on');
    const isTyping = document.activeElement && (document.activeElement.tagName === 'INPUT' || document.activeElement.tagName === 'TEXTAREA');
    const isLoggingIn = $('login-overlay') && $('login-overlay').style.display !== 'none';
    
    if (!isDrawerOpen && !isTyping && !isLoggingIn) {
      loadData(true);
    }
  }, 10000);
});
</script>
</body>
</html>
