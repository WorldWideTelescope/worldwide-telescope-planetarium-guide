+++
title = "Data Caches"
weight = 500
sort_by = "weight"
insert_anchor_links = "right"
+++

AAS WorldWide Telescope (WWT) is a great tool with access to petabytes of
image data from the cloud, but in some educational contexts the internet may
not be available. Fear not: WWT can operate in situations with poor or even
nonexistent internet connections.

Note that WWT already can operate offline if the user only browses data
previously viewed in WWT on that machine. In a new installation, there is no
cache history for a user to rely on and the experience is not acceptable. To
solve this issue we have created a tool that will allow for the creation of
curated cache content that can be installed offline (e.g., from a DVD or thumb
drive) along with the WWT client to allow a disconnected or poorly connected
machine to run most of WWT features without ever having to connect to the
internet.


# Video Tutorial

{{ youtube(id="MeBIFO245KA", class="youtube-embed") }}


# Tools

This list gives an overview of the cache management tools available in current
versions of the WWT Windows client:

* Cache measurement / purge utility in the Settings tab
* Cache Management Menu from right-click menu item in the Explore and Context tabs.
  * Cache Image Tile Pyramid
  * Show Cache Space Used
  * Remove from Image Cache
* Playing a tour caches all data it views
* Playing tours with “Play all” option will play and repeat tours in a collection
* Browsing collections will add images you view to the cache.
* “Play Collection as Slideshow” will go from image to image and cache data as it goes.
* Setting up WMS servers, and caching data they use.
* Running WWT in Solar System mode with Multi-Resolution planets will load in
  base maps needed for that mode.
* Save the Cache in {{ui(p="Settings > Advanced > Save Cache as Cabinet File …")}}.
* Load the Cache in {{ui(p="Settings > Advanced > Restore Cache from Cabinet
  File …")}}.

The WWT local data cache is found in the directory `C:\Users\{user name
here}\AppData\Local\Microsoft\WorldWideTelescope`.


# Workflow

1. Ensure your WWT instance has a fresh, clean cache.
2. Use tour playback, manual exploration, and/or cache tools to populate the
   local cache with the necessary data.
3. Measure the cache size as you go, budgeting for the data sets you need.
4. Use the UI or manual cache management in Explorer to trim excess if needed.
5. Use {{ui(p="Settings > Advanced > Save Cache as Cabinet File …")}} to save
   the cache.
6. Move the cabinet file to the machine needing a manual cache infusion.
7. Install a WWT on the target machine, if needed.
8. Start WWT and restore the cabinet file.
9. Verify operation and note any missing data.
10. Repeat the above steps as necessary until the cache meets the educational
    requirements.


# Automated Deployment

The WWT installer will detect the presence of a cache cabinet file and offer
to install it automatically. This file should be named `WwtFileCache.cabinet`
and be placed next to the `WWTSetup.*.msi` file. After installation WWT will
use this cache transparently as if it actually visited all the data already.
