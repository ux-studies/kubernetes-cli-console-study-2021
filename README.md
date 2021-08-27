# Comparing CLI and Graphical Tool Modalities for Kubernetes Tasks

Kubernetes is a platform for managing containerized workloads. According to the Cloud Native Computing Foundation (CNCF) 2020 survey, Kubernetes use in production has increased to 83%, up from 78% in 2019. However, this and other relevant surveys do not report on the types of Kubernetes tools that developers prefer. We present a three-part study to address this research gap.

The first part of our study is a generative survey on how *tool* preference varies across Kubernetes *tasks*. The survey has X respondents, and asks which of three tool modalities (CLI, Graphical Console, IDE) are preferred to aid each of three broad classes of tasks (CRUD, debugging, monitoring). The survey shows that preference radically skews towards modality X, except for Y.

The second part of our study drills down on a debugging task, to further explore why preference may skew towards the more primitive ASCII CLIs. We perform a within-subjects, remotely moderated user study with X participants. Each participant is asked to finish the debugging task twice: once using the `kubectl` CLI and once using the OpenShift web console. All participants of this second study successfully accomplish the task in both modalities, and a separate post-study survey corroborates the first survey: all participants prefer the CLI modality.

The third part of our study *quantifies* these preferences, to help us towards a more constructive perspective. To analyze preference for these disparate modalities, we identify a set of *comparable* metrics that can be easily deduced from screen recordings of the debugging task sessions. We show how to use these measurable quantities to quantify user *exhaustion* and *disruption*. When comparing these values, we found that the CLI modality can offer significantly lower counts for *both* metrics.

Finally, we share participant recommendations for improving each tool interface and our own design insights observed from the study to inform the future design of Kubernetes tool interfaces.

# Study 1: Survey of how Tool Preference Varies by Task and Breakdown of Task Type Frequencies

![Survey0](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey0.png)
![Survey1](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey1.png)

# Study 2: User Study of Kubernetes Debugging Task Using the `kubectl` CLI and the OpenShift web console

# Study 3: Quantifying User Tool Preference for a Kubernetes Debugging Task
