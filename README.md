# Projects-billboard
Ongoing projects - maintained libraries and research projects

## go-swagger

## go-openapi

A set of libraries to work with OpenAPI.

### testify (active Q1 2026)
A fork of github.com/stretchr/testify (testify/v2) to expose a dependency-free, assertion library with support for generics.

This project pioneereed a few aspects that we want to generalize across our go-openapi repos: doc site, testing patterns, mono-repo releases.

Roadmap:
* v2.4
### strfmt
Types supporting JSON schema and OpenAPI "format" validations.

Roadmap:
1. Remove dependency to the mongodb driver _without_ introducing a breaking change
2. Add integration tests to cover compatibility for mongodb and mysql
Plan for v2: yes.

### swag
A bag of tools that support go-openapi.

Tools of interest (will be reintegrated in go-openapi/core when published:
* JSON adapter
* is float an integer function

Plan for v2: no

### gh-actions (active)

The github actions that support our shared CI workflows.
* install actions
* job handling actions:
  * retrieve mono-repo settings
  * wait for jobs
* bot handling actions:
  * exchange credententials for bot (w/ github app + GPG credentials)
   
### Other repos

Keep maintained and in good shape. Most likely closed to new features: bug fixes & security issues only.

## go-fred-mcp (for now: private / WIP)

A MCP server in go and for go that adds features not present in the other mcp-gopls that I use.

It adds tools to handle in bulk and make amenable to an AI agent large scans such as:
* godoc string linting (typos, godoc conventions, optional: style issues)
* tested by / covered by dependency graphs to help write tests or improve test coverage
* test coverage details

Roadmap:
* test coverage details
* hunspell bindings w/ WASM
* binary releases
* github action integration

## core go-openapi (to reactive Q1 2026)

A WIP project for go-openapi/v2, with a new infrastructure and new concepts to support OAI v3.x, v2, jsonschema draft X.

It comes with a few novel ideas such as an infrastructure to work efficiently with JSON documents, new analyzers, new codegen and codegen testing tools.

## uri

A strict, yet fast URI parser.

Roadmap:
* v1.1
  * add normalizer and windows file path handling
  * add modern hostname validation like in go-openapi/strfmt
  * conversion to standard URL
* v2:
  * breaking: stop using interfaces and return concrete types
  * revamp builder

Rationalize maintenance:
  * reuse go-openapi shared workflows
  * refator tests for readability / lower maintenance
  * perhaps doc site

## go-vcsfetch (wip)

A small yet powerful library to fetch resources over git.
Single file fetch / Clone

## go-experiments

### Transactional rountrip

An experimental transactional gateway
(think: bank transfer, payments),
which works with an embedded NATS server.

The point is to prove transactional
acidity thanks to message protocol only
and not persistence (database / 2PC).

Other than that, it exposes a few interesting details that leverage other micro-service oriented libraries I've built for config management, db migrations...

k8s operated.

## git-janitor (new)

A TUI / headless server (e.g. nvim-like architecture) that performs git assignments of a janitorial nature.
Since this is really a task scheduler, it may be extended to run coding agents and perform smarter tasks.

## benchviz (new)

A CLI to swall benchmark results and produce a page with one or several charts, rendering the results following a configurable scenario (HTML/png).
