:root{
  --b5-maroon:#A32C3C;
  --b5-blue:#29527D;
  --b5-white:#ffffff;

  --b5-bg:#f6f8fc;
  --b5-card:#ffffff;
  --b5-border:#e6e8ef;
  --b5-soft:#f3f6fb;

  --b5-text:#0f172a;
  --b5-muted:#64748b;

  --b5-radius:16px;
  --b5-radius-sm:12px;
}

.t-Body{ background: var(--b5-bg) !important; }

.t-Header,
.t-Header-container{
  background: linear-gradient(90deg, var(--b5-maroon), var(--b5-blue)) !important;
  border: 0 !important;
  box-shadow: 0 10px 24px rgba(15,23,42,.12) !important;
}
.t-Header-branding,
.t-Header-navBar,
.t-Header-controls{
  background: transparent !important;
  border: 0 !important;
  box-shadow: none !important;
}

.t-Header *{ color: var(--b5-white) !important; }

.t-Header .t-Button,
.t-Header .t-Button--noUI,
.t-Header .t-Button--icon{
  background: transparent !important;
  border: 0 !important;
  box-shadow: none !important;
  border-radius: 12px !important;
}
.t-Header .t-Button:hover,
.t-Header a:hover{
  background: rgba(255,255,255,.14) !important;
}

.t-Body-nav{
  background: linear-gradient(180deg, #244a6f, #1f3f5e) !important;
  border-right: 0 !important;
  box-shadow: 8px 0 18px rgba(15,23,42,.10) !important;
}

.t-TreeNav .a-TreeView-content{
  display:flex;
  align-items:center;
  border-radius: 14px !important;
  margin: 6px 12px !important;
  padding: 12px 14px !important;
  transition: all .15s ease;
}

.t-TreeNav .a-TreeView-label{
  font-size: 15px !important;
  font-weight: 800 !important;
  letter-spacing: .2px;
  color: rgba(255,255,255,.94) !important;
}

.t-TreeNav .a-TreeView-icon{
  width: 22px !important;
  min-width: 22px !important;
  text-align:center !important;
  font-size: 18px !important;
  margin-right: 10px !important;
  color: rgba(255,255,255,.90) !important;
}

.t-TreeNav .a-TreeView-toggle{
  color: rgba(255,255,255,.75) !important;
}
.t-TreeNav .a-TreeView-toggle:hover{
  color: #fff !important;
}

.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content{
  background: rgba(255,255,255,.09) !important;
  transform: translateX(2px);
}

.t-TreeNav .a-TreeView-node.is-current > .a-TreeView-content,
.t-TreeNav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: rgba(255,255,255,.14) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 12px !important;
}

.vms-logout .a-TreeView-content{
  background: rgba(163,44,60,.22) !important;
  border: 1px solid rgba(255,255,255,.25) !important;
}
.vms-logout .a-TreeView-label,
.vms-logout .a-TreeView-icon{
  color: #fff !important;
}

.t-Region{
  background: var(--b5-card) !important;
  border: 1px solid var(--b5-border) !important;
  border-radius: var(--b5-radius) !important;
  box-shadow: 0 10px 26px rgba(15,23,42,.08) !important;
  overflow: hidden;
}
.t-Region-header{
  background: linear-gradient(90deg, rgba(163,44,60,.12), rgba(41,82,125,.12)) !important;
  border-bottom: 1px solid var(--b5-border) !important;
}
.t-Region-title{
  color: var(--b5-text) !important;
  font-weight: 900 !important;
}

.t-Form-label{
  color: var(--b5-text) !important;
  font-weight: 800 !important;
}
.t-Form-helpText{ color: var(--b5-muted) !important; }

.t-Form-inputContainer input,
.t-Form-inputContainer select,
.t-Form-inputContainer textarea{
  background: var(--b5-soft) !important;
  border: 1px solid #d7dbe7 !important;
  border-radius: var(--b5-radius-sm) !important;
  padding: 11px 12px !important;
  transition: all .15s ease;
}

.t-Form-inputContainer input:focus,
.t-Form-inputContainer select:focus,
.t-Form-inputContainer textarea:focus{
  background: #fff !important;
  border-color: var(--b5-blue) !important;
  box-shadow: 0 0 0 4px rgba(41,82,125,.15) !important;
  outline: none !important;
}

.t-Form-required{ color: var(--b5-maroon) !important; }

.t-Button{
  border-radius: 12px !important;
  font-weight: 900 !important;
}
.t-Button--hot{
  background: var(--b5-maroon) !important;
  border-color: var(--b5-maroon) !important;
  color: #fff !important;
  box-shadow: 0 12px 20px rgba(163,44,60,.18) !important;
}
.t-Button--hot:hover{ filter: brightness(.95); }

.b5-blue-btn{
  background: var(--b5-blue) !important;
  border-color: var(--b5-blue) !important;
  color: #fff !important;
}

table.t-Report-report{ border-collapse: separate; border-spacing: 0; }

.t-Report-colHead{
  background: #fff !important;
  color: var(--b5-blue) !important;
  font-weight: 900 !important;
  border-bottom: 1px solid var(--b5-border) !important;
}

.t-Report-cell{
  border-bottom: 1px solid var(--b5-border) !important;
  vertical-align: middle;
}

.t-Report-report tr:nth-child(even) .t-Report-cell{
  background: rgba(41,82,125,.04) !important;
}

.t-Report-report tr:hover .t-Report-cell{
  background: rgba(163,44,60,.06) !important;
}

a{
  color: var(--b5-maroon);
  font-weight: 800;
  text-decoration: none;
}
a:hover{ color: var(--b5-blue); text-decoration: underline; }

@media (max-width: 768px){
  .t-Header, .t-Header-container{ box-shadow:none !important; }
  .t-Region{ border-radius: 14px !important; }
  .t-Form-inputContainer input,
  .t-Form-inputContainer select,
  .t-Form-inputContainer textarea{
    padding: 12px 12px !important;
    border-radius: 14px !important;
  }
  .t-Report-reportWrap{ overflow-x:auto; }
  .t-Report-cell, .t-Report-colHead{ white-space: nowrap; }
  .t-Button{ width: 100%; justify-content:center; }
}

.u-hidden{ display:none !important; }

.t-Form-inputContainer input[type="text"],
.t-Form-inputContainer input[type="tel"],
.t-Form-inputContainer input[type="email"],
.t-Form-inputContainer input[type="number"],
.t-Form-inputContainer input[type="password"],
.t-Form-inputContainer input[type="search"],
.t-Form-inputContainer input[type="date"],
.t-Form-inputContainer select{
  min-height: 44px !important;
  line-height: 22px !important;
}

.t-Form-inputContainer textarea{
  min-height: 92px !important;
  line-height: 22px !important;
}

.t-Form-fieldContainer--floatingLabel input,
.t-Form-fieldContainer--floatingLabel select{
  padding-top: 22px !important;
  padding-bottom: 10px !important;
}

.t-Form-fieldContainer--floatingLabel textarea{
  padding-top: 26px !important;
}

.t-Form-fieldContainer--floatingLabel .t-Form-label{
  font-size: 12px !important;
  font-weight: 800 !important;
  margin-bottom: 0 !important;
  transform: translateY(-2px);
}

.t-Form-inputContainer .a-Button--calendar{
  height: 44px !important;
}

/* ===== Fix floating-label congestion on mobile ===== */
@media (max-width: 768px){

  /* Give more breathing space in floating label fields */
  .t-Form-fieldContainer--floatingLabel input,
  .t-Form-fieldContainer--floatingLabel select{
    padding-top: 26px !important;      /* more room for label */
    padding-bottom: 12px !important;
    min-height: 54px !important;       /* taller input */
  }

  .t-Form-fieldContainer--floatingLabel textarea{
    padding-top: 30px !important;
    min-height: 130px !important;
  }

  /* Make label smaller and move it higher */
  .t-Form-fieldContainer--floatingLabel .t-Form-label{
    font-size: 11px !important;
    font-weight: 800 !important;
    transform: translateY(-6px) !important;
    opacity: .85;
  }

  /* Slightly reduce placeholder size so it doesn't fight with label */
  .t-Form-fieldContainer--floatingLabel input::placeholder,
  .t-Form-fieldContainer--floatingLabel textarea::placeholder{
    font-size: 13px;
    opacity: .70;
  }
}


























/* ===== B5 Classic Report Buttons ===== */
.b5-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding: 8px 12px;
  border-radius: 12px;
  font-weight: 900;
  text-decoration: none !important;
  border: 1px solid transparent;
  transition: all .15s ease;
  line-height: 1;
}

/* Maroon button (Checkout) */
.b5-btn-maroon{
  background: #A32C3C;
  border-color: #A32C3C;
  color: #fff !important;
  box-shadow: 0 10px 18px rgba(163,44,60,.18);
}
.b5-btn-maroon:hover{
  filter: brightness(.95);
  transform: translateY(-1px);
}

/* Blue button (View Photo) */
.b5-btn-blue{
  background: #29527D;
  border-color: #29527D;
  color: #fff !important;
  box-shadow: 0 10px 18px rgba(41,82,125,.18);
}
.b5-btn-blue:hover{
  filter: brightness(.95);
  transform: translateY(-1px);
}

/* Mobile: smaller buttons inside table */
@media (max-width: 768px){
  .b5-btn{
    padding: 7px 10px;
    border-radius: 12px;
    font-size: 13px;
  }
}


/* ===== B5 Classic Report Action Buttons ===== */
.b5-action-btn{
  display:inline-flex;
  align-items:center;
  justify-content:center;
  padding: 8px 12px;
  border-radius: 12px;
  font-weight: 900;
  text-decoration: none !important;
  border: 1px solid transparent;
  transition: all .15s ease;
  line-height: 1;
  color:#fff !important;
  white-space: nowrap;
}

/* Checkout: brand gradient (maroon -> blue) */
.b5-checkout-btn{
  background: linear-gradient(90deg, #A32C3C, #29527D);
  box-shadow: 0 10px 18px rgba(15,23,42,.16);
}
.b5-checkout-btn:hover{
  filter: brightness(.96);
  transform: translateY(-1px);
}

/* Photo: solid blue */
.b5-photo-btn{
  background: #29527D;
  box-shadow: 0 10px 18px rgba(41,82,125,.16);
}
.b5-photo-btn:hover{
  filter: brightness(.96);
  transform: translateY(-1px);
}

@media (max-width: 768px){
  .b5-action-btn{
    padding: 7px 10px;
    font-size: 13px;
  }
}



/* ===== Acknowledgement Status Badges ===== */
.b5-badge{
  display:inline-block;
  padding: 6px 10px;
  border-radius: 999px;
  font-weight: 900;
  font-size: 12px;
  letter-spacing: .2px;
  border: 1px solid transparent;
  white-space: nowrap;
}

.b5-badge-green{
  background: rgba(34,197,94,.14);
  border-color: rgba(34,197,94,.35);
  color: #0f5132;
}

.b5-badge-yellow{
  background: rgba(245,158,11,.16);
  border-color: rgba(245,158,11,.38);
  color: #7c4a00;
}

.b5-badge-red{
  background: rgba(163,44,60,.14);   /* uses your maroon */
  border-color: rgba(163,44,60,.38);
  color: #A32C3C;
}

.b5-badge-gray{
  background: rgba(100,116,139,.12);
  border-color: rgba(100,116,139,.25);
  color: #334155;
}

.b5-badge{
  display:inline-block;
  padding:6px 10px;
  border-radius:999px;
  font-weight:900;
  font-size:12px;
  border:1px solid transparent;
  white-space:nowrap;
}

.b5-status-in{
  background: rgba(41,82,125,.14);
  border-color: rgba(41,82,125,.35);
  color: #29527D;
}
.b5-status-out{
  background: rgba(163,44,60,.14);
  border-color: rgba(163,44,60,.35);
  color: #A32C3C;
}

.b5-ack-green{
  background: rgba(34,197,94,.14);
  border-color: rgba(34,197,94,.35);
  color: #0f5132;
}
.b5-ack-yellow{
  background: rgba(245,158,11,.16);
  border-color: rgba(245,158,11,.38);
  color: #7c4a00;
}
.b5-ack-red{
  background: rgba(163,44,60,.14);
  border-color: rgba(163,44,60,.38);
  color: #A32C3C;
}

.b5-badge-gray{
  background: rgba(100,116,139,.12);
  border-color: rgba(100,116,139,.25);
  color: #334155;
}




/* ===== B5 Dashboard (VMS) ===== */
.b5dash{
  --m:#A32C3C;
  --b:#29527D;
  --w:#fff;
  --bg:#f6f8fc;
  --card:#ffffff;
  --border:#e6e8ef;
  --text:#0f172a;
  --muted:#64748b;
  --radius:18px;
  --radius2:14px;
  padding: 10px;
}

.b5dash__title{
  margin: 4px 6px 14px;
}
.b5dash__heading{
  font-size: 20px;
  font-weight: 900;
  color: var(--text);
}
.b5dash__sub{
  color: var(--muted);
  font-weight: 600;
  margin-top: 3px;
}

/* KPI cards grid */
.b5dash__grid{
  display:grid;
  grid-template-columns: repeat(5, minmax(160px, 1fr));
  gap: 12px;
  margin: 0 6px 14px;
}
.b5card{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 14px 14px 12px;
  box-shadow: 0 10px 26px rgba(15,23,42,.06);
  position: relative;
  overflow: hidden;
}
.b5card:before{
  content:"";
  position:absolute;
  top:0; left:0; right:0;
  height:4px;
  background: linear-gradient(90deg, var(--m), var(--b));
}
.b5card--maroon:before{ background: var(--m); }
.b5card--blue:before{ background: var(--b); }

.b5card__label{
  color: var(--muted);
  font-weight: 800;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: .5px;
}
.b5card__value{
  font-size: 30px;
  font-weight: 950;
  color: var(--text);
  margin-top: 6px;
  line-height: 1.05;
}
.b5card__hint{
  color: var(--muted);
  font-weight: 650;
  margin-top: 6px;
  font-size: 13px;
}

/* Panels */
.b5dash__lists{
  display:grid;
  grid-template-columns: repeat(2, minmax(320px, 1fr));
  gap: 14px;
  margin: 0 6px;
}
.b5panel{
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  box-shadow: 0 10px 26px rgba(15,23,42,.06);
  overflow: hidden;
}
.b5panel__head{
  display:flex;
  align-items:center;
  justify-content: space-between;
  padding: 12px 14px;
  border-bottom: 1px solid var(--border);
  background: linear-gradient(90deg, rgba(163,44,60,.08), rgba(41,82,125,.08));
}
.b5panel__title{
  font-weight: 950;
  color: var(--text);
}
.b5panel__body{
  padding: 12px 14px 14px;
}
.b5panel--danger .b5panel__head{
  background: rgba(163,44,60,.10);
}

/* Pills */
.b5pill{
  padding: 6px 10px;
  border-radius: 999px;
  font-weight: 900;
  font-size: 12px;
  border: 1px solid rgba(100,116,139,.25);
  background: rgba(100,116,139,.10);
  color: #334155;
}
.b5pill--maroon{
  border-color: rgba(163,44,60,.35);
  background: rgba(163,44,60,.12);
  color: var(--m);
}
.b5pill--blue{
  border-color: rgba(41,82,125,.35);
  background: rgba(41,82,125,.12);
  color: var(--b);
}
.b5pill--danger{
  border-color: rgba(163,44,60,.40);
  background: rgba(163,44,60,.14);
  color: var(--m);
}

.b5dash__region-note{
  color: var(--muted);
  font-weight: 650;
  font-size: 13px;
  padding: 4px 0;
}

/* Responsive */
@media (max-width: 1200px){
  .b5dash__grid{ grid-template-columns: repeat(3, minmax(160px, 1fr)); }
}
@media (max-width: 768px){
  .b5dash__grid{ grid-template-columns: repeat(2, minmax(140px, 1fr)); }
  .b5dash__lists{ grid-template-columns: 1fr; }
  .b5card__value{ font-size: 26px; }
}















/* ==========================================================
   NAV ONLY OVERRIDES (Header + Side Nav)
   Does NOT affect forms/reports/regions/buttons
   ========================================================== */
/* ==========================================================
   NAV ONLY: Professional hover + fix black icons (APEX side nav)
   ========================================================== */

:root{
  --nav-bg-top:#1b3b57;
  --nav-bg-bot:#142f47;
  --nav-text:#ffffff;
  --nav-muted:rgba(255,255,255,.78);
  --nav-child:rgba(255,255,255,.90);
  --nav-hover:rgba(255,255,255,.10);
  --nav-hover-strong:rgba(255,255,255,.14);
  --nav-active:rgba(255,255,255,.16);
  --nav-child-bg:rgba(255,255,255,.06);
  --nav-child-border:rgba(255,255,255,.10);
}

/* Sidebar background */
.t-Body-nav{
  background: linear-gradient(180deg, var(--nav-bg-top), var(--nav-bg-bot)) !important;
}

/* --------- FORCE ICON COLOR (fix black icons) --------- */
.apex-side-nav .a-TreeView-icon,
.apex-side-nav .a-TreeView-content .fa,
.apex-side-nav .a-TreeView-content .fa-solid,
.apex-side-nav .a-TreeView-content .fa-regular,
.apex-side-nav .a-TreeView-content .fa-light,
.apex-side-nav .a-TreeView-content .fa-brands{
  color: var(--nav-muted) !important;
  opacity: .95 !important;
}

/* Labels always readable */
.apex-side-nav .a-TreeView-label{
  color: var(--nav-text) !important;
}

/* --------- Parent rows (clean, not boxy) --------- */
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content{
  background: transparent !important;
  border: 0 !important;
  border-radius: 12px !important;
  margin: 4px 10px !important;
  padding: 12px 12px !important;
  transition: background .15s ease, box-shadow .15s ease;
}

.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 15px !important;
  font-weight: 950 !important;
  letter-spacing: .2px !important;
}

/* --------- Child rows (submenu) --------- */
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
  background: var(--nav-child-bg) !important;
  border: 1px solid var(--nav-child-border) !important;
  border-radius: 14px !important;
  margin: 6px 10px 6px 28px !important;
  padding: 10px 12px !important;
  transition: background .15s ease, box-shadow .15s ease;
}

.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 13.5px !important;
  font-weight: 850 !important;
  color: var(--nav-child) !important;
}

/* Submenu guideline */
.apex-side-nav .a-TreeView ul ul{
  position: relative !important;
  margin-top: 4px !important;
  margin-bottom: 8px !important;
}
.apex-side-nav .a-TreeView ul ul:before{
  content:"";
  position:absolute;
  left: 18px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: rgba(255,255,255,.12);
  border-radius: 2px;
}

/* --------- BEST HOVER EFFECT (professional, no jump) --------- */
/* Parent hover */
.apex-side-nav .a-TreeView > ul > li:hover > .a-TreeView-content{
  background: var(--nav-hover) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.12);
}

/* Child hover */
.apex-side-nav .a-TreeView ul ul > li:hover > .a-TreeView-content{
  background: var(--nav-hover-strong) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.14);
}

/* Icons brighten on hover */
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon{
  color: #fff !important;
}

/* --------- CURRENT PAGE highlight --------- */
.apex-side-nav .a-TreeView-node.is-current > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: var(--nav-active) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 12px !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.12);
}
.apex-side-nav .a-TreeView-node.is-current .a-TreeView-label,
.apex-side-nav .a-TreeView-node.is-selected .a-TreeView-label{
  color: #fff !important;
}
.apex-side-nav .a-TreeView-node.is-current .a-TreeView-icon,
.apex-side-nav .a-TreeView-node.is-selected .a-TreeView-icon{
  color: #fff !important;
}

/* Dropdown arrow (toggle) */
.apex-side-nav .a-TreeView-toggle{
  color: rgba(255,255,255,.88) !important;
  opacity: 1 !important;
}
.apex-side-nav .a-TreeView-node:hover .a-TreeView-toggle{
  color: #fff !important;
}

/* Logout button (if class vms-logout exists) */
.vms-logout .a-TreeView-content{
  background: rgba(163,44,60,.24) !important;
  border: 1px solid rgba(255,255,255,.28) !important;
  border-radius: 14px !important;
  margin-top: 14px !important;
}
.vms-logout .a-TreeView-label,
.vms-logout .a-TreeView-icon{
  color:#fff !important;
  font-weight: 900 !important;
}

/* Mobile */
@media (max-width: 768px){
  .apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
    margin-left: 22px !important;
  }
  .apex-side-nav .a-TreeView ul ul:before{
    left: 14px;
  }
}

