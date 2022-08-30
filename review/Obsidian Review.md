# Overview of Github + Obsidian  (or GitHub++) 
## Introduction
#Obsidian is a powerful **knowledge base** on top of  
a **local folder** of plain text Markdown files.
## Searchability
Search is a #powerful feature, and has the potential to be confusing. In most cases, if you just type what you want to find, it will work. But search has many capabilities for narrowing down to find exactly what you want.
- You can invoke search by pressing `Ctrl-Shift-F` or `Cmd-Shift-F`. You can also customize this hotkey in Settings => Hotkeys. When search is invoked, focus will be automatically put in the search bar so you can start typing your query right away.
## Search Settings

There are a couple of toggles available while searching:

-   `Match case` toggle case sensitive matching, but note that it can be overridden on a per-search basis using the `match-case:` and `ignore-case:` operators explained above.
-   `Explain search term` will show you what the search query actually does in plain terms.
-   `Collapse results` will toggle between just showing matching note names and showing the lines in which matches appear. These extended results can be toggled for each note by clicking on the folding triangle next to the file name.
-   `Show more context` will expand the display of the matches to show more text around the match.
-   `Change sort order` sorts the results by various orders, similar to how files are sorted in the [File explorer](https://help.obsidian.md/Plugins/File+explorer).
## Summary 
Search if understood is quite powerful and fast as you are not making a request but searching local files
## Ownership Constraint
- I imagine it would be the same constraints as we have on Github now
	- It would be possible to setup a workspace for docs and have a 'public and private section'
## Summary 
Not defined by the tool, so won't be rating.

## Cross Domain collaboration (MRD, SUP, TAL)
- collaboration with Mr D and Superbalist would be based on their access to the takealot GitHub workspace. 
## Business viewer access
- as there is no cost implication, business documents can continue to live in Google Drive
- anything that is a markdown file would be rendered on Github with 'readonly' access.

## Markdown support
- Markdown and mermaid are both supported
``` mermaid
pie title Users
"Mobile": 55.9
"Desktop": 40.9
"Tablet": 4
```
## Interoperability with other tools: Specially Slack, Lucidcharts, JIRA, giphy, emojis, Looker, etc
- What Github has, Obsidian at present doesn't have interoperability outside of what markdown offers😅

## Structural Templating
This is done by enabling a plugin and having a templates folder and can either be used to add snippets or an entire document structure.
There are also plugins to extend the templating functionality should you wish to go that route

## Workflow specification (approvals, todo stages, comments, creation of refresh alerts)

-   All workflow related tasks would have to be done with Github + Templating (to insert things like status, last updated, etc)
## Environment (Cloud vs in-House)
-   Local file system.
## History logs and recover data

-   Relying on Github again for this one. It is however an established and trusted process.

## Usability

- Design focuses on 'Zen mode experience' no UI - only editing, you can add more functionality and with plugins
-   depending on your use-case 
	- just editing how-to's: Easy
	- creating a graph view and setup + learing all the keyboard shortcuts: Medium to Hard
- Can use a theme you are comfortable with without being tied in to a 'system theme'
- How to guides and a demo vault to get you started
- Offline editing 
- etc.
- Plugins for those that want them.
- Backticks [[2022-08-29]] (linking to other files)
> [!Info]
> Call out blocks are also supported
> 

## Usage of MD or standard wiki languages

- Obsidian is strictly MD
- How does a code block look
```python
import pytest
import requests
from dotmap import DotMap
from setup.helper import import_file
from setup.error_messages import ErrorMessages
from setup.pretty_print import pretty_print_response


@pytest.mark.regression
    def test_patch_sku_validations_duplicate_sku(self):
        """
        PATCH /v2/offers/offer/SKU{identifier}
        - it returns an appropriate error when the sku is a duplicate
        - it returns an appropriate error code
        - it returns a status code of 200
        """
        request_json = {"sku": "mehmehmeh"}
        response = requests.patch(
            f'{self.base_url}/v2/offers/offer/SKUtest4122', json=request_json, headers=self.h, verify=False
        )
        response_message = response.json()
        error_message = DotMap(ErrorMessages.patch_offers).duplicate_sku
        assert response.status_code == 200,  f'Actual status code{response.status_code}'
        assert DotMap(response_message).validation_errors[1].code == 'E10'
        assert DotMap(
            response_message).validation_errors[1].message == error_message


```

## Maintainability
- Folders can become overcrowded with templates and docs as more people use the tool. Would be good to have a PR process in place.
## Hierarchy structure

-  Folder Structure, it is not prescriptive


## Additional Features
- Github has a fuzzy finder (press t)
- Add the chrome extension Octotree to view a fileviewer to Github
- see more here: https://github.blog/2020-04-09-github-protips-tips-tricks-hacks-and-secrets-from-lee-reilly/

## Final Notes
Don't like obsidian, use any IDE or editor (even vim) since it is just a git repo of markdown files
Should we want to migrate  it should be relatively easy (if time consuming)