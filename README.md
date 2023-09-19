# Composite GitHub Action

This action copies a file from a URL and sets environment variables.

## Inputs

### `collector_url`

**Required** URL of the Digma OTEL collector backend.

### `service_name`

**Required** The name of the application being observed.

### `environment`

**Required** The Digma environment name for this execution (e.g 'CI').

## Example usage

```yaml
uses: digma-ai/digma-java-instrumentation-action@v1.0.0
with:
  collector_url: 'http://MY_DIGMA_URL:5050'
  service_name: 'users_service'
  environment: 'load_tests'
