---
title: "Cloud Native Infrastructure with Kubernetes and Pulumi"
authors: ["joe-duffy"]
tags: ["Kubernetes"]
date: "2018-09-12"

description: "Announcing Pulumi for Kubernetes. A way to create, deploy and manage Kubernetes applications using your favorite programming language."
---


 

Today we're pleased to [announce Pulumi for
Kubernetes](https://info.pulumi.com/press-release/pulumi-cloud-native-sdk-delivers-cloud-native-infrastructure-as-code-for-kubernetes),
a way to create, deploy, and manage Kubernetes applications using your
favorite programming languages, bringing the same lovable experience
that works across AWS, Azure, Google Cloud, OpenStack, and other clouds,
now to Kubernetes and cloud native architectures. We have built this
support in response to significant user interest and real end users
scenarios, and are excited to share what we've been up to. You can [dive
right in here](https://pulumi.io/quickstart/kubernetes/index.html) and
look at some [powerful things Pulumi enables
here](../../../com/pulumi/blog/program-kubernetes-with-11-cloud-native-pulumi-pearls.html).

Why Pulumi?
===========

Kubernetes has quickly become the "gold standard" for running containers
in production, spanning public, private, and hybrid cloud scenarios.
It's been remarkable to watch its explosive progress in even just this
past year alone. Every cloud vendor now supports an easy-to-use managed
Kubernetes solution -- Google GKE, Azure AKS, and AWS AKS -- making it
easier than ever before to get started writing and deploying Kubernetes
applications.

Kubernetes is essentially the "POSIX" for the cloud and unlocks the
potential for a true cloud native development platform to be built on
top. We at Pulumi are tremendously excited by this opportunity -- it
aligns perfectly with our vision for the future, and our language-driven
and true platform approach.

Despite these advances, Kubernetes can still be intimidating to use.
This is true for newcomers and experts alike. The use of YAML for
configuration has led to the "Wall of YAML" problem, giving way to many
quasi-languages, often rudimentary templating systems bolted on top of
YAML. The lack of true end-to-end deployment support -- including
orchestrated rollouts, knowing when a deployment has completed
successfully, or even managing resources outside of Kubernetes itself
like databases, container registries, and other hosted services -- has
led to the "Mountains of Bash" problem. All aspects, from creation to
deployment to management, can be difficult, particularly at scale.

We envision a future where all developers and DevOps engineers
seamlessly leverage Kubernetes to program the cloud. To get there, we
need to bring joy, ease of use, and simplicity to the entire Kubernetes
software development lifecycle. We must eliminate toil and maximize
productivity. This is precisely what Pulumi for Kubernetes aims to do.

Real Languages
==============

Our favorite way to program Kubernetes is using TypeScript, as it
delivers strong typing where possible and dynamic typing where needed.
This delivers great IDE support out of the box, no matter your IDE of
choice, complete with auto-completion, interactive documentation and
error reporting, refactoring support, and more. The result is a
radically improved inner development loop. In addition to TypeScript,
JavaScript works too, and Python and Go are on the way.

Perhaps the best part of using a real language is instance access to an
ecosystem of libraries. Any NPM module is an npm install away. And you
can create your own libraries -- classes to encapsulate full
components, and functions to capture repeated patterns of code --
helping to reduce boilerplate, maximize reuse and sharing, and make you
more productive. The standard Kubernetes guestbook shrinks to a mere 20
lines of code thanks to abstraction!

Many of our customers have already used this capability to capture best
practices within their own team, shrinking 1,000s of lines of
copy-and-pasted YAML to just a handful of lines of real code.

We are just getting started with our own Kubernetes abstractions, but
we're most excited to see where you, the community, take things.

End-to-End Deployment Orchestration
===================================

Pulumi programs are deployed using a single CLI command

`$ pulumi up`

This command works the first time -- when all resources will be created
-- in addition to all subsequent updates. Each update will show a full
diff of what has changed before you deploy anything:

![diff-1](https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=2190&name=diff-1.gif){width="2190"
sizes="(max-width: 2190px) 100vw, 2190px"
srcset="https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=1095&name=diff-1.gif 1095w, https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=2190&name=diff-1.gif 2190w, https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=3285&name=diff-1.gif 3285w, https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=4380&name=diff-1.gif 4380w, https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=5475&name=diff-1.gif 5475w, https://blog.pulumi.com/hs-fs/hubfs/diff-1.gif?width=6570&name=diff-1.gif 6570w"}

Because Pulumi also supports resources for all clouds -- including AWS,
Azure, Google Cloud, OpenStack, and VMWare vSphere -- you can mix and
match all of your infrastructure needs using one consistent programming
language, model, tool, and workflow. This means, for example, that a
single program can provision your Kubernetes resources alongside Azure
CosmosDB, a Google Container Registry to publish your Docker builds to
before pulling them in your cluster, an AWS S3 Bucket for your
application, or even CDN and DNS entries for your cluster. Pulumi's
notion of stacks makes it easy to multi-instantiate your application for
different environments.

Programs are just code, unlocking sophisticated cloud native scenarios;
e.g.

-   Deploy a canary, wait for Prometheus health checks to pass, and then
    promote
-   Create a base class that injects Envoy sidecars automatically for
    any pod in your org
-   Manage your Envoy config as code, and version it alongside your
    Kubernetes config

The Pulumi Delivery Platform works in tandem with the CLI to ensure
continuous delivery of your infrastructure. This supports robust
deployments in a team environment with state checkpointing and
concurrency control. It integrates with any CI system and supports a
GitHub App that you can install to get previews of changes inside your
Pull Requests. This enables a true GitOps workflow -- for both
Kubernetes config updates, and your cloud infrastructure.

What's Next
===========

Today is just the beginning of an exciting journey, with Pulumi's
support for Kubernetes and cloud native architectures. We are excited to
tell you about what we've been up to, and hope that real languages will
bring you more joy, reduce toil, and ultimately lower the barriers to
entry for using Kubernetes with real components and reuse.

We can't wait to hear what you think. To learn more or give it a try,
please check out these resources:

Download Pulumi: <https://pulumi.io> 

These two tutorials will walk you through your first [Pulumi for
Kubernetes](https://pulumi.io/quickstart/kubernetes/index.html) project:

-   [Tutorial: Deploy a Stateless Nginx
    Application](https://pulumi.io/quickstart/kubernetes/tutorial-stateless-app.html)
-   [Tutorial: Deploy a Load-Balanced Guestbook App with Redis and
    Nginx](https://pulumi.io/quickstart/kubernetes/tutorial-guestbook.html)

[Program Kubernetes with 11
Pearls](../../../com/pulumi/blog/program-kubernetes-with-11-cloud-native-pulumi-pearls.html):
a companion blog post, also launched today, with 11 exciting examples.

If you have any questions or comments, we'd love to hear from you in our
[Community Slack](https://slack.pulumi.io) or over on
[GitHub](https://github.com/pulumi).

Happy cloud native hacking! 
