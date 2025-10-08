# Zahard's Welcome

## Challenge Description

The base of Citadel rises before you, its great doors sealed with fractured steel and dead circuitry. Faded corporate protocols still hum in the lock, relics of the world that fell.

Those who came before tried to climb but all failed. Their echoes linger as fragments of voices, reminders of broken attempts to free humanity. Now you have chosen to take their place. You will be the one to scale the Citadel and finish what they could not.

The voices of the fallen whisper through the static: "The path begins in the gathering place. There, candidates are chosen". Here is your invitation.

Step into the gathering place where all climbers are briefed before the ascent.

## Solve

**Flag:** `citadel{7h3_c174d3l_b3ck0n5}`

This challenge was a nice welcome. It said to go where "all climbers were briefed before the ascent" and I remembered that all participants were asked to join the discord server. I checked the official channels and found the flag hiding at the top of the rules section.



# The Social Network

## Challenge Description
🗼OSINT pt1: The ascent begins. The first floor is not metal or binaries but of memory. Among the echoes, one voice lingers, of an early climber. He was among the earliest to challenge the Citadel, and though he failed, his traces remain scattered across the ruins of the old world.

It is said that the key to the next floor can be found by tracing the socials of this legendary climber.

Start by checking out citadweller on Instagram.

## Solve
**Flag:** `citadel{17_1s_jus7_7h3_b3g1nn1ng}`

I thought this challenge was a nice way to ease into the ctf. The description gave me the first instruction which was to stalk the citadweller on instagram. After finding the account, I noticed the highlight on the page and opened it to find the first part of the flag and another instruction. That clue led me to the citadweller's X account which gave me the second part of the flag.

## New Learnings
I learned what OSINT meant (Open source intelligence) and was able to get a small taste of what an OSINT challenge would be like.



# track 8

## Challenge Description
Bypassing the second chamber leads to an empty floor except for a single artifact in the center: an old MP3 player, scratched and worn. On its surface, a cipher is etched, a message left behind for anyone who can decode it

`twj eys zpr ukm 'viamnwqw' bx lzgo: esmqqui{yyr_oshwwcm_bwupa}`

When you power it on, the sound fills the chamber. The tracks play like whispers from a lost world, and you recognize it as a song from Panchiko’s latest studio album, particularly track no. 8. Its title feels familiar, hinting at a famous cipher. Decrypt it by using the album name as your key and continue your ascent.

## Solve
**Flag:** `citadel{add_vinegar_twice}`

The clue from the description was to look at Panchiko's latest album: Ginkgo. We had to particularly look at track 8 which was "Vinegar". Now I didn't know what cipher vinegar was supposed to hint at so I just googled "Vinegar cipher" only to find out that the cipher I was supposed to use was "Vinegere". After I realized that, I realized I could find an online decoder tool and, as the description said, use "Gingko" as my key. It turned out that the decoded text tossed me another challenge to decipher the flag using the same cipher but with "Panchiko" as the key. After decoding the vinegere cipher twice, I got the flag. 

## New Learnings
I learned what the vingere cipher was and kind of looked into how it works as well. It's a way to encrypt messages using a keyword that essentially decides how much you shift the message. 



# Omniscient Flag's Metadata

## Challenge Description
As you step into the second chamber, a figure manifests. Before you stands a forgotten deity, a dead god spoken of only in whispers. Known by countless names: “Apostle of Epilogue and Eternity”, “Lone Messiah” and many more lost to time.

They leave nothing but a single image, a relic carrying his final secret. Hidden within its layers lies the key to ascend to the next chamber.

## Solve
**Flag:** `citadel{th1s_ch4ll3ng3_1s_f0r_th4t_0n3_ex1ft00l_4nd_b1nw4lk_enthus14st}`



## New Learnings




# Test of Sweetness

## Challenge Description
This floor feels like a digital world. The space is an illusion, all pink and sweet, stretching around you in impossible patterns. Here, you are no longer a climber but just another user.

Ahead, a door glows faintly. It is the only path forward and requires a level of authority you do not yet have. Fragments of session memory flicker, hinting at what it might take to gain higher access.

## Solve
**Flag:** `citadel{fru1tc4k3_4nd_c00k13s}`


## New Learnings




# Rotten Apple

## Challenge Description
Among the debris of this floor, you find a relic of sound: An album which turns out to be D>E>A>T>H>M>E>T>A>L by Panchiko, a long lost album. But the music is warped, as though it has undergone disc rot.

The path forward is hidden in the distortion. Similar to how the album was warped, the password to the next floor has been warped first by a factor of 47, then by a factor of 13. Untangle these changes to reveal the code and continue your ascent.

## Solve
**Flag:** `citadel{b3tt3r_ROTt3n}`

The challenge description hinted at two layers of transformation: first ROT47, then ROT13. Since ROT13 is its own inverse, I could undo that part immediately. Taking the given string and running it through ROT13 gave me:

`4:E256=L3bEEbC0#~%Eb?N
`

Then I applied ROT47 (because it's also its own inverse), which rotates all printable ASCII characters by 47 positions. That final decoding revealed the flag.

## New Learnings
I got to learn about ROT47, which is like ROT13 but works on a much bigger set of characters. Instead of only shifting A–Z, ROT47 rotates all printable ASCII characters.



# Randomly Accessed Memories

## Challenge Description
On your ascent to this floor, you hear these fragments being played back
```
clone it, pull it, reset it, stage it,
commit, push it, fork, rebase it,
merge it, branch it, tag it, log it,
add it, stash it, diff, untrack it.
```
You look around and discover a chamber containing a vast archive of Daft Punk’s music, intertwined with cryptic commits left behind by other musicians. They seem ordinary at first glance, but not everything in the history is what it seems.

## Solve
**Flag:** `citadel{w3_4r3_up_4ll_n1t3_t0_g1t_lucky}`


## New Learnings




# Selected Ambient Work

## Challenge Description
The symphonic adventure does not end here. On the next floor, a single song keeps echoing through the floor, repeating in a haunting loop. Amid the sound, you find a note left by a past candidate. It hints that the song holds a secret message, hidden in plain sight, much like how Aphex Twin concealed his face within his music with the help of spectrograms.

To move forward, you must find the message hidden in this sound.

Note: Separate the words in the flag with _ and make it UPPERCASE. Example: citadel{S3L3CT3D_AMB13NT_W0RK}

## Solve
**Flag:** `citadel{1_LOV3_1DM}`

This challenge produced a .wav file that had a bunch of ambient noise with a clear message: a bunch of morse code bleeps. However, I couldn't just run it through a morse translator because of the ambient music. So I used a spectogram tool to find out which frequencies the morse code tones were producing. This part was kind of cool because I could see the morse patterns in the audio waves. Technically, if I was experienced enough, I could've used the patterns to decode the message but that would've taken too long as the audio was over a minute long. So, I used an equalizer to isolate the morse code sounds and ran the filtered audio through a translator. It turns out the message was a bunch of information about Richard David James but there was one part of the message that didn't look like it belonged: "1 LOV3 1DM". That looked suspicious so I tried that out as the flag, and it worked.

## New Learnings
I learned how to use a spectogram and equalizer, and who Richard David James is.



# The Robot's Work

## Challenge Description
You enter a virtual maze, a labyrinth of shifting corridors and endless paths. A guardian robot patrols the floor, leaving a trail behind as it moves. Follow the path it carves, trace its movements carefully, and uncover the key it leads you to. Only by following the robot’s trail can you reach the door to the next floor.

## Solve
**Flag:** `citadel{p4th_tr4v3rs4l_m4st3ry_4ch13v3d}`


## New Learnings




# Rotting in the Deep
The floor is quiet, almost unnervingly so – like the Citadel has paused to take your measure. A soft ring of presence settles around the chamber, the kind that marks a true landing: from here, it will ask for more and, in return, grant more. Etched into its surface is a sequence of numbers, worn and faint, as if time itself is eating them away. A whisper from the echoes guides you:

The message lies beneath the surface. Push it three steps forward in the cycle of life, and only then will the words emerge from the void.

## Solve
**Flag:** `citadel{br0_r34lly_unr0tt3d_m3_b4ck_t0_l1f3}`

This challenge came with two files: chal.py and out.txt. After reading both I knew that out.txt was the output of chal.py. Chal.py was the program that encrypted the flag by first converting the bytes of the flag to an integer and that integer to a string. Then it performed a caesar shift on the string, moving all digits with a key of 3 (added 3 to each digit). I was having trouble figuring out how to decode the integer after undoing the caesar cipher, because I was unable to install the same library and module chal.py used to encode the flag (cryptodome). Additionally I couldn't find a website that handled such a long integer either and found that I could use python to solve this in one go. So I used the following program:
```
def long_to_bytes(n):
    """Convert a long integer to bytes"""
    if n == 0:
        return b'\x00'
    return n.to_bytes((n.bit_length() + 7) // 8, 'big')

KEY = 3
encrypted = "6895840967002953721051398351211751734500850509315790892845302801984496338433523326225010635779036738800318"

# Reverse the digit shift
decrypted_digits = ""
for digit in encrypted:
    decrypted_digits += str((int(digit) - KEY) % 10)

# Convert to integer then to bytes
decrypted_number = int(decrypted_digits)
flag_bytes = long_to_bytes(decrypted_number)

print(flag_bytes.decode())
```
I ran this and was able to get the flag.



# Coco Conjecture

## Challenge Description
The door to the next floor is guarded by a figure who calls herself "The Dragon CEO". She does not speak of mercy or choice, only of order and efficiency.

To enter the next chamber, you must complete the task presented by her. Complete it exactly as instructed, achieving operational efficiency by her standards, and the path forward will open.

Connection: nc chall_citadel.cryptonitemit.in 61234

## Solve
**Flag:** `citadel{k1ryu_c0c0_h4s_4_g0_4t_4n_uns0lv3d_m4th3m4t1cs_pr0bl3m}`




# schlagenheim

## Challenge Description
Your quest continues, but you feel something odd about this room. The only artifact on this floor is a corrupted file held in the hands of a jet-black statue, frozen in the pose of a band mid-performance. The passcode to the next floor is hidden within this piece of music, but it can’t be played, as if the wrong extension has scrambled it.

You must take the corrupted file and repair it to reveal the true code that will unlock the door forward.

## Solve
**Flag:** `citadel{8lackM1D1wa5c00l}`

This challenge came with a mysong.wav file. I first tried to look at the file's signature by running `file mysong.wav` in the terminal. That returned the type as generic "data" meaning the shell wasn't able to identify the file signature. So I used `hexdump -C mysong.wav` in order to see the magic bytes. The hex code was `4d 31 44 31` which doesn't match any file type but I noticed that it read M1D1 in ASCII. That told me that the file was supposed to be a midi file and thus I tried to edit the file signature by using `hexedit mysong.wav` in order to change the magic bytes to the regular midi file signature `4d 54 68 64`. After this I redefined the file type using `mv mysong.wav mysong.mid`. This meant I was able to play the file, but in order to see the patterns that MIDI sequences have I used an online midi player and saw that the pattern displayed was the flag.

## New Learnings
I learned that file signatures were defined using magic bytes.



# XOR Slide

## Challenge Description
You realise that a previous climber has set up a puzzle in what was otherwise an empty room, blocking the entrance to the next floor on the ceiling. You must slide the blocks forming the pyramid to create a path above.

## Solve
**Flag:** `citadel{pyr4m1d+x0r}`



# The Sound of Music

## Challenge Description
🗼OSINT pt2: citadweller had a newfound interest in tracking the music they last listened to and posting ratings of new albums on various online platforms.

The flag is hidden in these digital footprints across music platforms and split into three segments. You will need to find all three to uncover the complete code and move on to the next floor.

## Solve
**Flag:** `citadel{c0mputers_st0pped_exchang1ng_1nf0rmat10n_n_started_shar1ng_st0r1es_n_then_they_were_n0where_t0_be_f0und}`

This challenge was easy because we'd already found the last two parts while stalking the citadweller in OSINT pt1. We first found part 2 on rateyourmusic and found part 3 on spotify. Part 3 took us a bit but we finally found it on lastfm and combined all 3 parts to get the complete flag



# Echoes and Pings

## Challenge Description
You come across the remnants of a fallen corporation and the final network communication ever sent by them.

Allegedly, the message contained an image that predicted the rise of the Citadel. Your task is to uncover what was sent and decode the communication to extract the passcode that will unlock the next floor.

## Solve
**Flag:** `Citadel{l_r34lly_w4nt_t0_st4y_4t_y0ur_h0us3}`


