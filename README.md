# OBDX OAS DEFINITION

This project aims to provide a Open Api Specification (OAS) for the [obdx-backend](https://github.com/txomin55/obdx-backend) Java project.

## Technical specs

The OAS definition is provided by [Apidog](https://app.apidog.com/project/1189506) and it's syncronized with this repo, whenever a change is made, a branch is created with the new OAS spec.

### Pipeline

Whenever a branch is merged in master branch, the deploy job will download the [obdx-oas-generator-archetype](https://github.com/txomin55/obdx-oas-generator-archetype) archetype and will generate and publish the new spec [stub](https://gitlab.com/txominsirera/dog-trainer-pack/-/packages).

## Integration

The Integration between the [consumer](https://github.com/txomin55/obdx-frontend) and the [provider](https://github.com/txomin55/obdx-backend) should be done following the expand and contract pattern, so the consumer will use the [Apidog](https://app.apidog.com/project/1189506) mocked endpoints while the provider implements real endpoints, once its done, the API url can be updated to that one. 
