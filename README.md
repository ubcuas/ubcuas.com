[![Netlify Status](https://api.netlify.com/api/v1/badges/527f4e4e-eadf-4013-8709-14103812deb6/deploy-status)](https://app.netlify.com/sites/ubcuas/deploys)

## UBC UAS Website ([ubcuas.com](https://ubcuas.com))

This is the repository for the UBC UAS website. The website is built using [Hugo](https://gohugo.io/) and deployed using [Netlify](https://www.netlify.com/).

## Development

### Prerequisites

-   [Hugo](https://gohugo.io/getting-started/installing/)
-   [Node.js](https://nodejs.org/en/download/)

### Commands

#### Setup

- Clone theme submodule

    ```bash
    git submodule init
    git submodule update
    ```

- Install dependencies

    ```bash
    npm install
    ```

- Run Hugo server

    ```bash
    npm run dev
    ```

#### Update Theme

```bash
git submodule update --remote
```

#### Update Modules

```bash
npm run update-modules
```

#### Build

```bash
npm run build
```

### Structure

```
.vscode/
    extensions.json                    # Suggested extensions

assets/                                # Static assets
    images/                            # Images
    scss/                              # Custom CSS files

config/                                # Hugo configuration files
    _default/                          # Default configuration files
        languages.toml                 # Language configuration (only English for us)
        menus.en.toml                  # Menu configuration
        module.toml                    # Hugo modules configuration - can add new modules here
        params.toml                    # Theme site parameters

content/                               # Content files
    english/
        authors/                       # Author profiles
            _index.md                  # Author home page
            <author-url>.md            # Author profile
        blog/                          # Blog section
            _index.md                  # Blog home page
            <blog-post-url>.md         # Blog post
        contact/                       # Default contact page - not used for us
            _index.md
        homepage/                      # Homepage content
            _index.md
        pages/                         # Main pages
            <page-url>.md              # Page content
        sections/                      # Special pre-defined page sections
            call-to-action.md          # Call to action section - unused
            testimonials.md            # Testimonials section for home page - unused

data/
    social.json                        # Social media links for the footer
    theme.json                         # Theme configuration

i18n/                                  # Translation files
    en.yaml                            # English translation file

layouts/                               # Layout files (new items or overrides the theme layouts)
    partials/                          # Partial layout files (reusable components)
    shortcodes/                        # Shortcodes (reusable components, notably in markdown)

scripts/                               # Scripts from the theme for setup and updates

themes/hugoplate                       # Theme files - pulled from git submodule

.editorconfig                          # Editor configuration
.jshintrc                              # JSHint configuration
.markdownlint.json                     # Markdown linting configuration
.prettierrc                            # Prettier configuration
go.mod                                 # Hugo modules versioning
hugo.toml                              # Hugo configuration
netlify.toml                           # Netlify configuration
package.json                           # Node.js configuration
tailwind.config.js                     # Tailwind CSS configuration
```

### CI/CD

Upon submitting a pull request, Netlify will automatically build and deploy a preview of the website. Be sure to view this preview and check the build logs before merging it. Once the pull request is merged, Netlify will automatically build and deploy the website to production.
