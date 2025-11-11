# DITA Topic Model - Enter Title Here

This repo contains a DITA topic model (TM) related to ...

## Authors

Madison Greenstein
Alyssa Johnson
Stephen Synk

## Project Maps

### User Scenario 1: ...

<!-- NOVICE USER -->

Alyssa and Kaiya are college roommates in their early 20s. They need to set up a Wi-Fi router to get internet access for their school and work devices, but neither of them have ever installed one before and they don't have a lot of experience with installing hardware or with the terminology used to describe Wi-Fi routers. They just purchased a Synology WRX560 router and want quick, simple instructions.

Map Outline:
- c_what_is_router.dita (File title)
- c_router_description.dita (File title)
- r_router_hardware
- t_installing_router_hardware.dita (File title)
- t_installing_router_software
- r_glossary
<!-- map outline:
  - c - what does a router do
  - c - description of model
  - r - router hardware
  - t - installing hardware
  - t - installing software
  - r - glossary




 -->

### User Scenario 2: ...

<!-- EXPERIENCED USER, *NON-EXPERT* -->

Brittany is a wife and mother in her mid-30s who needs to replace her old Synology WRX560 Wi-Fi router with a new one due to some connectivity issues and slow service. She's familiar with the installation process, but is unsure how to safely and correctly uninstall her router and replace it with the new one. Her goal is to get through the replacement process as quickly and smoothly as possible so she can restore her family's Wi-Fi connection ASAP.

<!-- UPDATE FILE NAMES WHEN THEY ARE READY -->
Map Outline:
- c_router_description.dita (File title)
- t_replacing_router.dita (File title)
- r_router_hardware.dita (File title)

<!-- map outline:

  - c - description of the model
  - t - replacing
  - r - router hardware
 -->

### User Scenario 3: ...

<!-- EXPERIENCED USERS: Troubleshooting. Map should include reference and concept tasks -->

Pam and Gray are an elderly married, retired couple in their 70s who are having connectivity/speed issues with their Synology WRX560 Wi-Fi router. Although they're very familiar with the Synology WRX560 Wi-Fi router, including the installation and set-up process, they have no experience with troubleshooting and are unsure where to even start. They want to resolve the issue efficiently, but they don't have a major time constraint since they are retired. Their priority is to learn this information and be able to refer to it for future cases. They're also looking for a guide that is easily understandable to a non-technical audience and includes definitions for any technical terms.

Map Outline:
<!-- UPDATE FILE NAMES WHEN THEY ARE READY -->
- r_router_hardware.dita (File title)
- t_troubleshoot_hardware.dita (File title)
- t_troubleshoot_software.dita (File title)
- r_glossary

<!-- Map Outline -- will update names when files are finished

  - r - hardware parts
  - t - troubleshooting hardware
  - t - troubleshooting software
  - r - glossary
  - 
 -->

## Folders &amp; Files

- `assets`: Contains all assets used within the TM.
- `concepts`: Contains all concept topics.
- `references`: Contains all reference topics.
- `tasks`: Contains all task topics.
- `shared`: Contains all topic files that are shared across multiple maps.
- `out`: Contains all output folders.
- `themes`: Contains `.yaml` style configuration files.
- **Skeleton files**: All topic folders contain a single "skeleton" topic file for you to copy, whenever you need to quickly create a new file.
- `.keep` **files**: Ignore these files. They ensure that any empty folders are tracked by git. 
- `.gitignore`: This file tells git which files to ignore in the repo. You can leave this one be.

## Filenaming Conventions

- Task Topics: `t_verb_verbobject.dita`
- Concept Topics: `c_nounphrase.dita`
- Reference Topics: It varies, but something akin to `r_types_of_nounphrase.dita`
- Dita Maps: `_modelname.ditamap`

## Building Outputs Manually with the Command Line

See the DITA-OT user guide about how to generate output: [https://www.dita-ot.org/dev/topics/build-using-dita-command](https://www.dita-ot.org/dev/topics/build-using-dita-command)

### Sample DITA Commands

#### Help

To see all of the commands and parameters, use the following command:

```
dita --help
```

#### DITA options and arguments

```
-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file
```

#### Create an HTML5 site

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```

#### Create an HTML5 site with a custom CSS file

```
dita -f html5 -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
  -Dargs.cssroot='url/to/your/assets/folder' \
  -Dargs.css='${cssroot}/your-custom-css-file.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
```

#### Create a PDF

```
dita -f pdf -i 'url/to/your/wanted.ditamap' \
  -o 'url/to/your/output/folder' \
```
