Steps

1. Create your application integration with API Trigger
2. Create a service account (SA) with the role of Application Integration Invoker
3. In Apigee X, create a proxy, set the target URL to https://{region}-integrations.googleapis.com/v1/projects/{gcp-project-name}/locations/{region}/integrations/-:execute
4. Add Assign Message policy to the Preflow of the Proxy, to include trigger ID see the example AM-IntegrationRequest.xml
5. Deploy the API Proxy with the SA you created earlier
6. (Optional) Add other policy like Verify API Key / Quota to your Proxy Preflow 