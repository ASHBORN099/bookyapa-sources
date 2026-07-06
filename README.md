# Bookyapa Sources

Remote source repository for the [Bookyapa](https://github.com/ASHBORN099/BOOKYAPA) book reader app.

## How to use

1. Open Bookyapa app
2. Go to **Settings → Source Repositories**
3. Tap the **+** button
4. Enter this URL:
   ```
   https://raw.githubusercontent.com/ASHBORN099/bookyapa-sources/main/sources_repo.json
   ```
5. Go to **Explore → Catalog** tab
6. Tap **Add** on any source to install it

## Available Sources

| Source | Description |
|--------|-------------|
| **FanFiction.net** | The largest fan fiction archive |
| **Archive of Our Own** | Fanfiction, fanart, and more by the OTW |

## Adding your own sources

Edit `sources_repo.json` and add a new entry to the `sources` array. Each source needs:

- `id` — unique identifier
- `name` — display name
- `baseUrl` — site URL
- `lang` — language code
- `description` — short description
- `config` — CSS selectors for scraping (see below)

### Config fields

| Field | Purpose |
|-------|---------|
| `searchUrlPattern` | Search URL with `{query}` placeholder |
| `searchResultContainer` | CSS selector for search result items |
| `searchResultTitle` | CSS selector for title within each result |
| `searchResultLink` | CSS selector for link within each result |
| `searchResultCover` | CSS selector for cover image |
| `searchResultAuthor` | CSS selector for author name |
| `exploreUrlPattern` | Browse/explore URL |
| `bookTitle` | CSS selector on book detail page |
| `bookAuthor` | CSS selector for author on detail page |
| `bookCover` | CSS selector for cover on detail page |
| `bookDescription` | CSS selector for description |
| `chapterListItem` | CSS selector for chapter list items |
| `chapterTitle` | CSS selector for chapter title |
| `chapterLink` | CSS selector for chapter link |
| `chapterContent` | CSS selector for chapter text content |

## Contributing

1. Fork this repo
2. Add your source to `sources_repo.json`
3. Submit a pull request

## License

MIT
