[![TechDocs status](https://github.com/bcgov/efv-itk-docs/actions/workflows/publish.yaml/badge.svg)](https://github.com/bcgov/efv-itk-docs/actions/workflows/publish.yaml)

# Eligibility Factor Verification documentation

This repository contains the DevHub TechDocs for Eligibility Factor Verification
(EFV), a Connected Services capability. The documentation provides orientation
and guidance on when EFV may be useful, how eligibility factors are assessed,
and where teams can go next.

## About EFV

Eligibility Factor Verification is the administrative process of confirming
that information supplied by an applicant is accurate and meets the rules for a
government benefit or service. It is intended for deterministic checks against
trusted, authoritative sources, such as income thresholds, residency, identity,
or program enrolment.

The documentation is intended for developers, solution architects, product
owners, program and policy teams, adjudicators, and intake staff involved in
designing or operating eligibility services.

## Repository structure

- `docs/` contains the documentation pages. `docs/index.md` is the site home
  page and must remain present.
- `mkdocs.yml` configures the site name, navigation, and MkDocs extensions.
- `catalog-info.yaml` registers the documentation in the DevHub software
  catalogue.
- `.github/workflows/publish.yaml` validates and publishes the TechDocs site.

## Writing documentation

Add Markdown files under `docs/`, then add each page to the `nav` section of
`mkdocs.yml` in the order it should appear. Use one level-one heading (`#`) per
page and use relative links between documentation pages.

See the [MkDocs writing guide](https://www.mkdocs.org/user-guide/writing-your-docs/)
for Markdown and navigation details. DevHub uses the `techdocs-core` plugin, so
some MkDocs features or third-party plugins may not be available.

## Previewing locally

Follow the DevHub publisher's
[local preview instructions](https://github.com/bcgov/devhub-techdocs-publish/blob/main/docs/index.md#how-to-use-the-docker-image-to-preview-content-locally)
to build and view the site before submitting a pull request.

## Validation and publishing

The GitHub Actions workflow:

- validates documentation changes on pull requests without publishing them;
- publishes the `test` branch to the DevHub development environment;
- publishes the `main` branch to the DevHub production and development
  environments; and
- supports a manual run that targets either development or production.

Publishing requires the repository's DevHub S3 secrets to be configured. For
help with publishing, contact the
[Developer Experience team](mailto:Developer.Experience@gov.bc.ca).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request. All
participants must follow the [Code of Conduct](CODE_OF_CONDUCT.md).
