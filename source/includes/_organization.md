# Organization

## Fetching all organizations

```shell
$ http http://propeller-api.dev.cbsivideo.com/v1/organization
```

> The above command returns JSON structured like this:

```json
[
    {
        "channel_ids": [],
        "created_at": "2019-04-12 03:43:50.341151+00:00",
        "id": "techrf416",
        "logo_url": "http://propeller.cbsivideo.com/logos/techrepublic.png",
        "name": "TechRepublic",
        "owner": "flavio.ribeiro@cbsinteractive.com"
    },
    {
        "channel_ids": [],
        "created_at": "2019-04-12 03:41:50.018472+00:00",
        "id": "cbscd3fb",
        "logo_url": "http://propeller.cbsivideo.com/logos/allaccess.png",
        "name": "CBS.com All-Access",
        "owner": "flavio.ribeiro@cbsinteractive.com"
    }
]
```

This endpoint retrieves a list of organizations.

### HTTP Request

`GET /v1/organization`

## Getting one organization

```shell
$ http http://propeller-api.dev.cbsivideo.com/v1/organization/cbsi679d
```

> The above command returns JSON structured like this:

```json
{
    "channel_ids": [
        "airspdfah",
        "airsphc20"
    ],
    "created_at": "2019-04-12 03:45:50.631469+00:00",
    "id": "cbsi679d",
    "logo_url": "http://propeller.cbsivideo.com/logos/vtg.png",
    "name": "CBSi VTG",
    "owner": "flavio.ribeiro@cbsinteractive.com"
}
```

Returns the [organization](#organization), together with a list of associated [channel_ids](#channel).

`GET /v1/organization/:id`

### Response Structure

| Attribute     | Description                                                     |
| ------------- | ----------------------------------------------------------------|
| `id`          | Organization id                                                 |
| `created_at`  | Date and time for organization creation                         |
| `logo_url`    | Organization logo url                                           |
| `owner`       | Organization owner/responsible e-mail                           |
| `name`        | Organization name                                               |
| `channel_ids`  | List of [channel_ids](#channel) associated to the organization |