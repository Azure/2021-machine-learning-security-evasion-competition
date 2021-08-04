# ml_submit_sample_all
Submit a sample to all hosted ML models, and retrieve a `jobid`

**METHOD**: `POST`

**URL**: `https://api.mlsec.io/api/ml_submit_sample_all`

**PARAMETERS**: 
* `api_token`, obtained from [https://mlsec.io/myuser](https://mlsec.io/myuser/).

## Successful response
**Code**: `200 OK`

**Content**
```json
{
    "jobid": "{jobid}"
}
```


## Example
`curl -X POST https://api.mlsec.io/api/ml_submit_sample?api_token=0123456789abcdef0123456789abcdef --data-binary @random.dll`

```json
{
    "jobid": "1807ebb852e30fbf8b89529dbe76c35d2349822adae073aae12e0d47db5e3fee"
}
```


[Back to API](API.md)