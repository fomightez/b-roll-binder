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

Launch Binder session and then follow the steps below to kick things off and lay out the windows like so:

![b-roll_layout_look](imgs/sciencing_JupyterLab.png)

- Kick off the scrolling helix using the included FASTA sequence with the command below.

```shell
bash drawHelix.sh chrmt.fsa
```

- Want a sequence more to your liking to be scrolling by on your screen? OPTIONAL: Hit `q` to stop the included sequence from scrolling, upload a different DNA of you choosing (you can drag and drop into JupyterLab's file navigation panel)m and point the script at that. Such as:

```shell
bash drawHelix.sh myDNA.fa
```

Where `myDNA.fa` is replaces with the anem of your sequence file.

- OPTIONAL: Change setting to the dark theme by selecting it under 'Settings' > 'JupyterLab Theme' > 'JupyterLab Dark.

- start matrix ran with DNA focus by running the command below:
 
```shell
unimatrix -s 96 -u 'ACTG'
```

Type `q` at any point to stop the matrix-like rain.
OPTIONAL:If you don't want it restricted to DNA bases, just type the following instead to start the matrix-like panel running:

```shell
unimatrix -s 96 -u 'ACTG'
```


To do:
- make sure binder link opens JupyterLab

*In the future, I'd like to automate at least opening the terminal windows in the proper arrangement.*

## Licenses

The four featured software packages have the licenses linked below (most are GNU General Public License v3.0 and one is MIT:

- [Artem Babaian's drawHelix.sh](https://github.com/bioSyntax/bioSyntax/blob/master/LICENSE.md)
- [Can Güney Aksakalli's gtop](https://github.com/aksakalli/gtop/blob/master/LICENSE)
- [William Mannard's unimatrix](https://github.com/will8211/unimatrix/blob/master/LICENSE)
- [Torsten Rehn's termdown](https://github.com/trehn/termdown/blob/master/LICENSE)


## Technical notes

I could get [DustinKirkland's Hollywood](https://github.com/dustinkirkland/hollywood), suggested [in response to Mara Averick's post](https://twitter.com/yeedle/status/1119101335238926338), to sort of start in a Binder session via MyBinder.org after installing `tmux`; however, it didn't really do much but show a little text. Weird.
