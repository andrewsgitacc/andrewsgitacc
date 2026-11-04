# Hi, I'm Andrew Kyle

Senior Linux Engineer working on infrastructure automation, Kubernetes and CI/CD.
This GitHub is where I build and document hands-on infrastructure labs: real-world
platform patterns, built from scratch on a Mac with VMware Fusion and kept entirely in Git.

[LinkedIn](https://www.linkedin.com/in/andrew-kyle-1007591/)

## Projects

### [labs](https://github.com/andrewsgitacc/labs)
Infrastructure labs, one per folder, all built with **Ansible** on CentOS Stream 9 VMs:

- **Kubernetes v1.36** (kubeadm): 3 control planes behind HAProxy + keepalived, 3 workers, Calico CNI
- **BIND DNS** with a dynamic zone for external-dns, plus a utility server holding the admin CLI tools
- **Jenkins**, configured as code (JCasC) with jobs as code
- **OpenVox (Puppet)** server and agents, deployed with r10k

### Platform lab: a GitOps platform on Kubernetes
Built one phase at a time on the lab cluster. Plan and runbooks:
[labs/platform](https://github.com/andrewsgitacc/labs/tree/main/platform).

| Status | Components |
|---|---|
| ✅ Done | MetalLB, Envoy Gateway (Gateway API), cert-manager, external-dns, Argo CD, Sealed Secrets, Rook-Ceph |
| 🚧 In progress | Prometheus, Grafana, Alertmanager, Loki, Alloy |
| Planned | Keycloak SSO, Harbor + Trivy, GitHub Actions runners + Renovate, Kargo, Kyverno, Velero |

The platform's config lives in two repos:

- [**platform-gitops**](https://github.com/andrewsgitacc/platform-gitops): the source of truth.
  Argo CD (app-of-apps + ApplicationSets) deploys every component from pinned Helm charts,
  and GitHub Actions renders every chart and schema-checks the manifests on each pull request.
- [**sample-app-deploy**](https://github.com/andrewsgitacc/sample-app-deploy): dev/staging/prod
  config for a demo app, to be promoted by Kargo (coming in a later phase)

### [puppet-control-repo](https://github.com/andrewsgitacc/puppet-control-repo)
Puppet control repo for the OpenVox lab: roles and profiles, Hiera data, branch-per-environment
with r10k, and a Jenkins pipeline for linting and validation.

## Tools I work with

**Linux** (RHEL / CentOS Stream) · **Ansible** · **Puppet / OpenVox** · **Kubernetes** · **Helm** ·
**Argo CD** · **Ceph** · **Prometheus / Grafana / Loki** · **GitHub Actions** · **Jenkins** ·
**BIND DNS** · **VMware**
