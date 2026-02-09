/* ========================= NAV: FORCE FLAT BY DEFAULT ========================= */
/* Put at the VERY END of CSS */

/* Kill any default background/border/radius on all menu rows */
.t-TreeNav .a-TreeView-content,
.apex-side-nav .a-TreeView-content{
  background: transparent !important;
  border: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
}

/* Also kill border/background if APEX applies it on the ROW wrapper */
.t-TreeNav .a-TreeView-row,
.apex-side-nav .a-TreeView-row{
  background: transparent !important;
  border: 0 !important;
  box-shadow: none !important;
  border-radius: 0 !important;
}

/* Parent + submenu: keep them flat (no border) until hover */
.t-TreeNav .a-TreeView > ul > li > .a-TreeView-content,
.t-TreeNav .a-TreeView ul ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView > ul > li > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li > .a-TreeView-content{
  background: transparent !important;
  border: 0 !important;
  border-radius: 0 !important;
  box-shadow: none !important;
}

/* SHOW pill only on hover */
.t-TreeNav .a-TreeView-node:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView-node:hover > .a-TreeView-content{
  background: rgba(255,255,255,.10) !important;
  border: 1px solid rgba(255,255,255,.14) !important;
  border-radius: 14px !important;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.10) !important;
}

/* Submenu hover: smaller radius */
.t-TreeNav .a-TreeView ul ul > li:hover > .a-TreeView-content,
.apex-side-nav .a-TreeView ul ul > li:hover > .a-TreeView-content{
  border-radius: 12px !important;
}
