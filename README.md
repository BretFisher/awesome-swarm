# Awesome Swarm [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

<img src="images/awesome-swarm.png" align="right" width="250" />

> An awesome list of tools and info on Swarm Mode (SwarmKit)

Swarm (Swarm Mode, SwarmKit) is the simple orchestration and scheduling system built into Moby, Docker Engine, and Mirantis Container Engine (MCE). It is a distributed system that allows you to create and manage a cluster of container runtimes (nodes) and the container workloads running on them.

This Awesome List is maintained by [Bret Fisher](https://www.bretfisher.com) (and coming soon, maintainers [#3](https://github.com/BretFisher/awesome-swarm/issues/3)). This is a curated list of *working* tools and resources for using Swarm. It is not an official list, but a community effort to help people find the best tools and resources for Swarm in 2023 and beyond.

Want to contribute? Please read the (Coming soon [#2](https://github.com/BretFisher/awesome-swarm/issues/2)) [contribution guidelines](CONTRIBUTING.md), ask questions in this repositories [GitHub Discussions](https://github.com/BretFisher/awesome-swarm/discussions), or our [Discord Server #swarm channel](https://discord.gg/4jPPynEb2e).

- [Recent News and Updates (last 12 months) 🚨](#recent-news-and-updates-last-12-months-)
- [Official Main Resources 🏭](#official-main-resources-)
- [Chat and Forums 💬](#chat-and-forums-)
- [Community Tools 👩‍🚀](#community-tools-)
  - [Cluster Management](#cluster-management)
  - [Extra Functionality](#extra-functionality)
  - [Volumes and Storage](#volumes-and-storage)
  - [Networking](#networking)
- [Community Tutorials and Education 👩‍🏫](#community-tutorials-and-education-)
  - [Courses and Videos](#courses-and-videos)
  - [Articles and Sample Code](#articles-and-sample-code)
- [RIP ☠️](#rip-️)
- [Contributing 🙋‍♀️](#contributing-️)
- [Maintainers 🦸‍♀️🧑‍🚒🧑‍🎤](#maintainers-️)

## Recent News and Updates (last 12 months) 🚨

- [Mirantis - What's next for Swarm](https://www.mirantis.com/blog/what-s-next-for-swarm/)
- [Mirantis - Kubernetes vs Swarm - These companies use both](https://www.mirantis.com/blog/kubernetes-vs-swarm-these-companies-use-both)
- [Mirantis - Committed to Swarm](https://www.mirantis.com/blog/mirantis-is-committed-to-swarm/)

## Official Main Resources 🏭

- [Docker Swarm Docs](https://docs.docker.com/engine/swarm/)
- [Mirantis Swarm Homepage](https://www.mirantis.com/software/swarm/)
- [MCR - Mirantis Container Runtime Homepage](https://www.mirantis.com/software/mirantis-container-runtime/) - The Mirantis dockerd variant that supports Swarm Mode.
- [Mirantis Docs](https://docs.mirantis.com/) - Search Swarm for the various docs related to Swarm orchestration.
- [SwarmKit Repository](https://github.com/moby/swarmkit) - The upstream project that provides Swarm features to a container runtime.
- [Swarm Stack File reference](https://docs.docker.com/compose/compose-file/compose-file-v3/) - Compose file v3 format that works in Swarm for "stack files".

## Chat and Forums 💬

- [Discord - Cloud Native DevOps](https://devops.fan) - Maintained by [Bret Fisher](https://www.bretfisher.com) and friends. Join the very active `#swarm` channel.
- [SwarmKit.org Forum](https://swarmkit.org/forum/) - Maintained by [Portainer's](https://www.portainer.io/) co-founder Neil Cresswell.
- [Stack Overflow Swarm tag](https://stackoverflow.com/questions/tagged/docker-swarm)

## Community Tools 👩‍🚀

### Cluster Management

- [Portainer](https://www.portainer.io/) - A management UI which allows you to control Docker hosts, Swarm clusters, and Kubernetes clusters.
- [Swarmpit](https://swarmpit.io/) - Lightweight mobile-friendly Docker Swarm management UI.
- [AWS Docker Swarm Terraform Module](https://github.com/trajano/terraform-docker-swarm-aws)
- [Swarmsible](https://github.com/neuroforgede/swarmsible) - Tooling to create and manage Docker Swarm clusters based on Ansible.

### Extra Functionality

- [Swarm Cronjob](https://github.com/crazy-max/swarm-cronjob) - By @crazy-max. Create jobs on a time-based schedule.
- [Shepherd](https://github.com/djmaze/shepherd) - Automatically update services whenever their image is refreshed.
- [Swarm Sync](https://github.com/swarm-pack/swarm-sync) - GitOps for Swarm.
- [Dockersamples Swarm Visualizer](https://github.com/dockersamples/docker-swarm-visualizer) - A basic web GUI visualizing a Swarm cluster. More of a concept and teaching UI than a production tool.

### Volumes and Storage

Swarm previously only supported local volumes, NFS, and a limited set of Docker Engine Plugin drivers that supported Swarm Mode. Driver support has dwindled over time as vendors moved to Kubernetes. In 2023, with Docker Engine v23.x release, Docker Engine and Swarm Mode gained the Container Storage Interface (CSI) standard. Existing CSI drivers will need to add Swarm support.

- [CSI support issue tracking in 2023](https://github.com/olljanat/csi-plugins-for-docker-swarm) - A GitHub repository tracking various storage drivers PRs and issues for Swarm CSI support in Docker/Moby v23+.
- [GlusterFS](https://www.gluster.org/) - GlusterFS is a scale-out network-attached storage file system. It has found applications including cloud infrastructure, streaming media services, and content delivery networks.
- [Ceph](https://ceph.io/) - Ceph is a distributed object, block, and file storage platform designed to provide excellent performance, reliability, and scalability.
- [Portworx](https://docs.portworx.com/install-portworx/install-with-other/docker/swarm/) - Portworx is a sophisticated, production-quality container-native storage solution. It supports Swarm installs. Free for up to three nodes.
- [NetApp Trident](https://github.com/NetApp/trident) - A NetApp storage driver that has been known to work with Docker Engine and Swarm in the past. CSI Swarm support [has been requested](https://github.com/NetApp/trident/issues/804).

### Networking

- [Swarm Ports](https://www.bretfisher.com/docker-swarm-firewall-ports/) - List and description of all the ports used by Swarm Mode (and the very old classic Swarm, if you're into that).
- [Libnetwork Troubleshooting](https://github.com/moby/libnetwork/blob/master/cmd/diagnostic/README.md) - Official Doc on using network diagnostic tools.
- [Traefik Proxy](https://github.com/traefik/traefik) - A reverse proxy and load balancer that makes deploying HTTP (and more) published services easy. Swarm Mode docs [start here](https://doc.traefik.io/traefik/providers/docker/#docker-swarm-mode).

## Community Tutorials and Education 👩‍🏫

### Courses and Videos

- [Docker Mastery, with Kubernetes and Swarm](https://bret.show/dockermastery) - Via Docker Captain Bret Fisher. The most popular paid mega-course on Docker, Kubernetes, and Swarm. Link includes coupon.
- [Docker Swam Mastery](https://bret.show/swarmmastery) - Via Docker Captain Bret Fisher. The most popular paid course focusing on Docker Swarm (assumes you have basic Docker/Compose knowledge). Link includes coupon.

### Articles and Sample Code

- [Docker Swarm Rocks](https://dockerswarm.rocks/) - Collection of tutorials and code samples. Respository behind the site [tiangolo/dockerswarm.rocks](https://github.com/tiangolo/dockerswarm.rocks).
- [Vault + Swarm](https://blog.sunekeller.dk/2019/04/vault-swarm-plugin-poc/) - Vault + Swarm Docker secrets plugin (proof of concept).
- [dogvs.cat Sample Swarm Stacks](https://github.com/BretFisher/dogvscat) - Sample Docker Swarm cluster stack of tools including Traefik.
- [Swarm vs. Compose for Production](https://github.com/BretFisher/ama/discussions/146) - Only one host for production environment. What to use: docker-compose or single node swarm?
- [Cheat Sheet on Docker and Swarm 2022](https://cheatography.com/boulard/cheat-sheets/docker-and-swarm-2022/)
- [Podlike](https://github.com/rycus86/podlike) - Viktor Adam's idea on how you could link multiple containers together to emulate a Kubernetes pod.

## RIP ☠️

Honorable mentions of tools and information that is no longer maintained or supported. It may still work, but it's not being updated.

- [RexRay](https://github.com/rexray/rexray) - A container storage orchestration engine.
- [Swarmprom](https://github.com/stefanprodan/swarmprom) - A great Prometheus/Grafana stack for Swarm by @stefanprodan.

## Contributing 🙋‍♀️

This list thrives on contributions from the community, and being *up to date*. The Maintainers can't do it alone. We need Swarm fans to help us find the best Swarm resources.

Want to contribute? Please read the [contribution guidelines](CONTRIBUTING.md) (Coming soon [#2](https://github.com/BretFisher/awesome-swarm/issues/2)), ask questions in this repositories [GitHub Discussions](https://github.com/BretFisher/awesome-swarm/discussions), or our [Discord Server #swarm channel](https://discord.gg/4jPPynEb2e).

## Maintainers 🦸‍♀️🧑‍🚒🧑‍🎤

Lead by Bret Fisher, I'm looking for more maintainers. LMK in Discussions, Twitter, or Discord (above) if you'd like to get involved in making a better community for Swarm.
