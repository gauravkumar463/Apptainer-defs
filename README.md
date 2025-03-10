# Apptainer-defs
Definition files to build some useful containers

# Local download requirement
You need to have a local copy of openfoam and ThirdParty to build ofv2312basic.def container.

# Build instruction

Use the following command to build the container:

apptainer build <filename>.sif <filename>.def

Use the following command to run the container:

apptainer run <filename>.sif sh -c 'mpirun -n 4 icoFoam -parallel'    or,
apptainer exec <filename>.sif sh -c 'mpirun -n 4 icoFoam -parallel'

apptainer shell <filename>.sif   #to directly shell into the container

# Build debug
Run the following command if you see this error:

`ERROR  : Failed to create mount namespace: mount namespace requires privileges, check Apptainer installation`

`sudo sysctl -w kernel.apparmor_restrict_unprivileged_userns=0`

# More usage with gpus demonstrated in https://github.com/gauravkumar463/rhoLDFSSFoam_gpu.git
