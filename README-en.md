# CCNA Labs — Practice Repository

This repository brings together practical labs I use to study and review the topics required by the Cisco CCNA certification. The goal is to centralize materials from reliable sources in a single place, offering a variety of options for practicing switching, routing, and network services skills.

## Discord Server

I have also created a Discord server for anyone who wants to participate or contribute: [NetworkLabs](https://discord.gg/VTpuvYmp)

## Lab Sources

- **[CertSkills](https://www.certskills.com)**
- **[Packet Tracer Network](https://www.packettracernetwork.com)**
- **[Jeremy's IT Lab](https://www.jeremysitlab.com)**
- **[Gustavo Kalau Workshops](https://www.youtube.com/@GustavoKalau/playlists)**

Note: This repository organizes and references study materials. Please respect the original licenses and terms of use of the authors and courses.

## Repository Structure

The labs are organized by topic to make studying easier. Each lab directory contains:

- `instructions.md`: lab guide and objectives.
- `lab-solution.md`: solution reference.
- `assets/`: topology images, screenshots and `.zip` files with topologies (when applicable).

### 📁 Organization by Topic

#### `cli-basics/` - CLI Fundamentals

Basic switch and router configurations, CLI access security, SSH/Telnet, and command exploration.

- `01_basic-switch-configuration/`
- `02_basic-switch-setup/`
- `03_basic-router-setup/`
- `04_config-lab_cli-passwords-1/`
- `05_config-lab_cli-passwords-2/`
- `06_config-lab_enabling-ssh-and-disabling-telnet/`
- `07_config-lab_switch-ip-1/`
- `08_config-lab_login-security-1/`
- `09_config-lab_cli-miscellany-1/`
- `10_config-lab_switch-duplex-and-speed/`
- `11_config-lab_switch-admin-config/`
- `12_config-lab_switch-ip-config/`
- `13_config-lab_cli-exploration-1/`
- `14_config-lab_cli-exploration-2/`
- `15_config-lab_telnet-config/`
- `16_config-lab_ssh-config/`

#### `switching-layer2/` - Layer 2 Switching and Protocols

VLANs, trunking, STP/RSTP, VTP, EtherChannel (L2 and L3), and switching troubleshooting.

- `01_ethernet-lan-switching/`
- `02_configuring-switch-interfaces/`
- `03_vlan-and-vtp-configuration/`
- `04_lan-switching-troubleshooting/`
- `05_config-lab_vlan-basics-3/`
- `06_config-lab_data-and-voice-vlan-1/`
- `07_config-lab_data-and-voice-vlan-2/`
- `08_config-lab_trunking-puzzle-1/`
- `09_config-lab_basic-vlans/`
- `10_config-lab_trunking-for-only-some-vlans/`
- `11_config-lab_rstp-config-1/`
- `12_config-lab_rstp-config-2/`
- `13_config-lab_l2-etherchannel-1/`
- `14_config-lab_l2-etherchannel-2/`
- `15_config-lab_big-vlan-and-stp-lab-1/`
- `16_config-lab_roas-basics-1/`
- `17_config-lab_layer3-switching-1/`
- `18_config-lab_layer3-switching-2/`
- `19_config-lab_layer3-switching-with-svis/`
- `20_config-lab_layer3-switching-with-routed-ports/`
- `21_config-lab_l3-etherchannel-1/`

#### `static-routing/` - Static Routing

IPv4 and IPv6 static route configuration and routing troubleshooting.

- `01_static-routes/`
- `02_ip-routing-troubleshooting/`
- `03_config-lab_ipv4-static-routes-1/`
- `04_config-lab_ipv4-static-routes-2/`
- `05_config-lab_ipv4-static-routes-3/`
- `06_config-lab_ipv6-static-routes-1/`
- `07_config-lab_ipv6-static-routes-2/`
- `08_config-lab_ipv4-static-routes-practice-exam-question-1/`

#### `dynamic-routing/` - Dynamic Routing

Configuration and optimization of dynamic routing protocols such as OSPF and RIP.

- `01_rip-v2/`
- `02_config-lab_ospf-interface-config-1/`
- `03_config-lab_ospf-interface-config-2/`
- `04_config-lab_ospf-network-config-1/`
- `05_config-lab_ospf-network-config-2/`
- `06_config-lab_ospf-multi-area-ospf-1/`
- `07_config-lab_ospf-multi-area-ospf-2/`
- `08_config-lab_ospf-dr-priority/`
- `09_config-lab_ospf-network-type/`
- `10_config-lab_ospf-router-ids/`
- `11_config-lab_ospf-metrics/`

#### `basic-security/` - Basic Security

ACLs (standard and extended), Port Security, DHCP Snooping, DAI, and other layer 2 security techniques.

- `01_port-security/`
- `02_config-lab_standard-numbered-acl-1/`
- `03_config-lab_standard-named-acl-1/`
- `04_config-lab_extended-numbered-acl-1/`
- `05_config-lab_extended-named-acl-1/`
- `06_config-lab_basic-port-security-1/`
- `07_config-lab_basic-port-security-2/`
- `08_config-lab_basic-port-security-3/`
- `09_config-lab_basic-port-security-4/`
- `10_config-lab_dhcp-snooping-1/`
- `11_config-lab_dhcp-snooping-2/`
- `12_config-lab_dai-1/`

#### `ip-services/` - IP Services

IPv4/IPv6 addressing, DHCP, NAT/PAT, serial links (HDLC, PPP, Frame Relay), NTP, Syslog, and discovery protocols (CDP/LLDP).

- `01_configuring-serial-links/`
- `02_hdlc/`
- `03_ppp/`
- `04_frame-relay/`
- `05_config-lab_ipv4-addressess-1/`
- `06_config-lab_ipv4-addressess-2/`
- `07_config-lab_ipv4-addressess-3/`
- `08_config-lab_ipv4-addressess-4/`
- `09_config-lab_ipv4-addressess-5/`
- `10_config-lab_dhcp-relay/`
- `11_config-lab_router-as-dhcp-client/`
- `12_config-lab_ipv6-eui64-addressing-1/`
- `13_config-lab_ipv6-global-unicast-addressing-1/`
- `14_config-lab_ipv6-special-addresses-1/`
- `15_config-lab_ipv6-special-addresses-2/`
- `16_config-lab_cdp-lldp-1/`
- `17_config-lab_ntp-client-and-server/`
- `18_config-lab_syslog-1/`
- `19_config-lab_syslog-2/`
- `20_config-lab_syslog-3/`
- `21_config-lab_dynamic-nat-1/`
- `22_config-lab_static-nat-1/`
- `23_config-lab_interface-pat-1/`
- `24_config-lab_pat-with-a-pool-1/`

## Prerequisites

- PNETLab or EVE-NG
- Basic Cisco IOS CLI knowledge.

## How to Use

1. Clone the repository.
2. Navigate to the desired topic (e.g., `cli-basics/`, `switching-layer2/`, etc.).
3. Choose a lab directory (e.g., `cli-basics/02_basic-switch-setup/`).
4. Read the `instructions.md` to understand objectives and steps.
5. Open the corresponding topology in your tool (usually files in `assets/lab/` → `.zip` containing `.unl`).
6. Run the configurations according to the guide.
7. Compare your results with `lab-solution.md` and make adjustments as needed.

Example clone:

```bash
git clone https://github.com/bl4cktux89/labs-ccna.git
cd labs-ccna
```

### Importing a Lab into PNETLab/EVE-NG

To import a lab, download the `.zip` file inside the desired lab folder. Then, log in to your PNETLab (the process is similar in EVE-NG):

1. On the main screen, click 'Import' as shown below:
    ![Importing the Lab](./assets/img/00-import-lab.png)

2. Select the file and click 'Upload':
    ![Choosing the file](./assets/img/01-choose-file.png)

3. Click 'Upload' in the 'Actions' column:
    ![Uploading](./assets/img/02-upload.png)

4. At the end of the process, you will see a success message:
    ![Upload completed successfully](./assets/img/03-success.png)

5. The lab you uploaded will appear in the lab list:
    ![Listed lab](./assets/img/04-listed-lab.png)

6. Click the lab and then click 'Open':
    ![Opening the Lab](./assets/img/05-abrindo-o-lab.png)

7. Before starting the devices, complete the steps below to ensure they start with the pre-configured settings I prepared. Hover over the icon on the left to open the options menu:
    ![Options Menu](./assets/img/06-iniciando-o-lab-1.png)

8. Once the menu opens, click 'Setup Nodes':
    ![Setup Nodes](./assets/img/07-iniciando-o-lab-2.png)

9. Click 'Wipe All Nodes' to clear all device configurations:
    ![Wipe All Nodes](./assets/img/08-iniciando-o-lab-3.png)

10. Confirm you want to clear the configurations by clicking 'Yes':
    ![Wipe All Nodes? Yes!](./assets/img/09-iniciando-o-lab-4.png)

11. Check the right-hand notifications to see that the nodes have been wiped:
    ![Wiped](./assets/img/10-iniciando-o-lab-5.png)

12. Open the options menu again, then 'Setup Nodes' and click 'Set Nodes Startup-cfg To Exported':
    ![Set Nodes Startup-cfg To Exported](./assets/img/11-iniciando-o-lab-6.png)

13. Check the notifications to confirm that after boot, the devices will start with the previously applied configurations:
    ![Exported Notification](./assets/img/12-iniciando-o-lab-7.png)

14. Now we will finally start the devices. You can power them on individually or start them all at once. To start them all at once, open the options menu again, click 'Setup Nodes', and then click 'Start All Nodes':
    ![Start All Nodes](./assets/img/13-iniciando-o-lab-8.png)

15. When the 'Play' icon appears, you can access the devices:
    ![Devices Started](./assets/img/14-iniciando-o-lab-9.png)

16. Click one of the devices to confirm it already has the configuration applied, as the hostname should already be set:
    ![Devices Started](./assets/img/15-iniciando-o-lab-10.png)

To verify the configurations, the commands required may vary from lab to lab, but the commands below should be sufficient in most cases:

```cisco
enable
show running-config
```

## Study Best Practices

- **Redo**
- **Vary**
- **Document**

## Roadmap (future ideas)

- Include verification checklists (show commands) per topic.
- Add more advanced troubleshooting labs.

## Contributing

Suggestions and corrections are welcome. Open an Issue or submit a Pull Request with:

- Clear description of the issue or improvement.
- Screenshots/topologies if applicable.
- References (when derived from third-party content).

## License

See the `LICENSE` file for details. Third-party materials cited and organized here remain under their respective licenses.
