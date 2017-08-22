# Software Installation {#software-installation}

1.  ![C:\Users\v-dorobe\Pictures\WWT_installer_dialog1.jpg](assets/cusersv-dorobepictureswwtinst.jpeg)Install WWT Windows Client on all Servers both Master and Projector servers, [http://www.worldwidetelescope.org](http://www.worldwidetelescope.org/)

_Installation folder._

*   1.  Install with default folder path C:\Program Files (x86)\Microsoft Research\Microsoft WorldWide Telescope
    2.  The GUI or Master control channel needs to be a separate server from the projection channels

1.  Install Remote Control for Cluster Operation
    1.  Remote can:
        1.  Wake and shutdown projector server
        2.  Shutdown WWT on projector server
        3.  Startup WWT on projector server
    2.  Record IP and MAC address for each node
    3.  Turn off screen saver and energy saver settings for each node
    4.  Both WWT and WWTRemote Control should be running on each slave/node for the projection to work correctly
2.  Install Excel Add-In for WWT
3.  Run WWT on each server independently before attempting to setup cluster.
    1.  Run a tour or navigate around to load data into the cache
    2.  WWT needs the cache folder populated to run smoothly
4.  Populate cluster configuration files
    1.  Create a wwtconfig folder in the root directory of _each_ server including Master controller (C:\wwtconfig)
    2.  Start WWT on each node – master and projection servers
    3.  After WWT has fully started, exit program. This will cause a config.xml file to be created in the folder C:\wwtconfig
    4.  Using a text or XML editor, change the config.xml file as follows for _each_ of the projector nodes

_Example config.xml for projector nodes._

*   *   1.  Create a unique cluster ID
        2.  Create a node ID
        3.  Change node Display name (such as dome orientation – where it is aimed)
        4.  Set Master to False
        5.  Enter actual resolution for your display in Width, and Height
        6.  Set MultiChannelDome to True
        7.  Save file and close editor
    1.  Using a text or XML editor, change the config.xml file as follows for the Master node

_Example config.xml for Master node._

*   *   1.  Enter your unique cluster id
        2.  Change NodeId to -1
        3.  Check and ensure Master is set to True
        4.  Enter actual resolution for your display in Width, and Height
        5.  Set MultiChannelDome to True
        6.  Save file and close editor

1.  Open Remote Access Control under Settings&gt;Remote Access Control on _each_ node

_Select Remote Access Control._

*   1.  Enter the IP address of your Master Controller Node. This ensures only you will have control of your nodes at all times.
    2.  Check Accept Local Connections.

_Setting IP address for Remote Access Control._

1.  Launch WWT on Master Controller node
2.  On Master Controller Node Ensure under Settings&gt;Advanced that Master Controller is checked

_Setting a node as Master Controller._

1.  ![C:\Users\v-dorobe\Pictures\WWT_select_projection_server_list.jpg](assets/cusersv-dorobepictureswwtsele.jpeg)Open Projector Server List under Settings&gt; Advanced to ensure you can see all nodes, and they are green. This pane will also tell you frame rates and other useful information for each node.

_Opening Projector Server List._

1.  Open Settings&gt;Advanced&gt;Multi Channel Calibration

![C:\Users\v-dorobe\Pictures\WWT_select_multi_channel_calibration.jpg](assets/cusersv-dorobepictureswwtsele.jpeg)

_Selecting Multi-channel calibration._

1.  Set specifics for the projection area
    1.  Select the type of screen as Spherical
    2.  Set Screen Radius in meters
    3.  Set Tilt to locate center of interest in the display. (example: A value of 60 indicates that main focus of most viewers will be on a point 60 degrees up from the spring-

line)

1.  Set number of projectors in the top left panel
    1.  Left click to highlight a channel
    2.  The layout example is fixed and will not change from a six channel example
    3.  Five channels is considered the minimum for a dome setup
    4.  As you update your Projector names the text on the dome map will update
2.  Change properties for each channel by left clicking the channel you wish to edit and click the edit button
    1.  Set each channel with the unique id, and name that was set earlier in the XML file
    2.  View tab contains the idealized settings for the projector if it was centered exactly in the middle of the dome
    3.  Projector tab pertains to the actual physical location of the projector
    4.  Solved tab contains the temporary output from a Solve Alignment calculation