# IOU-Licence-EVE-NG-Python
IOL or IOS On linux and IOU or IOS On Unix, is a simulator available for Cisco internal use only. 
IOL/IOU iamges must end with the ".bin" extension and must be executable and License must be 
stored under the /opt/unetlab/addons/iol/bin.
##### Elearn EVE-NG created by Sohrabian_Hassan: https://www.aparat.com/playlist/1288629 (continue)
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
<li>Output will show you generated license:
   <p>
      ********************************************************************* <br />
      Cisco IOU License Generator - Kal 2011, python port of 2006 C version <br />
      hostid=520d3428, hostname=T470P, ioukey=520d3567 <br />
      ********************************************************************* <br />
      Create the license file $HOME/.iourc with this command: <br />
      echo -e '[license]\nT470P = 413b2074a06a8f08;' | tee $HOME/.iourc  <br />
      The command adds the following text to $HOME/.iourc: <br />
      <code>[license]</code> <br />
      <code>T470P = 413b2074a06a8f08;</code> <br />
      ********************************************************************* <br />
      Disable the phone home feature with this command: <br />
      grep -q -F '127.0.0.1 xml.cisco.com' /etc/hosts || echo '127.0.0.1 xml.cisco.com' | sudo tee -a /etc/hosts <br />
      The command adds the following text to /etc/hosts: <br />
      127.0.0.1 xml.cisco.com <br />
      ********************************************************************* <br />  
   </p>
</li>
<li>Copy generated lic info
   <p>
    <code>[license]</code> <br />
    <code>T470P = 413b2074a06a8f08;</code> <br />
   </p>
</li>
<li>Create iourc lic file for EVE
   <p><code>vim /opt/unetlab/addons/iol/bin/iourc</code></p>
</li>
<li>Paste lic info in "iourc"
   <p>
    <code>[license]</code> <br />
    <code>T470P = 413b2074a06a8f08;</code> <br />
   </p>
</li>
<li>Fix permissions with:
   <p><code>/opt/unetlab/wrappers/unl_wrapper -a fixpermissions</code></p>
</li>
</ol>



