---
layout: default
title: Workspaces
nav_order: 3
description: Structurizr documentation
permalink: /workspaces
---

# Workspaces

In Structurizr, a __workspace__ is the wrapper for your software architecture model, views, and supplementary documentation.

## Workspace scope

One of the most frequently asked questions is, "what should a workspace contain?".
Imagine that you're the engineering manager for a department in your organisation,
and you have three teams each building separate software systems - A, B, and C.

### Software system scoped workspaces

As a starting point, and following the [C4 model definition of a software system](https://c4model.com/#Abstractions),
it's recommended that a workspace contains the model, views, and documentation for a single software system.
Following this recommendation would result in three workspaces, each being owned by the respective teams:

1. Workspace 1 defines the system context, container, component, dynamic, and deployment diagrams, plus documentation and decisions, for software system A.
2. Workspace 2 defines the system context, container, component, dynamic, and deployment diagrams, plus documentation and decisions, for software system B.
3. Workspace 3 defines the system context, container, component, dynamic, and deployment diagrams, plus documentation and decisions, for software system C.

Each of these workspaces is referred to as a "software system scoped workspace" because they describe implementation details related to a individual software system.

### Landscape scoped workspaces

You may additionally wish to create another workspace (workspace 4) that describes the people and software systems in the landscape (e.g. department),
along with the relationships between them, visualised using one or more system landscape diagrams.

This is referred to as a "landscape scoped workspace". Organisations typically build one or more landscape scoped workspaces as "maps of their software systems".
The workspace could be configured so that double-clicking software system A in the system landscape diagram takes you workspace 1, where the details of that software system can be found.

### Unscoped workspaces

It's also possible, particularly for smaller software systems,
to merge all of the diagrams and documentation for a number of software systems into a single workspace.
Or perhaps a single workspace could contain all of the diagrams and documentation for all software systems owned by a single group/department.
These are referred to as "unscoped workspaces".

### Considerations

Creating all of the diagrams and documentation for all of your software systems in a single large workspace is more straightforward, but the end-result will be cluttered.
Distributing the diagrams and documentation across a number of smaller workspaces may better reflect the autonomous nature of teams within your organisation,
but needs some effort with regards to modelling dependencies between teams/software systems.
Structurizr DSL features such as [workspace extension](/dsl/cookbook/workspace-extension/) and [!include](/dsl/includes/) can help.
There are no right or wrong answers here, just trade-offs.
You need to find a level of workspace modularity that works for your team/organisation.