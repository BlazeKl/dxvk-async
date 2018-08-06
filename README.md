# What?
A **gross hack** to use discard shaders while waiting for real shaders to compile asynchronously. This "solves" shader compilation stutter, with the downside of graphical glitches. Depends heavily on what the game does with the shaders: could work on some games fine and others will be horribly broken.

### How to
In terminal:
```
git clone https://github.com/doitsujin/dxvk.git
cd dxvk
patch -Np1 -i ../pipeline.patch
```
and compile, or download already compiled binary from release tab

### Games tested
* Path of Exile: seems fine
* Overwatch: graphic bugs on first matches, seems fine after playing for a while
* Sonic Forces: in-game graphic bugs will fix when shaders finish compiling, menu is a bit broken


### Instructions

* patch dxvk with pipeline.patch
* Set env variables:
  * DXVK_USE_PIPECOMPILER=1
  * DXVK_USE_PLACEHOLDER_SHADERS=1

**Do not report issues to DXVK github even if you dont use the env variables, this hack could introduce new bugs even without them**
