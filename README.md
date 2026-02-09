/* ========================= B5 NAV (FLAT BY DEFAULT + ROUNDED ON HOVER) ========================= */
/* Paste at the VERY END of your CSS file */

/* ---------- DEFAULT: FLAT (NO PILL LOOK) ---------- */
.t-TreeNav .a-TreeView-content,
.apex-side-nav .a-TreeView-content{
  background: transparent !important;
  border: 0 !important;
  box-shadow: none !important;
  border-radius: 0 !important;          /* IMPORTANT: no radius by default */
}

/* ---------- PARENT (Top Level) : more compact ---------- */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content{
  margin: 6px 12px !important;          /* slightly tighter */
  padding: 10px 12px !important;        /* compact parent */
  transition: background .12s ease, box-shadow .12s ease, transform .12s ease, border-radius .12s ease;
}

/* Parent hover: show pill + highlight ONLY on hover */
.t-TreeNav .a-TreeView > ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li:hover > .a-TreeView-content{
  border-radius: 14px !important;
  background: rgba(255,255,255,.10) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.14) !important;
}

/* Parent open (submenu expanded): keep highlight, but still no radius unless you want it */
.t-TreeNav .a-TreeView-node.is-expanded > .a-TreeView-content,
.t-TreeNav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-expanded > .a-TreeView-content,
.apex-side-nav .a-TreeView-node[aria-expanded="true"] > .a-TreeView-content{
  background: rgba(255,255,255,.08) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.10) !important;
  /* if you ALSO want rounded when expanded, uncomment:
  border-radius: 14px !important;
  */
}

/* ---------- REMOVE DASH/LINE BEFORE SUBMENU (if template draws it) ---------- */
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

/* ---------- SUBMENU: very small height + LITTLE GAP ---------- */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
  margin: 4px 12px 4px 34px !important; /* little gap (was 2px) */
  padding: 6px 10px !important;        /* small height */
  min-height: 30px !important;
  transition: background .12s ease, box-shadow .12s ease, transform .12s ease, border-radius .12s ease;
  border-radius: 0 !important;         /* FLAT by default */
}

/* Submenu hover: show rounded pill + highlight ONLY on hover */
.t-TreeNav .a-TreeView ul ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li:hover > .a-TreeView-content{
  border-radius: 12px !important;
  background: rgba(255,255,255,.12) !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.16) !important;
  transform: translateX(1px);
}

/* Submenu label compact */
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content .a-TreeView-label{
  font-size: 12.5px !important;
  font-weight: 850 !important;
  color: rgba(255,255,255,.90) !important;
}

/* ---------- LEFT VERTICAL STRIP (hierarchy line) ---------- */
.t-TreeNav .a-TreeView ul ul,
.apex-side-nav .a-TreeView ul ul{
  position: relative !important;
  margin-top: 4px !important;
  margin-bottom: 6px !important;
}
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

/* ---------- CURRENT PAGE highlight (keep visible) ---------- */
.t-TreeNav .a-TreeView-node.is-current > .a-TreeView-content,
.t-TreeNav .a-TreeView-node.is-selected > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-current > .a-TreeView-content,
.apex-side-nav .a-TreeView-node.is-selected > .a-TreeView-content{
  background: rgba(255,255,255,.12) !important;
  border-left: 4px solid var(--b5-maroon) !important;
  padding-left: 10px !important;
  border-radius: 0 !important; /* keep flat unless hovered */
}

/* Icons calm by default; brighten on hover */
.t-TreeNav .a-TreeView-icon,
.apex-side-nav .a-TreeView-icon,
.apex-side-nav .a-Icon{
  color: rgba(255,255,255,.78) !important;
}
.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-TreeView-icon,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content .a-Icon{
  color: #fff !important;
}

/* Mobile tweak */
@media (max-width: 768px){
  .t-TreeNav .a-TreeView ul ul:before,
  .apex-side-nav .a-TreeView ul ul:before{ left: 16px; }

  .t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
  .apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
    margin-left: 26px !important;
  }
}
