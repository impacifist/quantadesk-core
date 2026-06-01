# Publishing Guide

Use this guide to publish QuantaDesk's public surface without exposing the private
development repository.

## 1. Create A Clean Repository

Create a new empty GitHub repository, for example:

```text
quantadesk-core
```

Do not make the private development repository public.

## 2. Copy Public Files

Copy the contents of this folder into the new repository root:

```text
public-site/* -> quantadesk-core/*
```

The new repository root should contain `index.html`, `README.md`, `LICENSE`,
`docs/`, `.github/`, and `assets/`.

## 3. Commit From A Clean History

Initialize and commit only inside the new public repository:

```powershell
git init
git add .
git commit -m "Initial public QuantaDesk project page"
git branch -M main
git remote add origin https://github.com/<owner>/quantadesk-core.git
git push -u origin main
```

## 4. Enable GitHub Pages

In GitHub:

1. Open repository settings.
2. Go to Pages.
3. Select `Deploy from a branch`.
4. Choose branch `main` and folder `/root`.
5. Save.

GitHub Pages should serve `index.html`.

## 5. Keep The Boundary

Before every public push, confirm:

- no private strategy implementation files,
- no private parameter files,
- no proprietary research notes,
- no market archive or operator state,
- no credentials or secret assignments,
- no screenshots with real account or strategy data.

The included GitHub Actions workflow adds a baseline safety scan, but it is not
a replacement for human review.
