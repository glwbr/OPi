<a name="readme-top"></a>

<!--
*** Estilo de referência em Markdown para facilitar a leitura.
*** Links de referência usam colchetes [ ] em vez de parênteses ( ).
*** Verifique o final deste documento para ver as referências.
https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- CABEÇALHO -->
<br />
<div align="center">
  <a href="/">
    <img src="https://res.cloudinary.com/djb3ju61n/image/upload/v1715744838/opi_orangepi_infrastructure_logo.webp" alt="Logo" width="200" height="200">
  </a>

  <h2 align="center">OPi | Orange Pi Infrastructure</h2>

  <p align="center">
    Let's bora!
    <br />
    <a href="https://www.readthefuckingmanual.com/"><strong>Leia a Fofa Documentação »</strong></a>
    <br />
    <a href="https://github.com/glwbr/OPi/issues">Reportar um Bug</a>
    ·
    <a href="https://github.com/glwbr/OPi/issues">Solicitar um Recurso</a><br />
    <a href="https://github.com/glwbr/OPi/blob/main/docs/en-us/README.md">English</a> | Português
  </p>
</div>
<!-- FIM DO CABEÇALHO -->

<!-- ÍNDICE -->
<details open>
  <summary>Índice</summary>
  <ol>
    <li>
      <a href="#sobre-o-projeto">Sobre o Projeto</a>
      <ul>
        <li><a href="#por-que">Por que?</a></li>
        <li><a href="#feito-com">Feito Com</a></li>
      </ul>
    </li>
   <li>
     <a href="#requisitos">Requisitos</a>
     <ul>
       <li><a href="#essenciais">Essenciais</a></li>
       <li><a href="#opcionais">Opcionais</a></li>
       <li><a href="#containers-runtime">Containers Runtime</a></li>
         <ul>
           <li><a href="#docker">Docker</a></li>
           <li><a href="#podman">Podman</a></li>
         </ul>
       <li><a href="#kubernetes">Kubernetes</a></li>
         <ul>
           <li><a href="#escolhendo-uma-distribuição-do-kubernetes">Escolhendo uma Distribuição do Kubernetes</a></li>
        </ul>
     </ul>
   </li>
    <li><a href="#utilidades">Utilidades</a></li>
    <li><a href="#como-usar">Como Usar</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contribuindo">Contribuindo</a></li>
  </ol>
</details>
<!-- FIM DO ÍNDICE -->

<!-- SOBRE -->
## Sobre o Projeto
Este repositório tem como objetivo oferecer instruções detalhadas para implantar vários serviços em uma Orange Pi. O objetivo principal é estabelecer uma infraestrutura totalmente funcional e de baixo consumo que tenha o tamanho de um cartão de crédito. 🧐

### Por que?
Diferentemente do Raspberry Pi, a comunidade Orange Pi ainda está crescendo. Você pode não encontrar tanto conteúdo sobre isso online, mas esse hardware é incrível e uma placa fantástica para se trabalhar. É mais acessível e, pessoalmente, nem mesmo estou considerando as capacidades de I/O dessa plaquinha nesta comparação.

Este repositório serve como prova de conceito para executar um servidor local com um Orange Pi 3B. Estou compartilhando meu processo em andamento para configurar uma infraestrutura usando runtimes de contêineres como `Docker`, `containerd`, `CRI-O` e `Podman`, junto com `Kubernetes` e possivelmente [NixOS][nix-arm-url], `Ansible` e `Proxmox`. Também pretendo incluir instruções para compilações automatizadas, implantação, testes, logs e ambientes efêmeros. Dê uma olhada no <a href="#roadmap">Roadmap</a> :). Qualquer dica ou referência para melhorias, principalmente de segurança são sempre bem-vindas.

> Por enquanto, deve funcionar apenas para mim.

### Feito Com
[![Docker][docker-badge]][Docker-url] [![Kubernetes][kubernetes-badge]][Kubernetes-url] [![Nix][nix-badge]][nix-url]  [![nginx][nginx-badge]][nginx-url] [![OrangePi][orangepi-badge]][orangepi-url] [![Podman][podman-badge]][podman-url]

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>
<!-- FIM SOBRE -->

<!-- PRIMEIROS PASSOS -->
## Primeiros Passos
Prepare seu sistema instalando as ferramentas necessárias e configurando permissões de acesso.

### Requisitos
Esta seção lista os requisitos cruciais necessários para configurar o sistema. Você precisará de um Orange Pi equipado com um sistema operacional compatível, como OPiOS ou Armbian. Um sólido entendimento de comandos de terminal e conceitos básicos de Kubernetes é necessário para a configuração e operação adequadas. Para armazenamento, recomenda-se um SSD pela sua velocidade e confiabilidade, embora um cartão SD possa ser suficiente, embora com desempenho potencialmente mais lento. Para maior flexibilidade, considere incluir um banco de energia para alimentar seu Orange Pi sem a necessidade de uma conexão contínua a uma tomada. Um switch Ethernet também pode ser benéfico se você planeja conectar vários dispositivos, facilitando uma configuração de rede mais robusta.

#### Essencial
- Um Orange Pi com um sistema operacional compatível instalado (por exemplo, OPiOS, Armbian). Você pode encontrar referências, links e onde comprar no site oficial [OrangePi][orangepi-url].
- Conectividade à internet no Orange Pi.
- Entendimento de comandos de terminal e conceitos de Kubernetes [Kubernetes][kubernetes-doc-url].
- SSD para armazenamento; é possível usar um cartão SD, mas isso pode ser muito lento para um desempenho ideal.

> PS: Para o OPi3B, o fabricante recomenda SSDs com fatores de forma `2230` ou `2242` [form factors](https://www.corsair.com/us/en/explorer/diy-builder/storage/ssd-form-factors-explained/).

#### Opcional
- Uma bateria portátil (*power bank*) para permitir o funcionamento mesmo sem uma fonte de energia.
- Um switch Ethernet para conectar vários dispositivos.

#### Containers Runtime
Esta subseção fornecerá instruções detalhadas para instalar uma runtime, garantindo que você tenha as ferramentas necessárias.
!TODO: listar instruções
#### Docker
#### Podman

### Kubernetes
#### Escolhendo uma Distribuição Kubernetes
!TODO: explicar
#### Instalação do Kubernetes
!TODO: descrever
<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>
<!-- FIM PRIMEIROS PASSOS -->

<!-- CONTEÚDO ÚTIL -->
## Utilidades
<ol>
  <li>
    <a href="SECURITY.md">Segurança</a>
  </li>
</ol>
<!-- FIM ÚTIL -->

<!-- COMO USAR -->
## Como Usar
Passos detalhados sobre como usar a infraestrutura para hospedar aplicações.

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>
<!-- FIM COMO USAR -->

<!-- ROADMAP -->
## Roadmap

- :white_check_mark: Adicionar README
- :x: Adicionar Changelog
- :x: Nix
  - :x: Como construir distribuição do kernel nixos para :arrow_right: [RK3566][firefly-kernel-url]
- :x: Logging, ELK, Prometheus, o que é isso?
- :x: Proxmox, Ansible, Terraform
- :x: Adicionar instrução para Podman
  - :x: Rede
  - :x: Persistência
- :x: Expandir configurações Kubernetes

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>
<!-- FIM ROADMAP -->

<!-- CONTRIBUIR -->
## Contribuir

!TODO
<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>
<!-- FIM CONTRIBUIR -->

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
<!-- FIM REFERENCE STYLE LINKS -->
