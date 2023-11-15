<!--lint disable awesome-contributing awesome-git-repo-age awesome-toc awesome-list-item-->
# Awesome Swarm [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<img src="images/awesome-swarm.png" align="right" width="250" />

> An awesome list of tools and info on Swarm Mode (SwarmKit)

Swarm (Swarm Mode, SwarmKit) is the simple orchestration and scheduling system built into Moby, Docker Engine, and Mirantis Container Engine (MCE). It is a distributed system that allows you to create and manage a cluster of container runtimes (nodes) and the container workloads running on them.

This Awesome List is maintained by [@BretFisher](https://github.com/BretFisher) and [@s4ke](https://github.com/s4ke). This is a curated list of *working* and *awesome* tools and resources for using Swarm. It is not an official list, but a community effort to help people find the best stuff for Swarm in 2023 and beyond.

## Contents<!-- omit from toc -->

- [Recent News and Updates](#recent-news-and-updates)
- [Official Main Resources](#official-main-resources)
- [Chat and Forums](#chat-and-forums)
- [Community Tools](#community-tools)
  - [Cluster Management](#cluster-management)
  - [Extra Functionality](#extra-functionality)
  - [Volumes and Storage](#volumes-and-storage)
  - [Networking](#networking)
  - [Monitoring](#monitoring)
- [Community Tutorials and Education](#community-tutorials-and-education)
  - [Courses and Videos](#courses-and-videos)
  - [Articles and Sample Code](#articles-and-sample-code)
- [Organisations Using Swarm](#organisations-using-swarm)
- [RIP](#rip)
- [Contributing](#contributing)
- [Maintainers](#maintainers)

## Recent News and Updates

- [Mirantis - What's next for Swarm](https://www.mirantis.com/blog/what-s-next-for-swarm/)
- [Mirantis - Kubernetes vs Swarm - These companies use both](https://www.mirantis.com/blog/kubernetes-vs-swarm-these-companies-use-both)
- [Mirantis - Committed to Swarm](https://www.mirantis.com/blog/mirantis-is-committed-to-swarm/)
- [Mirantis - Announcing the 23.0 major release for Mirantis Container Runtime — and Moby](https://www.mirantis.com/blog/announcing-the-23-0-major-release-for-mirantis-container-runtimeand-moby)

## Official Main Resources

- [Docker Swarm Docs](https://docs.docker.com/engine/swarm/)
- [Mirantis Swarm Homepage](https://www.mirantis.com/software/swarm/)
- [MCR - Mirantis Container Runtime Homepage](https://www.mirantis.com/software/mirantis-container-runtime/) - The Mirantis dockerd variant that supports Swarm Mode.
- [Mirantis Docs](https://docs.mirantis.com/) - Search Swarm for the various docs related to Swarm orchestration.
- [SwarmKit Repository](https://github.com/moby/swarmkit) - The upstream project that provides Swarm features to a container runtime.
- [Swarm Stack File reference](https://docs.docker.com/compose/compose-file/compose-file-v3/) - Compose file v3 format that works in Swarm for "stack files".

## Chat and Forums

- [Discord - Cloud Native DevOps](https://devops.fan) - Maintained by [Bret Fisher](https://www.bretfisher.com) and friends. Join the very active `#swarm` channel.<!--lint ignore double-link-->
- [SwarmKit.org Forum](https://swarmkit.org/forum/) - Maintained by [Portainer's](https://www.portainer.io/) co-founder Neil Cresswell.
- [Stack Overflow Swarm tag](https://stackoverflow.com/questions/tagged/docker-swarm)

## Community Tools

### Cluster Management

- [Portainer](https://www.portainer.io/) - A management UI that allows you to control Docker hosts, Swarm clusters, and Kubernetes clusters.
- [Swarmpit](https://swarmpit.io/) - Lightweight mobile-friendly Docker Swarm management UI.
- [AWS Docker Swarm Terraform Module](https://github.com/trajano/terraform-docker-swarm-aws)
- [Swarmsible](https://github.com/neuroforgede/swarmsible) - Tooling to create and manage Docker Swarm clusters based on Ansible.
- [Dockersamples Swarm Visualizer](https://github.com/dockersamples/docker-swarm-visualizer) - A basic web GUI visualizing a Swarm cluster. More of a concept and teaching UI than a production tool.
- [Swarm Dashboard](https://github.com/mohsenasm/swarm-dashboard) - A Simple Monitoring Dashboard for Docker Swarm Cluster.
- [swarmgate](https://github.com/neuroforgede/swarmgate) - Multitenancy for Docker Swarm - Docker Socket Proxy for use with Docker Swarm to have multiple tenants on a single Swarm..

### Extra Functionality

- [Swarm Cronjob](https://github.com/crazy-max/swarm-cronjob) - By [@crazy-max](https://github.com/crazy-max). Create jobs on a time-based schedule.
- [Shepherd](https://github.com/djmaze/shepherd) - Automatically update services whenever their image is refreshed.
- [Gantry](https://github.com/shizunge/gantry) - a tool to update docker swarm services, enhanced [Shepherd](https://github.com/djmaze/shepherd).
- [Swarm Sync](https://github.com/swarm-pack/swarm-sync) - GitOps for Swarm.
- [docker-stack-deploy (docker-sdp)](https://github.com/neuroforgede/docker-stack-deploy) - Automatic config/secret rotation for Docker stacks.
- [nothelm.py](https://github.com/neuroforgede/nothelm.py) - Opinionated docker stack project tool with templating support.
- [docker-stack-wait](https://github.com/sudo-bmitch/docker-stack-wait) - Tool to wait for your docker stack deployments to finish.
- [docker-swarm-proxy](https://github.com/neuroforgede/docker-swarm-proxy) - CLI plugin to that allows to exec into services. `docker exec` for Swarm.

### Volumes and Storage

Swarm previously only supported local volumes, NFS, and a limited set of Docker Engine Plugin drivers that supported Swarm Mode. Driver support has dwindled over time as vendors moved to Kubernetes. In 2023, with the Docker Engine v23.x release, Docker Engine and Swarm Mode gained the Container Storage Interface (CSI) standard. Existing CSI drivers will need to add Swarm support.

- [CSI support issue tracking in 2023](https://github.com/olljanat/csi-plugins-for-docker-swarm) - A GitHub repository tracking various storage drivers PRs and issues for Swarm CSI support in Docker/Moby v23+.
- [GlusterFS](https://www.gluster.org/) - GlusterFS is a scale-out network-attached storage file system.
- [Ceph](https://ceph.io/) - Ceph is a distributed object, block, and file storage platform. **Do you want Ceph support? [Upvote this issue](https://github.com/ceph/ceph-csi/issues/3769)**
- [juicefs](https://github.com/juicedata/juicefs) - JuiceFS is a distributed POSIX file system built on top of S3. It has a maintained [Docker plugin](https://github.com/juicedata/docker-volume-juicefs).
- [Portworx](https://docs.portworx.com/install-portworx/install-with-other/docker/swarm/) - Portworx is a container-native storage solution. It [supports Swarm installs](https://docs.portworx.com/install-portworx/install-with-other/docker/swarm/). Free for up to three nodes.
- [NetApp Trident](https://github.com/NetApp/trident) - A NetApp storage driver that has been known to work with Docker Engine and Swarm in the past. CSI Swarm support [has been requested](https://github.com/NetApp/trident/issues/804).
- [Hetzner Cloud Docker Volume Plugin](https://github.com/costela/docker-volume-hetzner) - Unofficial volume driver for [Hetzner Cloud](https://www.hetzner.com/cloud) by [@costela](https://github.com/costela).
- [Hetzner Cloud Volume CSI Driver](https://github.com/hetznercloud/csi-driver) - Hetzner Cloud Volume CSI Driver with experimental support for Docker Swarm.

### Networking

- [Swarm Ports](https://www.bretfisher.com/docker-swarm-firewall-ports/) - List and description of all the ports used by Swarm Mode (and the very old classic Swarm, if you're into that).
- [Libnetwork Troubleshooting](https://github.com/moby/libnetwork/blob/master/cmd/diagnostic/README.md) - Official Doc on using network diagnostic tools.
- [Traefik Proxy](https://github.com/traefik/traefik) - A reverse proxy and load balancer that makes deploying HTTP (and more) published services easy. Swarm Mode docs [start here](https://doc.traefik.io/traefik/providers/docker/#docker-swarm-mode).
- [Caddy Docker Proxy](https://github.com/lucaslorentz/caddy-docker-proxy) - Caddy based reverse proxy with automatic service discovery based on labels.
- [rawdns](https://github.com/tianon/rawdns) - a direct, raw DNS interface to the Docker API.

### Monitoring

- [docker-engine-events-exporter](https://github.com/neuroforgede/docker-engine-events-exporter) - Prometheus Exporter for Docker Engine Events.
- [docker-engine-networks-exporter](https://github.com/neuroforgede/docker-engine-networks-exporter) - Prometheus Exporter for additional network metrics such as usable ips.
- [promswarm](https://github.com/neuroforgede/promswarm) - Modernized version of [Swarmprom](https://github.com/stefanprodan/swarmprom), a great Prometheus/Grafana stack originally by [@stefanprodan](https://github.com/stefanprodan), now maintained by [@neuroforgede](https://github.com/neuroforgede).

## Community Tutorials and Education

### Courses and Videos

- [Docker Mastery, with Kubernetes and Swarm](https://bret.show/dockermastery) - Via Docker Captain Bret Fisher. The most popular paid mega-course on Docker, Kubernetes, and Swarm. The link includes a coupon.
- [Docker Swarm Mastery](https://bret.show/swarmmastery) - Via Docker Captain Bret Fisher. The most popular paid course focusing on Docker Swarm (assumes you have basic Docker/Compose knowledge). The link includes a coupon.
- [Docker Swarm Design and Production Tools from Bret Fisher at DockerCon](https://www.youtube.com/watch?v=V9fxU5zJKb4) - YouTube. DockerCon 2018. 40 minutes.

### Articles and Sample Code

- [Docker Swarm Rocks](https://dockerswarm.rocks/) - Collection of tutorials and code samples.
- [Vault + Swarm](https://blog.sunekeller.dk/2019/04/vault-swarm-plugin-poc/) - Vault + Swarm Docker secrets plugin (proof of concept).
- [dogvs.cat Sample Swarm Stacks](https://github.com/BretFisher/dogvscat) - Sample Docker Swarm cluster stack of tools including Traefik.
- [Swarm vs. Compose for Production](https://github.com/BretFisher/ama/discussions/146) - Only one host for a production environment. What to use: docker-compose or single node swarm?
- [Cheat Sheet on Docker and Swarm 2022](https://cheatography.com/boulard/cheat-sheets/docker-and-swarm-2022/)
- [Podlike](https://github.com/rycus86/podlike) - Viktor Adam's idea on how you could link multiple containers together to emulate a Kubernetes pod.
- [Operating Swarm](https://containers.goffinet.org/swarm/operatingswarm.html) - Useful tips for operating and troubleshooting Docker Swarm in production.

## Organisations Using Swarm

- [Co-op Cloud](https://coopcloud.tech)
- [NeuroForge](https://neuroforge.de)

## Related Awesome Lists

While this list is focused on Docker Swarm resources, general resources such as ones for Docker or Docker Compose can be helpful. The following keeps track of related awesome lists focused on this.

- [awesome-docker](https://github.com/veggiemonk/awesome-docker) - A list of awesome Docker tools.
- [awesome-compose](https://github.com/docker/awesome-compose) - A list of awesome Docker Compose samples.

## RIP

Honorable mentions of tools and information that are no longer maintained or supported. It may still work, but it's not being updated.

- [RexRay](https://github.com/rexray/rexray) - A container storage orchestration engine.

## Contributing

This list thrives on contributions from the community. The Maintainers can't do it alone. We need Swarm fans to help us find the best Swarm resources.

Want to contribute? Please read the [contribution guidelines](contributing.md). You can also ask questions in the [GitHub Discussions](https://github.com/BretFisher/awesome-swarm/discussions), or our [Discord Server #swarm channel](https://discord.gg/4jPPynEb2e).

## Maintainers

We're looking for more maintainers. Make some PRs to help, then LMK in Discussions, Twitter, or Discord (above) if you'd like to get involved in making a better community for Swarm.
