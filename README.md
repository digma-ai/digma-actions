# Digma Actions

This repo contains two Github actions:

## digma-ai/digma-actions/instrument 
This action can be used to instrument your Java application using OTEL and send observability data to the Digma Analytics Engine.

### Inputs

### `collector_url`

**Required** URL of the Digma OTEL collector backend.

### `service_name`

**Required** The name of the application being observed.

### `environment`

**Required** The Digma environment name for this execution (e.g 'CI').

## Example usage

```yaml
uses: digma-ai/digma-java-instrumentation-action@v1.0.10
with:
  collector_url: 'http://MY_DIGMA_URL:5050'
  service_name: 'users_service'
  environment: 'load_tests'
```

## digma-ai/digma-actions/assert-no-issues 

This insight can be used to validate there are no dismissed issues currently active in the application integration tests environment

### Inputs

### `digma_url`

**Required** URL of the Digma API

### `api_token`

**Required** API token to access the Digma API

### `environment`

**Required** The Digma environment name for this execution (e.g 'CI').

## Example usage
```yaml
  uses: digma-ai/digma-actions/assert-no-issues@v1.0.10
  with:
    # Assuming the action expects these inputs:
    digma_url: 'https://my.digma.api'
    api_token: ${{ secrets.DIGMA_TOKEN }}
    environment: 'load_tests'
```
