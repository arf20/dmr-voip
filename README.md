# dmr-voip
DMR VoIP gateway

## Architecture

 - [HBLink3](https://github.com/HBLink-org/hblink3)
    - [systemd](https://github.com/lz5pn/HBlink3)
    - [docker](https://github.com/ShaYmez/hblink3-docker-install)
 - [DMRGateway](https://github.com/g4klx/DMRGateway)
 - [MMDVMHost](https://github.com/g4klx/MMDVMHost)

```
Core

       +-------------+     #==============#     +-------------+
... -->| HBLink3     |<--->$ VoIP Gateway $<--->| VoIP Server |<-- ...
       +-------------+     #==============#     +-------------+
          ^                                            ^
RAN       |                                            |
          v                                            |
+------------+------+                                  |
| DMRGateway | ...  |                                  |
+------------+------+                                  |
| MMDVMHost         |                                  |
+-------------------+                                  |
| Raspberry Pi      |                                  |
+-------------------+                                  |
| MMDVM Hat         |                                  |
+-------------------+                                  |
         ^                                             |
UE       |                                             |
         v                                             v
     +-------+                                     +-------+
     | Radio |                                     | Phone |
     +-------+                                     +-------+
```

