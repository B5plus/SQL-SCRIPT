


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
