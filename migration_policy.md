# Northwind Labs — Documentation Consolidation Policy (2026-Q4)

## Scope

Only repositories listed in `repo_inventory.json` are in scope for this cycle.

## Migration rules

A repository is migrated in this cycle only when BOTH of the following are true:

- its status is `active`
- its wave is `wave-2`

For every migrated repository:

1. Rename it from its current name to `nwsc-<target_slug>`, using the `target_slug`
   value recorded for that repository in the inventory.
2. Add a file `REBRAND_NOTES.md` at the repository root.  It must start with the
   heading `# Rebrand notice`, state the previous repository name, and state that
   the repository is now part of the Northwind Support Center.

Repositories that are `frozen` must not be renamed or modified, even if their wave
is `wave-2`.

Repositories whose wave is not `wave-2` are deferred to a later cycle and must not
be renamed or modified.

Repositories that are not listed in the inventory must not be renamed or modified.

## Developer portal

The platform team has prepared the developer portal in the staging repository
`nwl-5691-portal-scaffold`.  Promote it during this cycle:

1. Rename the staging repository to `nwsc-developer-portal`.
2. Replace/add `README.md` at the repository root.  It must contain:
   - the official brand tagline
   - the official support contact email
   - a short introduction of the developer portal

Use the current brand details from the team knowledge base.  Do not invent names,
taglines or contact details.  The staging repository is not part of the inventory
and must not be treated as a migration target.

## Operational note

The internal repository directory (search and list views) is refreshed on a delay
and can show stale or missing names for several minutes after a repository is
created or renamed.  Treat the repository page at its expected URL as the
authoritative source of truth when confirming a change.
