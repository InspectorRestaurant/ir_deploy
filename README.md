# ir_deploy
Production deployment and documentation for InspectorRestaurant.

This repository includes [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) for the following repositories:

- [ir_data](https://github.com/InspectorRestaurant/ir_data) | [README]()

- [ir_web_client](https://github.com/InspectorRestaurant/ir_web_client) | [README]()

- [ir_web_api](https://github.com/InspectorRestaurant/ir_web_api) | [README]()

Each repository maintains its own README.md and deployment instructions - please consult each individual repository for development and deploy instructions.

### Updating submodules

1. Run `sh update.sh` - this will pull the latest changes for each repository. Commit and merge the changes to this repository ([ir_deploy](https://github.com/InspectorRestaurant/ir_deploy)).

### Deployment

These are the instructions to deploy the entire Inspector.Restaurant stack. We assume basic knowledge of server provisioning and dependency installation.

1. Provision a server (we use [DigitalOcean](https://www.digitalocean.com/)) running Ubuntu at version `16.04` with the following:
    - [Docker](https://www.docker.com/)
    - [Node.js](https://nodejs.org/)
    - [npm](https://www.npmjs.com/)
    - [nginx](https://www.nginx.com/)

2. Run the deploy instructions in the following submodules (order-specific)
    - `ir_data`
    - `ir_web_api`
    - `ir_web_client`

3. Copy the client build to `/www` with the following commands:
    - `cp ~/ir_deploy/ir_web_client/dist/index.html /www/index.html`
    - `cp -R ~/ir_deploy/ir_web_client/dist/static /www/`

4. Copy `inspector.restaurant.NGINX` to `/etc/nginx/sites-enabled/inspector.restaurant`

5. Run `sudo service restart nginx`

### Documents

This repository contains the following documents:

- Project proposal (`docs/PROPSAL.md`)
  - Objectives
  - Stretch Goals
  - Server Architecture & Supporting Infrastructure
  - Client Architecture & Supporting infrastructure

- Mid-term & final presentations (`docs/*_presentation.pdf`)
  - Team Intro
  - Methodology
  - Problem Statement
  - Solution
  - Architecture
  - Technology
  - Roadmap
  - Status & Progress
  - Challenges
  - Documentation
  - Demo
  - Next Steps

- API documentation is available at [inspector.restaurant/docs]()
