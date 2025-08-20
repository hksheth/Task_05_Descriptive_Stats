# Task_05_Descriptive_Stats

MotoGP World Championship Constructors (1949–2021).  

---

## Dataset
- 73 seasons (1949–2021)  
- 9 classes (125cc → MotoGP™)  
- 36 constructors  

---

## Part 1 — Basics

| Q | Query | Answer |
|---|-------|--------|
| Seasons | `df["Season"].min(), df["Season"].max()` | 1949–2021 |
| Classes | `df["Class"].unique()` | 9 |
| Constructors | `df["Constructor"].nunique()` | 36 |
| Most titles overall | `df["Constructor"].value_counts()` | Honda (65) |
| Top per class | `groupby(["Class","Constructor"]).size()` | Honda, MV Agusta, Kalex… |
| Latest winners (2021) | `df[df["Season"]==2021]` | MotoGP = Yamaha |

---

## Part 2 — Advanced

- **Longest streaks**: Kalex (9, Moto2), MV Agusta (9, MotoGP)  
- **Parity (HHI)**: MotoGP 1960s = 0.82 vs 1970s = 0.30  
- **Churn (winner changes YoY)**: MotoGP = 0.514, 125cc = 0.629  
- **Repeat probability**: MotoE = 1.0, Moto2 = 0.727  
- **Dominance index**: Honda tops with 2.12, breadth = 6 classes  


## Notes
- LLM queries require precise definitions (dominance, parity, streaks).  
- All answers validated with Python/Pandas.  
- Dataset not uploaded in repo. - https://www.kaggle.com/datasets/alrizacelk/moto-gp-world-championship19492022?resource=download
