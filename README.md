# SimpleVerifier API: OpenAPI spec, Postman and Insomnia collections

Ready-made files for the [SimpleVerifier](https://simpleverifier.com) REST API: verify an email address (syntax, domain, disposable and live SMTP mailbox check) or validate a phone number's format.

| File | Use it for |
| --- | --- |
| `openapi.json` | OpenAPI 3 spec. Generate a client, import into any API tool. Also at https://simpleverifier.com/openapi.json |
| `simpleverifier.postman_collection.json` | Postman: **Import**, then set the `apiKey` collection variable |
| `simpleverifier.insomnia.json` | Insomnia: **Create > Import**, then set `apiKey` in the base environment |

Create a key at https://simpleverifier.com/api-keys (keys start with `sv_live_`). API access comes with the Pro, Business and Agency plans. Never commit a filled-in key.

- `valid` means the recipient's mail server confirmed the mailbox. `risky` means delivery could not be confirmed. `invalid` means it will bounce or is a throwaway address.
- The phone endpoint checks format and numbering-plan line type. It never confirms that a number is in service.
- 120 calls a minute per key; `429` carries `Retry-After`.

Docs: https://simpleverifier.com/docs/api · Errors: https://simpleverifier.com/docs/errors

## License

MIT
