# phish/submit_sample
Submit a sample to one or more specific ML models to retrieve predicted score for each model.  A model is considered "evaded" when the predicted score is less than `0.1`.

**METHOD**: `POST`

**URL**: `https://api.mlsec.io/api/phish/submit_sample`

**PARAMETERS**: 
* `api_token`: obtained from [https://mlsec.io/myuser](https://mlsec.io/myuser/)
* `model`: a comma-separated list of model to query, e.g., `model=2,4,5`

## Successful response
**Code**: `200 OK`

**Content**
```json
**Content**
```json
{
    "n_models": 7,
    "p_mod_{id0}": "{model_{id0}_score}"
    ...
}
```
```

## Example
`curl -X POST https://api.mlsec.io/api/phish/submit_sample?api_token=0123456789abcdef0123456789abcdef&model=0,4,6 --data-binary @01.html`

```json
{
    "p_mod_00": 0.699,
    "p_mod_04": 0.878,
    "p_mod_06": 0.891
}
```

[Back to API](API.md)
