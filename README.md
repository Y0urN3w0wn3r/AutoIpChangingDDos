# AutoIpChangingDDos
DDos Bash Script written around torshammer with an automatic IP changer to avoid IP blocking durring attack

<h1>HOW TO USE</h1> 
First install torshammer on your server that is running Debian 9<br><br><br>
<code>sudo apt-get update -y && sudo apt-get install tor netcat screen git -y && systemctl enable tor && service tor start </code>
<br>
Then generate a password hash used in your torrc file located at 
/etc/tor/torrc<br>
<br>
<code>tor --hash-password "password"</code>
Then add it to line number 59 in /etc/tor/torrc 
example 
<code>
admin@vps:~# tor --hash-password "password"</code>
<code></code>
<code>16:D2DAF2F6F4419C9660155C7AED45177492363345A981CCCCB3659172F5</code>
</code>
In Your torrc file it should look like:
<code>#HashedControlPassword 16:D2DAF2F6F4419C9660155C7AED45177492363345A981CCCCB3659172F5</code>
<br><br>
At this point you want to install torshammer by running<br><br>
<code>git clone https://github.com/dotfighter/torshammer</code><br><br>
Then go into the folder torshammer and mv everything into the root folder<br>
<code>cd torshammer && mv * .. && cd ..</code><br><br>
At this point clone this repo but move the script to the root folder also <br>
<code>git clone https://github.com/Y0urN3w0wn3r/AutoIpChangingDDos && cd AutoIpChangingDDos && cp * ..</code><br><br>
Now you are ready to test your first target.<br> 
<code>nano run.sh</code><br>
Edit the IP address on line 34 to your targets ip you want to test
and save it using CTRL+O then CTRL+X
<br><br><br>
Allow it to execute with the following command
<br><code>sudo chmod +x run.sh</code>
Run it with 
<code>./run.sh</code>
You can use a distributed shell like "DSH" to make this a distributed attack by using multiple servers at one time. 
To learn how to do that see this guide
<a href="https://www.ostechnix.com/dsh-run-linux-command-multiple-hosts-time/">HERE</a>
<i><b>DISCLAIMER: The information provided is for educational/testing purposes only and is not intended to be used on any service without first obtaining consent for testing. This attack is Illegal and can get you arrested if you use it on a service without permission. This is your only warning
