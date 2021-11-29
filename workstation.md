# Aorus Gigabyte Z490

## Sound problem

  $pacmd list-cards

* Check the results on "ports". If you can't see something related to speaker, it means sound card can't be recognized by pulseaudio.
* Edit "/usr/share/alsa/ucm2/HDA-Intel/HDA-Intel.conf" file. If you see an empty string after "Define.Use", just input "3" into the string. Then save it.
* Reboot your machine. If you still can't get any sound, check whether it's "Dummy Output" as your sound card. If so, add "options snd-hda-intel model=generic" to the end of "/etc/modprobe.d/alsa-base.conf".
