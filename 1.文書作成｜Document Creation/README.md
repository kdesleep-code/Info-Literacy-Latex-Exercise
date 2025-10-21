# 1.文書作成｜Document Creation
文責：堀江和正

[English Version](README_en.md)

---

まず，本ディレクトリの`main.tex`をダウンロードしてみましょう．  
本ファイルの中身は以下のようになっています．

```LaTex

\documentclass[twocolumn,11pt]{jsarticle}
\usepackage[dvipdfmx]{graphicx}
\usepackage[dvipdfmx,bookmarks=true,colorlinks=true,linkcolor=blue,urlcolor=blue,citecolor=blue]{hyperref}
\usepackage{amsmath,amssymb}
\usepackage{booktabs}
\usepackage{geometry}
\usepackage{cite}
\geometry{margin=20mm}

\title{Sleep-CAM：説明可能な睡眠ステージ自動判定}
\author{堀江和正とゆかいな仲間たち\\筑波大学}
\date{\today}

\begin{document}
\maketitle

睡眠ステージ（W, REM, N1, N2, N3）は睡眠医療において重要であり，従来は専門家がPSG（EEG/EOG/EMG）から特徴波を同定して目視判定する。
自動化の研究は発展しているが，臨床での信頼を得るには，どの信号のどの部分を根拠に判定したかを提示できる説明可能性が鍵である。

\end{document}

```
