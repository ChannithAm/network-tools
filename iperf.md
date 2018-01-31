# ស្វែងយល់អំពី iPerf/iPerf3
----------------------------------

## <a name ="1">១. iPerf</a>
* iPerf ជាtoolសំរាប់វាស់ (active measurements) bandwidthអតិបរិមានៅលើIP networks។
* វាគាំទ្រ(support)ការលៃនូវដំលៃប៉ារ៉ាមែតទាក់ទងទៅនឹង timing, buffers & protocols (TCP, UDP, SCTP with IPv4 & IPv6)។
* សំរាប់ការធ្វើតេស្តនិមួយៗវាគាំទ្រ bandwidth, loss, & ដំលៃប៉ារ៉ាម៉ែតផ្សេងៗទៀត។
* **iPerf** ត្រូវបានបង្កើតឡើងដោយ NLANR/DAST។
* **iPerf** ត្រូវបានបង្កើតឡើងដោយ ESnet/Lawrence Berkeley National Laboratory។
* វាត្រូវបានចេញក្រោម three-cluase BSD lisense។

## <a name="2">២. លក្ខណៈ</a>

* TCP & SCTP (Stream Control Transmission Protocol)
  * វាស់bandwidth
  * ធ្វើរបាយការណ៍ MSS/MTU size & អង្កេតពីទំហំអាន(read size)
  * គាំទ្រសំរាប់ TCP window size តាមរយៈsocket buffers។
* UDP
  * Client អាចបង្កើត UDP stream នៃbandwidthជាក់លាក់
  * វាស់packet loss
  * វាស់delay jitter
  * Multicast capable
* Cross-platform:
  * Windows,
  * Linux,
  * Android,
  * MacOS X,
  * FreeBSD,
  * OpenBSD,
  * VxWorks,
  * Solaris,
  * ...
  

## <a name="3">៣. ការដំឡើង</a>
ចំពោះ Ubuntu អ្នកអាចប្រើcommand ដូខាងក្រោមដើម្បីដំឡើងៈ
```
sudo apt-get install iperf
```

## <a name="4">៤. Run test</a>
* iPerf/iPerf3អាចប្រើ២modes: 
  * Server mode
  * Client mode

## <a name="5">៥. ការប្រើប្រាស់</a>
```
iperf [-s|-c host] [options]
#
iperf [-h|--help] [-v|--version]
```

* Server mode អាចចាប់ផ្ដើមដោយ -s ឫ --server parameters
```
ipfer -s
```
or
```
iperf --server
```



## <a name="ref">អត្ថបទយោង</a>

[1] iPerf3 https://github.com/esnet/iperf/issues/480
