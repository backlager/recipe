# Backlager theory and practice

 > *a drunk man's words are a sober man's thoughts*
 
## Goals

The whole premise is to uncomplicate the mess that is project management
specifically with software development in mind. Project items should be:

 - In a human readable format
 - Low barrier to entry
 - Easily applied to distributed version control systems
 - Not dependent on service (i.e. Github, Gitlab, etc)

## Where to hang your hat

Since the data is all in-house it may be nice to know where the valuables
are.

```
  .brewery
    - config
    - additives/
    - grain/
```

## The basics

Each item may utilize different file format. For example,

 - Markdown
 - YAML
 - TOML
 - Something new we've never even heard of

A file should contain only one unique logical work unit and its contents
contain associated properties and values.
 
### Creating a new item

To add a new work unit create a new file in ```.brewery/grain/```. Feel good?

### Properties

It may seem odd but unit properties are completely optional. All of them.
Some recommended properties may include:

 - title
 - tags
 - ancestors
 - points
 - status
 - assigned
 - created
 - due
 - modified
 - description
 - comments

### Tagging

Another useful, but completely optional, notion is the ability to tag
work units. Think of it as a tool to apply generic categories to anything.
For Agile work you may use tags to describe the unit:

 - feature
 - backlog
 - sprint
 - story
 - task
 - issue

Or maybe your development team prefers tags as assignment:

 - sprint1
 - sprint2
 - release
 - icebox

The point being tags are a nice way to organize the work with minimal effort.

### Defined parental relations

Using a property such as ```ancestors``` it is possible to build the relationships
we all wish we had. For example, a task may have an ancestor to a user story, and
the user story to a sprint, and the sprint to a feature. How things are, or are
not, linked is completely up to each team and may be more rigidly defined by
additional tooling.

## Additives and other artifacts

It is quite normal for projects to associate other content types to work. When
this is necessary simply place the file within the ```.brewery/additives/```
directory. Then it may be referenced in any unit like

```
[my little pony](../additives/rainbow_delight.png)
```

## Configuration

The configuration file is more for tooling but may be a good crash course on
how to read and operate within the project. For example, it may detail acceptable
values for tags, statuses, or pointing systems. It could also inform tools on
what standard to use for time and other metrics.

Another alternative is to use the configuration file as a template detailing
the properties and accepted values so new work units may use it as a guide. Then
creating a new unit would be as simple as

```
cat .brewery/config > .brewery/grain/title.md && $EDITOR .brewery/grain/title.md
```