# Ujian Akhir Semester
### Semester Gasal Tahun Ajaran 2024/2025

Question  below are based on the trace file tcp-ethereal-trace-1 in in http://gaia.cs.umass.edu/wireshark-labs/wireshark-traces.zip

Answer the following questions for the TCP segments:

**1. What is the IP address and TCP port number used by your client computer (source) to transfer the file to gaia.cs.umass.edu? (10%)**

Because the one who initiates the TCP session is the source, we can conclude that the IP address is 192.168.1.102 and its TCP port number is 1161.

**2. What does gaia.cs.umass.edu use the IP address and port number to receive the file. (Attach the screenshot of your Wireshark's display) (10%)**

We can see that IP address is 128.119.245.12 and its port number is 80.

**3. What is the sequence number of the TCP SYN segment that is used to initiate the TCP connection between the client computer and gaia.cs.umass.edu? What is it in the segment that identifies the segment as a SYN segment? (Attach the screenshot of your Wireshark's display) (10%)**

The sequence number is 0. The selected flag bit identifies the segment as a SYN segment.

Link Youtube: https://youtu.be/DUAJn6-CvyU

**4. What is the sequence number of the SYNACK segment sent by gaia.cs.umass.edu to the client computer in reply to the SYN? What is the value of the ACKnowledgement field in the SYNACK segment? How did gaia.cs.umass.edu determine that value? What is it in the segment that identifies the segment as a SYNACK segment? (Attach the screenshot of your Wireshark's display) (10%)**

The sequence number is 0. The acknowledgment value is 1.

**5. What is the sequence number of the TCP segment containing the HTTP POST command? Note that in order to find the POST command, you’ll need to dig into the packet content field at the bottom of the Wireshark window, looking for a segment with a “POST” within its DATA field.(Attach the screenshot of your Wireshark's display) (15%)**

The sequence number is 164041. 

**6. Consider the TCP segment containing the HTTP POST as the first segment in the TCP connection. What are the sequence numbers of the first six TCP connection segments (including the HTTP POST segment)? At what time was each segment sent? When was the ACK for each segment received? Given the difference between when each TCP segment was sent, and when its acknowledgement was received, what is the RTT value for each of the six segments? What is the EstimatedRTT value (see page 237 in textbook) after the receipt of each ACK? Assume that the value of the EstimatedRTT is equal to the measured RTT for the first segment, and then is computed using the EstimatedRTT equation on page 237 for all subsequent segments. (30%)
Note: Wireshark has a nice feature that allows you to plot the RTT for each of the TCP segments sent. Select a TCP segment in the “listing of captured packets” window that is being sent from the client to the gaia.cs.umass.edu server. Then select: Statistics->TCP Stream Graph->Round Trip Time Graph.**

Here is the sequence number for each segment id:
Segment #4 -> Sequence number 1
Segment #5 -> Sequence number 566
Segment #7 -> Sequence number 2026
Segment #8 -> Sequence number 3486
Segment #10 -> Sequence number 4946
Segment #11 -> Sequence number 6406
Segment Number	Sent time	ACK received time	RTT
1	0.026477	0.053937	0.027460
2	0.041737	0.077294	0.035557
3	0.054026	0.124085	0.070059
4	0.054690	0.169118	0.114428
5	0.077405	0.217299	0.139894
6	0.078157	0.267802	0.189645

Generally, EstimatedRTT is a weighted average of the SampleRTT values, except for the first packet. Here is the formula for EstimatedRTT:
EstimatedRTT=0.875*EstimatedRTT+0.125*SampleRTT
EstimatedRTT after ACK received time of segment #4:
EstimatedRTT=0.027460

EstimatedRTT after ACK received time of segment #5:
EstimatedRTT=0.875*0.027460+0.125*0.035557=0.028472
EstimatedRTT after ACK received time of segment #7:
EstimatedRTT=0.875*0.028472+0.125*0.070059=0.033670
EstimatedRTT after ACK received time of segment #8:
EstimatedRTT=0.875*0.033670+0.125*0.114428=0.043765
EstimatedRTT after ACK received time of segment #10:
EstimatedRTT=0.875*0.043765+0.125*0.139894=0.055781
EstimatedRTT after ACK received time of segment #11:
EstimatedRTT=0.875*0.055781+0.125*0.189645=0.075214

**7. What is the length of each of the first six TCP segments?(Attach the screenshot of your Wireshark's display)  (15%)**
From the image above, the length of first TCP packet is 565 and the length of subsequent 5 packets are 1460.

