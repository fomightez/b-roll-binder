# b-roll-binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/b-roll-binder/master?urlpath=lab)

>'for the future when the camera crew wants B-roll and asks you to sit at your desk "doing bioinformatics"'  - *Mike Love in [this post](https://twitter.com/mikelove/status/1011270925868781568)*

Binderizes that featured software and some others in order make a fancy-looking sciencing background dashboard look using Jupyter session served from MyBinder.org.

![b-roll_layout_look](imgs/sciencing_JupyterLab.png)

-----

Additional inspiration also added from [Mara Averick](https://twitter.com/dataandme/status/1119027392838799361) and some other resources I deemed cool.

## Features
- [Artem Babaian's drawHelix.sh](https://github.com/bioSyntax/bioSyntax/blob/master/dev/scripts/drawHelix.sh)
- [Can Güney Aksakalli's gtop](https://github.com/aksakalli/gtop)
- [William Mannard's unimatrix](https://github.com/will8211/unimatrix)
- [Torsten Rehn's termdown](https://github.com/trehn/termdown)

## How to

Launch Binder session and then follow the steps below to kick things off and arrange the windows like the image above:



- **Open your first terminal window by using the menu to select 'File' > 'New' > 'Terminal'.**

- **Open your second terminal window by using the menu to select 'File' > 'New' > 'Terminal'. Left-click on the named tab for this panel, and keep pressing down the left-click, drag this new one over to the right until a blue outlined area fills roughly half the space in the window next to the first and release the click.**

- **Open your third terminal window by using the menu to select 'File' > 'New' > 'Terminal'.  Left-click on the named tab for this panel, and keep pressing down the left-click, drag this new one over just to the right of the first and to left of the second so the blue outline fills the space from top to bottom just to the left of the last one you dragged, and now release the click.**

- **Open your fourth terminal window by using the menu to select 'File' > 'New' > 'Terminal'.  Left-click on the named tab for this panel, and keep pressing down the left-click, drag this new one over right and down towards the middle so the blue outline fills the space below the one you just placed, and now release the click.**

- **Click the `File Browser` icon that looks like a folder  on the left upper side of the panels, or in the menu from under untoggle 'View' > 'Show LeftSidebar' , to toggle closing the file navigation panel to give the four panels more real estate.** Thee shortcut for this on Macs is `command-B`.

- OPTIONAL: Change setting to the dark theme by selecting it under 'Settings' > 'JupyterLab Theme' > 'JupyterLab Dark.

- **In the panel on the far left, kick off the scrolling helix using the included FASTA sequence with the command below followed by hitting return.**

```shell
bash drawHelix.sh chrmt.fsa
```

- Want a sequence more to your liking to be scrolling by on your screen?  
OPTIONAL: Hit `q` to stop the included sequence from scrolling, upload a different DNA of you choosing (you can drag and drop into JupyterLab's file navigation panel)m and point the script at that. Such as:

```shell
bash drawHelix.sh myDNA.fa
```

Where `myDNA.fa` above is replaced with the anem of your sequence file.

- **Move the right-hand border to the right of the scrolling DNA to the left if it leaves to much open space to the right side of the panel.**


- **In the panel in the middle top, start the matrix rain with DNA focus by running the command below:**
 
```shell
unimatrix -s 96 -u 'ACTG'
```

Type `q` at any point to stop the matrix-like rain.
OPTIONAL: If you don't want the matrix-looking panel restricted to DNA bases, just type the following instead to start the matrix-like panel running:

```shell
unimatrix
```

- **In the panel in the middle bottom pane, start the countdown by executing the command below:**
 
```shell
termdown 59m
```

- **Finally, in the far-right pane, start `grop` by typing the command below and hitting return:**
 
```shell
gtop
```

- You should now have something like below. 

![b-roll_layout_look](imgs/sciencing_JupyterLab.png)

Once you understand how to arrange, arrange the panels as you prefer.

TROUBLESHOOTING: note that if any of the middle, stacked panels seem to not be filling their area or the timer is really small, just use `q` to stop each one indivdually. And then use the up arrow to bring up the command last run and hit return to start running again. That usually fixes them.

*In the future, I'd like to automate at least opening the terminal windows in the proper arrangement.*

## Licenses

The four featured software packages have the licenses linked below (most are GNU General Public License v3.0 and one is MIT:

- [Artem Babaian's drawHelix.sh](https://github.com/bioSyntax/bioSyntax/blob/master/LICENSE.md)
- [Can Güney Aksakalli's gtop](https://github.com/aksakalli/gtop/blob/master/LICENSE)
- [William Mannard's unimatrix](https://github.com/will8211/unimatrix/blob/master/LICENSE)
- [Torsten Rehn's termdown](https://github.com/trehn/termdown/blob/master/LICENSE)


## Technical notes

I could get [DustinKirkland's Hollywood](https://github.com/dustinkirkland/hollywood), suggested [in response to Mara Averick's post](https://twitter.com/yeedle/status/1119101335238926338), to sort of start in a Binder session via MyBinder.org after installing `tmux`; however, it didn't really do much but show a little text. Weird.
