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
  

    Client and server can have multiple simultaneous connections (-P option).
    Server handles multiple connections, rather than quitting after a single test.
    Can run for specified time (-t option), rather than a set amount of data to transfer (-n or -k option).
    Print periodic, intermediate bandwidth, jitter, and loss reports at specified intervals (-i option).
    Run the server as a daemon (-D option)
    Use representative streams to test out how link layer compression affects your achievable bandwidth (-F option).
    A server accepts a single client simultaneously (iPerf3) multiple clients simultaneously (iPerf2)
    New: Ignore TCP slowstart (-O option).
    New: Set target bandwidth for UDP and (new) TCP (-b option).
    New: Set IPv6 flow label (-L option)
    New: Set congestion control algorithm (-C option)
    New: Use SCTP rather than TCP (--sctp option)
    New: Output in JSON format (-J option).
    New: Disk read test (server: iperf3 -s / client: iperf3 -c testhost -i1 -F filename)
    New: Disk write tests (server: iperf3 -s -F filename / client: iperf3 -c testhost -i1)
