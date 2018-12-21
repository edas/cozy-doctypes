[Table of contents](README.md#table-of-contents)

# Cozy Terms doctype

## `io.cozy.terms`

The `io.cozy.terms` doctype can be used to store some (application related or not) terms seen by the user inside the Cozy. A terms must be unique if this is the same id and the same version (the url can changed), if the id or the version changes, a new document must be created.

- `_id`: The document `_id` must be forced to be a concatenation (joined by `:`) of the terms `id` (slugified, with `*+~.()'"!:@` characters removed) and the `version` (slugified, with `*+~.()'"!:@` characters removed). For example, the terms with the id `My terms:app` and version `terms001` must give `My-termsapp:terms001` as document `_id`.
- `accepted`: (Boolean) The fact that the terms has been accepted by the Cozy user or not
- `acceptedAt`: (Date) The date when the Cozy user accepted these terms
- `termsId`: the id of the terms (`My terms:app` for the last example)
- `url`: The url of the terms (to redirect the Cozy user to if needed)
- `version`: The version of these terms
