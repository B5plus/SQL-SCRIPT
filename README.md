/* ========================= B5 NAV (Screenshot Style) ========================= */
/* Put this block at the VERY END of your CSS file */

/* Sidebar background already uses your variables */
.t-Body-nav{
  background: linear-gradient(180deg, var(--nav-bg-top), var(--nav-bg-bot)) !important;
}

/* ---------- PARENT (Top Level) = bigger pill ---------- */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content{
  background: rgba(255,255,255,.06) !important;
  border: 1px solid rgba(255,255,255,.10) !important;
  border-radius: 16px !important;
  margin: 8px 12px !important;
  padding: 14px 14px !important;  /* bigger */
  transition: background .15s ease, box-shadow .15s ease, transform .15s ease;
}

/* Parent label stronger */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content .a-TreeView-label,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 15px !important;
  font-weight: 950 !important;
  color: var(--nav-text) !important;
}

/* Parent icon */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content .a-TreeView-icon{
  color: var(--nav-muted) !important;
}

/* Parent hover */
.t-TreeNav .a-TreeView > ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li:hover > .a-TreeView-content{
  background: rgba(255,255,255,.10) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.12) !important;
}

/* ---------- OPEN/EXPANDED PARENT = highlighted (when submenu open) ---------- */
/* APEX often marks expanded nodes with is-expanded or aria-expanded=true */
.t-TreeNav .a-TreeView-node.is-expanded > .a-TreeView-content,
.t-TreeNav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-expanded > .a-TreeView-content,
.apex-side-nav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content{
  background: rgba(255,255,255,.12) !important;
  border-color: rgba(255,255,255,.14) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.14) !important;
}

/* ---------- SUBMENU = smaller pills + deeper indent ---------- */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
  background: rgba(255,255,255,.05) !important;
  border: 1px solid rgba(255,255,255,.10) !important;
  border-radius: 14px !important;

  /* smaller than parent */
  margin: 8px 12px 8px 34px !important;  /* indented */
  padding: 10px 12px !important;         /* smaller */
  transition: background .15s ease, box-shadow .15s ease, transform .15s ease;
}

/* Submenu labels slightly smaller */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 13.5px !important;
  font-weight: 850 !important;
  color: var(--nav-child) !important;
}

/* Submenu hover effect (like screenshot) */
.t-TreeNav .a-TreeView ul ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li:hover > .a-TreeView-content{
  background: rgba(255,255,255,.12) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.16) !important;
  transform: translateX(1px);
}

/* Current page highlight (submenu or parent) */
.t-TreeNav .a-TreeView-node.is-current > .a-TreeView-content,
.t-TreeNav .a-TreeView-node.is-selected > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-current > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: rgba(255,255,255,.14) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 12px !important;
}

/* ---------- THE LONG LEFT STRIP (hierarchy line) ---------- */
/* Draw a vertical line alongside submenu list */
.t-TreeNav .a-TreeView ul ul,
.apex-side-nav .a-TreeView ul ul{
  position: relative !important;
  margin-top: 6px !important;
  margin-bottom: 10px !important;
}

/* The line itself */
.t-TreeNav .a-TreeView ul ul:before,
.apex-side-nav .a-TreeView ul ul:before{
  content:"";
  position:absolute;
  left: 22px;          /* controls line position */
  top: 0;
  bottom: 0;           /* makes it stretch to all submenu items */
  width: 2px;
  background: rgba(255,255,255,.14);
  border-radius: 2px;
}

/* Optional: small connector from line to each submenu pill */
.t-TreeNav .a-TreeView ul ul > li,
.apex-side-nav .a-TreeView ul ul > li{
  position: relative !important;
}
.t-TreeNav .a-TreeView ul ul > li:before,
.apex-side-nav .a-TreeView ul ul > li:before{
  content:"";
  position:absolute;
  left: 22px;
  top: 50%;
  width: 12px;
  height: 2px;
  background: rgba(255,255,255,.12);
  transform: translateY(-50%);
}

/* Icons brighten on hover */
.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon{
  color: #fff !important;
}

/* Dropdown arrow */
.t-TreeNav .a-TreeView-toggle,
.apex-side-nav .a-TreeView-toggle{
  color: rgba(255,255,255,.88) !important;
  opacity: 1 !important;
}
.t-TreeNav .a-TreeView-node:hover .a-TreeView-toggle,
.apex-side-nav .a-TreeView-node:hover .a-TreeView-toggle{
  color: #fff !important;
}

/* Mobile spacing: keep indent but tighter */
@media (max-width: 768px){
  .t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
  .apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
    margin-left: 26px !important;
  }
  .t-TreeNav .a-TreeView ul ul:before,
  .apex-side-nav .a-TreeView ul ul:before{
    left: 16px;
  }
  .t-TreeNav .a-TreeView ul ul > li:before,
  .apex-side-nav .a-TreeView ul ul > li:before{
    left: 16px;
    width: 10px;
  }
}
