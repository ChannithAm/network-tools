# អត្ថបទស្ដីអំពី Nmap tool

## <a name="intro">សេចក្ដីផ្ដើម</a>

* Nmap (Network Mapper) គឺជាsecurity scanner​​ ដែលបង្កើដោយលោក **Gordon Lyon** នៅឆ្នាំ១៩៩៧​ ហើយបាន​ក្លាយជា de facto standard សំរាប់network mapping និង port scanning ដែលអាចអោយnetwork administrators​រកឃើញនូវhosts និងserviceនៅលើបណ្ដាញកុំព្យូទ័រ ហើយបង្កើតជាmapនៃnetwork។
* Nmap ត្រូវបានប្រើប្រាស់យ៉ាងទូលំទូលាយដោយnetwork admins និងpenetration testers (ក្រៅពីនោះក៏មាន malicious hackesផងដែរ)។ Nmap គឺfreeក្នុងការប្រើប្រាស់ ហើយreleaseក្រោមGPL license។ License នេះផ្ដល់ដល់​អ្នកមានសិទ្ធក្នុងការ run, សិក្សា, ចែករំលែក និងmodify the software​ ផងដែរ។ អ្នកអាចស្វែងរកNmap source code នៅ[ទីនេះ](https://github.com/nmap/nmap)។
* Nmap ត្រូវបានបង្កើតឡើងដំបូងសំរាប់Linux តែវាក៏ត្រូវបានផ្លាស់ប្ដូរសំរាប់ប្រើនៅលើប្រពន្ធប្រតិបត្តិការសំខាន់ៗដូចជា Windows, Solaris, HP-UX, -ល-។

## < name="feature">២. មុខងារ</a>

* ជាធម្មតាNmapត្រូវបានប្រើសំរាប់port scanning តែវាក៏ផ្ដល់នៅមុខងារបន្ថែមផ្សេងទៀតផងដែរ៖
  * Host discovery
  * Operating system detection
  * Service version detection
  * ពត័មានអំពីបណ្ដាញដែលជាtagetsដូចជា៖ DNS names, device types, MAC addresss
  * មានសមត្ថភាពscan for well-know vulunerabilities

## <a name="install">៣. ដំឡើង</a>

ខាងក្រោមនេះជារបៀបដំឡើងNmapនៅលើUbuntu។ នៅលើLinux distributionខ្លះមានNmapស្រាប់តែម្ដង ដូច្នេះជំហ៊ាន​ដំបូងយើងត្រូតពិនិត្យមើលថា តើបានដំឡើងNmapរួចហើយ ឫនៅ។ អ្នកប្រើcommand ខាងក្រោម៖
```
nmap --version
```

ប្រសិនបើវាបង្ហាញថា Nmapមិនទាន់បានដំឡើងទេ អ្នកប្រើcommandនេះដើម្បីដំឡើង
```
sudo apt-get install nmap
```

ការប្រើប្រាស់ផ្សេងទៀត អ្នកចូលទៅlinkនៅលើ ផ្នែកឯកសារយោង។


## <a name="reference">ឯកសារយោង</a>

[1] http://geek-university.com/nmap/install-nmap-on-linux/
