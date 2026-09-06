FLESH - 3D first person horror game
===================================

FILES
  FLESH.html   the whole game in one single file (graphics, sound, code)
  README.txt   this file


HOW TO PLAY
  Double click FLESH.html (opens in Chrome / Edge / Firefox).
  Click PLAY, then click the screen once - the mouse locks to the middle of the
  screen like Minecraft / Roblox shift-lock, and moving it turns your head.
  You need internet the first time you open it: the 3D engine (three.js) is
  loaded from the web.

CONTROLS
  W A S D   move
  SHIFT     run (10 seconds of stamina, 23 seconds to refill)
  MOUSE     look (locked to the centre of the screen while you play)
  F         flashlight (5 minutes of battery, the timer pauses when it is off)
  E         use a signal station, or open the glowing crate
  (the flashlight is a weapon too - see below)
  1         equip / unequip the key
  SPACE     continue the talking box / stop the needle in THE PULSE
  ESC       pause (RESUME / EXIT TO MENU), or leave a minigame


THE GAME
  You wake up in an abandoned shelter in a forest at night, in the rain. Three
  glowing signals are out in the trees, each one inside a small wooden shelter
  full of boxes. Repair all three (each one is a small minigame) and a gold lamp
  lights up in another shelter to the west - the key is in the glowing crate in
  there, open it with E. Equip the key with 1 and walk into the floating door to
  escape into your room.

  SHINING THE LIGHT AT IT
  Hold your flashlight on the monster for half a second and it catches fire,
  screams and stands there burning for 5 seconds - you cannot be caught while
  it burns, so that is your chance to run. It only falls for it ONCE per night.
  Do it a second time and it just gets angry: for 10 seconds it moves half
  again as fast as normal. Use it to escape, not to play with it.

  The black liquid thing hunts you the whole time. You can hear it walking in
  the dark, and it never wanders far from you. When the edges of your screen go
  red, it has seen you and is coming. If it touches you, the whole night starts
  again from zero.


=====================================================================
PUTTING THE GAME ON GITHUB SO IT ALWAYS UPDATES
=====================================================================

The smart way: do NOT send people a file at all. Send them a LINK. The game
lives at that link, and when you replace the file there, every person who opens
the link is playing the new version. Nothing to re-send, ever.

--- ONE TIME SETUP -------------------------------------------------

1. MAKE A GITHUB ACCOUNT
   Go to github.com and click "Sign up". Pick a username - it becomes part of
   your game link, so pick something you like (example: stefan123). Confirm the
   email they send you.

2. MAKE A REPOSITORY (a folder on GitHub)
   Top right: the "+" button -> "New repository".
     Repository name:  flesh
     Description:      (anything, or leave empty)
     Public:           MUST be Public, or the link will not work
     Leave the tick boxes alone.
   Click "Create repository".

3. UPLOAD THE GAME
   On the new page click "uploading an existing file"
   (or: "Add file" -> "Upload files").
   Drag FLESH.html from your Claud Code folder onto the page.
   Scroll down, click the green "Commit changes".

4. TURN ON GITHUB PAGES (this is what makes it a real web link)
   In the repository, click "Settings" (top row).
   In the left sidebar click "Pages".
   Under "Build and deployment" -> "Source" choose "Deploy from a branch".
   Branch: main    Folder: / (root)    then click "Save".
   Wait about 1-2 minutes.

5. YOUR LINK IS
       https://YOURNAME.github.io/flesh/FLESH.html
   (replace YOURNAME with your GitHub username, all lower case)
   Open it yourself first to check that the game runs.

6. SEND THAT LINK TO PEOPLE
   Discord, WhatsApp, anywhere. They click it and play in their browser. They
   always get the newest version automatically.

--- RELEASING AN UPDATE LATER --------------------------------------

   1. Change the game on your computer.
   2. Bump the version in the TWO lines at the top of FLESH.html:
          <!--FLESH_VERSION 1.4-->      ->   <!--FLESH_VERSION 1.5-->
          const GAME_VERSION = "1.4";   ->   const GAME_VERSION = "1.5";
      (the number shows under the menu buttons, so you can see what people run)
   3. On GitHub open your repository -> "Add file" -> "Upload files" -> drag the
      new FLESH.html in (same file name) -> "Commit changes".
   4. Done. Nobody has to download anything - they are playing your copy.

   NOBODY RE-DOWNLOADS ANYTHING
     People who use the link never download a file at all. The game runs in
     their browser, straight from your GitHub copy. On top of that, the game
     checks itself every time the menu opens: if your uploaded version has a
     higher version number than the one they are looking at, it says
     "NEW VERSION v1.5 - LOADING IT NOW..." and loads the new one by itself,
     even if their browser had the old one in its cache. So bumping the version
     number when you upload is worth doing.

     Only someone who SAVED FLESH.html onto their computer has an old copy. For
     them the menu shows an "UPDATE TO v1.5" button that plays the new version
     and saves the new file to their Downloads - but honestly, just give people
     the link instead.

--- TWO OPTIONAL EXTRAS --------------------------------------------

   SHORTER LINK
     In the repository, click FLESH.html, then the pencil (Edit), and change the
     file name at the top to  index.html  -> Commit. Your link then becomes just
         https://YOURNAME.github.io/flesh/
     Keep uploading it as index.html from then on.

   UPDATE BUTTON FOR PEOPLE WHO SAVED THE FILE
     If somebody downloaded FLESH.html instead of using the link, they can be
     told about new versions too. In FLESH.html find near the top:
          const UPDATE_URL = "";
     and put your link inside the quotes:
          const UPDATE_URL = "https://YOURNAME.github.io/flesh/FLESH.html";
     Upload that edited file. From then on, their menu checks your link and
     shows an "UPDATE TO v1.5" button that plays the new version and saves the
     new file to their Downloads folder.
