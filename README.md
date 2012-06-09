JComments-2.3.0-stable
======================

JComments project homepage:

   http://www.joomlatune.com/jcomments-downloads.html
   http://extensions.joomla.org/extensions/contacts-and-feedback/articles-comments/9985

JComments 2.3.0 fork homepage:

   http://www.github.com/kloverde/JComments-2.3.0-stable

Description:

   This fork of the JComments 2.3.0 Joomla extension corrects a usability issue which affects
   the visibility of status notifications.  It also fixes some CSS issues which corrupt the
   display of elements in Chrome.
  
   Status notification fix:
 
   Upon clicking Send, the user is presented with a message giving feedback on the status of
   his or her submission.  The message could indicate the comment has been accepted pending
   moderation, rejected due to an incomplete form, etc.  This message is held in a div at the
   top of the form.  The message displays and then, after several seconds, fades from view
   until it disappears.
   
   There is a small flaw with this system.  If the div is not in the active region of the
   browser window at the moment it appears, the user will never see the message.  This fork
   addresses this issue by jumping to the status message after the user clicks Send.

   CSS fix:

   The CSS for comment policy had incorrect values for lists.  UL and OL had a line-height
   of 5px, which didn't make sense because they shouldn't have a height property at all --
   the height should be determined by the number of elements in the list.  List items (LI)
   also had a line-height of 5px, which was physically smaller than the specified font size
   of 1em.

