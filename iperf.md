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
<img src="https://i.imgur.com/oORQ3T8.png?1">

ចំពោះករណីខាងលើ iPerfស្ដាប់ port 5001 ជាកំណត់។ ហើយយើងអាចកំណត់portបានដោយប្រើប៉ារ៉ាម៉ែត្រ -p ឫ --port។

ប៉ារ៉ាមែត្រៈ
```
Client/Server:
  -f, --format    [kmKM]   format to report: Kbits, Mbits, KBytes, MBytes
  -i, --interval  #        seconds between periodic bandwidth reports
  -l, --len       #[KM]    length of buffer to read or write (default 8 KB)
  -m, --print_mss          print TCP maximum segment size (MTU - TCP/IP header)
  -o, --output    <filename> output the report or error message to this specified file
  -p, --port      #        server port to listen on/connect to
  -u, --udp                use UDP rather than TCP
  -w, --window    #[KM]    TCP window size (socket buffer size)
  -B, --bind      <host>   bind to <host>, an interface or multicast address
  -C, --compatibility      for use with older versions does not sent extra msgs
  -M, --mss       #        set TCP maximum segment size (MTU - 40 bytes)
  -N, --nodelay            set TCP no delay, disabling Nagle's Algorithm
  -V, --IPv6Version        Set the domain to IPv6

Server specific:
  -s, --server             run in server mode
  -U, --single_udp         run in single threaded UDP mode
  -D, --daemon             run the server as a daemon

Client specific:
  -b, --bandwidth #[KM]    for UDP, bandwidth to send at in bits/sec
                           (default 1 Mbit/sec, implies -u)
  -c, --client    <host>   run in client mode, connecting to <host>
  -d, --dualtest           Do a bidirectional test simultaneously
  -n, --num       #[KM]    number of bytes to transmit (instead of -t)
  -r, --tradeoff           Do a bidirectional test individually
  -t, --time      #        time in seconds to transmit for (default 10 secs)
  -F, --fileinput <name>   input the data to be transmitted from a file
  -I, --stdin              input the data to be transmitted from stdin
  -L, --listenport #       port to receive bidirectional tests back on
  -P, --parallel  #        number of parallel client threads to run
  -T, --ttl       #        time-to-live, for multicast (default 1)
  -Z, --linux-congestion <algo>  set TCP congestion control algorithm (Linux only)

Miscellaneous:
  -x, --reportexclude [CDMSV]   exclude C(connection) D(data) M(multicast) S(settings) V(server) reports
  -y, --reportstyle C      report as a Comma-Separated Values
  -h, --help               print this message and quit
  -v, --version            print version information and quit

[KM] Indicates options that support a K or M suffix for kilo- or mega-
```

## <a name="ref">អត្ថបទយោង</a>

[1] iPerf3 https://github.com/esnet/iperf/issues/480
