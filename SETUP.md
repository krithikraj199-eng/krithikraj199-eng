# KIRUTHICKRAJ T — GitHub Profile Setup

This package is designed for the special GitHub profile repository:

`krithikraj199-eng/krithikraj199-eng`

## 1. Create the profile repository

On GitHub, create a **public** repository named exactly:

```text
krithikraj199-eng
```

Because the repository name matches your username, GitHub will display its `README.md` on your profile.

## 2. Copy the package into that repository

Final structure:

```text
krithikraj199-eng/
├── README.md
├── assets/
│   └── hero.svg
└── .github/
    └── workflows/
        ├── pacman.yml
        └── profile-3d.yml
```

The `profile-3d-contrib/` folder is generated automatically after the 3D workflow runs.

## 3. Push the files

```bash
git init
git add .
git commit -m "Create Matrix Space GitHub profile"
git branch -M main
git remote add origin https://github.com/krithikraj199-eng/krithikraj199-eng.git
git push -u origin main
```

If the repository is already connected, use your normal update flow:

```bash
git add .
git commit -m "Update GitHub profile"
git push
```

## 4. Enable GitHub Actions write access

The workflows need permission to save generated graphics.

Go to:

```text
Repository
→ Settings
→ Actions
→ General
→ Workflow permissions
→ Read and write permissions
→ Save
```

No personal token is required by the included Pac-Man or 3D workflows.

## 5. Run Pac-Man once

Go to:

```text
Actions
→ Generate Pac-Man Contribution Graph
→ Run workflow
```

The workflow creates an `output` branch containing:

```text
pacman-contribution-graph.svg
pacman-contribution-graph-dark.svg
```

After that, the README's Pac-Man section will appear.

It also refreshes automatically every day.

## 6. Run the 3D contribution graph once

Go to:

```text
Actions
→ Generate 3D Contribution Graph
→ Run workflow
```

The action creates:

```text
profile-3d-contrib/
```

The README uses:

```text
profile-3d-contrib/profile-green-animate.svg
```

It refreshes automatically every day.

## 7. Dynamic sections

The README already contains live/dynamic integrations for:

- GitHub contribution streak
- LeetCode stats + 52-week heatmap
- GitHub summary cards
- GitHub activity graph
- Profile visitor counter
- Pac-Man contribution animation
- 3D contribution visualization

## GitHub streak vs LeetCode streak

They are separate systems.

Your **GitHub streak** updates when GitHub records qualifying contributions such as commits, issues and pull requests.

Your **LeetCode card/heatmap** updates from your LeetCode account activity.

A true LeetCode *current/highest streak* card can be added later using the self-hosted `github-readme-leetcode-stats` project. That deployment is intentionally not included here because it requires a separate Vercel deployment. The current package works without extra hosting.

## Theme

The design uses:

- Matrix green: `#39FF14`
- Deep-space black: `#02040A`
- GitHub dark: `#0D1117`
- Nebula purple: `#7C3AED` / `#8A2BE2`

## Important

If any third-party card service changes its URL in the future, the rest of the profile will continue working; only that specific card would need its source URL updated.
