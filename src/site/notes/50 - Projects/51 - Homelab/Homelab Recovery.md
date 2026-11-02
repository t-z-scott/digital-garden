---
{"dg-publish":true,"permalink":"/50-projects/51-homelab/homelab-recovery/","noteIcon":"","created":"2026-11-01T17:21:58.438-08:00","updated":"2026-11-01T18:20:11.913-08:00","ctime":"2026-11-01T17:21:58.438-08:00","mtime":"2026-11-01T18:20:11.913-08:00","dg-note-properties":{}}
---

Date created: [[20 - Logs/2026-11-01\|2026-11-01]] 
Type: #type/original 
Area: #area/personal-development 
Keywords: #keyword/technology #keyword/cybersecurity 
Last updated: 

---

up: [[50 - Projects/51 - Homelab/Homelab README\|Homelab README]] 

# Disaster Recovery
## Scenario
Complete loss of the homelab VM.

## Recovery Steps
1. Create new Ubuntu Server VM (4GB RAM, 2 cores, 50GB disk)
2. Install OpenSSH during setup
3. Run: `ansible-playbook -i inventory.ini playbook.yml`
4. Restore data from backup:
	- `restic -r /mnt/usb/backups restore latest --target /tmp/restore`
	- Copy data directories back
5. Verify all services:
	- Gitea: `http://<vm-ip>:3000` 
	- Jellyfin: `http://<vm-ip>:8096` 
	- Grafana: `http://<vm-ip>:3001` 
6. Verify monitoring is collecting data
7. Verify security: fail2ban active, UFW enabled, auditd running
8. Test a backup restore

## Expected Time
Under 30 minutes.
## Last Tested
N/A
