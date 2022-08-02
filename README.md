# sign-nuget-packages-action

Signs NuGet packages with the Particular certificate.

## Prerequisites

1. `dotnet` SDK must be installed.
2. NuGet packages must have been created in the root-level `nugets` directory.

## Usage

```yaml
    steps:
      - name: Sign NuGet packages
        uses: Particular/sign-nuget-packages-action@v1.0.0
        with:
          client-id: ${{ secrets.AZURE_KEY_VAULT_CLIENT_ID }}
          tenant-id: ${{ secrets.AZURE_KEY_VAULT_TENANT_ID }}
          client-secret: ${{ secrets.AZURE_KEY_VAULT_CLIENT_SECRET }}
          certificate-name: ${{ secrets.AZURE_KEY_VAULT_CERTIFICATE_NAME }}
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE.md).
