# Comparing CLI and Graphical Tool Modalities for Kubernetes Tasks

Kubernetes is a platform for managing containerized workloads. According to the Cloud Native Computing Foundation (CNCF) 2020 survey, Kubernetes use in production has increased to 83%, up from 78% in 2019. However, this and other relevant surveys do not report on the types of Kubernetes tools that developers prefer. We present a three-part study to address this research gap.

The first part of our study is a generative survey on how *tool* preference varies across Kubernetes *tasks*. The survey has X respondents, and asks which of three tool modalities (CLI, Graphical Console, IDE) are preferred to aid each of three broad classes of tasks (CRUD, debugging, monitoring). The survey shows that preference radically skews towards modality X, except for Y.

The second part of our study drills down on a debugging task, to further explore why preference may skew towards the more primitive ASCII CLIs. We perform a within-subjects, remotely moderated user study with X participants. Each participant is asked to finish the debugging task twice: once using the `kubectl` CLI and once using the OpenShift web console. All participants of this second study successfully accomplish the task in both modalities, and a separate post-study survey corroborates the first survey: all participants prefer the CLI modality.

The third part of our study *quantifies* these preferences, to help us towards a more constructive perspective. To analyze preference for these disparate modalities, we identify a set of *comparable* metrics that can be easily deduced from screen recordings of the debugging task sessions. We show how to use these measurable quantities to quantify user *exhaustion* and *disruption*. When comparing these values, we found that the CLI modality can offer significantly lower counts for *both* metrics.

Finally, we share participant recommendations for improving each tool interface and our own design insights observed from the study to inform the future design of Kubernetes tool interfaces.

# Part 1: Survey of how Tool Preference Varies by Task and Breakdown of Task Type Frequencies

![Survey0](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey0.png)

*A majority of people prefer to use CLIs to work on Kubernetes CRUD tasks and half prefer to use CLIs to work on Kubernetes debugging and monitoring tasks.*

![Survey1](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey1.png)

*A majority of the time that people use Kubernetes, they are working on CRUD tasks many times each day.*

# Part 2: User Study of Tool Preference for a Kubernetes Debugging Task

![Study4](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study4.png)

*Participants P2 and P3 perceived that they were more successful at completing the debugging task using the kubectl CLI than using the OpenShift Console.*

![Study5](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study5.png)

*All participants said that they liked using the kubectl CLI to complete the debugging task, while half said they liked using the OpenShift Console.*

# Part 3: Quantifying User Tool Preference for a Kubernetes Debugging Task
![Study0](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study0.png)

*Participant breakdown of exhaustion measured by counting observed clicks, commands, and mouse movements. Participants P3 and P4 almost exclusively used commands to complete the debugging task using the kubectl CLI and all participants almost exclusively used clicks and mouse movements using the OpenShift Console.*

![Study1](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study1.png)

*Participant exhaustion measured by counting observed clicks, commands, and mouse movements are overall higher for clicks and mouse movements using the OpenShift and are overall higher for commands using the kubectl CLI.*

![Study3](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study3.png)

*Participant disruption measured by counting observed switches between mouse and keyboard inputs are overall higher for the OpenShift Console. Participants P2, P3, and P4 have lower frequencies of disruption using the kubectl CLI than the OpenShift Console.*

![Study2](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study2.png)

*Participant disruption measured by counting observed switches between mouse and keyboard inputs are overall higher for the OpenShift Console.*

![Study6](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study6.png)

*Participant breakdown of low level and high level interactions and totals for exhaustion and disruption. Low level interactions are represented as letters: clicks (C), commands (K), and mouse movements (M). Exhaustion calculated by counting each interaction (i.e. K = 1, KK = 2, etc.) and disruption calculated by counting each switch from mouse to keyboard (i.e. MC = 0, MK = 1, KMK = 2). High level interactions are represented as regular expressions composed of the low level interactions used to accomplish command execution, copy/paste, navigation, and tab completion. Exhaustion and disruption totals are overall higher for the OpenShift Console.*
