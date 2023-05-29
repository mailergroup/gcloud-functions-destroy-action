# gcloud-functions-destroy-action
A GitHub action to delete Google Cloud Functions

# Required Inputs: *

**service_account_key** - A Google service account key that has at least `roles/cloudfunctions.admin` and `roles/iam.serviceAccountUser`.

**project** - The Google account project

**name** - The Cloud Function's name

**region** - The GCP region where Cloud function exists

# Example usage

## HTTP-triggered GCF with VPC connector

``` yaml
- uses: mailergroup/gcloud-functions-destroy-action@main
  with:
    service_account_key: ${{ secrets.GOOGLE_SERVICE_KEY }}
    project: "mailergroup"
    name: "my-cloud-function"
    region: "europe-west1"
```
