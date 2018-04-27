# ir_deploy
Production deployment and documentation for InspectorRestaurant.

This repository includes [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) for the following repositories:

- [ir_web_data](https://github.com/InspectorRestaurant/ir_web_data)

- [ir_web_client](https://github.com/InspectorRestaurant/ir_web_client)

- [ir_web_api](https://github.com/InspectorRestaurant/ir_web_api)

Each repository maintains its own README.md and deployment instructions - please consult each individual repository for development and deploy instructions.

### Updating submodules

1. Run `sh update.sh` - this will pull the latest changes for each repository.

### Documentation

Our project proposal in in the `docs/PROPSAL.md` file. We have also included both our mid-term (`docs/midterm_presentation.pdf`) and final (`docs/final_presentation.pdf`) presentations for review.