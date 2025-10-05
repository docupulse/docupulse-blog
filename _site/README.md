# DocuPulse Blog

This is the official blog for DocuPulse, featuring use cases, tutorials, and insights about intelligent document management and Excel integration.

## Local Development

### Prerequisites

- Ruby 2.7 or higher (Ruby 3.4+ requires additional gems)
- Bundler gem

### Setup

1. **Clone the repository** (if not already done):
   ```bash
   git clone <repository-url>
   cd docupulse-blog
   ```

2. **Install dependencies**:
   ```bash
   bundle install
   ```

3. **Run the development server**:
   ```bash
   bundle exec jekyll serve
   ```

4. **Open your browser** and navigate to:
   ```
   http://localhost:4000/docupulse-blog/
   ```

### Windows Troubleshooting

If you get errors installing the `wdm` gem on Windows:

1. **The Gemfile has been updated** to comment out the problematic `wdm` gem
2. **Run bundle install again**:
   ```bash
   bundle install
   ```
3. **If you still get errors**, try:
   ```bash
   bundle install --without development
   ```

**Alternative Windows Setup**:
- Use **WSL (Windows Subsystem for Linux)** for a more reliable Jekyll experience
- Or use **Docker** with a Jekyll container

### Ruby 3.4+ Compatibility

If you're using Ruby 3.4 or higher, you may get errors about missing standard library gems:

1. **The Gemfile has been updated** to include `logger`, `csv`, and `base64` gems
2. **Run bundle install**:
   ```bash
   bundle install
   ```
3. **This should resolve the compatibility issues**

### Development Commands

- **Start development server**: `bundle exec jekyll serve`
- **Build site**: `bundle exec jekyll build`
- **Serve with drafts**: `bundle exec jekyll serve --drafts`
- **Incremental build**: `bundle exec jekyll serve --incremental`

### Project Structure

```
docupulse-blog/
├── _config.yml          # Site configuration
├── _includes/           # Reusable HTML components
├── _layouts/            # Page templates
├── _posts/              # Blog posts
├── assets/              # CSS, images, and other assets
├── index.md             # Homepage
├── blog.md              # Blog listing page
├── use-cases.md         # Use cases page
└── about.md             # About page
```

### Adding New Posts

1. Create a new file in `_posts/` with the format: `YYYY-MM-DD-title.md`
2. Add front matter with title, date, tags, etc.
3. Write your content in Markdown
4. The post will automatically appear on the blog

### Customization

- **Styling**: Edit `assets/css/style.scss`
- **Layouts**: Modify files in `_layouts/`
- **Navigation**: Update `_config.yml` header_pages
- **Site settings**: Edit `_config.yml`

## Deployment

This site is automatically deployed to GitHub Pages when changes are pushed to the main branch.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally with `bundle exec jekyll serve`
5. Submit a pull request

## License

This project is licensed under the MIT License.