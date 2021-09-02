# Comparing CLI and Graphical Tool Modalities for Kubernetes Tasks

Despite increased usage of Kubernetes, developer surveys lack reports on which Kubernetes tools are preferred in practice. We present a three-part study to address this gap. Part one surveys how preference of three *tool modalities* (CLI, Graphical Console, IDE) varies across three *tasks* (CRUD, debugging, monitoring). Among 8 respondents, preference radically skews towards CLIs, except for monitoring and debugging tasks. Part two observes how participants complete a debugging task using the `kubectl` CLI and the OpenShift web console. All 4 participants accomplished the task in both modalities and preferred the CLI over the web console. Part three quantifies preference with the goal of constructively informing the design of Kubernetes tools. We identified a set of comparable metrics from screen recordings of the debugging task sessions to quantify participant *exhaustion* and *disruption*. We found that in comparison to the web console, the CLI can offer significantly lower counts for *both* metrics.

# Part 1: Survey of how Tool Preference Varies by Task and Breakdown of Task Type Frequencies

The purpose of this survey is to understand how Kubernetes users accomplish certain tasks (CRUD, debugging, and monitoring) given the inherent limitations of broad classes of tool modalities (textual and graphical). Our survey results show that a majority of people prefer to use CLIs to work on Kubernetes CRUD tasks as opposed to using an IDE or Graphical Console and half prefer to use CLIs to work on Kubernetes debugging and monitoring tasks.

![Survey2](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey2.png)

*Participant levels of Kubernetes experience.*

![Survey0](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey0.png)

*A majority of people prefer to use CLIs to work on Kubernetes CRUD tasks and half prefer to use CLIs to work on Kubernetes debugging and monitoring tasks as opposed to using an IDE or Graphical Console.*

![Survey1](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Survey1.png)

*A majority of the time that people use Kubernetes, they are working on CRUD tasks many times each day.*

# Part 2: User Study of Tool Preference for a Kubernetes Debugging Task

![Study4](https://github.com/ux-studies/kubernetes-cli-console-study-2021/blob/main/Study4.png)

*Half of the participants perceived that they were more successful at completing the debugging task using the kubectl CLI than using the OpenShift Console.*

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

*Participant breakdown of low level and high level interactions and totals for high level exhaustion and disruption. Low level interactions are represented as letters: clicks (C), commands (K), and mouse movements (M). Exhaustion calculated by counting each interaction (i.e. K = 1, KK = 2) and disruption calculated by counting each switch from mouse to keyboard (i.e. MC = 0, MK = 1, KMK = 2). High level interactions are represented as regular expressions composed of the low level interactions used to accomplish command execution, copy/paste, navigation, and tab completion. High level exhaustion and disruption totals are overall higher for the OpenShift Console, which supports the overall higher total exhaustion and disruption frequencies for the OpenShift Console from counting the low level interactions.*
