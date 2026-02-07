/* ==========================================================
   B5 THEME (APEX 19.2 Universal Theme)
   Clean + Deduped + Fixed Nav Hover Grey Strip + Wider Nav
   ========================================================== */

/* =========================
   VARIABLES
   ========================= */
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

  /* NAV */
  --nav-bg-top:#1b3b57;
  --nav-bg-bot:#142f47;
  --nav-text:#ffffff;
  --nav-muted:rgba(255,255,255,.78);
  --nav-hover:rgba(255,255,255,.10);
  --nav-active:rgba(255,255,255,.16);

  /* Wider nav (desktop) */
  --b5-nav-width: 280px;
}

/* Body background */
.t-Body{ background: var(--b5-bg) !important; }

/* ==========================================================
   HEADER
   ========================================================== */
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

/* ==========================================================
   SIDE NAV WIDTH + BACKGROUND
   ========================================================== */

/* Try UT variable first (works on some builds) */
.t-Body{
  --ut-nav-width: var(--b5-nav-width);
}

/* Hard fallback for APEX 19.2 */
.t-Body-nav{
  background: linear-gradient(180deg, var(--nav-bg-top), var(--nav-bg-bot)) !important;
  border-right: 0 !important;
  box-shadow: 8px 0 18px rgba(15,23,42,.10) !important;

  width: var(--b5-nav-width) !important;
  max-width: var(--b5-nav-width) !important;
  flex: 0 0 var(--b5-nav-width) !important;
}

/* ==========================================================
   TREE NAV (remove grey strip + apply clean hover)
   ========================================================== */

/* Base row */
.t-TreeNav .a-TreeView-content{
  display:flex;
  align-items:center;
  border-radius: 14px !important;
  margin: 6px 12px !important;
  padding: 12px 14px !important;
  transition: background .15s ease, transform .15s ease, box-shadow .15s ease;
  background: transparent !important;
  box-shadow: none !important;
  outline: none !important;
}

/* Text + icons */
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

/* ---- REMOVE APEX GREY STRIP/OVERLAY STATES ---- */
.t-TreeNav .a-TreeView-content.is-selected,
.t-TreeNav .a-TreeView-content.is-hover,
.t-TreeNav .a-TreeView-content.is-focused,
.t-TreeNav .a-TreeView-node.is-focused > .a-TreeView-content,
.t-TreeNav .a-TreeView-node:focus > .a-TreeView-content,
.t-TreeNav .a-TreeView-node:focus-within > .a-TreeView-content{
  background-image: none !important;
  box-shadow: none !important;
  outline: none !important;
}

/* Pseudo overlays that often create the grey strip */
.t-TreeNav .a-TreeView-content::before,
.t-TreeNav .a-TreeView-content::after{
  content: none !important;
  background: transparent !important;
  box-shadow: none !important;
  border: 0 !important;
}

/* Hover + current */
.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content{
  background: var(--nav-hover) !important;
  transform: translateX(2px);
}
.t-TreeNav .a-TreeView-node.is-current > .a-TreeView-content,
.t-TreeNav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: var(--nav-active) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 12px !important;
}

/* Logout row highlight */
.vms-logout .a-TreeView-content{
  background: rgba(163,44,60,.24) !important;
  border: 1px solid rgba(255,255,255,.28) !important;
  border-radius: 14px !important;
}
.vms-logout .a-TreeView-label,
.vms-logout .a-TreeView-icon{
  color:#fff !important;
  font-weight: 900 !important;
}

/* Optional support if template adds .apex-side-nav */
.apex-side-nav .a-TreeView-label{ color: var(--nav-text) !important; }
.apex-side-nav .a-TreeView-icon,
.apex-side-nav .a-TreeView-content .fa,
.apex-side-nav .a-TreeView-content .fa-solid,
.apex-side-nav .a-TreeView-content .fa-regular,
.apex-side-nav .a-TreeView-content .fa-light,
.apex-side-nav .a-TreeView-content .fa-brands{
  color: var(--nav-muted) !important;
  opacity: .95 !important;
}

/* ==========================================================
   REGIONS / FORMS / BUTTONS
   ========================================================== */
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

/* ==========================================================
   REPORTS
   ========================================================== */
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

/* Links */
a{
  color: var(--b5-maroon);
  font-weight: 800;
  text-decoration: none;
}
a:hover{ color: var(--b5-blue); text-decoration: underline; }

/* Helpers */
.u-hidden{ display:none !important; }

/* Input sizing */
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

/* Floating label tuning */
.t-Form-fieldContainer--floatingLabel input,
.t-Form-fieldContainer--floatingLabel select{
  padding-top: 22px !important;
  padding-bottom: 10px !important;
}
.t-Form-fieldContainer--floatingLabel textarea{ padding-top: 26px !important; }
.t-Form-fieldContainer--floatingLabel .t-Form-label{
  font-size: 12px !important;
  font-weight: 800 !important;
  margin-bottom: 0 !important;
  transform: translateY(-2px);
}
.t-Form-inputContainer .a-Button--calendar{ height: 44px !important; }

/* ==========================================================
   CLASSIC REPORT BUTTONS
   ========================================================== */
.b5-btn,
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
  white-space: nowrap;
}

.b5-btn-maroon{
  background: #A32C3C;
  border-color: #A32C3C;
  color: #fff !important;
  box-shadow: 0 10px 18px rgba(163,44,60,.18);
}
.b5-btn-maroon:hover{ filter: brightness(.95); transform: translateY(-1px); }

.b5-btn-blue{
  background: #29527D;
  border-color: #29527D;
  color: #fff !important;
  box-shadow: 0 10px 18px rgba(41,82,125,.18);
}
.b5-btn-blue:hover{ filter: brightness(.95); transform: translateY(-1px); }

.b5-checkout-btn{
  background: linear-gradient(90deg, #A32C3C, #29527D);
  color:#fff !important;
  box-shadow: 0 10px 18px rgba(15,23,42,.16);
}
.b5-checkout-btn:hover{ filter: brightness(.96); transform: translateY(-1px); }

.b5-photo-btn{
  background: #29527D;
  color:#fff !important;
  box-shadow: 0 10px 18px rgba(41,82,125,.16);
}
.b5-photo-btn:hover{ filter: brightness(.96); transform: translateY(-1px); }

/* ==========================================================
   STATUS BADGES
   ========================================================== */
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
  background: rgba(163,44,60,.14);
  border-color: rgba(163,44,60,.38);
  color: #A32C3C;
}
.b5-badge-gray{
  background: rgba(100,116,139,.12);
  border-color: rgba(100,116,139,.25);
  color: #334155;
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

/* ==========================================================
   RESPONSIVE (Mobile)
   ========================================================== */
@media (max-width: 768px){

  .t-Header, .t-Header-container{ box-shadow:none !important; }
  .t-Region{ border-radius: 14px !important; }

  /* Mobile nav width (drawer) */
  .t-Body-nav{
    width: 260px !important;
    max-width: 260px !important;
    flex: 0 0 260px !important;
    display: block !important;
    visibility: visible !important;
  }

  /* Ensure drawer can appear */
  .t-Body--navExpanded .t-Body-nav,
  .t-Body--navExpanded .t-Body-content,
  .t-Body--navExpanded .t-Body-title{
    transform: none !important;
  }

  .t-TreeNav .a-TreeView-content{
    margin: 6px 10px !important;
  }

  .t-Form-inputContainer input,
  .t-Form-inputContainer select,
  .t-Form-inputContainer textarea{
    padding: 12px 12px !important;
    border-radius: 14px !important;
  }

  .t-Report-reportWrap{ overflow-x:auto; }
  .t-Report-cell, .t-Report-colHead{ white-space: nowrap; }

  .t-Button{ width: 100%; justify-content:center; }

  /* Floating label spacing on mobile */
  .t-Form-fieldContainer--floatingLabel input,
  .t-Form-fieldContainer--floatingLabel select{
    padding-top: 26px !important;
    padding-bottom: 12px !important;
    min-height: 54px !important;
  }
  .t-Form-fieldContainer--floatingLabel textarea{
    padding-top: 30px !important;
    min-height: 130px !important;
  }
  .t-Form-fieldContainer--floatingLabel .t-Form-label{
    font-size: 11px !important;
    transform: translateY(-6px) !important;
    opacity: .85;
  }
  .t-Form-fieldContainer--floatingLabel input::placeholder,
  .t-Form-fieldContainer--floatingLabel textarea::placeholder{
    font-size: 13px;
    opacity: .70;
  }

  /* Smaller table buttons on mobile */
  .b5-btn, .b5-action-btn{
    padding: 7px 10px;
    font-size: 13px;
  }
}
