Click Code->Download ZIP. Use Gamecube File Tools to import your ISO, then click Add/Replace Files From Folder and select the midna-scritches-patch folder (the one with "files" and"sys" in it). Then export the new ISO and get scritches.

# **What does the mod do** 

**1. It replaces 2 of Midna's idle animations** : the one where she rotates how she's sitting and looks backwards to the player (like what's going on?? press some buttons!) and the one where she stands on wolfie and gazes around like she's getting the lay of the land. 

Those idle animations aren't used in any cutscenes or dialogue scenes (unlike yawn, fold arms, etc.), so this won't affect the story scenes in any way. 

Midna still has her other idles (yawning, patting wolfies' back, etc) and she'll still do them 

**2. WARNING: this patch modifies the the decompiled code to give Midna's current animation buffer about 250kb extra** . 

**The gamecube has extremely limited memory (only 24mb wth!), so that's a significant request and it's possible this will cause crashes in some areas of the game** **_._** Granted, we tested for about 3 hours just loading up different save files in the twilight, bosses, dungeons, and areas that seem memory intensive, and it hasn't crashed yet! Fingers crossed! But this isn't super safe. Dolphin has an option to increase the gamecube's memory beyond the original console, but you have to make changes to the code for this to actually get utilized and we haven't figured out how to do this yet. We'll release another patch if we do! 

Keep a copy of your original ISO! 

## **3. It modifies wolfies' (wolflink's) idle behavior so that she won't yawn, stretch or sit while Midna is doing scritches.** 

He'll still yawn/sit any other time, but we needed to make this change so wolfie wouldn't interrupt the scritches animation as it's kind of long. 

If wolfie starts yawning/stretching first, it's possible Midna will start the scritches animation before she's finished. This happens rarely, but it will result in midna doing her scritches floating above linklink's head for a few seconds, which is a little funky but not super disturbing. 

**And that's basically it!** The changes to link's behavior & the buffer size increase would have been virtually impossible without the zelda decomp and help from folks in their discord server (thank you so much). 

# **How do install it?** 

Well buckle up buttercup and I'll tell you! First download the patch 

You need the Gamecube File Tools (GCFT) and a copy of the ISO that you didn't get from the piracy fairies, no, no, no! Only legal and legitomato! 

It can be the Linkle modded iso, that's what we used. Open up GCFT, click _Import GCM_ , pick your iso. 

Then click _Add/Replace files from folder_ and pick my little folder (midna_scritches_patch). Note that this _won't_ override your original ISO. When you're done, click _Export GCM_ . This will let you save a new copy of the ISO with my little scritches anim in it! Boot that baby up and Receive <3. 

# **Limitations** 

1. The sounds from the original idle animation aren't modified, although they fit pretty well for the first half of the animation. If you're a sound hon, go for it baby! 

2. The orignal animators did the idle animation design beautifully, each one speaks to a different part of who Midna is. But they follow this rule of keeping Midna mostly centered on wolfies' back, so if you cancel the animation, it won't look jarring. I broke that rule! (but I did it for love!) If you cancel the anmiation in some spots, she'll kind of quickly float back to the base position which breaks immersion a little. 

3. It's too beautiful haha kidding no such thing gorgeous wink 

# **How we made it** 

<u>This video</u> describes a process & plugins for importing gamecube bck animations into blender, and exporting them as maya animations, and then repackaging them for gamecube 

Animating with the imported rig is **difficult** . 

The video says that using full IK with targets is impossible, but you can actually add some IK targets that work reasonably well and remove them as long as you bake the animation (you can reach out to me if you're interested). 

Our advice for animating: picture it in your head but also run some of the motions in your body & see how they feel in your muscles and use that as reference too! You can film yourself doing the action, but do it to understand what's happening in your body. We keyframe the landing poses for the limbs that are driving motion, spread out joint keyframes for overlapping motion, try to add bounce back & follow-through where it feels right, go into the motion curves to fine tune. If you can't make an action work physically it might just mean it doesn't feel right for the moment! 

It's ok to try out alternatives or go back to thinking about like how midna's feeling when she does it and what she wants. 

Baking the animation results in files significantly larger than the original animations which will cause memory problems in the vanilla game, so this is really only feasible if you modify a decompiled code base to increase buffer sizes (which is risky). 

Once you have an animation, the open source j3d-animation-tool lets you re-save it in a gamecube bck format. It also lets you make texture animations, which is just specifying image indexes at different frames (e.g. "1" means eyes wide open, "4" means eyes closed). You can use Gamecube File Tools to replace the original files (the video walks through it). 

Without changing the code, importing most animation will cause (kind of disturbing) weird visual effects (i hated this the most) because your animations will get loaded into buffers that are too small and overflow into other memory locations (like actors' rigs & stuff). The only way to avoid this realistically is to make tiny animations (no fun) or modify the decompiled code and rebuild new binaries. 

The Zelda RET decompiled the binaries for Twilight Princess into C++ code (an insane amount of work). 

Midna's d_a_midna.cpp file has a line (368) that sets the buffer size to 0x3800 (that's hexidecimal for 14,000, so roughly 14kb). you can increase this, but go too large and you'll see crashes happen consistently, go less large but still to large and you'll see crashes happen infrequently. any change to this number is risky for the game being stable. 

The decomp page & its' discord server have lovely instructions on how to rebuild the game and <u>a script</u> for packaging it back into a playable format for testing. You need to provide your own ISO, but it can be a modded ISO with your new assets added. 

Then you just keep fucking with it till it works! It takes a long time and a lot of patience 

# **There ya go!** 

I made this with love! Please enjoy! If you want to do this too I'm all kinds of a mess and burdened with the busies of life but please reach out! 

