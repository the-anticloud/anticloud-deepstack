# DEEPSTACK

![license](https://img.shields.io/badge/license-license-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![category](https://img.shields.io/badge/category-surveillance_camera-lightgrey)

> Anticloud-hardened packaging of the upstream project `DEEPSTACK` in category **SURVEILLANCE CAMERA**. Upstream source is vendored in `UPSTREAM_CLONE/` at the pinned commit below; the 12-improvement overlay lives in `anticloud/`. Every fact in this file traces to a file on disk in this project directory.

**Category:** SURVEILLANCE CAMERA · **Upstream:** https://github.com/johnolafenwa/DeepStack · **Upstream pin:** `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042` · **Vendor:** Anticloud FZ LLE

---

## What This Project Does

# DeepStack
The World's Leading Cross Platform AI Engine for Edge Devices, with over `10 million` installs on [**Docker Hub**](https://hub.docker.com/r/deepquestai/deepstack).

[![black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

[![license](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](hhttps://github.com/johnolafenwa/DeepStack/blob/dev/LICENSE)

![DevTest](https://github.com/johnolafenwa/DeepStack/workflows/DevTest/badge.svg)

**Website**: [https://deepstack.cc](https://deepstack.cc)

**Documentation**: [https://docs.deepstack.cc](https://docs.deepstack.cc)

**Forum**: [https://forum.deepstack.cc](https://forum.deepstack.cc)

**Dev Center**: [https://dev.deepstack.cc](https://dev.deepstack.cc/)

**DeepStack** is owned and maintained by [DeepQuest AI](https://www.deepquestai.com/).

# Introduction
DeepStack is an AI API engine that serves pre-built models and custom models on multiple edge devices locally or on your private cloud. Supported platforms are:

- **Linux OS** via Docker ( CPU and NVIDIA GPU support )
- **Mac OS** via Docker
- **Windows 10** ( native application, CPU and GPU )
- **NVIDIA Jetson** via Docker.
- **Rasperry Pi & ARM64 Devices** via Docker.

DeepStack runs completely offline and independent of the cloud. You can also install and run DeepStack on any cloud VM with docker installed to serve as your private, state-of-the-art and real-time AI server.

# Features

- **Face APIs**: Face detection, recognition and matching.

    ![Face API](demo/face_api.jpg)

- **Common Objects APIs**: Object detection for [80 common objects](https://docs.deepstack.cc/object-detection/index.html#classes)

    ![Detection API](demo/detection_api.jpg)

- **Custom Models**: Train and deploy new models to detect any custom object(s)

    ![Custom Models API](demo/custom_model.jpg)

- **Image Enhance**: 4X image superresolution

    `Input`

    ![Image Enhance API Iput](demo/enhance_input.jpg)

     `Output`
    ![Image Enhance API Iput](demo/enhance_output.jpg)

- **Scene Recognition**: Image scene recognition
- **SSL Support**
- **API Key support**: Security options to protect your DeepStack endpoints

# Installation and Usage
Visit [https://docs.deepstack.cc/getting-started](https://docs.deepstack.cc/getting-started/) for installation instructions. The documentation provides example codes for the following programming languages with more to be added soon.

- **Python**
- **C#**
- **NodeJS**

# Build from Source (For Docker Version)

- **Install Prerequisites**

    - [Install Golang](https://golang.org)
    - [Install Docker](https://docker.com)
    - [Install GIT](https://git-scm.com)
    - [Install GIT LFS](https://github.com/git-lfs/git-lfs/wiki/Installation)
    - [Install Redis Server](https://redis.io/)
    - [Install Python3.7](https://python.org)
    - [Install Powershell 7+](https://docs.microsoft.com/en-us/powershell/scripting/windows-powershell/install/installing-windows-powershell?view=powershell-7.1)

- **source DeepStack project** 

    ```git source https://github.com/johnolafenwa/DeepStack.git```

- **CD to DeepStack project Dir**

    ```cd DeepStack```

- **Fetch project Files**

    ``git lfs pull``
- **Download Binary Dependencies With Powershell**
    ```.\download_dependencies.ps1```

- **Build DeepStack CPU Version**

    ```cd .. && sudo docker build -t deepquestai/deepstack:cpu . -f Dockerfile.cpu```

- **Build DeepStack GPU Version**

    ```sudo docker build -t deepquestai/deepstack:gpu . -f Dockerfile.gpu```

- **Build DeepStack Jetson Version**

    ```sudo docker build -t deepquestai/deepstack:jetpack . -f Dockerfile.gpu-jetpack```

- **Running and Testing Locally Without Building**
    - Unless you wish to install requirements system wide, create a virtual environment with ```python3.7 -m venv venv``` and activate with ```source venv/bin/activate```

    - Install Requirements with ```pip3 install -r requirements.txt```

    - For CPU Version, Install PyTorch with ```pip3 install torch==1.6.0+cpu torchvision==0.7.0+cpu -f https://download.pytorch.org/whl/torch_stable.html```

    - For GPU Version, Install Pytorch with ```pip3 install torch==1.6.0+cu101 torchvision==0.7.0+cu101 -f https://download.pytorch.org/whl/torch_stable.html```

    - Start Powershell
        ```pwsh```

    - For CPU Version, Run ```.\setup_docker_cpu.ps1```

    - For GPU Version, Run ```.\setup_docker_gpu.ps1```

    - CD To Server Dir
        ```cd server```

    - Build DeepStack Server
        ```go build```

    - Set Any of the APIS to enable;
        ```$env:VISION_DETECTION = "True"```, ```$env:VISION_FACE = "True"```, ```$env:VISION_SCENE = "True"```

    - Run DeepStack
        ```.\server```

    You can find all logs in the ```directory``` in the project root.
    Note that DeepStack will be running on the default port ```5000```.

# Integrations and Community
The DeepStack ecosystem includes a number of popular integrations and libraries built to expand the functionalities of the AI engine to serve IoT, industrial, monitoring and research applications. A number of them are listed below

- **[HASS-DeepStack-Object](https://github.com/robmarkcole/HASS-Deepstack-object)**: An [Home Assistant](https://www.home-assistant.io/) addon by [Robin Cole](https://github.com/robmarkcole) for detecting common and custom objects
- **[HASS-DeepStack-Face](https://github.com/robmarkcole/HASS-Deepstack-face)**: An [Home Assistant](https://www.home-assistant.io/) addon by [Robin Cole](https://github.com/robmarkcole) for face detection, registration and recognition
- **[HASS-DeepStack-Scene](https://github.com/robmarkcole/HASS-Deepstack-scene)**: An [Home Assistant](https://www.home-assistant.io/) addon by [Robin Cole](https://github.com/robmarkcole) for scene recognition
- **[DeepStack with Blue Iris - YouTube video](https://www.youtube.com/watch?v=fwoonl5JKgo)**: A DeepStack + BluIris setup tutorial by [TheHookUp](https://www.youtube.com

*(excerpt; full text in `UPSTREAM_CLONE/`)*

*Quoted from the upstream `README.md` file in `UPSTREAM_CLONE/`.*
Project-specific facts detected in this directory:

- Ecosystem: **Python (requirements)** (manifests: requirements.txt; scanned in UPSTREAM_CLONE)
- Top-level source layout: `base/`, `demo/`, `intelligencelayer/`, `platform/`, `results/`, `rpi/`, `server/`, `tests/`
- Snapshot size: **294 files**, **6622 lines of code** (measured; see Benchmarks)
- Primary languages: `.png` (117), `.jpg` (51), `.py` (43), `.scss` (12), `.css` (10), `.go` (7)
- Upstream commit pinned for this packaging: `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`

---

## Installation

[![black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

[![license](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](hhttps://github.com/johnolafenwa/DeepStack/blob/dev/LICENSE)

![DevTest](https://github.com/johnolafenwa/DeepStack/workflows/DevTest/badge.svg)

**Website**: [https://deepstack.cc](https://deepstack.cc)

**Documentation**: [https://docs.deepstack.cc](https://docs.deepstack.cc)

**Forum**: [https://forum.deepstack.cc](https://forum.deepstack.cc)

**Dev Center**: [https://dev.deepstack.cc](https://dev.deepstack.cc/)

**DeepStack** is owned and maintained by [DeepQuest AI](https://www.deepquestai.com/).

*Section quoted from the upstream readme.*
Overlay install (this project):

```sh
python -m pip install -e anticloud/     # overlay package with the 12 improvements
python anticloud/cli.py --help          # 13 subcommands, JSON stdout
```

---

## Usage

Visit [https://docs.deepstack.cc/getting-started](https://docs.deepstack.cc/getting-started/) for installation instructions. The documentation provides example codes for the following programming languages with more to be added soon.

- **Python**
- **C#**
- **NodeJS**

*Section quoted from the upstream readme.*
Anticloud overlay CLI (available in every project):

```sh
python anticloud/cli.py --help     # 13 subcommands, JSON stdout
python anticloud/cli.py checks     # run the 16-check suite
```

---

## API

**Forum**: [https://forum.deepstack.cc](https://forum.deepstack.cc)

**Dev Center**: [https://dev.deepstack.cc](https://dev.deepstack.cc/)

**DeepStack** is owned and maintained by [DeepQuest AI](https://www.deepquestai.com/).

*Section quoted from the upstream readme.*
---

## Dependencies

| Metric | Value |
|--------|-------|
| Ecosystem | Python (requirements) |
| Manifests detected | requirements.txt |
| Files in snapshot | 294 |
| Lines of code | 6622 |
| Dependency references | 14 |
| Dependencies by ecosystem | go: 14 |
| Upstream license | Apache-2.0 |
| Overlay license | Anticommons 0.1.0 |

Top dependency references recorded in the benchmark snapshot:

| Ecosystem | Name | Version | Source file |
|-----------|------|---------|-------------|
| go | github.com/gin-gonic/gin | v1.7.0 | server/go.mod |
| go | github.com/go-ole/go-ole | v1.2.4 | server/go.mod |
| go | github.com/go-redis/redis | v6.15.2+incompatible | server/go.mod |
| go | github.com/imroc/req | v0.2.4 | server/go.mod |
| go | github.com/mattn/go-sqlite3 | v1.11.0 | server/go.mod |
| go | github.com/modern-go/concurrent | v0.0.0-20180306012644-bacd9c7ef1dd | server/go.mod |
| go | github.com/modern-go/reflect2 | v1.0.1 | server/go.mod |
| go | github.com/onsi/ginkgo | v1.12.0 | server/go.mod |
| go | github.com/onsi/gomega | v1.9.0 | server/go.mod |
| go | github.com/satori/go.uuid | v1.2.0 | server/go.mod |
| go | github.com/shirou/gopsutil | v2.18.12+incompatible | server/go.mod |
| go | github.com/shirou/w32 | v0.0.0-20160930032740-bb4de0191aa4 | server/go.mod |
| go | golang.org/x/crypto | v0.0.0-20200622213623-75b288015ac9 | server/go.mod |
| go | golang.org/x/net | v0.0.0-20190503192946-f4e77d36d62c | server/go.mod |

Pinned lockfile: `anticloud/requirements.lock` (hash-pinned, PEP 508). SBOM: `sbom.cdx.json` (CycloneDX 1.5, pinned to the upstream SHA).

---

## Configuration

No configuration section was found in the upstream readme. Configuration-relevant files detected in this project directory:

- None detected at the snapshot root; consult the upstream documentation link in the Upstream section.

Overlay configuration (Anticloud):

- `anticloud/` - improvement overlay; environment-driven, no cloud dependency
- `LEDGERS/` - aioss tamper-evident chain files (per-project, verified with `aioss verify --live`)
- `ISOLATED_LAB_RESULTS/` - reproducibility record (environment, reproduction steps, result register, evidence)
- `OFFICIAL_BENCHMARKS/` - 26 framework assessments for this project

---

## Contributing

Upstream contributions: fork the `DEEPSTACK` project, create a feature branch, and open a pull request against upstream. Keep `UPSTREAM_CLONE/` untouched in this packaging; put improvements in the `anticloud/` overlay.

Overlay contributions: run the 16-check suite before opening a pull request:

```sh
python anticloud/bench/runner.py --cwd anticloud
```

---

## License

**Upstream license: Apache-2.0** (evidence: `LICENSE` in the upstream snapshot).

License file excerpt:

```text
                                 Apache License
                           Version 2.0, January 2004
                        http://www.apache.org/licenses/

   TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION

   1. Definitions.

      "License" shall mean the terms and conditions for use, reproduction,
      and distribution as defined by Sections 1 through 9 of this document.

      "Licensor" shall mean the copyright owner or entity authorized by
      the copyright owner that is granting the License.

      "Legal Entity" shall mean the union of the acting entity and all
      other entities that control, are controlled by, or are under common
      control with that entity. For the purposes of this definition,
      "control" means (i) the power, direct or indirect, to cause the
      direction or management of such entity, whether by contract or
      otherwise, or (ii) ownership of fifty percent (50%) or more of the
```

### Anticommons 0.1.0 overlay

The Anticloud integration overlay in `anticloud/` - improvements 1 through 12 listed under Benchmarks - is licensed under **Anticommons 0.1.0**. Upstream code remains under its original Apache-2.0 terms. See `ANTICOMMONS_LICENSE.md` in this directory for the overlay terms and contact.

SPDX: `Apache-2.0` (upstream) + Anticommons 0.1.0 (overlay, dual).

---

## Upstream

- **Project:** `DEEPSTACK` (category: SURVEILLANCE CAMERA)
- **Upstream URL:** https://github.com/johnolafenwa/DeepStack
- **Pinned commit (SHA):** `73b6f7ab0f9a8acc8f7a49c6f13594fe470de042`
- **Branch:** dev
- **Pin provenance:** GitHub API commits/dev. The parent-project stamp is explicitly rejected for this project.
- **Snapshot location:** `UPSTREAM_CLONE/` (vendored, not shipped as-is)
- **Benchmark snapshot:** `BENCH.json`

---

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`2b0fb7a1f7318b9dceb28ca66c333795ab0ea199fa00d40e51ec5329f8be9bfd`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

