- [Create and Deploy a Static Website with Github Pages](#create-and-deploy-a-static-website-with-github-pages)
  - [Create a repository](#create-a-repository)
    - [Clone Repository](#clone-repository)
    - [Commit and push local to remote](#commit-and-push-local-to-remote)
  - [Create an `index.html` file in `main`](#create-an-indexhtml-file-in-main)
    - [Push file to repo](#push-file-to-repo)
  - [Go to *repo* `Settings` and then `Pages`](#go-to-repo-settings-and-then-pages)
  - [Go to domain registrar website](#go-to-domain-registrar-website)
  - [Go to `Github` again](#go-to-github-again)
- [Static Site Generator](#static-site-generator)
  - [HUGO Themes](#hugo-themes)
  - [Checklist for my portfolio website](#checklist-for-my-portfolio-website)


#   Create and Deploy a Static Website with Github Pages

##  Create a repository
*   [Create a new repository](https://github.com/new)
    *   Repository name*
    *   Description(optional)
    *   Initialize this repository with README (check this option)
    *   Create repository

### Clone Repository

*   `git clone https://github.com/<username>/<repository_name>`: clone the repository from github to local
*   `cd <repository_name>`: change directory to `repository`.
*   Now files can be modified, added, deleted.

### Commit and push local to remote
*   `git add .`: add all repo files.
    *   `git add <file_name>`: add specific file.
*   `git commit -m "<message>"`: commit changes.
*   `git commit -am "<message>"`: this command work do both jobs, `add` and `commit`.
*   `git push`: push all files local to remote.

##  Create an `index.html` file in `main` 

```html
    <!DOCTYPE html>
    <html>
        <head>
            <title>My Website</title>
        </head>
        <body>
            <h1>This is Website Content</h1>
        </body>
    </html>
```

### Push file to repo
*   `git add .`: add all repo files.
*   `git commit -m "<message>"`: commit changes.
*   `git push`: push all files local to remote.

##  Go to *repo* `Settings` and then `Pages`

*   Select `branch` in which there is code
![select source](../cources/files/github/selectSourceAndRoot.png)
*   The site will be published soon

##  Go to domain registrar website
*   Here `namecheap.com`
*   Under profile go to `Dashboard`

![](../cources/files/github/selectDashboardNamecheap.png)

*   Click on Manage
![](../cources/files/github/manageDomainNamecheap.png)
*   Click `Advanced DNS`
![](../cources/files/github/manageDomainHostNamecheap.png)
*   Click `Host Records`
*   Click `ADD NEW RECORD` to update host records
    *   Under _Type_ put "A Record"
    *   Under _Host_ put "@"
    *   Under _Value_ put following IP addresses of github
        *   185.199.108.153
        *   185.199.109.153
        *   185.199.110.153
        *   185.199.111.153
    *   Under _TTL_ put "Automatic"
    *   Put fifth record `CNAME Record`, `www`, `<repo_name>.github.io`, `Automatic`
    *   Save

##  Go to `Github` again

*   Go to `https://github.com/<username>/<repo>/settings/pages`
![](../cources/files/github/customDomainGithub.png)

*   Update _Custom Domain_ with `www.<domain>.com`
*   Check mark on _Enforce HTTPS_
*   Congratulations, site will be published soon...

![](../cources/files/github/sitePublishedGithub.png)



#   Static Site Generator

First Select the static site generator from these two [hugo vs jekyll](https://forestry.io/blog/hugo-and-jekyll-compared/)

##  HUGO Themes
-   [portio](https://themes.gohugo.io//theme/portio-hugo/)
-   [terrassa](https://themes.gohugo.io//theme/hugo-terrassa-theme/)

##  Checklist for my portfolio website
- [ ]   Logo of name
- [ ]   Sticky navigation
- [ ]   Hamburger menu for small screens
- [ ]   Show viewer where they are located (highlight specific page)
- [ ]   Pages
  - [ ]   About me
    - [ ]   Contact information
    - [ ]   Experience
      - [ ]   Throughout life brief
      - [ ]   Design and Development
- [ ]   Contact me
