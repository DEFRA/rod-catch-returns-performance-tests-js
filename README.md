# Rod Catch Returns Performance Tests JS

Performance tests for the RCR application using the Artillery JS library.

## Prerequisites

- Node v18.x (see .nvmrc)

It is recommended to use [NVM](https://github.com/nvm-sh/nvm) to manage the node versions.

# Environment variables

| name    | description              | required | default | valid | notes |
| ------- | ------------------------ | -------- | ------- | ----- | ----- |
| WEB_URL | The frontend url to test | yes      | n/a     |       |       |

## Installation

Copy the example environment file and replace the relevant variables.

```shell script
cp .env.example .env
```

Install the project.

```shell script
npm i
```

## Running

This will run the tests and output the results in the console. Make sure the environment is started!

```shell script
npm test
```

## Reporting

To create a report, you first have to run the tests using the command below. This will output a report in JSON format in the reports folder.

```shell script
npm run report:json
```

You then take that JSON report and convert it to a HTML report by running the command.

```shell script
npm run report:html
```

## Contributing to this project

Please read our [contribution guidelines](CONTRIBUTING.md).

## License

THIS INFORMATION IS LICENSED UNDER THE CONDITIONS OF THE OPEN GOVERNMENT LICENCE found at:

http://www.nationalarchives.gov.uk/doc/open-government-licence/version/3

The following attribution statement MUST be cited in your products and applications when using this information.

> Contains public sector information licensed under the Open Government license v3

### About the license

The Open Government Licence (OGL) was developed by the Controller of Her Majesty's Stationery Office (HMSO) to enable information providers in the public sector to license the use and re-use of their information under a common open licence.

It is designed to encourage use and re-use of information freely and flexibly, with only a few conditions.
