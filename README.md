


/* ===== KILL GREY STRIP (APEX TreeView row states) ===== */
#t_TreeNav .a-TreeView-row,
#t_TreeNav .a-TreeView-row.is-hover,
#t_TreeNav .a-TreeView-row.is-selected,
#t_TreeNav .a-TreeView-row.is-focused{
  background: transparent !important;
  background-image: none !important;
  box-shadow: none !important;
  outline: none !important;
}

/* If strip is drawn via pseudo elements */
#t_TreeNav .a-TreeView-row::before,
#t_TreeNav .a-TreeView-row::after{
  content: none !important;
}





/* --- Child menu strip fix (submenu rows) --- */
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row.is-hover,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row.is-selected,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row.is-focused{
  background: transparent !important;
  background-image: none !important;
  box-shadow: none !important;
}

#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row::before,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-row::after{
  content: none !important;
}

/* Some builds paint the strip on the CONTENT inside child rows */
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content.is-hover,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content.is-selected,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content.is-focused{
  background: transparent !important;
  background-image: none !important;
  box-shadow: none !important;
}



#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content a,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content a:hover,
#t_TreeNav.t-TreeNav--styleA .a-TreeView ul ul .a-TreeView-content a:focus{
  background: transparent !important;
  box-shadow: none !important;
}



/* ===== Remove Vista/UT style background #c5bbbb from topLevel containers ===== */
.t-TreeNav .a-TreeView-node--topLevel ul,
.t-TreeNav .a-TreeView-node--topLevel:is-collapsible > .a-TreeView-row,
.t-TreeNav .a-TreeView-node--topLevel .a-TreeView-row.is-current--top{
  background-color: transparent !important;
  background-image: none !important;
  box-shadow: none !important;
}

/* If the submenu container still shows a strip, force transparent on nested UL too */
.t-TreeNav .a-TreeView-node--topLevel ul ul{
  background-color: transparent !important;
  background-image: none !important;
}


