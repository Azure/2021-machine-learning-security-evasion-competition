# Attacker Challenge
<!-- vscode-markdown-toc -->
* [Overview](#overview)
    * [Challenge Dates](#challenge-dates)
    * [Rules / Terms](#rules-/-terms)
* [Tracks](#tracks)
    * [Anti-malware evasion track submission requirements](#anti-malware-evasion-track-submission-requirements)
    * [Anti-phishing evasion track submission requirements](#anti-phishing-evasion-track-submission-requirements)
* [Sample Solution](#sample-solution)
* [Resources](#resources)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->


## <a name='overview'></a>Overview

### <a name='challenge-dates'></a>Challenge Dates
Aug 06 - Sep 17, 2021 (AoE)

### <a name='rules-/-terms'></a>Rules / Terms
[https://mlsec.io/tos](https://mlsec.io/tos)


## <a name='tracks'></a>Tracks
### <a name='anti-malware-evasion-track-submission-requirements'></a>Anti-malware evasion track submission requirements
A valid antimalware evasion submission consists of the following:
1. a ZIP file containing modified malware samples with their original names (`001`, `002`, etc.)
2. samples in the ZIP file have been verified as functional in a [Windows 10 Sandbox (disable networking!)](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/)
3. partial uploads are okay, and can be used to "update" or "complete" a solution
4. uploads are rate limited; only infrequent uploads are allowed


### <a name='anti-phishing-evasion-track-submission-requirements'></a>Anti-phishing evasion track submission requirements
A valid antiphishing evasion submission consists of the following:
1. a ZIP file containing modified malware samples with their original names (`001`, `002`, etc.)
2. when rendered in a Chromium-based browser like [Microsoft Edge](https://www.microsoft.com/en-us/edge?r=1), each sample renders identically to the original
3. partial uploads are okay, and can be used to "update" or "complete" a solution
4. uploads are rate limited; only infrequent uploads are allowed

## <a name='sample-solution'></a>Sample Solution
We encourage solutions that extend Microsoft Counterfit. A partial solution is included in the [mlsecevasion/2021 branch](https://github.com/Azure/counterfit/tree/mlsecevasion/2021).

To get started, visit
* [Getting Started](https://github.com/Azure/counterfit/blob/mlsecevasion/2021/docs/getting_started.md)

## <a name='resources'></a>Resources
For additional questions, the following resources are available:
* [REST API Interface](docs/API.md) API documentation for submitting samples and uploading ZIP files
* [Frequently Asked Questions](FAQ.md) markdown file with solutions to common problems
* [Join the Slack channel](https://join.slack.com/t/evademalwareml/shared_invite/zt-9birv1qf-KJFEiyLLRVtrsNDuyA0clA) to interact with other contestants
* [Submit an issue](https://github.com/Azure/2021-machine-learning-security-evasion-competition/issues) for issues relating to the sample code