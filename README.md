/* ===== Force remove Vista/TreeNav grey background (#c5bbbb) ===== */

/* This is the exact selector family shown in your Inspect (Vista.min...) */
.t-TreeNav .a-TreeView-node--topLevel .a-TreeView-row.is-current--top,
.t-TreeNav .a-TreeView-node--topLevel ul,
.t-TreeNav .a-TreeView-node--topLevel:is-collapsible > .a-TreeView-row{
  background-color: transparent !important;
  background-image: none !important;
  background: transparent !important;
  box-shadow: none !important;
}

/* Also clear nested submenu containers (child menu background) */
.t-TreeNav .a-TreeView-node--topLevel ul ul,
.t-TreeNav .a-TreeView-node--topLevel ul[role="group"],
.t-TreeNav .a-TreeView-node--topLevel ul[role="group"] ul{
  background-color: transparent !important;
  background-image: none !important;
  background: transparent !important;
}

/* Fallback: clear any row wrapper backgrounds */
.t-TreeNav .a-TreeView-row,
.t-TreeNav .a-TreeView-row.is-hover,
.t-TreeNav .a-TreeView-row.is-selected,
.t-TreeNav .a-TreeView-row.is-focused{
  background-color: transparent !important;
  background-image: none !important;
  background: transparent !important;
  box-shadow: none !important;
}
