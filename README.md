# Getting Started

Welcome to the test project for testing shared hana cloud instances.

used [Blog Entry](https://community.sap.com/t5/technology-blogs-by-members/sharing-sap-hana-cloud-instance-to-multiple-subaccounts-and-creating-hdi/ba-p/13640781).

Most changes were done here: [mta.yaml](mta.yaml)

It contains these folders and files, following our recommended project layout:

File or Folder | Purpose
---------|----------
`db/` | your domain models and data go here
`srv/` | your service models and code go here
`package.json` | project metadata and configuration
`readme.md` | this getting started guide

Authentication is mocked ([guide](https://community.sap.com/t5/technology-q-a/error-authentication-kind-quot-jwt-quot-configured-but-no-xsuaa-instance/qaq-p/13615566)) --> after running this app, switch it off


## Next Steps

- Open a new terminal and run `cds watch`
- (in VS Code simply choose _**Terminal** > Run Task > cds watch_)
- Start adding content, for example, a [db/schema.cds](db/schema.cds).


## Manual Deployment to CF

In terminal, e.g. in BAS:

npx mbt build --mtar app.mtar

cf api https://api.cf.euXX-XXX.hana.ondemand.com
cf login ...
cf deploy mta_archives/app.mtar -f

Then you can find the app here:

<base url>/odata/v4/catalog/Books

## Learn More

Learn more at https://cap.cloud.sap/docs/get-started/.
