# Apptainer-defs
Definition files to build some useful containers

Run the following command if you see this error:

`ERROR  : Failed to create mount namespace: mount namespace requires privileges, check Apptainer installation`

`sudo sysctl -w kernel.apparmor_restrict_unprivileged_userns=0`
