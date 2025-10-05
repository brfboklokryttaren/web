# BRF BoKlok Ryttaren Website

This is the official website for BRF BoKlok Ryttaren, built with Jekyll and hosted on GitHub Pages.

## Getting Started

Follow these instructions to set up and run the website locally on your machine.

### Prerequisites

Before you begin, make sure you have the following installed:

- **Ruby** (version 2.7 or higher)
- **Bundler** (Ruby gem manager)
- **Git**

### Installation

#### 1. Install Ruby

**On macOS** (using Homebrew):

```bash
brew install ruby
```

**On Ubuntu/Debian**:

```bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev
```

**On Windows**:
Download and install Ruby from [rubyinstaller.org](https://rubyinstaller.org/)

#### 2. Install Bundler

```bash
gem install bundler
```

#### 3. Clone the Repository

```bash
git clone https://github.com/brfboklokryttaren/web.git
cd web
```

#### 4. Install Dependencies

```bash
bundle install
```

### Running the Site Locally

#### Start the Development Server

```bash
bundle exec jekyll serve
```

Or with live reload (automatically refreshes the browser when files change):

```bash
bundle exec jekyll serve --livereload
```

#### Access the Site

Once the server is running, open your web browser and navigate to:

```
http://localhost:4000
```

The site will automatically reload when you make changes to the files.

### Project Structure

```
├── _config.yml          # Jekyll configuration
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
├── _site/               # Generated site (don't edit directly)
├── assets/              # CSS, images, and other static files
├── Gemfile              # Ruby dependencies
├── index.md             # Homepage content
└── README.md            # This file
```

### Making Changes

1. **Content**: Edit the Markdown files (`.md`) to update page content
2. **Styling**: Modify files in the `assets/css/` directory
3. **Layout**: Edit templates in the `_layouts/` directory
4. **Components**: Update reusable elements in the `_includes/` directory

### Building for Production

To build the site for production (generates static files in `_site/`):

```bash
bundle exec jekyll build
```

### Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the `main` branch. No manual deployment is needed.

### Troubleshooting

#### Common Issues:

**"Could not find gem" errors:**

```bash
bundle update
bundle install
```

**Port already in use:**

```bash
bundle exec jekyll serve --port 4001
```

**Permission errors on macOS:**
Add this to your shell profile (`.zshrc` or `.bash_profile`):

```bash
export GEM_HOME="$HOME/.gem"
export PATH="$GEM_HOME/bin:$PATH"
```

### Contributing

1. Create a new branch for your changes
2. Make your modifications
3. Test locally using `bundle exec jekyll serve`
4. Commit your changes with a descriptive message
5. Push to your branch and create a pull request
