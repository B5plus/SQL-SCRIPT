If it STILL doesn’t work (fast test)

We will quickly check if APEX is receiving your selected roles.

Step 7 — Add a quick “test message” (no coding skills needed)

Page Designer → Processing

Right click Processes → Create Process

Type: PL/SQL Code

Name it: TEST_ROLE_VALUE

Process Point: After Submit

Sequence: 30

Paste this:

apex_error.add_error(
  p_message => 'Roles selected = ' || nvl(:P4_ROLE_IDS,'(NULL)'),
  p_display_location => apex_error.c_inline_in_notification
);


Save → Run → Create user → select roles → Create.

What you will see:

If it shows (NULL) → your checkbox value is not being submitted (we fix the checkbox settings)

If it shows 1:2:3 → roles value is coming, then we check table constraints/triggers

Very important question (so I finalize the fix immediately)

After you create the user and click Create:
✅ Does it show any error message at the top?
And when you edit the same user again, do you see the roles automatically ticked or not?

If you answer those 2 things, I’ll tell you the exact final adjustment (checkbox settings vs insert constraint issue).
