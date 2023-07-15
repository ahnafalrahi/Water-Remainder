# Water-Remainder

# The Final Exercise

import time
import win32com.client as wincl
print("What shall I remind you about?")
text = str(input())
print("In how many minutes?")
local_time = float(input())
local_time = local_time * 60
time.sleep(local_time)
print(text)

#---------------------------------
speaker_number = 1
spk = wincl.Dispatch("SAPI.SpVoice")
vcs = spk.GetVoices()
SVSFlag = 11
print(vcs.Item (speaker_number) .GetAttribute ("Name")) # speaker name
spk.Voice
spk.SetVoice(vcs.Item(speaker_number)) # set voice (see Windows Text-to-Speech settings)

#--------------------------------

from winotify import Notification,audio
 
pop_message = Notification(app_id= "Time to drink water",
                           title="massage title",
                           duration="long",
                          )
    

pop_message.set_audio(audio.LoopingAlarm10,loop=False)

pop_message.add_actions(label="Clik For Stop")
#using voice module is optional
pop_message.show(),spk.Speak(f"time to drink water{text}")
