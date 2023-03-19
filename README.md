# Next.js + WordPress

It's headless WordPress! - <https://nextjswp.com>

## Features

- Next.js w/ TypeScript
- WordPress environment with [@wordpress/wp-env](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-env/)
- React Components from [Mantine](https://mantine.dev)
- Apollo and WP GraphQL
- On-demand revalidation
- Date based blog routing (`YYYY/MM/DD/slug`)
- Yoast SEO support
- CPT UI support
- Menus support
- Preview support
- Comments support
- Post reactions support
- Advanced Custom Fields support
- ESLint, Stylelint, Prettier, and more!

---

## Monorepo

This project is a monorepo managed by [Turborepo](https://turbo.build/repo).

```text
nextjs-wordpress
├── apps
│   ├── docs
│   ├── nextjs
│   └── wordpress
├── packages
│   ├── eslint-config-custom
│   ├── nextjs-wordpress-plugin
│   ├── nextjs-wordpress-theme
│   ├── prettier-config-custom
│   └── tsconfig
└── turbo.json
```

### `apps/`

The applications directory. This includes the documentation, Next.js (frontend), and WordPress (backend).

### `packages/`

Shared packages used by the apps. This includes ESLint, Prettier, and TypeScript configs. As well as the WordPress plugin and theme.

### `turbo.json`

The repo config file. Learn more about configuring [Turborepo](https://turbo.build/repo/docs/reference/configuration).

---

## Quick Start

View the [Quick Start instructions](https://github.com/gregrickaby/nextjs-wordpress/blob/main/apps/docs/setup.md#quick-start).

---

## Full Documentation

View the [full documentation](./apps/docs/index.md).

---

## FAQ

### Do I have to use @wordpress/env?

Nah, you can use any WordPress environment you want. I've tested with Local and Dreamhost and both work fine. Using [@wordpress/env](https://developer.wordpress.org/block-editor/reference-guides/packages/packages-env/) is just a convient way to shared and automate the setup process.

Follow [the Manual Setup documentation](https://github.com/gregrickaby/nextjs-wordpress/blob/main/apps/docs/setup.md#manual-setup-nextjs) to turn any WordPress environment into a headless one.

---

### Why Mantine and not Tailwind, MUI, or \_\_\_\_?

I preferred not to create or maintain complex UI components such as forms, notifications, dropdowns, and so on. The reason for this is explained in more detail in [this discussion](https://github.com/gregrickaby/nextjs-wordpress/discussions/76#discussioncomment-5203206).

---

### Why Apollo and not \_\_\_\_?

Although Apollo can sometimes negatively impact performance, it was specifically designed for GraphQL and it is a reliable and effective tool for this purpose.

---

### When will you support the Next.js 13 `app` router?

> As of March 2023, the `app` router is still in `beta`.

There are two primary reasons why this repo hasn't already adopted the `app` router:

1. The Next.js team [does not recommend using it in production](https://capture.dropbox.com/ZXzRKgIruGnyF5wP)
2. Mantine (which uses Emotion) doesn't fully support Server Components yet (see [#2815](https://github.com/mantinedev/mantine/issues/2815) and [#2928](https://github.com/emotion-js/emotion/issues/2928))

I understand that there's a lot of excitement around the new `app` router and Server Components in React-based projects. However, it's important to recognize that this represents a significant paradigm shift, and it will take time for the community to fully understand and adopt this approach. While refactoring to use Server Components is no small task, I am [exploring and experimenting](https://github.com/gregrickaby/nextjs-app-directory) with this new technology.

That being said, I want to assure you that the existing `pages` router is still a reliable and established approach in Next.js. It will continue to be around [for the foreseeable future](https://www.reddit.com/r/nextjs/comments/11a5vp9/comment/j9x3e4h/), and can still be used effectively for many use cases.

---

## Contributing

Contributions are welcome! Please see the [contributing guidelines](./CONTRIBUTING.md) for more information.

---

## Props

A special thanks to the following people:

- [Rae Van Epps](https://github.com/ravewebdev) wrote the bulk of the PHP code for the Next.js WordPress Plugin, giving this project a jumping off point.
- [Amor Kumar](https://github.com/itsamoreh) insipired me to deep dive into Docker with his [BYOB Headless WordPress](https://github.com/itsamoreh/byob-headless-wordpress) project.
- [John Jeeves](https://github.com/orgs/AEWP/people/john-jeeves-americaneagle) and [Adam Hollister](https://github.com/ahollister) for their work on registering Gutenberg Blocks in the WordPress REST-API.
- [Jason Bahl](https://github.com/jasonbahl) for his tireless work on [WP GraphQL](https://www.wpgraphql.com/), and all of our chats/DMs over the years.

I ❤️❤️❤️ the open source community, and hope this project inspires you to create something awesome.

Cheers! 🍻

---
