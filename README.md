<p align="center"><img src="https://kubecrow.com/assets/icon-512.png" alt="KubeCrow" width="128"></p>

<h1 align="center">KubeCrow</h1>

<p align="center"><a href="https://github.com/kubecrow/kubecrow/releases/latest"><img src="https://img.shields.io/github/v/release/kubecrow/kubecrow?label=latest&color=2f6fed" alt="Latest release"></a> <img src="https://img.shields.io/badge/macOS-13%2B-black?logo=apple" alt="macOS 13 or later"> <img src="https://img.shields.io/badge/price-free-2ea043" alt="Free"></p>

<p align="center"><strong>The free Kubernetes IDE for Mac.</strong><br>
A native macOS desktop GUI for every cluster in your kubeconfig: pods and every other resource, logs, shells, YAML, Helm, Amazon EKS, and a Health page that tells you what is wrong before it pages you.</p>

<p align="center">
  <a href="https://github.com/kubecrow/kubecrow/releases/latest"><strong>Download for Apple Silicon</strong></a> ·
  <a href="https://github.com/kubecrow/kubecrow/releases/latest"><strong>Download for Intel</strong></a> ·
  <a href="https://kubecrow.com">kubecrow.com</a> ·
  <a href="https://kubecrow.com/releases.html">Release notes</a> ·
  <a href="https://kubecrow.com/guides.html">Guides</a>
</p>

<p align="center"><a href="https://kubecrow.com"><img src="https://kubecrow.com/assets/screenshots/hero.png" alt="KubeCrow's Health page: cluster score, CPU and memory capacity, usage over time with rollout markers, warning events and the problems list" width="900"></a></p>

This repository hosts the **downloads** for KubeCrow and is where the app checks for updates. The source code is not published here. Questions and bug reports are welcome in [Issues](https://github.com/kubecrow/kubecrow/issues).

## Why KubeCrow

- **Free.** Every feature, every cluster, no trial period and no paid tier. Sign in once with Google or GitHub.
- **Nothing installed in your cluster.** KubeCrow talks to the Kubernetes API from your Mac, the same way kubectl does. No agents, no operators.
- **No telemetry.** The app sends nothing about you or your clusters anywhere.
- **Native on Apple Silicon**, with a separate build for Intel Macs. Signed with an Apple Developer ID and notarised, so macOS opens it like any other app. Updates install themselves.

## What it does

| | |
|---|---|
| **Health at a glance** | A score for the cluster, capacity tiles for CPU, memory and pods, usage over time with rollout, OOM and node markers, warning events, node heatmap, pending pods, full volumes and expiring TLS certificates. Prometheus when you have it, the app's own samples when you don't. |
| **Problems, before they page you** | Crash loops, stuck rollouts (with one-click rollback), failing probes, pending pods, each with the reason and a fix. |
| **What changed** | A timeline of rollouts, rollbacks, scaling, restarts and ConfigMap edits, so "what happened at 14:32" has an answer. |
| **Ask AI** | Ask why a pod is failing, using the AI tool already on your Mac. Nothing is sent until you allow it. |
| **Every resource, live** | Pods, Deployments, StatefulSets, Jobs, Services, Ingresses, ConfigMaps, Secrets, PVCs, nodes, CRDs and everything else, updated as the cluster changes. |
| **Logs that read well** | Stream a container's logs with search, timestamps and pretty-printed JSON, or search every pod's logs in a namespace through Loki. |
| **Shells and port forwards** | A shell in any container or on any node, and a port forward to any Service or pod, in one click. |
| **Edit YAML in place** | Edit any resource with a diff before you save. |
| **Helm** | Install, upgrade and roll back releases, with values and history. |
| **Right-sizing** | CPU and memory requests and limits against real use from Prometheus, with suggested values. |
| **Security** | Privileged and root containers, host access, plain-text secrets, cluster-admin bindings, open network paths and image vulnerabilities. |
| **Cost** | Cost per namespace, workload and node, priced from AWS's Price List API or your own rates. |
| **Amazon EKS** | Sign in with AWS SSO inside the app, no AWS CLI needed, and KubeCrow finds your clusters in every account and region. GKE, AKS and any other cluster work through your kubeconfig. |
| **Production guard** | Mark a cluster Protected and every change asks you to type its name first, or Read-only to refuse changes and shells altogether. |
| **⌘K and themes** | A command palette for everything, light and dark modes, three colour themes. |

<p align="center">
  <a href="https://kubecrow.com"><img src="https://kubecrow.com/assets/screenshots/stuck-rollout.png" alt="A stuck rollout in KubeCrow, with the reason and a one-click rollback" width="440"></a>
  <a href="https://kubecrow.com"><img src="https://kubecrow.com/assets/screenshots/ai-chat.png" alt="Ask AI in KubeCrow explaining why a pod is crash-looping" width="440"></a>
</p>
<p align="center">
  <a href="https://kubecrow.com"><img src="https://kubecrow.com/assets/screenshots/eks-clusters.png" alt="Amazon EKS clusters discovered across AWS accounts and regions" width="440"></a>
  <a href="https://kubecrow.com"><img src="https://kubecrow.com/assets/screenshots/rightsizing.png" alt="Right-sizing: requests and limits compared with real CPU and memory use" width="440"></a>
</p>

## Install

With [Homebrew](https://brew.sh/):

```bash
brew install kubecrow/tap/kubecrow
```

Or by hand:

1. Download the `.dmg` for your Mac from the [latest release](https://github.com/kubecrow/kubecrow/releases/latest): `arm64` for Apple Silicon (M1 and later), `x64` for Intel.
2. Open it and drag KubeCrow into Applications.
3. Open KubeCrow and sign in with Google or GitHub. Your kubeconfig contexts are listed straight away; EKS clusters from your AWS profiles appear alongside.

**Requirements:** macOS 13 or later. A kubeconfig (`~/.kube/config` or `$KUBECONFIG`). For Helm, the `helm` CLI (`brew install helm`). For EKS, an AWS sign-in (SSO or access keys) added in Settings.

Each release lists the SHA-256 of its files; the same hashes are on [kubecrow.com](https://kubecrow.com/#install).

## Guides

- [Connect to Amazon EKS from your Mac](https://kubecrow.com/amazon-eks.html)
- [Prometheus, Mimir and Loki in KubeCrow](https://kubecrow.com/prometheus-loki.html)
- [Right-size Kubernetes requests and limits](https://kubecrow.com/kubernetes-right-sizing.html)
- [The Kubernetes RBAC permissions KubeCrow needs](https://kubecrow.com/kubernetes-permissions.html)

## About the name

One word, **KubeCrow**, said "kube crow": *Kube* as in Kubernetes, *crow* as in the bird and the crow's nest, the lookout at the top of a ship's mast. Kubernetes is Greek for helmsman, and KubeCrow is the lookout for your clusters. Also written Kube Crow or kubecrow. Not related to KubeCon, the conference, or to kro, the Kube Resource Orchestrator.

[Privacy policy](https://kubecrow.com/privacy.html) · [Release feed (Atom)](https://kubecrow.com/releases.xml)
