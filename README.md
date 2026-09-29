# **UPDATE:** Midna's scritches are memory-safe now!

You can get your scritches without worrying about the game crashing! There's a setting you need to change in dolphin so read the quick instructions for installing bellow.

# **How do install it?** 

Well buckle up buttercup and I'll tell you! 

**1. Dolphin Memory settings**
First open up Dolphin, go to Config, Advanced, and then check "Enable Emulated Memory Size Override." Then bump the first (MEM1) slider up to **28MB** specifically. Any less or more and the game will probably crash.

![increasing the MEM1 slider to 28MB as described above](https://cdn.discordapp.com/attachments/1156676738416390264/1554332899426308188/image.png?backend=b2&ex=6abc80d1&is=6abb2f51&hm=5090241a28d695ac9f48bf2a30cfb17c033fc9a1314d04d9c52205baac946744&)

*Turn this off before you emulate other games as it can mess em up!*

**2. Patching your ISO**
You need the [Gamecube File Tools (GCFT)](https://github.com/LagoLunatic/GCFT) and a copy of the ISO that you didn't get from the piracy fairies, no, no, no! Only legal and legitomato! 

It can be the Linkle modded iso, that's what we used (credit to the creators, it's so beautiful). Open up GCFT, click _Import GCM_ , pick your iso. 

![Screenshot of Gamecube File Tools with the buttons described in the instruction highlighted in red](https://64.media.tumblr.com/6db72e24cbf9b4e97a61772fa57c38a1/9d7e0cb24a762870-c3/s2048x3072/3afb4b7818ca0bc178b583683cfd5c1002e3b501.pnj)

Then click _Add/Replace files from folder_ and pick my little folder ("midna_scritches_patch", it should have "files" and "sys" folders in it). Note that this _won't_ override your original ISO. When you're done, click _Export GCM_ . This will let you save a new copy of the ISO with my little scritches anim in it! Boot that baby up and Receive <3. 

# **What is the mod?**

X) this is an idle animation mod for midna you can add to your gamecube ISO for Twilight Princess! We worked Many hours on it, it was made to be enjoyed by ourselves and anyone who finds it beautiful, so if that's you, please Enjoy this hon, i mean that with all my heart, ok? alright sweetheart let gets you good to go

You can see what the animation looks like [here](https://youtu.be/iH-9HokRIvs)

# **What does it do to the game?** 

**1. It replaces 2 of Midna's idle animations** : the one where she rotates how she's sitting and looks backwards to the player (like what's going on?? press some buttons!) and the one where she stands on wolfie and gazes around like she's getting the lay of the land. 

![midna performing the first idle animation where she looks back towards the player](https://64.media.tumblr.com/bab45564e834a46919275fb2f64b91fa/9d7e0cb24a762870-cf/s1280x1920/f2896c105c34418ef5acba80f2760c0055357d03.pnj) ![midna performing the second animation where she stands on wolfies' back](https://64.media.tumblr.com/dc5919dd83dfb3f99ab2d7b7125ed50d/9d7e0cb24a762870-1d/s1280x1920/e425589c9ccfaccaaced08bf9806e08bdd2760a5.pnj)

Those idle animations aren't used in any cutscenes or dialogue scenes (unlike yawn, fold arms, etc.), so this won't affect the story scenes in any way. 

Midna still has her other idles (yawning, patting wolfies' back, etc) and she'll still do them 

**2. It removes the region lock and allows you to use additional emulated memory on Dolphin, and it increases the memory available to the game so the animation can be stored and run safely**

The animation is significantly larger than Midna's other animations partially because of how it gets exported & also it's kind of long. This means we had to increase all the buffers that store Midna animations in the decompiled code so they won't overflow when they try to store & play our custom one. Overall, the patch causes the game to reserve about 1MB more memory for itself, so you'll need to play this with additional emulated memory turned on (4MB extra or 28MB total for MEM1 is what worked for us, so we'll recommend that).

Reserving additional memory beyond the US gamecube's original resources isn't possible without removing the region lock, so that's included as well.

## **3. It modifies wolfies' (wolflink's) idle behavior so that she won't yawn, stretch or sit while Midna is doing scritches.** 

He'll still yawn/sit any other time, but we needed to make this change so wolfie wouldn't interrupt the scritches animation as it's kind of long. 

If wolfie starts yawning/stretching first, it's possible Midna will start the scritches animation before she's finished. This happens rarely, but it will result in midna doing her scritches floating above linklink's head for a few seconds, which is a little funky but not super disturbing. 

**And that's basically it!** The changes to link's behavior & the buffer size increase would have been virtually impossible without the zelda decomp and help from folks in their discord server (thank you so much). 


# **Limitations** 

1. The sounds from the original idle animation aren't modified, although they fit pretty well for the first half of the animation. If you're a sound hon, go for it baby! 

2. The orignal animators did the idle animation design beautifully, each one speaks to a different part of who Midna is. But they follow this rule of keeping Midna mostly centered on wolfies' back, so if you cancel the animation, it won't look jarring. I broke that rule! (but I did it for love!) If you cancel the anmiation in some spots, she'll kind of quickly float back to the base position which breaks immersion a little. 

3. It's too beautiful haha kidding no such thing gorgeous wink 


# **There ya go!** 

I made this with love! Please enjoy! If you want to do this too I'm all kinds of a mess and burdened with the busies of life but please reach out! 

