# Mermaid
[![Build Status](https://travis-ci.org/mermaid-js/mermaid.svg?branch=master)](https://travis-ci.org/mermaid-js/mermaid) [![NPM](https://img.shields.io/npm/v/mermaid)](https://www.npmjs.com/package/mermaid) [![Coverage Status](https://coveralls.io/repos/github/mermaid-js/mermaid/badge.svg?branch=master)](https://coveralls.io/github/mermaid-js/mermaid?branch=master) [![Join our Slack!](https://img.shields.io/static/v1?message=join%20chat&color=9cf&logo=slack&label=slack)](https://join.slack.com/t/mermaid-talk/shared_invite/enQtNzc4NDIyNzk4OTAyLWVhYjQxOTI2OTg4YmE1ZmJkY2Y4MTU3ODliYmIwOTY3NDJlYjA0YjIyZTdkMDMyZTUwOGI0NjEzYmEwODcwOTE) [![This project is using Percy.io for visual regression testing.](https://percy.io/static/images/percy-badge.svg)](https://percy.io/Mermaid/mermaid)

![banner](./img/header.png)
**Edit this Page** [![N|Solid](./img/GitHub-Mark-32px.png)](https://github.com/mermaid-js/mermaid/blob/develop/docs/README.md)

:trophy: **Mermaid was nominated and won the [JS Open Source Awards (2019)](https://osawards.com/javascript/#nominees) in the category "The most exciting use of technology"!!!**

**Thanks to all involved, people committing pull requests, people answering questions and special thanks to Tyler Long who is helping me maintain the project 🙏**

## About

<!-- <Main description> -->
Mermaid is a Javascript based diagramming and charting tool that uses Markdown-inspired text definitions and a renderer to create and modify complex diagrams.  The main purpose of Mermaid is to help documentation catch up with development.

> Doc-Rot is a Catch-22 that Mermaid helps to solve.

Diagramming and documentation costs precious developer time and gets outdated quickly.
But not having diagrams or docs ruins productivity and hurts organizational learning. <br/>
Mermaid addresses this problem by cutting the time, effort and tooling that is required to create modifiable diagrams and charts, for smarter and more reusable content.
The text definitions for Mermaid diagrams allows for it to be updated easily, it can also be made part of production scripts (and other pieces of code).
So less time needs be spent on documenting, as a separate and laborious task. <br/>

Even non-programmers can create diagrams through the [Mermaid Live Editor](https://github.com/mermaidjs/mermaid-live-editor), visit [Mermaid Overview](./n00b-overview.md) for the video tutorials.

Want to see what can be built with mermaid, or what applications already support it? Read the [Integrations and Usages for Mermaid](./integrations.md).

For a more detailed introduction to Mermaid and some of it's more basic uses, look to the [Beginner's Guide](./n00b-overview.md) and [Usage](./usage.md).

🌐 [CDN](https://unpkg.com/mermaid/) | 📖 [Documentation](https://mermaidjs.github.io) | 🙌 [Contribution](https://github.com/mermaid-js/mermaid/blob/develop/CONTRIBUTING.md) | 📜 [Version Log](./versionUpdates.md)

> 🖖 Keep a steady pulse: mermaid needs more Collaborators, [Read More](https://github.com/knsv/mermaid/issues/866).

## Diagrams

### [Flowchart](https://mermaid-js.github.io/mermaid/#/flowchart)

```
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

![Flowchart](./img/flow.png)

### [Sequence diagram](https://mermaid-js.github.io/mermaid/#/sequenceDiagram)

```
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

![Sequence diagram](./img/sequence.png)

### [Gantt diagram](https://mermaid-js.github.io/mermaid/#/gantt)

```
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d
```

![Gantt diagram](./img/gantt.png)

### [Class diagram - :exclamation: experimental](https://mermaid-js.github.io/mermaid/#/classDiagram)

```
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

![Class diagram](./img/class.png)

### Git graph - :exclamation: experimental

```
gitGraph:
options
{
    "nodeSpacing": 150,
    "nodeRadius": 10
}
end
commit
branch newbranch
checkout newbranch
commit
commit
checkout master
commit
commit
merge newbranch

```
![Git graph](./img/git.png)

### [Entity Relationship Diagram - :exclamation: experimental](https://mermaid-js.github.io/mermaid/#/entityRelationshipDiagram)

```
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses

```

![ER diagram](./img/simple-er.png)

### [User Journey Diagram](https://mermaid-js.github.io/mermaid/#/user-journey)

```markdown
journey
    title My working day
    section Go to work
      Make tea: 5: Me
      Go upstairs: 3: Me
      Do work: 1: Me, Cat
    section Go home
      Go downstairs: 5: Me
      Sit down: 5: Me
```
![Journey diagram](./img/user-journey.png)

## Installation

In depth guides and examples can be found in [Getting Started](./n00b-gettingStarted.md) and [Usage](./usage.md).
To learn more about Mermaid's Syntax, please read the [Syntax Reference](./n00b-syntaxReference.md).

### CDN

You can get Mermaid from [unpkg](https://unpkg.com/) or [jsDelivr](https://www.jsdelivr.com/):

- https://unpkg.com/mermaid@8.7.0/dist/mermaid.min.js
- https://cdn.jsdelivr.net/npm/mermaid@8.7.0/dist/mermaid.min.js

The latest version is 8.7.0.

### Install Mermaid

You can use `npm` to install Mermaid as a dependency in your JavaScript project:

1. You will need to install the current stable version of Node (which include `npm`)
2. Open a terminal, and type the following command:

        $ npm i mermaid --save

**TIP:** If you want to install Mermaid as a development dependency, you can replace `--save` by `--save-dev`:

    $ npm i mermaid --save-dev


**NOTE:** If you are more familiar with Yarn, you can use the following command:

    $ yarn add --dev mermaid

### Usage

The easiest way to add Mermaid on your website is to add the following code:

```html
<script src="https://cdn.jsdelivr.net/npm/mermaid@8.7.0/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true})</script>
```

`mermaid.initialize({startOnLoad:true})` will read diagram/chart definitions from all the `<div>` elements that have the `mermaid` class and render them as SVG.

Examples can be found in [Getting Started](./n00b-gettingStarted.md)

## Sibling projects

- [mermaid live editor](https://github.com/mermaidjs/mermaid-live-editor)
- [mermaid CLI](https://github.com/mermaidjs/mermaid.cli)
- [mermaid webpack demo](https://github.com/mermaidjs/mermaid-webpack-demo)
- [mermaid Parcel demo](https://github.com/mermaidjs/mermaid-parcel-demo)

## Request for assistance

Things are piling up and I have a hard time keeping up. To remedy this
it would be great if we could form a core team of developers to cooperate
with the future development of mermaid.

As part of this team you would get write access to the repository and would
represent the project when answering questions and issues.

Together we could continue the work with things like:

- Adding more types of diagrams like mindmaps, ert diagrams, etc.
- Improving existing diagrams

Don't hesitate to contact me if you want to get involved.

## Credits

Many thanks to the [d3](http://d3js.org/) and [dagre-d3](https://github.com/cpettitt/dagre-d3) projects for providing the graphical layout and drawing libraries!

Thanks also to the [js-sequence-diagram](http://bramp.github.io/js-sequence-diagrams) project for usage of the grammar for the sequence diagrams. Thanks to Jessica Peter for inspiration and starting point for gantt rendering.

_Mermaid was created by Knut Sveidqvist for easier documentation._

_[Tyler Long](https://github.com/tylerlong) has became a collaborator since April 2017._

Here is the full list of the projects [contributors](https://github.com/knsv/mermaid/graphs/contributors).
