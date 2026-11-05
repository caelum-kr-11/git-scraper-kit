# git-scraper-kit

Free, unattended web scraping on a schedule with **GitHub Actions**. You don't need a server or a database.
Every day a workflow runs your scrapers and commits the results to `data/`, so your git history becomes a versioned dataset ("git scraping").

Tutorial: [Run a web scraper on a schedule for free with GitHub Actions](https://caelum-kr-11.github.io/blog/free-cron-scraper-github-actions.html)

## Use it
1. Click **Use this template**, or fork the repo.
2. Put a scraper in `scrapers/`. Any `*.mjs` file that writes to `data/` works (Node 20, no dependencies needed).
3. Go to Actions → `scrape` → **Run workflow** to test it. After that it runs daily at 06:17 UTC; edit the cron line to change that.

See the change history of any file with `git log -p data/books.csv`.

## Included example
`scrapers/books.mjs` collects all 1,000 books from [books.toscrape.com](https://books.toscrape.com), a sandbox site made for scraping practice, into `data/books.csv`, with retries and polite delays.

## Good practice
Scrape public data only, respect each site's terms and robots.txt, keep the schedule gentle, and identify your bot honestly.

## License
MIT. Built with AI assistance.
