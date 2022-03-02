# firebase-real-time-collaborative-text-editor
This is a real time, collaborative text editor I created myself from scratch; it utilizes nothing but Firebase!

To try the live demo, check out https://simplexshotz.github.io/firebase-real-time-collaborative-text-editor/

Note that you should use different UIDs if testing it on multiple devices. In an real-world setting, you would likely use Firebase Auth, which generates UIDs automatically for each user, which is perfect for this!

All code is free to use.

Currently, it only supports entering and deleting text (at any position), but I plan to add support for selections, cutting/pasting, cursor/active user display, and more.

Also of note: the program will (rarely, but it still happens occasionally) get out of sync. The way to fix this is quite simple: just pull the most up-to-date-content once the input field is blurred and pending changes have been pushed (since the content is no longer being edited by the user, meaning we don't care about the cursor position).

I would also like to get line breaks working, but they're quite finicky in HTML for some reason. Doing something similar to what I did with spaces (change them to Unicode character 160, a non-breaking space) might work. Another way to get line breaks working would be to create a new document for each new-line entered, which does work, but is less user-friendly.
