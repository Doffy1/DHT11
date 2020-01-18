# DHT11
Read data from DHT11 sensor with error checking and retries.

<b>Files:</b><br>
<tt>read_DHT11.c</tt> - the C source code<br>
<tt>read_DHT11</tt> - the binary code<br>
Compiled on RPi3B+ Linux 4.19 with "<tt>gcc -o read_DHT11 read_DHT11.c -lwiringPi -lwiringPiDev</tt>" command<br>

<b>Details of operation:</b><br>
Run "<tt>sudo ./read_DHT11</tt>" with wPi (wiringPi) PIN number parameter like: "<tt>sudo ./read_DHT11 2</tt>".<br>
Because the read is very sensitive for CPU loads, the data integrity check is required. 
When read error detected, then after 2 seconds wait retry the read. After 4 retry exit with error (in tests never reached this limit :-)

<b>Requirements</b><br>
WiringPi must be installed.

<b>Install:</b><br>
Copy binary code to /usr/bin/ and use it.

<b>Tested environment:</b><br>
RPi3B+

