# Try Docker-for-Windows

## Share files
0. Select the devices on the settings of Docker
  + Open Settings > Shared Drives
  + Check and input your Windows' password
0. Create a directory and a file to share
  + <code>mkdir hostdir</code>
  + <code>echo "foo piyo" > a.txt</code>
0. Run with `-v` option
  + <code>docker run -v C:\Users\hostdir:/root/contdir -it ubuntu /bin/bash</code>
0. Check files
  + <code># ls /root/contdir</code>
0. Create a file in the container
  + <code># echo "hello piyo" > /root/contdir/bar.txt</code>
0. Check the file on your Windows
