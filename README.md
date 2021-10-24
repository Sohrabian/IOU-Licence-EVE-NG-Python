# IOU-Licence-EVE-NG-Python
IOL or IOS On linux and IOU or IOS On Unix, is a simulator available for Cisco internal use only. 
IOL/IOU iamges must end with the ".bin" extension and must be executable and License must be 
stored under the /opt/unetlab/addons/iol/bin.
##### Downlaod Cisco iron L2/L3 IOL/IOU images for gns3 and eve-ng: https://mega.nz/folder/dZ4SHDIA#PWjm84au6LyjeBGVzUTNbg 
#### Correct instruction how to create IOU Licence <br />
All Operation are done on EVE cli: 
<br />
<ol>
<li>Login into EVE root/yourpassword</li>
<li>Verify if your internet is ok ping www.google.com, if success do next:</li>
<li>Install nano/vim editor
   <p><code>apt-get update</code></p>
   <p><code>apt-get install vim nano</code></p>
</li>   
<li>Go to location:
   <p><code>cd /opt/unetlab/addons/iol/bin/</code></p>
</li>
<li>Create iou keygen file
   <p><code>vim ioukeygen.py</code></p>
</li>   
<li>File opens and copy python script I pushed in this repo </li>
   <p></p>
<li>Save keygen file with key combos:
  	<ul>
    <li>in nano Editor:
        <ul>
            <li>ctrl+o, answer yes, Enter key </li>
            <li>ctrl+x, for exit</li>
        </ul>
    </li>
    <li>in vim Editor:</li>
  		<ul>
            <li>chit "i" on your keyboard, for Insert mode  </li>
            <li>hit "ESC" on your keyboard, To exit VISUAL mode</li>
          	<li>write ":wq", for save and exit </li>
        </ul>
</ul>
</li>
   <p></p>
<li> fix permissions for new created script file:
   <p><code>chmod + x ioukeygen.py</code></p>
</li>
<li>Run this script
   <p><code>./ioukeygen.py</code></p>
</li>
   
</ol>

