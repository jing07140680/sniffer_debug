# sniffer_debug

## case1
UE: srsRAN_4G(release 22.04)
gNB: srsRAN_Project(release 23.5)
band: 3
bandwith: 10MHz

I first tried sampling rate 11.52 to make sure the configuration and communication between gNB and UE is correct.
Then try to force center frequency (ssb_freq and the dl_freq) aligned (arfcn: 38410).
But the UE cannot sync with gNB.

Besides release 22.04 complains the bandwidth confiugration larger than 10MHz


## case2
UE: srsRAN_4G(release 22.04)
eNB(5G SA): srsRAN_4G(release 22.04)
band: 3
bandwith: 10MHz

Do the connection check first, passed.
force DL center frquency to be the same as SSB, failed.

Maybe I should force ssb cf aligend with DL frequency instead?

