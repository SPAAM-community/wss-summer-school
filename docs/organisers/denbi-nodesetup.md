# deNBI node setup

# SPAAM summer school deNBI cloud nodes preparation 2025

## Pre-preparation

- Have requested and been granted a deNBI project on [deNBI portal](https://cloud.denbi.de/portal/)
- Create workshop on [SimpleVM portal](https://simplevm.denbi.de)
  - Projects on Side Bar > Select Project > New Workshop
- Tutor workflow (required extra step to allow access to all nodes)
  - On deNBI Portal > Projects > Add Members to see instructions
  - [New tutor] Send deNBI LifeSciences sign up link
  - [New and old tutors] Once signed up follow participants workflow invite link (See next step in instructions)
  - [Admin] may need to make tutors 'admins' also on deNBI project too
- Send to ALL participants and tutors workshop invite link (all need elixir account (orcid etc.))
  - Go to [SimpleVM portal](https://simplevm.denbi.de)
  - Go to _workshop_ on sidebar
  - Send 'Create invitation' link to all students
- Participant (Student) workflow
  - Go to SimpleVM invite link
  - Pick log-in and/or register with system of choice
  - Register elixir
  - Confirm email
  - T&Cs Elixir
  - T&Cs Denbi
  - Email for SPAAMsumScho
  - Confirm email
  - [Admin approve] (SimpleVM Portal -> Project -> <Project Name/> -> Project Member List > See Applications)
- Once all invited
  - [Admin] SimpleVM: Accept all participant requests on project
  - [Admin] SimpleVM: On workspace page, 'show addable Tutors' and add tutors (remember must still be on the deNBI project too!)

## Base Snapshot VM Set up

> Can request last years archived, if requested for archiving, by contacting helpdesk to move to current project:
>
> The volume is: SPAAMSumScho2024Final2
>
> The snapshot is: SPAAMSumScho24-FinalPatch1

- Log into [SimpleVM portal](https://simplevm.denbi.de)
- Go to workshops on side bar
- 'Create new instances' section > 'New Instance' > Follow workflow

Create a machine:

- de.NBI medium + ephemeral: 14 VCPUs - 32 GB RAM - 50 GB root disk + 150 GB ephemeral disk
- Research environment: [Guacamole](https://cloud.denbi.de/wiki/simple_vm/customization/#apache-guacamole))
- Add user (yourself)
- Start VM

Once spun up, log in and clean up desktop environment

- Guacamole user: denbi, denbi
- Select Ubuntu Server US Keyboard Layout (can also be the recent connection one)
  - If asked to authenticate color managed device use password below
- Ubuntu user pass: `denbi` (old: `ogvkyf`)
- Deactivate screensaver/lockscreen & apperance dark mode
  - X applications (top left menu on desktop) -> Settings -> Screensaver -> (Tab) Screensaver Disable
  - X applications (top left menu on desktop) -> Settings -> (Tab) Lock Screen -> Disable
  - X applications (top left menu on desktop) -> Appearance -> Greybird-dark
- Download and set wallpaper from SPAAM summer school website github repo (assets/media/spaam-background-dark.png - 1920 x 965)
- Turn off unsafe paste warnings in terminal
  - Open Terminal -> Edit -> Preferences -> 'Untick Show unsafe paste dialog'

Now install required general software

- Install a PDF viewer

  ```bash
  sudo apt install evince
  ```

  Once made, can also drag and drop to the desktop from X Applications > Office > Document Viewer (click on the desktop shortcut once and 'mark as executable')

- Install general useful extras
  ```bash
  sudo apt install tree
  sudo apt install rename
  ```
- Install additional libraries (required for Tempest and MEGAX etc.)

  ```bash
  sudo apt install openjdk-11-jdk ## tempest
  sudo apt install libgconf-2-4 ## MEGAX
  sudo apt install libgsl-dev libeigen3-dev ## metadmg
  ```

- Bookmark textbook to Firefox webbrowser

Install bioinformatics software

- Install Conda & libmamba
  ```bash
   mkdir ~/bin
   cd ~/bin
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
  bash Miniconda3-latest-Linux-x86_64.sh
  ```
  - Install into `/home/ubuntu/bin/miniconda3`
  - Run init(ialise): Yes
  - To load conda into PATH:`source ~/.bashrc`
  - To turn off base: `conda config --set auto_activate_base false`
  - Restart terminal
  - Delete Miniconda SH
    ```bash
    cd ~/bin
    rm Miniconda3-latest-Linux-x86_64.sh
    ```
  - Set up channels
    ```bash
    conda config --add channels bioconda
    conda config --add channels conda-forge
    ```
- Create session conda environments

  - Download the environment ymls from https://github.com/SPAAM-community/intro-to-ancient-metagenomics-book/tree/main/assets/envs, and create each env

    ```bash
    wget https://github.com/SPAAM-community/intro-to-ancient-metagenomics-book/raw/main/assets/envs/{accessing-ancient-metagenomic-data,ancient-metagenomic-pipelines,authentication,bare-bones-bash,contamination,genome-mapping,git-github,phylogenomics,python-pandas,r-tidyverse,taxonomic-profiling}.yml ## denovo-assembly, coming later! removed from list - 2024-05-29

    for i in *.yml; do
        printf "\n###### PREPARING $i #######\n"
        conda env create -q -f "$i"
    done
    ```

    > ⚠️ monitor to look for failures in log!

- Install [docker](https://docs.docker.com/engine/install/ubuntu/)

  ```bash
  ## Prepare apt repo
  sudo install -m 0755 -d /etc/apt/keyrings
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  sudo chmod a+r /etc/apt/keyrings/docker.gpg
  echo \
    "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
    sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  sudo apt update

  ## Install docker itself
  sudo apt -y install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

  ## Test Install
  docker run hello-world

  ## Fix permissions if 'permissions denied error'
  sudo groupadd docker ## May already exist
  sudo usermod -aG docker $USER
  newgrp docker

  sudo reboot ## will kick you out, but it'll be back in a minute or two; note volume will need to be re-mounted after

  cd ~/bin

  ## Retest
  docker run hello-world
  ```

- Install rename

  ```bash
  sudo apt install rename
  ```

  > ⚠️ you may get weird kernal/reboot quesitons, went with default... it didn't cause any problems for me...

- Download and install (move to bin, remove any additional)
  - [PHYLOGENOMICS ONLY] Tempest:
    - Manually download using the Guacamole firefox instance from
      ```bash
      wget https://github.com/beast-dev/Tempest/releases/download/v1.5.3/TempEst_v1.5.3.tgz
      tar -xf TempEst_v1.5.3.tgz
      rm TempEst_v1.5.3.tgz
      echo "alias tempest='bash /home/ubuntu/bin/TempEst_v1.5.3/bin/tempest'" >> ~/.bashrc && source ~/.bashrc
      tempest ## test that opens window
      ```
  - [PHYLOGENOMICS ONLY] MEGAX
    ```bash
    wget https://www.megasoftware.net/releases/mega_11.0.13-1_amd64.deb
    sudo dpkg -i mega_11.0.13-1_amd64.deb
    rm mega_11.0.13-1_amd64.deb
    which mega ## test that opens window
    ```
    > ⚠️ you may get weird kernal/reboot quesitons, went with default... it didn't cause any problems for me...
- [FUNCTIONAL PROFILING ONLY] Install humann3 database to volume (note need to have mounted VM before!)
  ```
  humann3_databases --download uniref uniref90_ec_filtered_diamond /vol/volume/5c-functional-genomics/humann3_db
  ```
- [DE NOVO ASSEMBLY ONLY] Install metaWRAP <!-- TODO: Replace with metawrap-mg from bioconda? -->

  ```bash
  conda create -n metawrap-env python=2.7
  conda activate metawrap-env
  conda install biopython bwa maxbin2=2.2.7 metabat2 samtools=1.9
  cd ~/bin/
  git clone https://github.com/bxlab/metaWRAP.git
  echo "export PATH=$PATH:~/bin/metaWRAP/bin" >> ~/.bashrc && source ~/.bashrc
  ```

- Set up Volume (NOTE: this now may happen automatically on instance generation, however instructions here in case you reboot and have to remount)

  - Cloud Portal > Virtual Machines > Instances > Volumes > Create and Attach Volume
    - Specify e.g. roughly total amount divided by number of nodes
    - Attach to the setup VM
  - Go back to VM and follow these [instructions](https://cloud.denbi.de/wiki/simple_vm/volumes/#mount-a-volume)

    ```bash
    lsblk -o NAME,SIZE,MOUNTPOINT,FSTYPE,TYPE | egrep -v "^loop"
    ## Record NAME column i.d, e.g. `vdd`
    sudo mkfs.ext4 /dev/<NAME> ## Don't do if already existing
    sudo mkdir -p /vol/volume
    sudo mount /dev/<NAME> /vol/volume
    cd ~/vol/volume && touch hello ## test can write, if not next command
    sudo chown -R ubuntu:ubuntu /vol/volume
    cd ~/vol/volume && touch hello ## test can write, if not panic
    rm hello
    ```

  - In the file browser, navigate to `/vol/volume`, right click on it and 'Send to' Desktop and Sidebar (to make accessing easier)

- Download session Data

  - Inside `/vol/volume` make a directory for each of the sessions, then download the required data.

    e.g. to download from the [Zenodo archives](https://zenodo.org/communities/spaam-community/records?q=%22Introduction%20to%20Ancient%20Metagenomics%20Textbook%20%28Edition%202023%29%22&l=list&p=1&s=10&sort=bestmatch) from 2023

    ```bash
    cd /vol/volume/
    mkdir <SESSION>/
    cd <SESSION>/
    wget <ZENODO_URL WITHOUT ?download=1 at the end>
    tar xzvf *.tar.gz && mv */* .
    rm -r <UNTARRED_ZENODO_FILENAME>* day*.yml README.md
    ```

      <!-- TODO 2024: split authentication and decontamination! -->
      <!-- TODO 2024: minimise pipelines -->
      <!-- TODO 2024: get denovo assembly when ready -->

    > :warning: In some cases (r-tidyverse, taxonomic-profiling), this may require a clone from elsewhere

      <!-- TODO ADD ISNTRUCTORS TO TEST -->

- Once installation and volume set up is finished, go back to deNBI cloud portal dashboard, find the VM, stop the VM running (don't delete!) Once stopped, Actions > Create SNapShot

<!-- TODO: DATA! -->
<!-- TODO: pipelines conda env installation! -->

- Creae

## Spinning up Participant VM

On simpleVM workspace

- Manage Workshop > Select Workshop NAme > Add VM
- Select flavor (here: 14 core, 32GB RAM, 50GB root disk)
- Select Image as Snapshot > The workshop (will auto-select denbi)
- Add User: the User and ALL admins
- Add (pre-made) volume!
  - Make sure tell deNBI ASAP to create copies!
  - Mount with e.g. ` sudo mount /dev/vdd /vol/volume`
  - To check device name double check '86 GB volume' on desktop or `lsblk` and look for disk with same space size
- Send email via Workshops > Manage

## Misc

- Need to mount the volumne (to be created)

  - Must contain all software, data
  - bashrc needs to be updated to point to miniconda install on volume

- Volume for data/software/saving
  - https://cloud.denbi.de/wiki/simple_vm/volumes/#create-the-volume-file-system-once
  - Make it once (create file system),
  - then each time spinning up node will need to make mount point and mount the node
- Use snapshot to include all the software etc?

### METADMG

```bash
(authentication) ubuntu@james-fellows-yates-ca0f5:~/bin$ cat metadmg.yml
name: metaDMG
channels:
  - conda-forge
  - bioconda
  - defaults
dependencies:
  - conda-forge::python=3.9.15
  - bioconda::htslib=1.17
  - conda-forge::eigen=3.4.0
  - conda-forge::cxx-compiler=1.5.2
  - conda-forge::c-compiler=1.5.2
  - conda-forge::gsl=2.7
  - conda-forge::iminuit=2.17.0
  - conda-forge::numpyro=0.10.
  - conda-forge::joblib=1.2.0
  - conda-forge::numba=0.56.2
  - conda-forge::flatbuffers=22.9.24
  - conda-forge::psutil=5.9.4

conda env create -f metadmg.yml
conda activate metaDMG
git clone https://github.com/metaDMG-dev/metaDMG-cpp.git
cd metaDMG-cpp
make clean && make CPPFLAGS="-L${CONDA_PREFIX}/lib -I${CONDA_PREFIX}/include" HTSSRC=systemwide -j 8
#git checkout abd303e808c7d74166f305ac88ef538af9b1d44d
pip install git+https://github.com/metaDMG-dev/metaDMG-core #@stopiferrors_branch
pip install metaDMG[viz]
conda deactivate

## DIDNT WORK
echo "alias metaDMG-cpp='/home/ubuntu/bin/metaDMG-cpp/metaDMG-cpp'" >> ~/.bashrc && source ~/.bashrc

##BETTER -> So use proper path update in bashrc
export PATH="$PATH:/home/ubuntu/bin/metaDMG-cpp"
```
