# hugo pangu spacing shortcode
a Hugo shortcode to automatically add spaces between Chinese/Japanese/Korean (CJK) characters and English alphanumeric characters in your Hugo site content. 

This ensures better readability and maintains a consistent typographical appearance. Inspried by [Emacs pangu-spacing mode](https://github.com/coldnew/pangu-spacing).

# Usage
wrap the markdown content (apart from the frontmatter) with the `panguSpacing` shortcode. For example:

```markdown
{{% panguSpacing %}}
This is a text with ひらがな123 and中文字符intermixed.
{{% /panguSpacing %}}
```

This will output the text with appropriate spaces added between CJK and English characters:
```text
This is a text with ひらがな 123 and 中文字符 intermixed.
```

# Installation
To use the Pangu Spacing module in your Hugo site, follow these steps:

## Add the Module to Your Site Configuration:

Add the following lines to your Hugo site's configuration file (config.toml or config.yaml):

For `config.toml`:

```toml
[module]
  [[module.imports]]
    path = "github.com/nohzafk/hugo-pangu-spacing"
```

For `config.yaml`:
```yaml
module:
  imports:
    - path: github.com/nohzafk/hugo-pangu-spacing
```

## Update Your Hugo Modules:

Run the following command to fetch the new module:

```bash
hugo mod get -u github.com/nohzafk/hugo-pangu-spacing
hugo mod tidy
```
