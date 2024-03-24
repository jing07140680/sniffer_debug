# sniffer_debug

## case1
UE: srsRAN_4G(release 22.04)
gNB: srsRAN_Project(release 23.5)
band: 3
bandwidth: 10MHz

I first tried sampling rate 11.52 to make sure the configuration and communication between gNB and UE is correct.
Then try to force center frequency (ssb_freq and the dl_freq) aligned (arfcn: 38410).
But the UE cannot sync with gNB.

Besides release 22.04 complains the bandwidth confiugration larger than 10MHz


## case2
UE: srsRAN_4G(release 22.04)
eNB(5G SA): srsRAN_4G(release 22.04)
band: 3
bandwidth: 10MHz

Do the connection check first, passed.
Force DL center frquency to be the same as SSB, failed.

Maybe I should force ssb cf aligend with DL frequency instead?
The reason I moved DL cf is because I tried to move SSB but seems there is an algorithm about how to choose best SSB in frequency so that it has less overlapp with some other blocks (cannot remeber) in newest release. Not sure if it is the case in this release, might need to check.

## case3
UE: srsRAN_4G(release 23.11)
gNB: srsRAN_Project(23.10.1)
band:3
bandwidth: 20HMz

Do the connection check first, passed.
Force DL center frquency to be the same as SSB, passed.
Collected IQ samples.
5Gsniffer synced.
MIB decoded.
Decode DCI, failed.

IQsamples file is at: https://drive.google.com/drive/folders/1XpqJkzNukiZE9lJt90GcJfn6xDsRjzAr?usp=drive_link

## case4
UE: srsRAN_4G(release 23.11)
gNB: srsRAN_Project(23.5)
Plan to see if this one works
