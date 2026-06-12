Here’s a **concise but comprehensive Slack “markdown” (mrkdwn) guide** you can copy/paste for real use.

***

# 🧠 Slack Markdown (mrkdwn) — TL;DR

* Slack **does NOT use standard Markdown**
* It uses a **custom subset called `mrkdwn`** [\[docs.slack.dev\]](https://docs.slack.dev/messaging/formatting-message-text/)
* Biggest differences:
  * `*bold*` (not `**bold**`)
  * `_italic_` (underscores only)
  * `<url|text>` (not `url`)
  * No headings, tables, or images [\[macmdviewer.com\]](https://macmdviewer.com/blog/markdown-in-slack)

***

# ✅ Core Syntax Cheat Sheet

## Text formatting

```text
*bold*
_italic_
~strikethrough~
*_bold italic_*
```

* Single characters only (`*`, `_`, `~`) [\[allmarkdowntools.com\]](https://allmarkdowntools.com/slack-markdown)

***

## Code

```text
`inline code`

```

multi-line code block

```
```

* Triple backticks for blocks
* No syntax highlighting support [\[unmarkdown.com\]](https://unmarkdown.com/blog/slack-formatting-masterclass)

***

## Links

```text
<https://example.com|display text>
<https://example.com>
```

* Standard Markdown links don’t reliably work (except in UI composer auto-conversion) [\[markdownfo...atting.com\]](https://markdownformatting.com/slack)

***

## Mentions & notifications

```text
<@U123456>        // user
<#C123456>        // channel
<!here>           // online users
<!channel>        // channel members
<!everyone>       // workspace
```

 [\[allmarkdowntools.com\]](https://allmarkdowntools.com/slack-markdown)

***

## Lists (basic)

```text
- bullet item
- bullet item

1. numbered item
2. numbered item
```

* Not “true Markdown lists” — just text formatting behavior [\[magicbell.com\]](https://www.magicbell.com/blog/slack-text-formatting)

***

## Quotes

```text
> single line quote

>>> multi-line quote
```

 [\[bing.com\]](https://bing.com/search?q=Slack+message+formatting+documentation)

***

## Line breaks

```text
Line 1\nLine 2   // API

Shift + Enter   // UI
```

 [\[docs.slack.dev\]](https://docs.slack.dev/messaging/formatting-message-text/)

***

## Emoji

```text
:rocket:
:smile:
```

 [\[magicbell.com\]](https://www.magicbell.com/blog/slack-text-formatting)

***

# ⚠️ Key Differences vs Standard Markdown

| Feature       | Standard Markdown | Slack           |
| ------------- | ----------------- | --------------- |
| Bold          | `**text**`        | `*text*`        |
| Italic        | `*text*`          | `_text_`        |
| Strike        | `~~text~~`        | `~text~`        |
| Link          | `url`             | `<url\|text>`   |
| Headings      | `# H1`            | ❌ not supported |
| Tables        | ✅                 | ❌               |
| Images inline | ✅                 | ❌               |

 [\[macmdviewer.com\]](https://macmdviewer.com/blog/markdown-in-slack)

***

# 🧩 Practical Patterns (what you’ll actually use)

## Status update

```text
*Deployment Status:* ✅ Complete
_Service:_ `matchmaking-api`
_Notes:_ No errors observed
```

## Action items

```text
*Action Items*
- Fix auth retry bug
- Validate metrics dashboard
- Schedule rollback test
```

## Alert / incident

```text
<!here> *P1 Incident*
Service: `login-gateway`
Impact: Elevated 500s
Dashboard: <https://grafana|View>
```

***

# 🚫 Unsupported / Gotchas

* ❌ No headings (`#`)
* ❌ No tables
* ❌ No nested formatting (unreliable)
* ❌ No HTML
* ❌ No syntax-highlighted code blocks [\[markdownguide.org\]](https://www.markdownguide.org/tools/slack/)

***

# 🧭 Mental model (helps avoid mistakes)

Think of Slack formatting as:

> “Chat-friendly formatting with a Markdown-like *skin*, not a document language.”
