## Installation / adding posts

This repo is set up to require no authentication: content is written locally
and then pushed to a remote git repository (e.g. GitHub). A web daemon will
watch for changes to a specific branch [document which one] and build using
[Hugo](https://gohugo.io), automatically deploying new content.

### Installation

1. Clone the repository from https://github.com/opensidewalks/opensidewalks.github.io

2. (optional) If you want to use a built-in CMS, install `
netlify-cms-proxy-server`, a local NodeJS proxy server. If you have NodeJS
installed, this will happen automatically the first time you run
`npx netlify-cms-proxy-server` in the CMS section below.

### Editing

To add content, edit markdown files within the `content/` directory of the root
directory. For example, blog posts are in `content/posts` and end with `.md`.

### Building

Run `hugo server` and check `localhost:1313` in your browser.

### (optional) Use the built-in CMS

This repo is set up to use [`netlify-cms`](https://www.netlifycms.org), a CMS
for static site generators. The CMS itself is already installed and built by
your local Hugo instance, but requires a local server,
`netlify-cms-proxy-server` to run without using
[Netlify](https://www.netlify.com/) as an intermediary. Running this server
requires installing [NodeJS](https://nodejs.org). Run this server by running
`npx netlify-cms-proxy-server`. This will run at `localhost:8081` and raise an
error if this port is already in use.

Once running, you can access the CMS by going to `localhost:1313/admin` and
clicking the "Log in" button. From here, you can create new content, including
uploading images and embedding videos, using a WYSIWYG editor.
