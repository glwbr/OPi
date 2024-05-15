<a name="readme-top"></a>

<!--
*** Markdown "reference style" para facilitar a leitura.
*** Reference links use brackets [ ]  instead of parenthesis ( ).
*** Check the bottom of this document to see the references
https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- LOGO -->
<br />
<div align="center">
  <a href="/">
    <img src="https://res.cloudinary.com/djb3ju61n/image/upload/v1715744838/opi_orangepi_infrastructure_logo.webp" alt="Logo" width="200" height="200">
  </a>

  <h2 align="center">OPi | Orange Pi Infrastructure</h2>

  <p align="center">
    Let's bora!
    <br />
    <a href="https://www.readthefuckingmanual.com/"><strong>Read The Fluffy Docs »</strong></a>
    <br />
    <a href="https://github.com/glwbr/OPi/issues">Report Bug</a>
    ·
    <a href="https://github.com/glwbr/OPi/issues">Request Feature</a><br />
    English | <a href="../pt-br/README.md">Português</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details open>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#why">Why?</a></li>
        <li><a href="#made-with">Made With</a></li>
      </ul>
    </li>
   <li>
     <a href="#requirements">Requirements</a>
     <ul>
       <li><a href="#essential">Essential</a></li>
       <li><a href="#optional">Optional</a></li>
       <li><a href="#container-runtime">Container Runtime</a></li>
         <ul>
           <li><a href="#docker">Docker</a></li>
           <li><a href="#podman">Podman</a></li>
         </ul>
       <li><a href="#kubernetes">Kubernetes</a></li>
         <ul>
           <li><a href="#choosing-a-kubernetes-distribution">Choosing a Kubernetes Distribution</a></li>
        </ul>
     </ul>
   </li>
    <li><a href="#useful-content">Useful Content</a></li>
    <li><a href="#how-to-use">How to Use</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
  </ol>
</details>
<!-- END TABLE OF CONTENTS -->

<!-- ABOUT -->
## About The Project

This repository offers detailed instructions for deploying multiple services on an Orange Pi. The primary goal is to establish a fully functional, low-consumption infrastructure thats the the size of a credit card.

### Why
Unlike the Raspberry Pi, the Orange Pi community is still growing. You might not find as much content about it online, but this piece of hardware is incredible and a fantastic board to work with. It's more affordable, and personally, I'm not even including the I/O capabilities.

This repo serves as a proof of concept for running an on-premise server with an Orange Pi 3B. I am sharing my ongoing process for setting up an infrastructure using container runtimes such as `Docker`, `containerd`, `CRI-O`, and `Podman`, along with `Kubernetes` and possibly [NixOS][nix-arm-url], `Ansible`, and `Proxmox`. I also plan to include instructions for automated builds, deployment, testing, logging, and ephemeral environments, check the <a href="#roadmap">Roadmap</a> :). Any tips or references for improvements, security, and hardening are always welcome.

> By now it should only work for myself.

### Made With

[![Docker][docker-badge]][Docker-url] [![Kubernetes][kubernetes-badge]][Kubernetes-url] [![Nix][nix-badge]][nix-url]  [![nginx][nginx-badge]][nginx-url] [![OrangePi][orangepi-badge]][orangepi-url] [![Podman][podman-badge]][podman-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- END ABOUT -->

<!-- FIRST STEPS -->
## First Steps

Prepare your system by installing the necessary tools and configuring access permissions.

### Requirements

This section lists the crucial requirements needed to set up the system. You will need an Orange Pi equipped with a compatible operating system, such as OPiOS or Armbian. A solid grasp of terminal commands and basic Kubernetes concepts is necessary for proper setup and operation. For storage, an SSD is recommended for its speed and reliability, though an SD card could suffice, albeit with potentially slower performance. For added flexibility, consider including a power bank to power your Orange Pi without the need for a continuous connection to a wall outlet. An Ethernet switch could also be beneficial if you plan to connect multiple devices, facilitating a more robust network setup.

#### Essential
- An Orange Pi with a compatible operating system installed (e.g., OPiOS, Armbian). You can find reference, links and where to Buy in the official [OrangePi][orangepi-url] website.
- Internet connectivity on the Orange Pi.
- Understanding of terminal commands and Kubernetes concepts [Kubernetes][kubernetes-doc-url].
- SSD for storage; it is possible to use an SD card, but this may be too slow for optimal performance.

> PS: For the OPi3B, the manufacturer recommends SSDs with `2230` or `2242` [form factors](https://www.corsair.com/us/en/explorer/diy-builder/storage/ssd-form-factors-explained/).

#### Optional
- A power bank to enable operation detached from a wall power source.
- An Ethernet switch for connecting multiple devices.

#### Container Runtime
This subsection will provide detailed instructions for installing your chosen container runtime, ensuring you have the necessary tools and processes in place for a smooth deployment.
!TODO: list instructions
#### Docker
#### Podman

### Kubernetes
#### Choosing a Kubernetes Distribution
!TODO: explain
#### Kubernetes Installation
!TODO: describe
<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- END FIRST STEPS -->

<!-- USEFUL -->
## Useful Content
<ol>
  <li>
    <a href="Security.md">Security</a>    
  </li>
</ol>
<!-- END USEFUL -->

<!-- HOW TO USE -->
## How to Use

Detailed steps on how to use the infrastructure for hosting applications.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- END HOW TO USE -->

<!-- ROADMAP -->
## Roadmap

- :white_check_mark: Add Readme
- :x: Add Changelog
- :x: Nix
  - :x: How to build nixos kernel distribution for :arrow_right: [RK3566][firefly-kernel-url]
- :x: Logging, ELK, Prometheus, what's that ?
- :x: Proxmox, Ansible, Terraform
- :x: Add instruction for Podman
  - :x: Networking
  - :x: Persistence
- :x: Expand Kubernetes configurations

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- END ROADMAP -->

<!-- CONTRIBUTING -->
## Contributing

!TODO
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- END CONTRIBUTING -->

<!-- IMAGES -->
[opi_infra_logo]: https://res.cloudinary.com/djb3ju61n/image/upload/v1715744838/opi_orangepi_infrastructure_logo.webp
<!-- END IMAGES -->

<!-- REFERENCE STYLE LINKS -->
[docker-badge]: https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white
[docker-url]: https://docker.com
[firefly-kernel-url]: https://wiki.t-firefly.com/en/ROC-RK3566-PC/kernel_introduction.html
[kubernetes-badge]: https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white
[kubernetes-url]: https://kubernetes.io/
[kubernetes-doc-url]: https://kubernetes.io/docs/home/
[nix-badge]: https://img.shields.io/badge/nix-5277C3?style=for-the-badge&logo=nixos&logoColor=white
[nix-url]: https://nixos.wiki/wiki
[nix-arm-url]: https://nixos.wiki/wiki/Nix_on_ARM
[nginx-badge]: https://img.shields.io/badge/nginx-009639?style=for-the-badge&logo=nginx&logoColor=white
[nginx-url]: https://nginx.org/en/docs/
[orangepi-badge]: https://img.shields.io/badge/OrangePi-FAF9F6?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAA81BMVEVHcEzroSvroCzrpDfspDProizspDTrozLVoi7TpDLroSvroi3roSvroi3roSvroSvroSviozDroSvroS3roSvroSvsoSvroi3spDPtrVXrojHtojB1rj3ur1zsozLurld3rj3roSt3rjzroSt3rj15rjzur1zroSvroSvroizroSvroSvroSt8rTzpoSt3rj3roSt3rj3soSvusWLusF/usGLsoSt3rj2BrTt3rj3roSvur17roSvqoSvroi53rj13rj3RpC93rj12rj13rj3sozHur13usGHspTh3rj2sqDXusWPtrVr/7QB3ACTroSt3rj0nqX9WAAAATnRSTlMA0SEOGBIJBgEDmB7lJvL97TNvfU7A3iQ5dWZDI5QthA6eCPj6UVKQWCm2hGBgyMPb2KS9sbOs7K/9tKp3sSKJmV6qepGJfMuGcWSin7CZY3i7AAACE0lEQVQ4y31Th3LbMAylFrW3ZW3Je+8Z24mTOrNN76j//5qSireT4k5HkHgEH4AnAH4wsVIqVS6PBPEQi+rPT7vh3e/oElB67OdXopfhMsuycb90nfRp9YIR9eF4ucpWu+j22WhYq4NoN65lWe2x9B2x6Lkf/rpb1mrjfuWbMAcBW65WB3/qdVO4DcNg4EwohK04WVBd9gYQajhWXdv2ukpQ1g2gi4yOZEGcqidNFNSBF1FetQwqhMKW9IrmRdOpNpNziKUgI8SrzOEMW+yY+EA6IdQiQh0GOwwNAEv4iRImVDgC2gpyPBcjRFcENOGxTSRdbx0BDKWYALqsAM2G73GAUxnAOVpyekKRSFpZ9qfx+yaWaZ7wOj3BldF97jTSWRrP4kY+9xYaqHtAgJDEY4Of728fr/50yuKNeI9Qed9xGyGnvd1uVT/2qZH/N03whsZ1POwlVDBQM+c6nwf2h7+Z5oNo6bp9UIqld/PV8+dpOotDPr+ml5kDS3a0wMlwnW+fm3kasyqJdDXvpARKK+TFw6TRwDOArgy8omYeAaaBRj1SvOjieZCOsgUsjd4RwA4QoggzTv76gDhBSPHO1LJWkC183eZd7ISG5gTiuSA8SrNVrk18WqaDotGCV4qycE5q4UFefqWK+rGJJ0tGRIqG08lXrXWjScFs2j2JKPchsKQC/8MvHVCjJgP+YyIrX5H7B9QkP7pEI+5XAAAAAElFTkSuQmCC
[orangepi-url]: http://www.orangepi.org/
[podman-badge]: https://img.shields.io/badge/podman-892CA0?style=for-the-badge&logo=podman&logoColor=white
[podman-url]: https://podman.io/
<!-- END REFERENCE STYLE LINKS -->
