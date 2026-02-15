# Quan Nguyen - Academic Website

This is the academic website for Quan Nguyen, built with [Hugo](https://gohugo.io/) and the [Hugo Blox Research Group](https://github.com/HugoBlox/theme-research-group) theme.

## About

**Quan Nguyen** is an Assistant Professor in Computer Science at Thompson Rivers University. His research focuses on:

- Learning Analytics
- Generative AI in Education
- Data Science Education
- Student Success Modeling

## Site Structure

- **Home** (`_index.md`): Introduction and highlights
- **Publications** (`content/publication/`): 7 peer-reviewed papers
- **Events** (`content/event/`): Talks, awards, and recognitions (20+ events)
- **Teaching** (`content/teaching/`): Course information
- **Contact** (`content/contact/`): Contact information

## Technical Details

- **Generator**: Hugo v0.142.0+
- **Theme**: Hugo Blox Research Group
- **Build Command**: `hugo --gc --minify`
- **Output Directory**: `public/`

## Local Development

```bash
# Install Hugo (extended version required)
# Download from: https://github.com/gohugoio/hugo/releases

# Clone the repository
git clone <repo-url>
cd research-lab

# Start development server
hugo server -D

# Build site
hugo --gc --minify
```

## Deployment

This site is configured for deployment on Netlify. See `netlify.toml` for build configuration.

## License

Content © Quan Nguyen. Code released under the MIT License.
