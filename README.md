# networking-labs

Hands-on networking labs moving progressively from CCNA level to advanced.

## About

A collection of hands-on networking labs I built while learning and practising, from CCNA fundamentals to advanced routing, data center and automation topics. Each lab is self-contained and includes a topology, configs, a step-by-step walkthrough, verification output etc.

## Tools and vendors

**Emulation / virtualisation**

| Tool                                                           | Used for                                                 |
| -------------------------------------------------------------- | -------------------------------------------------------- |
| [Packet Tracer](https://www.netacad.com/courses/packet-tracer) | Cisco Specific or Cisco Only labs                        |
| [GNS3](https://www.gns3.com/)                                  | Multi-vendor labs / labs that require real device images |
| [containerlab](https://containerlab.dev/)                      | Topologies defined as code.                              |

**Vendors:** Cisco, MikroTik, and more as the repo grows

## Repository structure

```
networking-labs/
├── README.md
├── 01-fundamentals/
│   └── 01-device-hardening/
│       ├── README.md          <- lab write-up
│       ├── topology.png       <- diagram
│       ├── configs/           <- per-device configs
│       ├── lab files/         <- .gns3project / .clab.yml / .pkt
│       └── verification/      <- command output, captures, scans
├── 02-routing/
├── 03-wan-and-services/
├── 04-security/
├── 05-data-center/
└── 06-automation/
```

## Lab index

## How to use a lab

1. Open the lab folder and read its `README.md`.
2. Check **Tools and versions** and **Prerequisites** (earlier labs, images you need).
3. Follow the **Setup** section to deploy the topology:
   - **GNS3:** import the `.gns3project` file.
   - **containerlab:** `sudo containerlab deploy -t <lab>.clab.yml`
   - **Packet Tracer:** open the `.pkt` file.
4. Work through the walkthrough, then compare your results against the `verification/` folder.

## License

Documentation and configs are released under the [MIT License](LICENSE).  
Vendor software and images remain the property of their respective owners.
