# Devansh Tayal 🚀

[![GitHub Followers](https://img.shields.io/github/followers/DevT02?label=Followers&style=social)](https://github.com/DevT02)
[![GitHub Stars](https://img.shields.io/github/stars/DevT02?affiliations=OWNER&style=social)](https://github.com/DevT02?tab=repositories)

## 🔥 Most Used Technologies
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=DevT02&layout=compact&theme=tokyonight&langs_count=6)

## 📌 Most Starred Repositories
```yaml
name: Update GitHub Stats
on:
  schedule:
    - cron: "0 0 * * *" # Runs once a day
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: anuraghazra/github-readme-stats@master
        with:
          username: DevT02
          show_icons: true
          theme: tokyonight
          include_all_commits: true
      - name: Update README.md
        run: |
          curl -s "https://api.github.com/users/DevT02/repos?sort=stargazers_count&per_page=5" |
          jq -r '.[] | "- [\(.name)](\(.html_url)) (\(.stargazers_count) ⭐)"' > most_starred.md
          sed -i '/## 📌 Most Starred Repositories/r most_starred.md' README.md
      - name: Commit Changes
        run: |
          git config --global user.name "GitHub Actions"
          git config --global user.email "actions@github.com"
          git add README.md
          git commit -m "Updated most-starred repositories"
          git push
```

---

## 📊 GitHub Stats
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=DevT02&show_icons=true&theme=tokyonight&count_private=true)

---

## 🔒 Other Work
Older projects and contributions are available **[here](https://github.com/imnobodyxd)** *(obfuscated for privacy 😉)*.

---

## 📡 Connect with Me
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR-LINKEDIN)
[![Email](https://img.shields.io/badge/Email-%23D14836.svg?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

---

🚀 **Always open to new opportunities and collaborations!**
