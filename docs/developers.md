# Developers

The current server setup uses Pterodactyl to host and manage server instances across one or more nodes. We use Velocity for the proxy that allows players to move between servers and then use custom mods and plugins to handle whitelisting and inventory sync.

## Pterodactyl

## Velocity Proxy

## Server Whitelist

## Inventory Sync

### World Sync
Some things require a bit of world to world syncing as well. Currently we use rsync to automatically sync photos from the exposure mod across servers.

## Technical specs
Our main node is an [AX102 from Hetzner](https://www.hetzner.com/dedicated-rootserver/matrix-ax/). This server currently supports around 10 Minecraft server instances without any issues. Here are the specs for that server.

| Specification         | Details                                                                                                                                                                      |
| --------------------- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CPU Model**         | AMD Ryzen™ 9 7950X3D                                                                                                                                                         |
| **CPU Details**       | 16 Cores (Raphael, Zen 4) with AMD 3D V-Cache™, Simultaneous Multithreading, AMD-V virtualization ([hetzner.com][1])                                                         |
| **Memory**            | 128 GB DDR5 ECC                                                      ([hetzner.com][1])                                                                               |
| **NVMe Storage**      | 2 × 1.92 TB Gen 4 NVMe SSD         ([hetzner.com][1])                                                                                  |
| **Network Interface** | 1 Gbit/s port (guaranteed bandwidth 1 Gbit/s)                                                        ([hetzner.com][1])                                                      |
| **Traffic**           | Unlimited, unmetered data transfer                                                                   ([hetzner.com][1])                                                      |
| **IP Addresses**      | 1 × Primary IPv4 & IPv6 /64 subnet                                          ([hetzner.com][1])                                                                               |

[1]: https://www.hetzner.com/dedicated-rootserver/matrix-ax/ "AMD Processors Server – High-Performance Hetzner Servers"
