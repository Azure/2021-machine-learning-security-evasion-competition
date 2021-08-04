# phish/submit_sample_all
Submit a sample to all hosted ML models to retrieve predicted score for each model.  A model is considered "evaded" when the predicted score is less than `0.5`.

**METHOD**: `POST`

**URL**: `https://api.mlsec.io/api/phish/submit_sample_all`

**PARAMETERS**: 
* `api_token`, obtained from [https://mlsec.io/myuser](https://mlsec.io/myuser/).

## Successful response
**Code**: `200 OK`

**Content**
```json
{
    "n_models": 7,
    "p_mod_00": "{model_00_score}",
    "p_mod_01": "{model_01_score}",
    "p_mod_02": "{model_02_score}",
    "p_mod_03": "{model_03_score}",
    "p_mod_04": "{model_04_score}",
    "p_mod_05": "{model_05_score}",
    "p_mod_06": "{model_06_score}"
}
```


## Example
`curl -X POST https://api.mlsec.io/api/phish/submit_sample_all?api_token=0123456789abcdef0123456789abcdef --data-binary @01.html`

```json
{
    "n_models": 7,
    "p_mod_00": 0.699,
    "p_mod_01": 0.699,
    "p_mod_02": 0.699,
    "p_mod_03": 0.699,
    "p_mod_04": 0.878,
    "p_mod_05": 0.878,
    "p_mod_06": 0.891
}
```

[Back to API](API.md)