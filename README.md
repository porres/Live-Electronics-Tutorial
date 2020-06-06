--------------------------------------------------------------------------

# Live Electronics Tutorial

### With examples in Pure Data and the ELSE Library

--------------------------------------------------------------------------

	Copyright © 2008-2020 Alexandre Torres Porres

**Link:** <https://github.com/porres/Live-Electronics-Tutorial>.

--------------------------------------------------------------------------

#### Version: 1.0 beta-28: Released june 7th 2020

 - This particular version of the tutorial requires **Pd 0.51-0** or later and depends on **ELSE 1.0 beta 28** (https://github.com/porres/pd-else/releases/tag/v1.0-beta28)! 

--------------------------------------------------------------------------

**About:**

This tutorial presents theory and practice of Live Electronics topics without any prerequisite. It's aimed at newbies, dummies, enthusiasts and also experts. 

This didactic work is licenced via Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) which allows downloading and sharing with proper credit. It also forbids its usage for comercial purposes. Check the license at: <https://creativecommons.org/licenses/by-nc-nd/4.0/>.


   This is a didactic project developed with Pure Data (or just "Pd", a.k.a. "Pd vanilla" distribution), an open source software developed by Miller Puckette - get it at <http://msp.ucsd.edu/software.html>. Also Access <http://puredata.info> for other resources on Pd. The official Pd mailing list is found here: <http://lists.puredata.info/listinfo/pdlist>. Pure Data is adopted  in the examples for its accessibility and for being a powerful didactic tool. Nonetheless, this work relies heavily in the ELSE library for Pure Data, also developed by Alexandre Torres Porres, the author of this tutorial. Note that forks of Pd like Pd-Extended and Purr Data are incompatible to this tutorial and the ELSE library.

   This project started in 2008 as a textbook for a computer music course. In 2009, the author presented a paper about it in the 3rd International Pure Data Convention. Currently, the work is divided into two volumes and solely presented as example patches that the author uses in his courses/workshops. The plan now is to write a book accompanied by these examples. Originally developed in brazilian portuguese and relying on Pd Extended 0.42-5 for years, this has just been rewritten from scratch in english and ported to rely only in objects from the ELSE external library and the newer Pd Vanilla versions.

   This is still in the early drafts from the first translation rounds, so typos and mistakes may exist. There are plans to include more topics and examples in this tutorial, which can furtherly be split into 3 volumes. The developments now depend mostly on the software development of the ELSE library to include more examples. Since the ELSE library is still in an early beta stage of development, some objects may change in functionality, new objects are being developed and others might even be deleted until a final version is out. If so, future updates of this didactc material will reflect these changes.  

--------------------------------------------------------------------------

   ### Downloading and Installing this tutorial:

​	This version of the tutorial needs at least Pd 0.51-0! You can look for releases of this tutorial in https://github.com/porres/Live-Electronics-Tutorial/releases - where early versions of it are also still present, but it's best just to download this directly via Pd or get the ELSE library, because this tutorial is also provided as part of it.

​	You need to install the "ELSE" library in order to use this tutorial anyway. So if you try to download the ELSE library directly via Pd, you'll find a download that also contains this tutorial. In the same way, if you try to download the tutorial directly from Pd, you'll also get ELSE as part of the download. So in Pd just go to the "Help" menu and click on "Find Externals", then just search for 'else' or 'live electronics tutorial'. For more details on the ELSE library, check: <https://github.com/porres/pd-else/>, where you can also download and check earlier versions of the library. You can also download ELSE from its GitHub repository and it'll also contain this tutorial as part of the download. In this combo download, you'll always get compatibility between the tutorial and the ELSE library.

​	If installed directly via Pd, the 'live electronics folder' resides inside the 'else' folder. To install the tutorial, just add the folder's path to Pd via "Preferences => Path", so you can navigate through it in Pd's browser (Help => Browser). You can and probably should also move the folder from inside the else folder. A good place to move it to is *~/pd/documents*, so I suggest you to do this before adding the path, leaving the 'externals' folder just for actual externals as the ELSE library.