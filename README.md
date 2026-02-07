/* ==== FORCE REMOVE Grey Strip from Universal Theme TreeNav styleA ==== */
#t_TreeNav.t-TreeNav--styleA .a-TreeView-row,
#t_TreeNav.t-TreeNav--styleA .a-TreeView-row.is-hover,
#t_TreeNav.t-TreeNav--styleA .a-TreeView-row.is-selected,
#t_TreeNav.t-TreeNav--styleA .a-TreeView-row.is-focused{
  background: transparent !important;
  background-image: none !important;
  box-shadow: none !important;
  outline: none !important;
}

#t_TreeNav.t-TreeNav--styleA .a-TreeView-row::before,
#t_TreeNav.t-TreeNav--styleA .a-TreeView-row::after{
  content: none !important;
}
