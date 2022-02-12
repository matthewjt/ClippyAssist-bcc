I am not the original author.  I simply updated this to work with TBC.

See https://www.curseforge.com/wow/addons/clippy-assist for the original.

 

Clippy is back, and here to hang out with you in World of Warcraft! He's draggable anywhere on your screen, and he'll do his best to be a good friend. He can also display any text through a custom WeakAura interface, as a simple custom action.

The addon has a number of slash commands, which can be viewed by typing /clippy -help.

Slash Commands
/clippy -help: Lists all commands.
/clippy -hide: Temporarily hide Clippy.
/clippy -show: Show Clippy (if hidden).
/clippy -reset: Resets Clippy's position.
/clippy -list: Lists all available animations.
/clippy{everything else}: Attempts to play that animation.
WeakAura Support
A list of pre-made sample WeakAuras can be found here on Wago.io.

Clippy can display any text, using the full power of any regular WeakAura! This is accomplished with a custom Action.

In your desired WeakAura, go to the "Actions" tab.
Under the "On Show" category, check the "Custom" option.
Check that Clippy is loaded with ClippyAssist.isReady().
Display text with ClippyAssist.SetText(msg, duration).
It's that easy! msg can be any text you'd like to display, and duration is counted in seconds.

Here's an example:

if ClippyAssist and ClippyAssist.isReady() then

local message =

"It looks like you're trying to write a letter." .. "|n|n" ..

"Would you like some help with that?"

ClippyAssist.SetText(message, 10.0)

OR

ClippyAssist.SetTextAnimation(message, "GestureDown2", duration)

end