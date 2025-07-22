# deNBI node setup

# SPAAM summer school deNBI cloud nodes preparation 2025

## Pre-preparation

- Have requested and been granted a deNBI project on [deNBI portal](https://cloud.denbi.de/portal/)
- Create workshop on [SimpleVM portal](https://simplevm.denbi.de)
  - Projects on Side Bar > Select Project > New Workshop
- Go to Workshops side bar > SPAAMSumScho25 > Get invitation link (send to participants and tutors)
- Tutor workflow (this required extra step to allow access to all nodes)
  - On deNBI Portal > Projects > Add Members to see instructions
  - [New tutor] Send deNBI LifeSicnceRI sign up link
  - [New and old tutors] Send deNBI project sign up link
  - [Admin] Check emails for joining, accept requests
  - DO NOT MAKE ALL TUTOTRS deNBI ADMIN - OTHER THAN PEOPLE FAMILIAR WITH DENBI PORTAL!
    - Anyone in the deNBI portal project, can act as tutors in the workshop itself
- Student workflow (send to ALL participants)
  - Go to [SimpleVM portal](https://simplevm.denbi.de)
  - Go to _workshop_ on sidebar
  - Get both Portal and Share invitation links, send to all participants with instructions on website with workflow instructions
    - Go to SimpleVM invite link
    - Pick log-in and/or register with system of choice
    - Register LifeScienceRI AAI
    - Confirm email
    - Register elixir
    - T&Cs Elixir
    - T&Cs Denbi / SimplVM release
    - Send request to join workshop
    - [Admin approve] (SimpleVM Portal -> Project -> <Project Name/> -> Project Member List > See Applications)
- Once all invited and accepted for the _workshop_ (deNBI portal project alone insufficient!), go to SimpleVM portal.
  - [Admin] SimpleVM: Accept all participant requests on project
  - [Admin] SimpleVM: On workspace page, 'show addable Tutors' and add tutors (remember must still be on the deNBI project too!)

## Creating SimpleVM workshop

1. On the [SimpleVM portal](https://simplevm.denbi.de/), go to the 'Projects' section on the sidebar and select SPAAMSumSchoXX
2. Press 'New Workshop'
3. Fill in the form:
   1. Workshop name: `SPAAM Summer School 20XX` (where XX is the year of the summer school)
   2. Short name: `SPAAMSumSchoXX` (where XX is
   3. Workshop description: (Copy from [https://www.spaam-community.org/wss-summer-school/#/?id=about](https://www.spaam-community.org/wss-summer-school/#/?id=about))
   4. Press 'Submit Workshop'

## Base Snapshot VM Set up

> Can request last years archived, if requested for archiving, by contacting helpdesk to move to current project:
>
> The volume is: SPAAMSumScho2024Final2
>
> The snapshot is: SPAAMSumScho24-FinalPatch1

- Log into [SimpleVM portal](https://simplevm.denbi.de)
- Go to workshops on side bar > Select the SpaamSumScho25 > 'Create new instances' section > 'New Instance' > Follow workflow
  - Select workshop
  - Create a machine:
    - de.NBI medium + ephemeral: 14 VCPUs - 32 GB RAM - 50 GB root disk + 150 GB ephemeral disk
    - Research environment: [Guacamole](https://cloud.denbi.de/wiki/simple_vm/customization/#apache-guacamole))
    - New volume
      - Volume Name: `SPAAMSumScho20250623`
      - Mountpath: `/vol/volume`
      - Volume size 80
    - Add user (yourself)
    - Start VM

Switch to Instance tab, and wait for VM to spin up

- Once VM is running, expand info of VM
- Switch to the 'guacamole' tab
- Open the link
- Guacamole user: denbi, denbi
- Select Ubuntu Server UK Keyboard Layout (can also be the recent connection one)
  - If asked to authenticate color managed device use password below
- Ubuntu user pass: `denbi`
- Deactivate screensaver/lockscreen & appearance dark mode
  - X applications (top left menu on desktop) -> Settings -> Xfce Screensaver > (Tab) Screensaver Disable
  - X applications (top left menu on desktop) -> Settings -> (Tab) Lock Screen -> Disable
  - X applications (top left menu on desktop) -> Appearance -> Greybird-dark
- Download and set wallpaper from SPAAM summer school website github repo
  - Download from [here](https://github.com/SPAAM-community/spaam-community.github.io/blob/master/assets/media/spaam-background-darkmode.png) (1920 x 965)
  - Right click on desktop -> Desktop Settings -> Background -> Select the downloaded image > STyle Centered
- Turn off unsafe paste warnings in terminal
  - Open Terminal -> Edit -> Preferences -> 'Untick Show unsafe paste dialog'
- In file browser navigate to `/vol/volume/` and bookmark to the side bar by pressing 'Bookmarks' menu and 'Add Bookmark' (or <kbd>Ctrl</kbd> + <kbd>D</kbd>)

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

- Install extra packages for basic functionality to work

  ```bash
  sudo apt install libqt5svg5 ## for below
  sudo apt install xdg-desktop-portal xdg-desktop-portal-kde xdg-desktop-portal-gtk ## for pavian to work
  ```

  Restart!

- Install additional libraries (required for Tempest and MEGAX etc.)

  ```bash
  sudo apt install openjdk-11-jdk ## tempest
  sudo apt install libgconf-2-4 ## MEGAX
  sudo apt install libgsl-dev libeigen3-dev ## metadmg
  ```

- Bookmark textbook and summer school website to Firefox webbrowser

Install bioinformatics software

- Install miniforge (conda)

  ```bash
   mkdir ~/bin
   cd ~/bin
   wget https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Linux-x86_64.sh
  bash Miniforge3-Linux-x86_64.sh
  ```

  - Install into `/home/ubuntu/bin/miniforge3`
  - Run init(ialise): `yes`
  - To load conda into PATH:`source ~/.bashrc`
  - To turn off base: `conda config --set auto_activate_base false`
  - Restart terminal
  - Delete miniforge SH

    ```bash
    cd ~/bin
    rm Miniforge3-Linux-x86_64.sh
    ```

  - Set up channels

    ```bash
    conda config --add channels bioconda
    conda config --add channels conda-forge
    ```

- Clean up environment to preserve space (useful when running on a different site with less root disk space)

  ```bash
  sudo apt-get clean
  sudo apt-get autoclean
  sudo apt-get autoremove
  ```

- Create session conda environments

  - Download the environment ymls from https://github.com/SPAAM-community/intro-to-ancient-metagenomics-book/tree/main/assets/envs, and create each env

    ```bash
    wget https://github.com/SPAAM-community/intro-to-ancient-metagenomics-book/raw/main/assets/envs/{accessing-ancient-metagenomic-data,ancient-metagenomic-pipelines,authentication,bare-bones-bash,contamination,denovo-assembly,genome-mapping,git-github,phylogenomics,python-pandas,r-tidyverse,taxonomic-profiling}.yml

    for i in *.yml; do
        printf "\n###### PREPARING $i #######\n"
        conda env create -v -q -f "$i"
        conda clean all -y
    done
    ```

    > ⚠️ monitor to look for failures in log!
    > 2025:
    >
    > - denovo-assembly.yml -> tried adding binette but causes conflict with concoct, comment out concoct first, then inside environment after construction install with `conda install concoct`. However left as original for now

<!-- IN 2025 - Docker was already installed on the VM by default!
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
  -->

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
      conda activate phylogenomics ## Required to have a working java version
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

<!--
- [AUTHENTICATION ONLY] & and only **if old version of metaDMG required** (latest in 2025 - 0.4.1 - now in conda env, and apparently works!):

  ````
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
  ````

  -->

- Set up Volume

  NOTE: **this now may happen automatically on instance generation**, however instructions here in case you reboot and have to remount)

  - Cloud Portal > Virtual Machines > Instances > Volumes > Create and Attach Volume
    - Specify e.g. roughly total amount divided by number of nodes
    - Attach to the setup VM
  - Go back to VM and follow these [instructions](https://simplevm.denbi.de/wiki/simple_vm/volumes/)

    ```bash
    ## THIS WAS AUTOM
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

    e.g. to download from the [Zenodo archives](https://zenodo.org/communities/spaam-community/records?q=%22Introduction%20to%20Ancient%20Metagenomics%20Textbook%20%28Edition%202023%29%22&l=list&p=1&s=10&sort=bestmatch) from 2024

    ```bash

    mkdir <SESSION>/
    cd <SESSION>/
    ```

    And download

    ```bash
    cd /vol/volume/

    for i in 13759270/files/bare-bones-bash.tar.gz 13758879/files/r-tidyverse.tar.gz 11394586/files/python-pandas.tar.gz 13759333/files/git-github.tar.gz 13759163/files/accessing-ancient-metagenomic-data.tar.gz 13760277/files/taxonomic-profiling.tar.gz 13759321/files/genome-mapping.tar.gz 13759302/files/denovo-assembly.tar.gz 13759782/files/phylogenomics.tar.gz 13759285/files/contamination.tar.gz 13759228/files/authentication.tar.gz 13759228/files/authentication.tar.gz 13759201/files/ancient-metagenomic-pipelines.tar.gz; do
      archive=$(echo $i | rev | cut -f 1 -d '/' | rev)
      session=${archive%%.tar.gz}
      wget https://zenodo.org/records/$i
      tar xzvf $archive
      rm -r "$session".tar.gz "$session"/*.yml "$session"/README.md
    done
    ```

    > ⚠️ some cases (r-tidyverse, taxonomic-profiling), this may require a clone from elsewhere

- If running nf-core/eager in the pipelines session, run test profile to pull the container image once

  ```bash
  cd /vol/volume/ancient-metagenomic-pipelines/eager/
  conda activate ancient-metagenomic-pipelines
  nextflow run nf-core/eager -profile test,docker
  rm -r results/ work/ .nex*
  ```

  If you get a a 'GitHub API limit exceeded' error, you will need to follow the solution [here](https://github.com/nextflow-io/nextflow/discussions/2459#discussioncomment-13342927), and creating a temporary PAT token via your GitHub account [here](https://github.com/settings/tokens/new) (you just need a token, no extra permissions).

- Run a conda-clean up to save you some space

  ```bash
  conda clean --all
  ```

## Setting up test nodes to Instructors

Once installation and volume setup is finished we need to prepare the testing nodes for instructors.

- Go back to the SimpleVM portal
- Go to the SPAAMSumScho25 1workshop
- Go to instances
- Stop node (yellow button!)
- Make a snapshot (camera icon)
  - Call the snapshot something generic and in a way to allow iteration when changes are requested `SPAAMSumScho25-1`
- While the snapshot image is uploading, go to 'Instance Management'
- Volumes
- Find the existing volume generated for the node used for installing
- Press the 'edit' button (pencil icon), and rename to a generic name for iteration, e.g. `SPAAMSumScho25Beta1`
  - Note: volume names cannot contain any punctuation, only A-Z, a-z, 0-9 characters.
- Go back to instances, and monitor until image is uploaded
- Once uploaded, first make sure all tutors are added under 'Workshops > SPAAMSumSchoXX > Tutors > Show Hidable tutors, and add all missing
- Go to Workshops > Instances > Details ([i] icon) > Volumes tab > Select volume > Detach (yellow chain with line through icon)
- Go to 'Start Workshop Instances'
  - Select workshop
  - Select de.NBI medium + epehemeral
  - Image > Snapshots > SPAAMSumScho2025-1
  - Additional settings > Volumes > (!! Important!) **Available** volumes > SAAMSumSchoXXBetaX > mount path: `/vol/volume`
- Available participants/tutors > Add all tutors
- Start instances
- Once spun up - send information mails
<!-- TODO: pipelines conda env installation! -->

## Recreating exact environments

For future reference, we can re-create a 'complete' environment file with all specific versions of packages installed in the conda environments, by running the following command in each conda environment:

```bash
for i in accessing-ancient-metagenomic-data ancient-metagenomic-pipelines authentication bare-bones-bash contamination denovo-assembly genome-mapping git-github phylogenomics python-pandas r-tidyverse taxonomic-profiling; do
  conda env export -n $i -f "$i"_withversions.yml
done
```

We can also record the structure of all the `/vol/volume/` sessions, by running the following command:

```bash
for i in accessing-ancient-metagenomic-data ancient-metagenomic-pipelines authentication bare-bones-bash contamination denovo-assembly genome-mapping git-github phylogenomics python-pandas r-tidyverse taxonomic-profiling; do
  tree $i/ > "$i"_treestructure.txt
done
```

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

- Need to mount the volume (to be created)

  - Must contain all software, data
  - bashrc needs to be updated to point to miniforge install on volume

- Volume for data/software/saving
  - https://cloud.denbi.de/wiki/simple_vm/volumes/#create-the-volume-file-system-once
  - Make it once (create file system),
  - then each time spinning up node will need to make mount point and mount the node
- Use snapshot to include all the software etc?

<!--
Changes from 2024:
mi
- Remi: wanted polars (added, but won't be taught)
- Clemens: will maybe teach purrr (doesn't require any changes)
- Giulia:
  - wanted latest version on metaDMG which is now on bioconda
  -
- Alex:
  - optionally try with binnette to replace metawrap (didn't work because gunc has overly strict pinning )
  - latest visidata (via pip)
  - Add markdown file with commands
  - Redownload k8s calN50.js file
- Tessa: pin to ancient IGV (2.4) and GATK to v8
- Keri
  - New taxdb file
  - New analyslys.pynbnb file
  - Check pavian in firefox file upload works
- Nikolay
  - Added the plotPMD.v2.R script directly to /vol/volume as bioconda version is broken
-->
