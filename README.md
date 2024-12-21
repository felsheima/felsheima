## Malware Analysis 
This capstone project investigates the effectiveness of various malware analysis tools and techniques. With the increasing prevalence of malware, choosing the right tools is crucial for successful analysis. This research employs static, dynamic, and hybrid analysis methodologies using a lab environment with FlareVM and Remnux virtual machines. By comparing tools like IDA Pro, Regshot, Ghidra, and Procmon, this study aims to provide a guide for cybersecurity professionals to enhance malware detection and defense strategies. The research highlights the need for a combined approach, leveraging the strengths of different tools for optimal results.
## Table of Contents
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Methodology](#methodology)
- [Results](#results)
- [Tools Used](#toolsused)
- [Challenges and Lessons Learned](#challengesandlessonslearned)
- [Repository Structure](#repositorystructure)

# Introduction
As technology dependence increases, so does the prevalence of malware. This project addresses the challenge of selecting appropriate malware analysis tools by comparing their performance in detecting file system changes, registry modifications, and import detections. The project employs a mixed-methods approach, combining literature review with practical experimentation in a controlled lab environment. This repository provides the project's methodology, results, and lessons learned.

# Objectives 
This research aims to assist cybersecurity professionals in selecting the most suitable malware analysis tools for their specific tasks. This is achieved by comparing the detection capabilities of various tools in relation to key malware features. The research questions guiding this study are:

1.  What are the strengths and weaknesses of static versus dynamic analysis in identifying malware threats?
2.  How effective are various malware analysis tools in detecting specific types of malware?
3.  What emerging trends in malware analysis tools and techniques are expected to shape the field in the next five years?
4.  How do different types of malware impact the selection of analysis techniques?

# Methodology
This project utilized a mixed-methods approach, incorporating static, dynamic, and hybrid analysis techniques. The lab environment consisted of a FlareVM and Remnux virtual machine (VM) within VirtualBox. Remnux simulated an internet environment using InetSim. Three malware samples were analyzed: WannaCry ransomware, a Remote Access Trojan (RAT), and a BackDoor malware, sourced from the TCM Security repository.

The following tools were used:

*   **Static Analysis:** IDA Pro, Ghidra
*   **Dynamic Analysis:** Procmon, Regshot
*   **Hybrid Analysis:** Hybrid Analysis (CrowdStrike Falcon Sandbox), Cuckoo Sandbox

The analysis focused on detecting the following malware features:

*   File system changes
*   Registry modifications
*   Import detections

Data was collected using templates to log results at each analysis phase. The effectiveness of each tool in detecting the specified features was then compared.

# Results
The following table summarizes the effectiveness of the tools:

| Feature           | Procmon        | IDA Pro                               | Ghidra                               | Regshot            |
|-------------------|----------------|---------------------------------------|---------------------------------------|--------------------|
| File System Changes | Highly Effective | Effective (with limitations in obfuscation) | Effective                              | Not Supported      |
| Registry Changes  | Highly Effective | Effective                               | Effective                              | Highly Effective |
| Import Detection  | Effective      | Highly Effective                       | Highly Effective                       | Not Supported      |

Procmon proved to be the most versatile tool, performing well across all features. IDA Pro and Ghidra were effective for static analysis, but struggled with obfuscation. Regshot was highly effective for registry analysis but limited in scope. The results reinforce the need for a hybrid approach, combining multiple tools for comprehensive malware analysis.

# Tools Used
*   **Virtualization:** VirtualBox
*   **Virtual Machines:** FlareVM, Remnux
*   **Malware Analysis Tools:** IDA Pro, Ghidra, Procmon, Regshot, Hybrid Analysis (CrowdStrike Falcon Sandbox), Cuckoo Sandbox
*   **Network Simulation:** InetSim

# Challenges and Lessons Learned 
*   **Challenge:** Obfuscation techniques in malware samples made static analysis more difficult.
*   **Lesson:** Dynamic and hybrid analysis are crucial for overcoming obfuscation.
*   **Challenge:** Time constraints limited the number of malware samples and features analyzed.
*   **Lesson:** Future research should involve a larger sample size and a wider range of features.
*   **Challenge:** Each tool has its own learning curve and requires specific expertise.
*   **Lesson:** Combining tools and leveraging their individual strengths is essential.
