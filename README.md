# Zitadel Resource Provider

The Zitadel Resource Provider lets you manage [Zitadel](https://zitadel.com/) resources.

This is a fork of [pulumiverse/pulumi-zitadel](https://github.com/pulumiverse/pulumi-zitadel) that bridges
[terraform-provider-zitadel](https://github.com/zitadel/terraform-provider-zitadel) v3.8.7. The Node.js SDK is
named `@studio-vaai/pulumi-zitadel`. It and the provider plugin are attached to this repository's
[GitHub releases](https://github.com/studio-vaai/pulumi-zitadel/releases); neither is published to a package
registry. The other SDKs keep their upstream package names and are not released from this fork.

## Installing

This package is available for several languages/platforms:

### Node.js (JavaScript/TypeScript)

To use from JavaScript or TypeScript in Node.js, install the SDK from a release, for example with `npm`:

```bash
npm install https://github.com/studio-vaai/pulumi-zitadel/releases/download/v0.3.0/studio-vaai-pulumi-zitadel-0.3.0.tgz
```

Pulumi downloads the matching provider plugin from the same release on first use.

### Python

To use from Python, install using `pip`:

```bash
pip install pulumi_zitadel
```

### Go

To use from Go, use `go get` to grab the latest version of the library:

```bash
go get github.com/pulumiverse/pulumi-zitadel/sdk/go/...
```

### .NET

To use from .NET, install using `dotnet add package`:

```bash
dotnet add package Pulumiverse.Zitadel
```

## Configuration

The following configuration points are available for the `zitadel` provider:

- `zitadel:domain` - domain used to connect to the ZITADEL instance
- `zitadel:port` - used port if not the default ports 80 or 443 are configured
- `zitadel:insecure` - use insecure connection
- `zitadel:insecureSkipVerifyTls` - disable TLS certificate verification
- `zitadel:accessToken` - personal access token to connect to ZITADEL
- `zitadel:jwtFile` - path to the file containing a presigned JWT to connect to ZITADEL
- `zitadel:jwtProfileFile` - path to the file containing credentials to connect to ZITADEL
- `zitadel:jwtProfileJson` - JSON value of credentials to connect to ZITADEL
- `zitadel:systemApi` - authenticate against the ZITADEL System API with a PEM encoded key
- `zitadel:transportHeaders` - custom headers to add to the requests sent to ZITADEL
- `zitadel:token` - deprecated, use `zitadel:jwtProfileFile` or `zitadel:accessToken`

Exactly one of `accessToken`, `jwtFile`, `jwtProfileFile`, `jwtProfileJson`, `systemApi` or `token` is required.

## Reference

For detailed reference documentation, please visit [the Pulumi registry](https://www.pulumi.com/registry/packages/zitadel/api-docs/).
