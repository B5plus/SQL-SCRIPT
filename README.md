/* ========================= B5 NAV (COMPACT SUBMENU) ========================= */
/* Paste at the VERY END of your CSS file */

/* ---------- TURN OFF DEFAULT "HOVER/ACTIVE" LOOKS (keep clean by default) ---------- */
.t-TreeNav .a-TreeView-content,
.apex-side-nav .a-TreeView-content{
  background: transparent !important;
  box-shadow: none !important;
  border: 0 !important;
}

/* Parent (top level) pills – normal size, no “always-hover” look */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content{
  border-radius: 16px !important;
  margin: 8px 12px !important;
  padding: 12px 14px !important;
  background: rgba(255,255,255,.05) !important;  /* clean */
  border: 1px solid rgba(255,255,255,.10) !important;
  transition: background .12s ease, box-shadow .12s ease, transform .12s ease;
}

/* Parent hover ONLY when user hovers */
.t-TreeNav .a-TreeView > ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li:hover > .a-TreeView-content{
  background: rgba(255,255,255,.10) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.14) !important;
}

/* Parent highlight when expanded (submenu open) */
.t-TreeNav .a-TreeView-node.is-expanded > .a-TreeView-content,
.t-TreeNav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-expanded > .a-TreeView-content,
.apex-side-nav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content{
  background: rgba(255,255,255,.12) !important;
  border-color: rgba(255,255,255,.16) !important;
}

/* ---------- REMOVE THE “--” BEFORE SUBMENU ITEMS ---------- */
/* APEX draws it using pseudo elements in some templates */
.t-TreeNav .a-TreeView ul ul > li:before,
.t-TreeNav .a-TreeView ul ul > li:after,
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content:before,
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content:after,
.apex-side-nav .a-TreeView ul ul > li:before,
.apex-side-nav .a-TreeView ul ul > li:after,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content:before,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content:after{
  content: none !important;
}

/* ---------- SUBMENU: VERY COMPACT + NO GAPS ---------- */
.t-TreeNav .a-TreeView ul ul,
.apex-side-nav .a-TreeView ul ul{
  position: relative !important;
  margin: 4px 0 8px !important;
  padding: 0 !important;
}

/* Left vertical strip (long line) */
.t-TreeNav .a-TreeView ul ul:before,
.apex-side-nav .a-TreeView ul ul:before{
  content:"";
  position:absolute;
  left: 22px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: rgba(255,255,255,.14);
  border-radius: 2px;
}

/* Submenu item container: remove vertical gap */
.t-TreeNav .a-TreeView ul ul > li,
.apex-side-nav .a-TreeView ul ul > li{
  margin: 0 !important;
  padding: 0 !important;
}

/* Submenu pills: small height + tight stacking */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
  margin: 2px 12px 2px 34px !important; /* almost no gap */
  padding: 6px 10px !important;         /* VERY small height */
  min-height: 30px !important;          /* compact height */
  border-radius: 12px !important;
  background: rgba(255,255,255,.04) !important;
  border: 1px solid rgba(255,255,255,.10) !important;
  transition: background .12s ease, box-shadow .12s ease, transform .12s ease;
}

/* Submenu label smaller */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 12.5px !important;
  font-weight: 850 !important;
  color: var(--nav-child) !important;
}

/* Submenu hover ONLY when hovering */
.t-TreeNav .a-TreeView ul ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li:hover > .a-TreeView-content{
  background: rgba(255,255,255,.12) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.16) !important;
  transform: translateX(1px);
}

/* Current page highlight */
.t-TreeNav .a-TreeView-node.is-current > .a-TreeView-content,
.t-TreeNav .a-TreeView-node.is-selected > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-current > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: rgba(255,255,255,.14) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 10px !important;
}

/* Icons: keep calm by default, bright on hover only */
.t-TreeNav .a-TreeView-icon,
.apex-side-nav .a-TreeView-icon,
.apex-side-nav .a-Icon{
  color: var(--nav-muted) !important;
}
.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-Icon{
  color: #fff !important;
}

/* Mobile: keep the line + compact spacing */
@media (max-width: 768px){
  .t-TreeNav .a-TreeView ul ul:before,
  .apex-side-nav .a-TreeView ul ul:before{
    left: 16px;
  }
  .t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
  .apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
    margin-left: 26px !important;
  }
}
