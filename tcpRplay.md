# អទ្ថបទស្ដីអំពីtcpreplay
=====================================================
Control and replay network traffic withh *tcpreplay*
=====================================================

មាតិការ
=======

* [១.​ សេចក្ដីផ្ដើម](#intro)
* [២. Toolsនៅក្នុងtcpreplay package](#tools)
* [៣. ដំឡើង(install)](#install)
* [៤. Sample lab](#lab)
* [៥. ឯកសារយោង](#ref)


## <a name="intro">១.​ សេចក្ដីផ្ដើម</a>

* Tcpreplay គឺជាឧបករណ៍សំរាប់ប្រពន្ធUNIX-like​ ដែលគេប្រើសំរាប់ editing & replaying network traffic ដែលត្រូវបានcapturedពីមុនមកដោយសារ tools ដូចជា `tcpdump`, `wireshark`។
* Tcpreplay ផ្ដល់ជាមធ្យោបាយដ៏ទុកចិត្ត និងការធ្វើត្រាប់ឡើងវិញនូវtraffic ក្នុង​ការធ្វើតេស្ត ឧបករណ៍ផ្សេងៗគ្នានៃnetworkដូចជា៖ switch, router, firewall, network intrusion detection systems (NIDS) និង intrusion prevention systems (IPS)។
* គួកត់សំគាល់ដែរថា​ tcpreplayជាប្រភេទstateless ហើយមិនអាចupdating TCP sequence & acknowledgement numbers។ ដូច្នេះ វាមិនsupport replaying traffic to a server។
* Tcpreplay ផ្ដល់toolsក្នុងការបែងចែករវាងclient ឫserver, editing packetsនៅlayers 2-3-4នៃOSI model ហើយreplay the traffic ជាមួយ​ល្បឿនណាមួយនៅលើបណ្ដាញ ដើម្បីsniffing ឫឆ្លងកាតតាមរយៈdevices។

## <a name="tools">២. Toolsនៅក្នុងtcpreplay package</a>

* tcpbridge - អាចអោយយើងភ្ជាប់រវាង 2 network segments & bridge them.
* tcpprep - បែងចែកលក្ខណៈpackets ជាclient-server, server-client
* tcpreplay - replay network traffic ផ្ទុកនៅក្នុង pcap fileដោយ​ប្រើTCP connectionថ្មី
* tcpreplay-edit - replays & edits pcap files នូវល្បឿនមួយ​ នៅលើnetwork ជាមួយនឹងoptionsជាច្រើនក្នុងការmodify packets
* tcprewrite - edit packets ( mostly at L2-L4)

## <a name="install">៣. ដំឡើង(install)</a>

នេះជារបៀបដំឡើងនៅលើ Ubuntu 16.04
```
sudo apt-get update
sudo apt-get install tcpreplay
```

## <a name="lab">៤. Sample lab</a>

* Capture live network traffic by tcpdump
```
$ sudo tcpdump -i wlp2s0 -w dump.pcap
```
* Synopsis
```
tcpreplay [-flag [value]]... [--opt-name [[=| ]value]]...

    <pcap_file(s)> 
```


## <a name="ref">៥. ឯកសារយោង</a>
[1] https://tournasdimitrios1.wordpress.com/2011/02/14/control-and-replay-network-traffic-with-tcpreplay/

[2] http://xmodulo.com/how-to-capture-and-replay-network-traffic-on-linux.html

