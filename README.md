# Cloud Foundry Multi CUPS (Create User Provided Service) Plugin

*cf plugin for creating or updating multiple user provided services*

## Installation

Download the latest version from the [releases][releases] page and make it executable.

```
$ go build path/to/downloaded/cf_multi_cups.go
$ cf install-plugin path/to/generated/binary
```

[releases]: https://github.com/18f/releases

## Usage

```
$ cf multi-cups-plugin -p path/to/servicesfile.json
```

The json should be in an array of objects with the key of "name" as the service name and the "credentials" key being an object with a series of keys that are any valid json.

### Example
```
[
  {
    "name": "servicename1",
    "credentials": {
  	"key1": "anytype",
  	"key2": "anytype"
  	}
  },
  {
    "name":"servicename1",
    "credentials" : {
          "key3": "anytype",
          "key4": "anytype"
  }
]
```

## Contributing

See [CONTRIBUTING](CONTRIBUTING.md) for additional information.

## Public domain
This project is in the worldwide [public domain](LICENSE.md). As stated in [CONTRIBUTING](CONTRIBUTING.md):

> This project is in the public domain within the United States, and copyright and related rights in the work worldwide are waived through the [CC0 1.0 Universal public domain dedication](https://creativecommons.org/publicdomain/zero/1.0/).
>
> All contributions to this project will be released under the CC0 dedication. By submitting a pull request, you are agreeing to comply with this waiver of copyright interest.
