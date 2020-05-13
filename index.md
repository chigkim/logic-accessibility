Below you can find known accessibility issues on Logic for VoiceOver users.

This webpage is not associated with Apple any way. This is simply to track of issues that VoiceOver users discover while using Logic Pro.

If you find more issues, please [comment below](#disqus_thread). It will be added to the list when verified.

Version: Logic Pro X 10.5

---

## Bugs

### Record enable in track header 
When you check record enable for an audio track, VO (Voice Over) reports the status as checked only when the indicator is flashing.

This causes VO to report sometimes checked sometimes unchecked even though the track is record enabled.

If it's record enabled enabled, VO should report as checked all time.

### Channel strip type 
In mixer, tracks header, inspector, VO can't tell if it's an instrument, aux, audio, and so on.

VO users should hear their names along with their types when navigating across mixer/tracks area.

### Bypass 
When a plugin is activated, VO says "Bypass unchecked" in inspector and mixer, but it says "Bypass checked" in the plugin window. 

### Automation control
After pressing "a to show automation"  in track header, VO can get to the automation enable button only when approaching from left to right, and "show region based automation" can be reached only when VO approached from right to left. 

### Track alternative 
VO can't find track alternative UI element after you check track alternative from track header components. 

### Groove track 
In track header, VO can tell you which one is groove track, but you can't reassign another track as a groove track. 

### Selection report 
VO can't tell which regions/tracks are selected.

In either very early logic or garage band, it used to say either "selected region name" if selected or just "region name" when not selected. 

When multiple tracks are selected, it would be nice to indicate how many tracks are selected in the inspector how it does for regions.

### Playhead announcement 
It's great that VO announces the playhead location when playhead moves. However it is very distracting to hear playhead position whenever you play/stop especially when you try to do fine audio editing such as finding particular syllable from vocal track, attack of instrument, and so on.

It makes it hard to pinpoint exact audio spot when VO keeps chattering playhead position against audio playback.

It should announce the position when it stops, but not when it starts playing.

### Flex pitch/time 
Even though we can enable flex time/pitch and apply to a track. VO users have very limited capability of editing them. 

It would be nice to have key commands to move to next/previous, nudge, create, and delete flex marker with keyboard.

### Position in event list 
Whenever you change position column of an event in event list, VO cursor get booted out of the control. 

This forces VO users to keep interacting with the slider in order to make further adjustment.

### Midi environment 
In midi environment window, there are many unlabeled UI elements. 

### Project start marker
VO can't move project start marker in the tracks ruler. It simply appears as a button instead of slider.

### Control Toolbar LCD display
For punch in/out left/right locator, it has "000" front of actual value.

If it's bar 1 beat 1 division 1 tic 1, it should just read "1 1 1 1" instead of "000 1 1 1 1 ".

### Performance meter
Performance meter in lcd display is not accessible when you check it from customize control bar and display setting.

### HMS Playhead
When you change hour/minute/second of playhead In control toolbar LCD display with VO cursor, it sometimes reads MBT position instead of HMS.

Logic wants to announce MBT since it's moving, and VO wants to announce the value of the slide that it's moving. Two announcements are fighting each other.

### Multisampler 
In EXS24, VO users were able to edit zones, group, and many properties in edit window. However, it seems like we can't do that in multisampler.

It's being investigated by VO users, but at least it's not easily found how to do it.

If there's no way to do that now, it would be great to be able to do it similar to EXS24 in future updates. 

### Send
In inspector, send control has the word "button" in label, so it says "button" twice once from label again from role type. It says "send button button." 
  
### Group
In both mixer and inspector, group control always has the word "Off" even though assigned group is on.

When a track has no group assigned, it says "off group group" in inspector.

### VoiceOver Item chooser is broken in plugin window
When you bring up item chooser from a plugin window with control view, VO only gives few parameters instead of all parameters.

For example in Archemy, VO users are forced to literally spend more than 10 minutes to go through hundreds of items inside the table just to locate a parameter and turn off a feature in certain cases.

It's is crutial to let VO users to quickly locate specific parameter by searching.

---

## Suggestions

### Record enable
When you press control+r, VO just says "toggle track record enable".

It would be nice to say on or off status just like how VO now announces mute and solo status when pressing m or s. 
 
### Input monitor
When pressing control+i to toggle input monitor, it should announce the status like solo/mute.

### Confirm selection with audio 
It would be good to have a key command for logic to play to selection end.

Right now shift+space plays from the selection, but you can't confirm where the selection ends by listening.

You can move to selection end with control+end, but it would be nice to be able to confirm by listening the audio as well.

It would great to have a key command that starts playing from current playhead, and stops at the end of selection.

### Only allow VO to edit track/region name either after pressing vo+space or interact with the name
When VO cursor lands on a text field such as track name, the keyboard focus sometimes stays there even though you stop interact with header and go somewhere else.

This causes users to edit the name when pressing x to open mixer, e for open editor, and so on. You can easily end up with track name xe by mistake.

### Triggering to Play Live loop cell 
It would be nice to be able to trigger play by simly pressing vo+space on a cell without interacting with the cell.

 Playing live loop requires time sesitive interaction, so minimizing number of keyboard interaction is crutial.

### Live loop Cell status
Now cells says "selected looping, play/stop", and you have to interact with it in order to check it's playback status. 

It would be nice to be able to tell if a cel is playing or not without interacting with it.

### Plugin window 
Now plugin window only has name of the track. It would be nice to have name of the plugin in the window name as well. 

Especially this would be very helpful for automation script to identify which plugin window is open. 

### General UI element description 
Some of the controls only have value. It would be nicer if it has label as well value. 

For example, if output of channel strip is assigned to a bus, it just says "bus 1 button". It would be nice to say "bus 1, output button".

It's Same for input, send, insert, and so on. 

* Input: "Input 1" as value, "input" as label, and "popup button" as role. Then it'll say "Input 1 input popup button". 
* Insert: "Channel eq" as value, "Plugin" as label, "group" as role. Then it should read "Channel EQ Plugin Group" 
* Send: "Bus 1" as value, "Send" as label, "group" as role. Then it'll read "bus 1 send group". 

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
                            
