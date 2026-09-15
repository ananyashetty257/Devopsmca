# Explore India - DevOps Lab Project

A simple web application showcasing tourist destinations in India, built as part of a DevOps laboratory exercise on Git branching.

## Project Structure

```
devops/
├── Labs/
│   ├── index.html          # Main homepage
│   ├── gallery.html         # Image gallery page
│   ├── Lab1.gitignore       # Git ignore file
│   ├── css/
│   │   └── style.css        # Styling
│   ├── scripts/
│   │   └── script.js        # JavaScript functionality
│   └── images/
│       ├── tajmahal.jpg     # Taj Mahal image
│       ├── kerala.jpg       # Kerala Backwaters image
│       └── goa.jpeg         # Goa Beaches image
└── README.md
```

## Features

- **Homepage**: Displays information about Indian tourist destinations (Taj Mahal, Kerala Backwaters, Goa Beaches)
- **Gallery**: Image gallery showcasing the destinations
- **Navigation**: Links between Home and Gallery pages
- **Interactive Button**: "Explore More" button with JavaScript alert

## Git History

### Original Commits (by ArdenDiago)
| Commit | Description |
|--------|-------------|
| `2e12cb7` | Added the gitignore file |
| `c71d42a` | Added the About.md |
| `f0a4347` | Added the HTML, CSS, and JS code to the remote |
| `5f4d138` | Added the Gallery Code and the images to the project |
| `3041752` | Revert "added the About.md" |

### Author Changes

**Before:**
- Author: ArdenDiago
- Email: diagoarden@gmail.com

**After:**
- Author: Ananya shetty
- Email: ananyashetty257@gmail.com

### Commands Used

```bash
# Changed git config for future commits
git config user.name "Ananya shetty"
git config user.email "ananyashetty257@gmail.com"

# Rewrote entire git history to update author information
git stash
git filter-branch --env-filter '
OLD_NAME="ArdenDiago"
OLD_EMAIL="diagoarden@gmail.com"
NEW_NAME="Ananya shetty"
NEW_EMAIL="ananyashetty257@gmail.com"

if [ "$GIT_COMMITTER_NAME" = "$OLD_NAME" ]; then
    export GIT_COMMITTER_NAME="$NEW_NAME"
fi
if [ "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL" ]; then
    export GIT_COMMITTER_EMAIL="$NEW_EMAIL"
fi
if [ "$GIT_AUTHOR_NAME" = "$OLD_NAME" ]; then
    export GIT_AUTHOR_NAME="$NEW_NAME"
fi
if [ "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL" ]; then
    export GIT_AUTHOR_EMAIL="$NEW_EMAIL"
fi
' -- --all
git stash pop

# Cleaned up backup refs
git update-ref -d refs/original/refs/heads/main
git update-ref -d refs/original/refs/heads/afe
git update-ref -d refs/original/refs/heads/tmp-afe
```

## Current Git Status

- **Branch**: main
- **Author**: Ananya shetty (ananyashetty257@gmail.com)
- **Commits**: 5 (all updated with new author)

## Author

**Ananya Shetty**
- Email: ananyashetty257@gmail.com
