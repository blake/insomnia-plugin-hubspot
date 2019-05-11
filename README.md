# insomnia-plugin-hubspot

HubSpot HTTP API request signing for Insomnia.

## Installation

Install `insomnia-plugin-hubspot` plugin from Preferences > Plugins.

## Usage

Configure your HubSpot secret and desired request signature type under the
`hubspot` environment variable.

```json
{
    "hubspot": {
        "secret": "[YOUR API SECRET]",
        "signatureType": "[OPTIONAL: <application/webhook>]"
    }
}
```

Note: `signatureType` defaults to 'application' if not specified.

Insomnia will automatically generate and append an `X-HubSpot-Signature` header
to the outgoing request for configured signature type.

The signature type can be overridden on a per-request basis by manually
configuring the `X-HubSpot-Signature` header, and selecting the template tag for
the desired HubSpot signature type (application or webhook).

## Request Signature formats

For more information on HubSpot's Webhook API request signatures, see
[Webhooks Overview - Security](https://developers.hubspot.com/docs/methods/webhooks/webhooks-overview#security).

For application request signatures, see [Validating requests from HubSpot](https://developers.hubspot.com/docs/faq/validating-requests-from-hubspot).
