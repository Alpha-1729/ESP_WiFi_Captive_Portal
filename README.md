# ESP8266 Wifi Captive Portal

WiFi captive portal for the NodeMCU (ESP8266 Module) with DNS spoofing.

<!-- Disclaimer -->

# <u>Disclaimer</u>

This project is for testing and educational purposes. Use it only against your own networks and devices. I don't take any responsibility for what you do with this program.

<!-- Features -->

# <u>Features</u>

- :muscle: The LED will blink 5 times when a password is posted.
- :muscle: All captured password will be stored in the ESP8266 itself.
- :muscle:Your saved passwords will <b> not </b> disappear when you:

  - :arrow_forward: Restart/power off the ESP8266.
  - :arrow_forward: Change the SSID.

- :muscle: You can clear saved password when necessary.
- :muscle: You can change the SSID name from the portal itself.

<!-- Usage -->

# <u>Usage</u>

- :pencil2: <b>Changing the SSID: </b>:arrow_forward: <b>172.0.0.1/ssid</b>:arrow_backward:
- :boom:<b>Clearing the passwords: </b>:arrow_forward: <b>172.0.0.1/clear</b>:arrow_backward:
- :see_no_evil: <b> To see saved passwords: </b> :arrow_forward: <b>172.0.0.1/pass</b>:arrow_backward:
- :scroll: <b> Testing victim page: </b> :arrow_forward: <b>172.0.0.1/index</b>:arrow_backward:

# <u>Demo Video</u>

<a target="_blank" href="https://youtu.be/v4-5oX3RG94"><img width="700px" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/thumbnail.png"></a>

# <u>Screenshot</u>

<table>
  <tr>
    <th>172.0.0.1/index</th>
    <th>172.0.0.1/post</th> 
    <th>172.0.0.1/pass</th>
    <th>172.0.0.1/ssid</th>
  </tr>
  <tr>
    <td>This is the main page. Here the user will write his password and send it.</td>
    <td>This is the post page. The user will be redirected here after posting the password.</td>
    <td>This is where the attacker can retrieve all the passwords that has been posted and saved passwords can be cleared.</td>
    <td>Here the attacker can change the SSID name of the Access Point on the go.</td>
  <tr>
    <td><img width="200px" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/index.jpg" title="index"></td>
    <td><img width="200px" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/post.jpg" title="post"></td>
    <td><img width="200px" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/pass.jpg" title="pass"></td>
<td><img width="200px" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/ssid.jpg" title="ssid"></td>
  </tr>
</table>

# <u>Installation</u>

## 1. ESP8266 Flasher - Easy way

1. Download <a href="https://github.com/nodemcu/nodemcu-flasher"><b>ESP8266 Flasher</b></a>.

2. Download the <b><a href="https://github.com/Alpha-1729/esp-wifi-captive-portal/releases/download/v1.0/esp-wifi-captive-portal-v1.0.bin">esp-wifi-captive-portal-v1.0.bin</b></a> file.

3. Open the ESP8266 Flasher and select the Node MCU port

<img width="80%" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/flasher_1.png">

4. Then, go to the config tab and select the .bin file you've just downloaded.

<img width="80%" src="https://raw.githubusercontent.com/Alpha-1729/esp-wifi-captive-portal/master/src/flasher_2.png">

5. Finally, go back to the first tab and press "Flash"

6. Your Node MCU is ready!

## 2. Arduino IDE

1. Open your <a href="https://www.arduino.cc/en/main/software">Arduino IDE</a> and go to File :mag_right: Preferences :mag_right: Boards Manager URLs and paste the following link:
   `https://arduino.esp8266.com/stable/package_esp8266com_index.json`
2. Go to Tools :mag_right:Board :mag_right: Boards Manager, search "esp8266" and install esp8266.
3. Go to Tools :mag_right: Board and select you board.
4. Download and open the sketch "<a href="https://github.com/Alpha-1729/esp-wifi-captive-portal/blob/master/esp-wifi-captive-portal.ino"><b>esp-wifi-captive-portal.ino</b></a>".
5. You can optionally change some parameters like the SSID name and texts of the page like title, subtitle, text body...
6. Upload the code into your board.
7. You are done!
