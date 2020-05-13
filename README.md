# logic-accessibility
Here are accessibility issues for VoiceOver users.
Version: Logic Pro X 10.5

## Bugs

### Record enable in track header 
When you check record enable for an audio track, VO (Voice Over) reports the status as checked only when the indicator is flashing. Thus VO says sometimes checked sometimes not checked even though the track is record enabled. If it's enabled, VO should report as checked all time.

### Channel strip type 
In mixer, tracks header, inspector, VO can't tell if it's an instrument, aux, audio, and so on until you actually interact with the track and investigate the contents inside. 

### Bypass 
When a plugin is activated, VO says "Bypass unchecked" in inspector and mixer, but it says "Bypass checked" in the plugin window. 

### Automation control
After pressing "a to show automation"  in track header, VO can get to the automation enable button only when approaching from left to right, and "show region based automation" can be reached only when VO approached from right to left. 

### Track alternative 
VO can't find track alternative UI element after you check track alternative from track header components. 

### Groove track 
In track header, VO can tell you which one is groove track, but you can't reassign another track as a groove track. 

### Selection report 
VO can't tell which regions/tracks are selected. It would be amazing if you can toggle track/region selection with vo+space instead of Logic automatically selecting whichever VO cursor lands on. 
In either very early logic or garage band, you could toggle a selection with vo+space on a region, and it used to say either "selected region name" if selected or just "region name" when not selected. 

### Non-contiguous selection 
VO users can only select regions (with shift+left/right) and tracks (with shift+up/down) that are next to each other. 
If the selection behavior works as described above, it would address this problem as well. 

### Playhead announcement 
It's great that VO announces the playhead location when playhead moves. However it is very distracting to hear playhead position whenever you play/stop especially when you try to do fine audio editing such as finding particular syllable from vocal track, attack of instrument, and so on. It's hard to pinpoint exact audio spot when VO keeps chattering playhead position against audio playback. It would be even ok if it announces when it stops, but not when it starts playing. 
Maybe the playhead should be only announced when user manually move it with key commands like rewind/forward, rewind/forward by transient, rewind/forward by division, go to left/right locator, go to next/previous marker, and so on. 

### Flex pitch/time 
Even though we can enable flex time/pitch and apply to a track. VO users have very limited capability of editing them. 
It would be nice to have key commands to move to next/previous, nudge, create, and delete flex marker with keyboard.

### Position in event list 
Whenever you change position column of an event in event list, VO cursor get booted out of the control. 
It's really nice it doesn't do that for length and velosity anymore 

### Midi environment 
In midi environment window, there are many unlabeled UI elements. 

### Group
In both mixer and inspector, group control always has the word "Off" even though assigned group is on.
When a track has no group assigned, it says "off group group" in inspector.

### Project start marker
VO users can move project end marker from ruler, but we can't move project start marker. It simply appears as a button instead of slider.

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
 
### Suggestions

### Record enable
When you press control+r, VO just says "toggle track record enable". It would be nice to say on or off status just like how VO now announces mute and solo status when pressing m or s. 
 
### Input monitor
When pressing control+i to toggle input monitor, it should announce the status like solo/mute.

### Confirm selection with audio 
It would be good to have a key command for logic to play only the selection. Right now shift+space plays from the selection, but you can't confirm where the selection ends by listening. You can move to selection end with control+end, but it would be nice to be able to confirm by listening the audio as well.

### Live loop cell 
It would be nice to be able to trigger play by simly pressing vo+space on a cell. Now you have to interact with the cell and press play. 
Also it would be nice for cells to indicate whether it's playing or not. Now cells says "selected looping, play/stop". You have to interact with it in order to check it's playback status. 
 
### Plugin window 
Now plugin window only has name of the track. It would be nice to have name of the plugin in the window name as well. 
Especially this would be very helpful for automation script to identify which plugin window is open. 

### General UI element description 
Some of the controls only have value. It would be nicer if it has label as well value. 
For example, if output of channel strip is assigned to a bus, it just says "bus 1 button". It would be nice to say "bus 1, output button". 
Same for input, send, insert, and so on. 
* Input: "Input 1" as value, "input" as label, and "popup button" as role. Then it'll say "Input 1 input popup button". 
* Insert: "Channel eq" as value, "Plugin" as label, "group" as role. It should read "Channel EQ Plugin Group" 
* Send: "Bus 1" as value, "Send" as label, "group" as role. Then it'll read "bus 1 send group". 

### Send
In inspector, send control has the word "button" in label, so it says "button" twice once from label again from role type. It says "send button button." 
 
### Only allow VO to edit track/region name either after pressing vo+space or interact with the name. 
When VO cursor lands on a text field such as track name, the focus sometimes stays there even though you stop interact with header and go somewhere else.
Then you accidentally start editing the name when you press x to open mixer, e for open editor, and so on.  
