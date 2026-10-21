# Assignment 5 – GitHub Repository Link

This document records the remote repository connection for the HTML & CSS coursework, including remote push steps and free hosting configuration via GitHub Pages.

## Remote Push Instructions

1. Log into [GitHub](https://github.com/) and create a new repository:
   - **Repository name:** `HTML-Assignment`
   - **Visibility:** Public
   - **Initialize with README:** Unchecked (since our local repository already has commits)

2. Link local repository and push changes:
   ```bash
   git remote add origin https://github.com/ruchirsaxena01/HTML-Assignment.git
   git branch -M main
   git push -u origin main
   ```

3. Confirm that all local branches and files have synced to the GitHub remote repository.

## GitHub Pages Deployment

To host the assignments online for peer and instructor review:
1. Navigate to **Settings → Pages** in the GitHub repository.
2. Under **Build and deployment → Branch**, choose `main` branch and `/ (root)` folder.
3. Click **Save**.
4. The site becomes accessible within 1–2 minutes at the custom GitHub Pages URL.

## Submission Details

- **Author:** Ruchir Saxena
- **Program:** BCA (Artificial Intelligence), Invertis University, Bareilly
- **GitHub Repository URL:** `https://github.com/ruchirsaxena01/HTML-Assignment`
- **Live Deployment URL:** `https://ruchirsaxena01.github.io/HTML-Assignment/`
