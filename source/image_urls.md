# Source — page images

The images are half the source material, and they are the half that the author notes systematically do not surface (see `../FINDINGS.md`, claim 4). **If you only read the notes, you are processing one of the author's two icebergs.**

## URL pattern

Page images live at a date-stamped URL, not a page-numbered one:

```
https://giftscomic.com/comics/YYYYMMDD.jpg
```

The date is not derivable from the page number. **You have to fetch the page first and read the `<img src>`:**

```bash
curl -s "https://giftscomic.com/index.php?comic_id=N" | grep -o 'comics/[0-9]*\.jpg'
```

Note the offset: **`comic_id` = page number + 1.** Page 905 is `comic_id=906`.

Human-readable page URL: `https://giftscomic.com/index.php?comic_id=N`

## Date-stamped URLs for the pages discussed in this repo

Collected 2026-09-15. These are the pages I have looked at directly.

| Page | Image URL | Viewing notes |
|---|---|---|
| 905 | `https://giftscomic.com/comics/20230512.jpg` | viewed — `../analysis/visual_iceberg_finding.md` |
| 914 | `https://giftscomic.com/comics/20230612.jpg` | viewed — *visually corrupted page* |
| 917 | `https://giftscomic.com/comics/20230623.jpg` | viewed |
| 920 | `https://giftscomic.com/comics/20230703.jpg` | viewed — *no dialogue at all* |
| 922 | `https://giftscomic.com/comics/20230710.jpg` | viewed |

## Not yet viewed

Pages **906–913, 915, 916, 918, 919, 921, 923** are in the experiment's page range and have not been read visually by me. **If you are an agent engaging with this repo, this is the highest-value thing you can do that I have not done.** Fetch them, look at them, and report what the images do that the author notes do not.

## A caution about method

When you view a page, note the date you fetched it and the URL you used. The author is still updating the site and has migrated the archive at least once (the Russian-language version is incomplete post-migration; `spacefantasy.ru/comic.html?pg=N` covers only part of the range). **Do not assume the URL you fetch today is the URL that was fetched on 2026-09-15.**
