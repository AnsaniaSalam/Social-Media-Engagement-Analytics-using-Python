<!-- BANNER -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,6,2,24&height=220&section=header&text=Social%20Media%20Engagement%20Analytics&fontSize=38&fontColor=ffffff&animation=fadeIn&desc=%E2%9D%A4%EF%B8%8F%20Likes%20%C2%B7%20%F0%9F%92%AC%20Comments%20%C2%B7%20%F0%9F%94%81%20Shares%20%C2%B7%20%F0%9F%91%81%EF%B8%8F%20Impressions&descSize=17&descAlignY=72" alt="banner" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&pduration=2500&duration=3500&pause=900&color=E1306C&center=true&vCenter=true&width=640&lines=What+makes+a+post+perform%3F;5%2C000+posts+%C2%B7+19+columns+%C2%B7+2+years;Clean+%E2%86%92+Explore+%E2%86%92+Visualise+%E2%86%92+Test" alt="typing" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Instagram-E4405F?style=flat-square&logo=instagram&logoColor=white" />
  <img src="https://img.shields.io/badge/TikTok-000000?style=flat-square&logo=tiktok&logoColor=white" />
  <img src="https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white" />
  <img src="https://img.shields.io/badge/X-000000?style=flat-square&logo=x&logoColor=white" />
  <img src="https://img.shields.io/badge/Facebook-1877F2?style=flat-square&logo=facebook&logoColor=white" />
  <img src="https://img.shields.io/badge/Status-Completed-2ea44f?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=flat-square" />
</p>

---

## 📱 About the Project

An exploratory analysis of **5,000 social media posts** across eight content categories, four post types and ten countries. The notebook cleans the data, builds new engagement features, draws **16 charts** (Matplotlib, Seaborn and interactive Plotly) and finishes by testing whether the differences it finds are real or just chance.

> 💡 **Question it answers:** does the type of post, the topic, the country, the device or the sentiment make a post perform better?

<p align="center">
  <img src="https://img.shields.io/badge/❤️_Likes-engagement-E1306C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/💬_Comments-conversation-833AB4?style=for-the-badge" />
  <img src="https://img.shields.io/badge/🔁_Shares-reach-FD1D1D?style=for-the-badge" />
  <img src="https://img.shields.io/badge/👁️_Impressions-visibility-FCB045?style=for-the-badge" />
</p>

---

## 🧾 The Dataset at a Glance

| 📊 Posts | 🧱 Columns | 🧹 After cleaning | 📅 Period |
|:---:|:---:|:---:|:---:|
| **5,000** | **19** | **4,850** | **Jan 2022 – Dec 2023** |

| Group | Columns |
|-------|---------|
| 👤 User | `user_id`, `age`, `gender`, `country`, `follower_count`, `is_verified`, `device_type` |
| 📝 Post | `post_id`, `post_type`, `post_category`, `hashtags`, `posted_at`, `sentiment` |
| 📈 Performance | `likes`, `comments`, `shares`, `watch_time_sec`, `impression_count`, `engagement_rate` |

---

## 🔄 Workflow

```mermaid
flowchart LR
    A[📥 Load CSV] --> B[🧹 Clean data]
    B --> C[🛠️ New features]
    C --> D[📊 Charts]
    D --> E[🔍 Insights]
    E --> F[🧪 Significance tests]
    style A fill:#833AB4,color:#fff,stroke:none
    style B fill:#C13584,color:#fff,stroke:none
    style C fill:#E1306C,color:#fff,stroke:none
    style D fill:#FD1D1D,color:#fff,stroke:none
    style E fill:#F77737,color:#fff,stroke:none
    style F fill:#FCAF45,color:#000,stroke:none
```

---

## 🧹 Data Cleaning

| Problem found | What was done |
|---------------|---------------|
| 150 missing values in each of `age`, `gender`, `likes`, `comments`, `shares`, `sentiment` | Numbers filled with the median, missing gender set to `Unknown`, rows with missing sentiment dropped |
| 589 posts (12.1%) had more reactions than impressions, with engagement rates up to 191.5 | Reactions scaled down so no engagement rate is above 1 |
| Dates stored as text (`17-12-2022`) | Converted to dates using the day-month-year format |
| Duplicates | Checked, none found |

**5,000 rows → 4,850 rows**

---

## 🛠️ Features Created

- **Engagement score** = likes + 2 × comments + 3 × shares
- **Engagement rate** recalculated after cleaning
- **Age groups** (13-24 up to 55-64)
- **Day of week** and **month** from the post date
- **Region** added by merging a small country lookup table

---

## 📊 Charts Included

| Library | Charts |
|---------|--------|
| 🎨 **Matplotlib** | Histogram, bar charts, line chart, scatter plot |
| 🌈 **Seaborn** | Box plot, violin plot, heatmap, swarm plot, pair relationships |
| ⚡ **Plotly (interactive)** | Monthly trend lines, country comparison, bubble chart of categories |

---

## 🔍 Key Findings

<table>
<tr>
<td width="50%">

### 🏆 Content
- Text, video and image posts are level at about **0.38** engagement rate; reels are lowest at **0.36**
- Fitness (**0.384**) and music (**0.383**) lead the categories; food is lowest (**0.360**)
- Australia is highest (**0.398**), India lowest (**0.344**)

</td>
<td width="50%">

### 👥 Users and behaviour
- Engagement rate dips slightly with age, **0.382 → 0.355**, but the link is very weak (−0.026)
- Verified accounts: **0.351** against **0.375**, just short of significance (p = 0.055)
- Mobile has the longest watch time (**4,088 s**)

</td>
</tr>
</table>

```mermaid
pie showData title Share of posts by sentiment
    "Positive" : 2363
    "Neutral" : 1527
    "Negative" : 960
```

> 📌 **Main takeaway:** the one strong pattern is that **engagement rate falls as impressions rise** (correlation −0.79), because likes, comments and shares do not grow as fast as reach. Beyond that, the group differences are mostly within chance.

### 🧪 Are the differences real?

| Comparison | Test | p-value | Real difference? |
|------------|------|:------:|:---:|
| Engagement rate by post type | Kruskal-Wallis | 0.825 | ❌ |
| Engagement rate by category | Kruskal-Wallis | 0.976 | ❌ |
| Engagement rate by country | Kruskal-Wallis | 0.331 | ❌ |
| Engagement rate by sentiment | Kruskal-Wallis | 0.985 | ❌ |
| Verified vs not verified | Mann-Whitney | 0.055 | ❌ |
| Impressions by weekday | Kruskal-Wallis | 0.577 | ❌ |

---

## 📂 Project Structure

```
Social-Media-Engagement-Analytics/
│
├── 📓 Social_Media_Engagement_Analytics.ipynb   # Full analysis
├── 📄 social_media_engagement_5000.csv          # Dataset
├── 📘 README.md
└── 📜 LICENSE
```

| File | Description |
|------|-------------|
| [📓 Social_Media_Engagement_Analytics.ipynb](Social_Media_Engagement_Analytics.ipynb) | Notebook with every task, code, output and explanation |
| [📄 social_media_engagement_5000.csv](social_media_engagement_5000.csv) | The 5,000-post dataset |
| [📜 LICENSE](LICENSE) | MIT License |

---

## 🧰 Concepts Used

`pandas` · `numpy` · `matplotlib` · `seaborn` · `plotly.express` · `scipy.stats` · missing value handling · outlier correction · `groupby` · `merge` · date handling · correlation · hypothesis tests

---

## 🚀 Running the Project

1. **Clone the repository**
   ```bash
   git clone https://github.com/AnsaniaSalam/Social-Media-Engagement-Analytics.git
   cd Social-Media-Engagement-Analytics
   ```
2. **Install the libraries**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scipy jupyter
   ```
3. **Open the notebook**
   ```bash
   jupyter notebook Social_Media_Engagement_Analytics.ipynb
   ```
4. Keep the CSV **in the same folder** as the notebook and run the cells from top to bottom.

> Plotly charts are interactive in Jupyter. On GitHub they may show as static images.

---

## 👩‍💻 Author

<p align="center">
  <b>Ansania Salam</b><br><br>
  <a href="https://www.linkedin.com/in/ansania-salam">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="https://github.com/AnsaniaSalam">
    <img src="https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white" />
  </a>
</p>

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,6,2,24&height=100&section=footer" />
</p>
