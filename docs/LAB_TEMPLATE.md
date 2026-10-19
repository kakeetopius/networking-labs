# Lab NN: Lab Title

## 1. Description

## 2. Background

## 3. Objectives

By the end of this lab you will have:

- [ ] Objective 1
- [ ] Objective 2
- [ ] Objective 3

## 4. Topology and addressing

**Devices**

| Device | Role       | Vendor / Image | Version |
| ------ | ---------- | -------------- | ------- |
| R1     | Router     | Cisco IOSv     | 15.9    |
| R2     | Router     | MikroTik CHR   | 7.x     |
| Admin  | Admin host | Linux          | -       |

**Addressing**

| Device | Interface | IP address / mask | Connected to | Notes      |
| ------ | --------- | ----------------- | ------------ | ---------- |
| R1     | Gi0/0     | 10.10.10.1/24     | Switch       | Management |
| R2     | ether1    | 10.10.10.2/24     | Switch       | Management |

**VLAN TABLE**

## 5. Tools and versions

| Item                                | Version         |
| ----------------------------------- | --------------- |
| GNS3 / containerlab / Packet Tracer | x.y.z           |
| Host OS                             | Ubuntu 24.04    |
| Device images                       | see table above |

## 6. Prerequisites

- Lab NN: previous lab title
- Knowledge of ...
- RAM / CPU needed, e.g. 8 GB RAM, 4 vCPUs

## 7. Setup

1. Obtain and add the images.
2. Deploy the topology:
   - GNS3: `File > Import portable project` and select `file.gns3project`
   - containerlab: `sudo containerlab deploy -t file.clab.yml`
   - Packet Tracer: open `file.pkt`
3. Start all devices and wait for boot.
4. Apply the starting configs from `configs/initial/` if provided.

## 8. Walkthrough

### Step 1: Task name

**Why:**

**Vendor 1**

```
commands
```

**Vendor 2**

```
commands
```

### Step 2: Task name

Repeat the pattern above.

### Command comparison (optional)

| Goal   | Vendor 1  | Vendor 2  |
| ------ | --------- | --------- |
| Goal 1 | `command` | `command` |
| Goal 2 | `command` | `command` |

## 9. Verification

### Objective 1

```
command
expected output
```

### Objective 2

```
command
expected output
```

**Evidence:** see `verification/`(verification/) for full output and packet captures.

## 10. Troubleshooting challenge

## 11. Key takeaways

- Takeaway 1
- Takeaway 2

## 12. References

- Vendor documentation: title and link
- RFC NNNN: title and link
- Original tutorial this lab was adapted from, and what you changed

---

**Files in this folder**

| Path            | Contents                               |
| --------------- | -------------------------------------- |
| `topology.png`  | Network diagram                        |
| `configs/`      | Per-device configs (initial and final) |
| `lab file`      | `.gns3project` / `.clab.yml` / `.pkt`  |
| `verification/` | Command output, scans and captures     |
