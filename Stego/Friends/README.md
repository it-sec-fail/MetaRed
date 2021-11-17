# Friends
Bielsa: 'Everything is allowed, except stop fighting'

## Todos

Like always - I check strings and exiftools and the file itself!
But no command give us something.

```shell
$ ~ # file messi.jpg 
messi.jpg: JPEG image data, JFIF standard 1.01, aspect ratio, density 1x1, segment length 16, baseline, precision 8, 720x628, components 3

exiftool messi.jpg > messi.jpg_exifdata

strings messi.jpg > messi.jpg_strings
```

Then I checked it with `stegcracker`.
```shell
stegcracker messi.jpg ~/Documents/Tools/SecLists/Passwords/xato-net-10-million-passwords-1000000.txt
[...]
Successfully cracked file with password: Messi6wyougues
Tried 632584 passwords
Your file has been written to: messi.jpg.out
Messi
```
And got what I need!

```shell
$ ~ # cat messi.jpg.out                                                                                                                    ✔  4m 9s  
flag{WarmUp_Ch4ll3ng3}
```

> flag{WarmUp_Ch4ll3ng3}
