# Astro Plyr

> Plyr is a simple, lightweight, accessible and customizable HTML5, YouTube and Vimeo media player that supports modern browsers.

Using [Plyr](https://plyr.io/) in Astro project.


## Installation

| npm                	| pnpm                	| yarn                  	|
|--------------------	|---------------------	|-----------------------	|
| `npm i astro-plyr` 	| `pnpm i astro-plyr` 	| `yarn add astro-plyr` 	|

## Usage

```Astro
---
import Plyr from "astro-plyr";
import type { Options, SourceInfo } from "astro-plyr";

const source: SourceInfo = {
  type: "video",
  title: "Example title",
  poster:
    "https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.jpg",
  sources: [
    {
      src: "https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4",
      type: "video/mp4",
      size: 576,
    },
    {
      src: "https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-720p.mp4",
      type: "video/mp4",
      size: 720,
    },
  ],
  tracks: [
    {
      kind: "captions",
      label: "English",
      srcLang: "en",
      src: "https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.en.vtt",
      default: true,
    },
    {
      kind: "captions",
      label: "French",
      srcLang: "fr",
      src: "https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.fr.vtt",
    },
  ],
};

const options: Options = {
  debug: true,
};

---

<Plyr options={options} source={source} />

```
