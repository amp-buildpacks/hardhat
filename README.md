# `ghcr.io/amp-buildpacks/hardhat`

A Cloud Native Buildpack that provides the Hardhat Tool Suite

## Configuration

| Environment Variable      | Description                                                                                                                                                                                                                                                                                       |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `$BP_ENABLE_HARDHAT_PROCESS`    | Configure the Hardhat launch process, default: `false`. Set to `true` means execute the `npm start` command.   |


## Usage

### 1. To use this buildpack, simply run:

```shell
pack build <image-name> \
    --path <hardhat-samples-path> \
    --buildpack ghcr.io/amp-buildpacks/hardhat \
    --builder cnbs/sample-builder:jammy
```

For example:

```shell
pack build hardhat-sample \
    --path ./samples/solidity/hardhat \
    --buildpack ghcr.io/amp-buildpacks/hardhat \
    --builder cnbs/sample-builder:jammy
```

### 2. To run the image, simply run:

```shell
docker run -it <image-name>
```

For example:

```shell
docker run -it hardhat-sample
```

## Contributing

If anything feels off, or if you feel that some functionality is missing, please
check out the [contributing
page](https://docs.amphitheatre.app/contributing/). There you will find
instructions for sharing your feedback, building the tool locally, and
submitting pull requests to the project.

## License

Copyright (c) The Amphitheatre Authors. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits

Heavily inspired by https://buildpacks.io/docs/buildpack-author-guide/create-buildpack/
