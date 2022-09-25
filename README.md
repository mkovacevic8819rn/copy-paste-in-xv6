# copy-paste-in-xv6
<p align="justify">
The purpose of this project was to edit the xv6 system so it could support copy and paste functions in a terminal. There needed to be a clear distinction when a user has entered copy mode; selection and copying of the selected text needed to be enabled, as well as pasting the previously selected text. Special attention was given to ensure the current system functions and work was not affected, resulting in the system crashing down. 

Copy mode is entered when a user presses the key combination **shift + alt + c**. Once in copy mode, the user can move the cursor up and down, left or right using the **w**, **s**, **a** or **d** keys, respectively. To mark the beginning of the selection of text, the user presses the **q** key. In case we have already begun the selection, the **q** key does nothing. To mark the ending of the selection, the **e** key is used. The **e** key also does nothing if we have already begun the selection. The user exits the selection mode using the **shift + alt + c** key combination. 

Selection begins with the pressed **q** key, only when in copy mode. Attention was paid so that if the user moves forward from the starting position (this includes going right or down), character in the starting position has to be included in the selection; however, if the user moves backwards (left or up), character in the starting position is not included in the selection. Upon exiting the copy mode, the cursor resets to the position it was at before entering copy mode.

Paste functionality needs to be enabled only when the user isn’t in copy mode, and only in case the user has previously used copy mode. Using the key combination **shift + alt + p**, the user pastes the selected text at the current position. 
</p>
