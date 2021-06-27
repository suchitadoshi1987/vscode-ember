# vscode-ember

**Note: This extension is experimental and will be migrated to the original [Ember Language Server extension](https://github.com/ember-tooling/vscode-ember) in the future**

This is the VSCode extension to use the [Experimental Ember Language Server](https://github.com/suchitadoshi1987/ember-language-server). 

`Experimental Ember Language Server` is full-featured fork of [Unstable Ember Language Server](https://github.com/lifeart/ember-language-server). It's `stable` and `extremely` power-featured.


All `Ember Language Server` features included.

![preview](preview.gif)

## Features

- Autocomplete (including installed addons and in-repo addons)
  - Components (Curly, Angle Bracket)
  - Component Arguments (if used in template)
  - Services
  - Route/Controller transition functions route names
  - Model names (store methods, model relation definition)
  - Transform names (model definition)
  - Helpers
  - Modifiers
  - Get / Set / ... / Computed macros
  - Local paths in templates (`this...`)
  - Route autocompletion in `link-to`
  - `<LinkTo />` @route argument autocomplete


- Definition providers for (enable features like "Go To Definition" or "Peek Definition"):
  - Components (in Templates)
  - Helpers (in Templates)
  - Modfiers
  - Models
  - Transforms
  - Routes
  - Services
  - Ember-addons imports
  - Component block arguments (`as | name | `)
  - Any local paths (`this...`)

- Lense provider
  - Related Files (tests, styles, templates, etc)

- Component usages
  - Route Templates
  - Component Templates

- ember-template-lint Diagnostics integration (if it is included in a project)
  - Template parsing issues
  - Template linting
  - Template linting inside tests
  - Auto-fix action for fixable linting issues

- Supported layouts
  - Classic 
  - Template Collocation
  - Pods
  - Module Unification

- Supported Script Files
  - JavaScript
  - TypeScript

## Settings

* `els.codeLens.relatedFiles` - disable / enable related files
* `els.local.addons` - globally defined local language server addons entry folders, for example:
   
```js
{
    "els.local.addons": ["C:\\Users\\ember\\els-addon-typed-templates"],
}

```
* `els.local.ignoredProjects` -  Supports Ignoring of LS initialization on unneeded projects, for example, the below setting will ignore the initialization of the project named, `sample-project-name`:

```js
{
    "els.local.ignoredProjects": ["sample-project-name"],
}

```

* `els.local.disableInitialization` -  Disabling eager initialization of projects

```js
{
    "els.local.disableInitialization": true,
}
```

* `els.local.includeModules` - node_modules packages to be included during the lazy init phase for autocomplete.

```js
{
    "els.local.includeModules": ['@foo', '@bar'],
}
```

_Note: `ignoredProjects` leverages the projectName from the `name` property of the project's `package.json`_
