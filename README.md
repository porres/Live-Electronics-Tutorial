--------------------------------------------------------------------------

# Live Electronics Tutorial

### With examples in Pure Data and the ELSE Library

--------------------------------------------------------------------------

	Copyright © 2008-2023 Alexandre Torres Porres

**Link:** <https://github.com/porres/Live-Electronics-Tutorial>.

--------------------------------------------------------------------------

#### Version: 1.0-0 RC-11 (Release Candidate #11): Released: January 30th 2024

 - This particular version of the tutorial requires **Pd 0.54-1** or later and depends on **ELSE 1.0-0 RC 11** (<https://github.com/porres/pd-else/releases/tag/v1.0-rc11>)! 

--------------------------------------------------------------------------

**About:**

This tutorial presents theory and practice of Live Electronics and computer music, synthesis/DSP (digital Signal Processing) topics without any prerequisite. It's aimed at newbies, dummies, enthusiasts and also experts. 

This didactic work is licenced via Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0), which allows downloading and sharing with proper credit. It also forbids its usage for comercial purposes. Check the license at: <https://creativecommons.org/licenses/by-nc-nd/4.0/>.

   This is a didactic project developed with Pure Data (or just "Pd", a.k.a. "Pd vanilla" distribution) and the ELSE library for Pd. Pd is an open source software developed by Miller Puckette - get it at <http://msp.ucsd.edu/software.html>. Note that the major forks of Pd (Pd-Extended and Purr Data) are incompatible to this tutorial (and the ELSE library). Also Access <http://puredata.info> for other resources on Pd. The official Pd mailing list is found here: <http://lists.puredata.info/listinfo/pdlist>. 

​	Pure Data is adopted in this tutorial amongst other possibilities because of its accessibility, friendliness and for being a powerful didactic tool. Nonetheless, this work relies heavily in the ELSE library for Pure Data, also developed by Alexandre Torres Porres, the author of this tutorial. 

   This project started in 2008 as part of a textbook for a computer music course with included examples in Pd. In 2009, the author presented a paper about it in the 3rd International Pure Data Convention. Currently, this is solely presented as example patches that the author uses in his courses/workshops. The plan now is to write a book accompanied by these examples. Originally developed in brazilian portuguese and relying on Pd Extended 0.42-5 for years. In 2018 this has been rewritten from scratch and translated into english. It was also ported to rely only in objects from the ELSE external library and the newer Pd Vanilla versions.

   There are plans to include more topics, which also depends on the software development of the ELSE library to include more examples. Since the ELSE library is still in an early and unstable stage of development, some objects may change in functionality, new objects are being developed and others might even be deleted until a final version is out. If so, future updates of this didactc material will reflect these changes.  

--------------------------------------------------------------------------

#### Downloading and Installing this tutorial:

​	This version of the tutorial needs at least Pd 0.54-1! You can look for releases of this tutorial in https://github.com/porres/Live-Electronics-Tutorial/releases - where early versions of it are also still present, but it's best just to download this directly via Pd along with the ELSE library, because this tutorial is also provided as part of it (and you need to install the "ELSE" library in order to use this tutorial anyway).

​	So in Pd just go to the "Help" menu and click on "Find Externals", then just search for 'else' for the latest version (1.0-0rc8 by the time of this release). You can also download ELSE from its GitHub repository  <https://github.com/porres/pd-else/> and it'll also contain this tutorial as part of the download. In this combo download, you'll always get compatibility between the tutorial and the ELSE library.

​	Once you download the library (via Pd or Github), look for the  'live-electronics-folder' inside the else folder and move it somewhere else, preferably to **~/Documents/Pd** (leave **~/Documents/Pd/externals** just for proper external libraries, like the ELSE library). Then you can add the folder's path (such as **~/Documents/Pd/Live-Electronics-Tutorial**) to Pd via "Preferences => Path", so you can navigate through the tutorial via Pd's browser (Help => Browser). 

--------------------------------------------------------------------------

#### Loading the examples from the tutorial:

​	Once you have the ELSE library and moved the tutorial to your preferred place, you can can just open the examples. Note that the tutorial uses **[declare -path else]** in all the examples that need externals from the ELSE library. With this particular strategy, it is possible to run into conflicts, and by conflicts I mean loading by mistake another external from another library that has the same name as an external from ELSE. In order to avoid this, you must not have loaded such other externals from other libraries before opening Pd with these examples. One good practice is to not load other libraries via "Preferences => Startup", because this loads these externals every time Pd is started.
