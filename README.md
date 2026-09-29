# Agentic SDLC at Tricentis

A presentation by David Maltby, written entirely as Markdown "slides" and viewed through GitHub's Markdown rendering.

## [▶ Start the presentation](01-title.md)

---

## How this presentation works

These are the conventions for maintaining the deck. Anyone editing it, person or AI agent, should follow them.

### One file per slide

- Each slide is a single Markdown file at the repo root.
- Keep a slide to roughly one screen of content. If it needs scrolling, split it into two slides.
- This `README.md` is the entry point, not a slide.

### File naming

- Name files `NN-short-slug.md`, for example `01-title.md` or `02-agenda.md`.
- `NN` is a zero-padded, two-digit sequence number, so the files sort in presentation order in File Explorer and on GitHub.
- The slug is lowercase and hyphenated, and briefly describes the slide.

### Navigation links

Every slide ends with a horizontal rule followed by its navigation links:

```markdown
---

[← Back](01-title.md) | [Next →](03-next-slide.md)
```

- The first slide has only **Next →**.
- The last slide has only **← Back**.
- Links are relative filenames, so they work both on GitHub and in a local Markdown previewer.

### Speaker notes and placeholders

- Speaker notes go in an HTML comment (`<!-- ... -->`) after the navigation links. GitHub doesn't render comments, so the notes stay off the slide.
- Mark unfinished content with a `TODO-<TOPIC>` comment, for example `TODO-SURVEY`, so it's easy to find with a search.

### Adding, inserting, or removing slides

- **Adding at the end:** Create the new file with a **← Back** link, then add a **Next →** link to the slide that was previously last.
- **Inserting in the middle:** Renumber every later file to keep the sequence contiguous, then update the Back/Next links on the new slide and on both of its neighbours.
- **Removing a slide:** Renumber the files that follow it, then relink the two slides on either side of the gap.
- **Check:** After any change, confirm that no link points to a file that doesn't exist.

### Title slide

The title slide (`01-title.md`) shows the presentation title, the presenter's name, and the presentation date written as *Month D, YYYY*, followed by a short "What is the Agentic SDLC?" introduction.
