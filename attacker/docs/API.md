# REST API
<!-- vscode-markdown-toc -->
* [Anti-malware](#anti-malware)
    * [Query Hosted ML anti-malware models](#query-hosted-ml-anti-malware-models)
    * [Upload malware ZIP files and check on status](#upload-malware-zip-files-and-check-on-status)
* [Anti-phishing](#anti-phishing)
    * [Query Hosted ML anti-phishing models](#query-hosted-ml-anti-phishing-models)
    * [Upload phishing ZIP files and check on status](#upload-phishing-zip-files-and-check-on-status)

<!-- vscode-markdown-toc-config
	numbering=false
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->
​
## <a name='anti-malware'></a>Anti-malware
### <a name='query-hosted-ml-anti-malware-models'></a>Query Hosted ML anti-malware models
Submit a sample to all hosted ML models, and retrieve a `jobid`
* [ml_submit_sample_all](ml_submit_sample_all.md): `POST https://api.mlsec.io/api/ml_submit_sample_all?api_token={api_token}`
​

Submit a sample to one or more specific ML models, and retrieve a `jobid`
* [ml_submit_sample](ml_submit_sample.md): `POST https://api.mlsec.io/api/ml_submit_sample?api_token={api_token}?model={model1,model2}`

​
Retrieve resuts from sample submission, referenced by `jobid`
* [ml_get_sample](ml_get_sample.md): `GET https://api.mlsec.io/api/ml_get_sample?api_token={api_token}&jobid={jobid}`
​
### <a name='upload-malware-zip-files-and-check-on-status'></a>Upload malware ZIP files and check on status
**Rather than using these API routes, you may submit and view the status of your submission at [https://mlsec.io/zipfile](https://mlsec.io/zipfile/).**
​
Upload a ZIP file containing malware samples, returns a HTML including the ZIP id
* [post_one_zip](post_one_zip.md): `POST https://api.mlsec.io/api/post_one_zip/new/?url=%2Fzipfile%2F&api_token={api_token}`
​

Query specific ZIP status
* [get_one_zip](get_one_zip.md): `GET https://api.mlsec.io/api/get_one_zip/<ID>?api_token={api_token}`
​

It may take several minutes for the status to show that the ZIP is ready.  Each sample must be submitted to each ML model (which counts against your API count on the leaderboard).  Those samples that evade at least one ML models are subsequently detonated in a sandbox to verify functionality of the original sample.  
​
Query status of all samples, optionally provide a ZIP id to query status of samples in one specific ZIP
* [get_all_sample](get_all_sample.md): `GET https://api.mlsec.io/api/get_all_sample/?api_token={api_token}[&zipid=<ZIPID>]`
​

Query status of a specific sample
* [get_one_sample](get_one_sample.md): `GET https://api.mlsec.io/api/get_one_sample/<ID>?api_token={api_token}`
​
​
## <a name='anti-phishing'></a>Anti-phishing
### <a name='query-hosted-ml-anti-phishing-models'></a>Query Hosted ML anti-phishing models 
Submit a sample to all hosted ML models (unlike the antimalware API, this is a blocking call that returns a result immediately without a jobid)
* [phish/ml_submit_sample_all](phish/submit_sample_all.md): `POST https://api.mlsec.io/api/phish/submit_sample_all?api_token={api_token}`
​

Submit a sample to one or more specific ML models (unlike the antimalware API, this is a blocking call that returns a result immediately without a jobid)
* [phish/submit_sample](phish/submit_sample.md): `POST https://api.mlsec.io/api/phish/submit_sample?api_token={api_token}?model={model1,model2}`
​

### <a name='upload-phishing-zip-files-and-check-on-status'></a>Upload phishing ZIP files and check on status
**Rather than using these API routes, you may submit and view the status of your submission at [https://mlsec.io/phishing](https://mlsec.io/phishing/).**
​
Upload a ZIP file containing HTML phishing samples, returns a HTML including the ZIP id
* [phish/post_one_zip](phish/post_one_zip.md): `POST https://api.mlsec.io/api/phish/post_one_zip/new/?url=%2Fzipfile%2F&api_token={api_token}`
​

Query specific phishing ZIP status
* [phish/get_one_zip](phish/get_one_zip.md): `GET https://api.mlsec.io/api/phish/get_one_zip/<ID>?api_token={api_token}`
​

It may take several minutes for the status to show that the ZIP is ready.  Each sample must be submitted to each ML model (which counts against your phishing API count on the leaderboard).   
​
Query status of all samples, optionally provide a ZIP id to query status of samples in one specific ZIP
* [phish/get_all_sample](phish/get_all_sample.md): `GET https://api.mlsec.io/api/phish/get_all_sample/?api_token={api_token}[&zipid=<ZIPID>]`
​

Query status of a specific sample
* [phish/get_one_sample](phish/get_one_sample.md): `GET https://api.mlsec.io/api/phish/get_one_sample/<ID>?api_token={api_token}`