# Automating Fedora Core OS Bare Metal Installation

Clone `ign-embed` to the directory in which an FCOS ISO file resides. `make embed` adds `installation.service` an automated installation unit to the FCOS ISO file.

(Also enables login as core/fcos)

```
# Transpile installer.yaml to installer.json 
make

# Embed installer.json to the ISO file in parent directory
make embed
```

To monitor the installations which occur on first boot:
```
watch -n 2 sudo systemctl list-jobs
```
