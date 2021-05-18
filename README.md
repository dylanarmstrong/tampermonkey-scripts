## Userscripts and Userstyles

### Notes
My personal collection of userscripts. These can all be used independently of each other, so just grab the ones that sound interesting. I primarily use Safari, and haven't tested any of these in other browsers. If you run into issues, please open an issue.

From Sept. 2020 onwards, these are designed and being updated to work with [Userscripts](https://github.com/quoid/userscripts) instead of Tampermonkey.

Userstyles are stored in the styles folder.

Archived scripts are stored in archive folder.

### Scripts

### cnbc
CNBC is removing the article because of my adblocking, so double the article, it won't remove both.

### facebook-marketplace-local-only
Remove 'Ships to you' items from marketplace. I'm not sure this does what I want, but it's somewhat useful at the moment.

#### fakespot
Add fakespot link above buy box on amazon

#### fanfiction
Modify fanfiction.net to be better. There's a customizable cors proxy url that can be used on the profile page.
If you change this to your own, you can view mobile favorites (without 500 limit) on the desktop.

#### google-placeholder
Pulled in some uBlock scripts that have drop-in no-op replacements for google tracking, might cause less sites to break.

#### imgur
Bypass imgur login

#### reddit-filter
Adds a filter at end of tagline that has a popup to filter on subreddit, domain, or user (only on r/all). They're stored in the localStorage keys starting with 'filter'. Filtered items must be removed from localStorage manually.

![reddit-filter screenshot](./screenshots/reddit-filter.png)

#### reddit-load
When you scroll to the bottom, load the next page of results. Compatible with reddit-filter.

#### reddit-nsfw
Filter all NSFW tags from appearing on any page

#### reddit-override
Override Reddit's official window.r functionality that *may* be interesting, I don't really know. The isMobile method stops video pinning though, which is useful.

#### reddit-redirect
Redirects www calls to old.reddit.com

#### wikipedia-chess
Fixes chessboards on Safari wikipedia

#### xenforo-popular
Hides unpopular stories on spacebattles / sufficientvelocity, so it's easier to go through recently updated and find good stories.

#### xenforo-reactions
Adds first message reaction score on alternate-history, sufficientvelocity and spacebattles.

### Styles
* fanfiction
* hacker-news
* reddit
* royalroad
* teddit
* wormstorysearch
* xenforo
* youtube

### Archived Scripts
These scripts are ones I am not actively maintaining, they may continue to work. If you run into an issue with them, please open an issue and I will take a look.

#### facebook-marketplace [archived]
Sort facebook marketplace by date

#### outline [archived]
Open some outgoing links (mostly news) from HN and Reddit using the awesome [outline.com](https://outline.com) service.

#### paradoxwikis [archived]
Achievements page on EU4 wiki is using some new mobile style, so just delete it all and use no style. Tables are usable as-is.

#### stylize [archived]
Allows me to write custom styles for websites matching hosts by string or regex. Not very user friendly and you'd be best off copying the js directly into your tampermonkey extension and ignoring updates.

Replaced with styles in Cascadea.

```javascript
const csses = {
  '((old|www)\.)?reddit\.com$': {
    type: 'regex',
    css: `
      .subreddit {
        border: 1px solid blue;
      }
    `
  },
  'old.reddit.com': {
    type: 'string',
    css: `
      .subreddit {
        border: 1px solid red;
      }
    `
  }
};
```

#### xenforo-no-fanwork [archived]
Remove fanwork discussions from main user forum on sufficientvelocity

#### xenforo-no-worm [archived]
Remove worm stories, except from worm specific forums

#### xenforo-search [archived]
Remove posts from search results, only show threads

#### youtube [archived]
Disable youtube polymer
