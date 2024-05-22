# Create a Release Tag Action (GHA)

This action(GHA) creates a GitHub release tag.

## Inputs

### `tag_name`

**Required** The name of the tag to create.

### `message`

**Required** The message associated with the tag.

### `tag_exists_error`

Whether to throw an error if the tag already exists. Default is `false`.

## Example usage

```yaml
name: Create a Release Tag

on:  
  push:
    branches:      
      - "live"

jobs:
  create-tag:
    runs-on: ubuntu-latest
    name: Create Tag

    steps:
      - name: Create a Release Tag        
        uses: vishalpatel-73/create-a-release-tag@main
        with:
          tag: "v1.0"
          message: "Latest Live Release"
