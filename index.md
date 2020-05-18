Below you can find known accessibility issues on Logic for VoiceOver users.

This webpage is not associated with Apple any way. This is simply to track of issues that VoiceOver users discover while using Logic Pro.

If you find more issues, please [comment below](#disqus_thread). It will be added to the list when verified.

Version: Logic Pro X 10.5

---

## Bugs

### Inconsistent status of Record enable in track header
When you check record enable for an audio track, VO reports the status as checked depending on when the indicator is flashing. This causes VO to report sometimes checked sometimes unchecked even though the track is record enabled. If it's record enabled, VO should always report as checked.

### Cannot distinguish channel strip type
In mixer, tracks header, and inspector, VO cannot tell if a channel strip is an instrument, aux, audio, and so on. VO users should hear their names along with their types when navigating across mixer/tracks area.

### Inconsistent plugin bypass status
When a plugin is active, VO says "Bypass unchecked" in inspector and mixer, but it says "Bypass checked" in the plugin window.

### Cannot locate automation control consistently
After pressing "a to show automation"  in track header, VO can get to the automation enable button only when approaching from left to right, and "show region based automation" can be reached only when VO approached from right to left.

### Track alternative control is not visible to VO
VO cannot find track alternative control after you check track alternative from track header components.

### Cannot assign a track as a groove track
In track header, VO can tell which one is groove track, but you cannot reassign another track as the groove track with VO.

### Cannot tell which tracks/regions are selected
It would be great if it says "selected region/track name" if selected or just "region/track name" when not selected.

###Cannot find track Selection Count
When multiple tracks are selected, it would be nice to indicate how many tracks are selected in the track inspector same as how it appears for region inspector.

### Distracting playhead announcement
It is great to announce the playhead location when playhead moves. However, it is very distracting to hear playhead position whenever you play/stop especially when you try to do fine audio editing such as finding syllable from vocal track, attack of instrument, and so on. It makes it hard to pinpoint exact audio spot when VO keeps chattering playhead position against audio playback. It should announce the position when it stops, but not when it starts playing.

### Can't edit flex pitch/time markers
Even though we can enable flex time/pitch and apply to a track. VO users have very limited capability of editing them. It would be nice to have key commands to move to next/previous, nudge, create, and delete flex marker with keyboard.

### VO Cursor gets bootted out of position Column in event list
Whenever you change position column of an event in event list, VO cursor get booted out of the control. This forces VO users to keep interacting with the slider in order to make further adjustment.

### Cannot access midi environment
In midi environment window, there are many unlabeled UI elements.

### Cannot adjust project start marker
VO cannot adjust project start marker in the ruler. It simply appears as a button instead of a slider.

### Strange values for punch and Locators in Control Toolbar LCD display
Punch in/out left/right locator in control toolbar have "000" front of actual value. If it is bar 1 beat 1 division 1 tic 1, it should just read "1 1 1 1" instead of "000 1 1 1 1 ".

### Cannot access performance meter in Control Toolbar
Performance meter in LCD display is not accessible when you check it from customize control bar and display setting.

### Wrong announcement in HMS Playhead in Control Toolbar
When you change hour/minute/second of playhead in control toolbar LCD display with VO cursor, it sometimes reads MBT position instead of HMS. Logic wants to announce MBT as playhead moves, and VO wants to announce the value of the slider. Two announcements are fighting each other.

### Cannot edit zones in Multisampler
In EXS24, VO users were able to edit zones, group, and many properties in edit window. However, it's not possible with VoiceOver in Multisampler.

### VO reads "send button button."
In inspector, send control has the word "button" in label, so it says "button" twice once from label again from role type. It says "send button button."
  
### Group Control always has the word "off" in the label
In both mixer and inspector, group control always has the word "Off" even though assigned group is on. When a track has no group assigned, it says "off group group" in inspector.

### Cannot search all UI elements with Item chooser in plugin window
When you bring up VO item chooser from a plugin window with control view, VO only gives few parameters instead of all parameters. For example in Alchemy, VO users are forced to go through hundreds of items inside the table just to locate a parameter and turn off a feature in certain cases. It is crucial to let VO users to quickly locate specific item by searching.

### Cannot access global tracks
Some of them (tempo, signature, and marker) have list view, but other global tracks such as arrangement have no other workaround.

### When pressing command+s, VO says nothing
VO should say "save" to confirm the action like how it does for copy and cut.

---

## Suggestions

### When pressing control+r, it doesn't speak the status
It should say on or off status just like how VO now announces mute and solo status when pressing m or s.
 
### When pressing control+i to toggle input monitor, VO says nothing
It should announce the on/off status like solo/mute.

### Cannot confirm selection with audio
There should be a key command for logic to play to selection end. Sshift+space plays from the selection, but you cannot confirm where the selection ends by listening. You can move to selection end with control+end, but it would be nice to be able to confirm with audio as well.

### Should only allow VO to edit track/region name either after pressing vo+space or interact with the name
When VO cursor lands on a text field such as track name, the keyboard focus sometimes stays there even though you stop interact with header and go somewhere else. This causes users to edit the name when pressing x to open mixer, e for open editor, and so on. You can easily end up with track name xe by mistake.

### Minimize keyboard interaction to trigger a loop cell
Now, you have to interact with a cell and press play in order to trigger the cell. Playing live loop requires time sensitive interaction, so minimizing number of keyboard interaction is crucial.

### Live loop Cell should indicates playing status
Now cell says "selected looping, play/stop", and you have to interact with it in order to check it's playback status. It would be nice to be able to tell if a cell is playing or not without interacting with it.

### Plugin window name should have plugin name
Plugin window only has name of the track. It would be nice to have name of the plugin in the window name as well. Especially this would be very helpful for automation script to identify which plugin window is open.

### Input, plugin, send, output should have clearer label
Some of the controls only have value. It would be nicer if it had label as well as value. For example, if output of channel strip is assigned to a bus 1, it just says "bus 1 button". It would be nice to say "bus 1, output button". It is Same for input, send, insert, and so on. If assign "input 1" as value, "input" as label, and "popup button" as role, it should say "Input 1 input popup button". If assign "Channel eq" as value, "Plugin" as label, "group" as role. Then it should say "Channel EQ Plugin Group". If assign "Bus 1" as value, "Send" as label, "group" as role, it should say "bus 1 send group".

---

## Comments
<div id="disqus_thread"></div>
<script>

/**
*  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
*  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables*/
/*
var disqus_config = function () {
this.page.url = "https://chigkim.github.io/logic-accessibility/";
this.page.identifier = "                            logic-accessibility";
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');
s.src = 'https://logic-accessibility.disqus.com/embed.js';
s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
                            

                            
