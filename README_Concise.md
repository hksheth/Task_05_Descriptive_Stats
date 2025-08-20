{\rtf1\ansi\ansicpg1252\cocoartf2862
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\margl1440\margr1440\vieww38200\viewh21600\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 \
# Task_05_Descriptive_Stats\
\
MotoGP World Championship Constructors (1949\'962021).  \
\
Dataset\
\
- 73 seasons (1949\'962021)  \
- 9 classes (125cc \uc0\u8594  MotoGP\'99)  \
- 36 constructors  \
\
Part 1 \'97 Basics\
\
| Q | Query | Answer |\
|---|-------|--------|\
| Seasons | `df["Season"].min(), df["Season"].max()` | 1949\'962021 |\
| Classes | `df["Class"].unique()` | 9 |\
| Constructors | `df["Constructor"].nunique()` | 36 |\
| Most titles overall | `df["Constructor"].value_counts()` | Honda (65) |\
| Top per class | `groupby(["Class","Constructor"]).size()` | Honda, MV Agusta, Kalex\'85 |\
| Latest winners (2021) | `df[df["Season"]==2021]` | MotoGP = Yamaha |\
\
Part 2 \'97 Advanced\
\
- **Longest streaks**: Kalex (9, Moto2), MV Agusta (9, MotoGP)  \
- **Parity (HHI)**: MotoGP 1960s = 0.82 vs 1970s = 0.30  \
- **Churn (winner changes YoY)**: MotoGP = 0.514, 125cc = 0.629  \
- **Repeat probability**: MotoE = 1.0, Moto2 = 0.727  \
- **Dominance index**: Honda tops with 2.12, breadth = 6 classes  \
\
Notes\
\
- LLM queries require precise definitions (dominance, parity, streaks).  \
- All answers validated with Python/Pandas.  \
- Dataset not uploaded in repo.}