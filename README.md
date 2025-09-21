# Simple-website-template

This guide explains how you can setup your own website using this template, and using markdown to write pages

## Dependencies

- Git for version control and publishing as a GitHub page
- Ruby and Bundler for local preview
- A text editor, optimally one made for markdown like [MarkText](https://github.com/marktext/marktext)
	- You can also use [Obsidian](https://obsidian.md/), create an obsidian vault in the project root, and add `.obsidian` to `.gitignore`. Although Obsidian is not fully open source, all its extensions are and it fully complies with markdown standards.

## Installing Bundler

- Install Ruby (through package manager or official site)
- Open terminal/PowerShell and run `gem install bundler`

## Quick start

- Setup your GitHub account and terminal git according to `resources/git-guide.md`
- Clone this repo using `git clone https://github.com/Daniel-42-z/simple-website-template.git`
- Open the repo root folder in terminal/PowerShell and run:
	- `bundle config set --local path .bundle`
	- `bundle install`
- To preview the local version of the website, run `bundle exec jekyll serve` in a terminal/PowerShell window in the project root folder, and preview the website in a browser at [http://localhost:4000](http://localhost:4000), press control+C in the terminal/PowerShell to stop the preview.
	- After editing a file in the project, save the file and reload the (local) website to see the changes applied
	- If `_config.yml` or some css file is edited, live reloading might not work, and the command need to be stopped using control+C and re-run to see changes

## Editing pages

- Edit the markdown (`.md`) files to change the pages' contents, compare the sample page at `articles/sample-page.md` and its preview to learn commonly used markdown syntax, including headings, text styling, and inserting media and math equations

### Creating pages

- When creating a new markdown page, add the frontmatter shown below:

	```
	---
	layout: default
	title:  "My Topic"    # displayed in browser tab and heading 1 (heading 1 in body text will overwrite it)
	permalink: /my-topic/ # clean URL → http://…/my-topic/
	---
	```

- If you want the page to show up in the top-right navigation bar (usually important pages like about, resources, etc.), open `_config.yml` and add the file's path to the `header_pages:` section
- If you want to hide the page from any way of access from the website (e.g. `README.md`), add its path to the `exclude:` section in `_config.yml`

### Images, videos, and files

- Put images and videos in `media/` and link relatively: `![Alt text](media/diagram.png){: width="60%"}`
- Large binaries (PDFs, ZIPs) go in `files/`, but for non-embedded files it is recommended to use a link to an external website for download

### Using `.gitignore`

- If you don't want certain files or folders to be tracked by the git repository (and thus uploaded to GitHub), add their paths relative to the project root to `.gitignore`. Do not remove the lines currently in `.gitignore` unless you know what you are doing.

## Publishing to your GitHub page

- Create a GitHub account (skip if you already have one, even if the website name you want is different to your username)
- Link your `git` command with your GitHub account following the guide in `resources/git-guide.md`
- Create a GitHub organization (your website URL will be `<organization-name>.github.io`) or just use your personal account (your website URL will be `<user-name>.github.io`) (replace the contents in angle brackets with the actual names)
- From GitHub, create a repository named `<organization-name>.github.io` or `<user-name>.github.io` depending on whether you create the repository as the organization or as your personal account. Select "no license", and follow the guide on the website to push the local git repository to the remote (it is generally recommended to use the HTTPS protocol instead of SSH, as the connection is faster and it does not require generating ssh key pairs)
- Refresh the GitHub repository page, and you should see a website deployment status. Refresh a few times and once you see a green ✅ you can go to the URL and see the newest webpage
