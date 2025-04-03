
\documentclass[10pt, letterpaper]{article}

% Packages:
\usepackage[
    ignoreheadfoot, % set margins without considering header and footer
    top=2 cm, % seperation between body and page edge from the top
    bottom=2 cm, % seperation between body and page edge from the bottom
    left=2 cm, % seperation between body and page edge from the left
    right=2 cm, % seperation between body and page edge from the right
    footskip=1.0 cm, % seperation between body and footer
    % showframe % for debugging 
]{geometry} % for adjusting page geometry
\usepackage[explicit]{titlesec} % for customizing section titles
\usepackage{tabularx} % for making tables with fixed width columns
\usepackage{array} % tabularx requires this
\usepackage[dvipsnames]{xcolor} % for coloring text
\definecolor{primaryColor}{RGB}{0, 79, 144} % define primary color
\usepackage{enumitem} % for customizing lists
\usepackage{fontawesome5} % for using icons
\usepackage{amsmath} % for math
\usepackage[
    pdftitle={Aryan Yadav CV},
    pdfauthor={Aryan Yadav},
    pdfcreator={ARYAN CV},
    colorlinks=true,
    urlcolor=primaryColor
]{hyperref} % for links, metadata and bookmarks
\usepackage[pscoord]{eso-pic} % for floating text on the page
\usepackage{calc} % for calculating lengths
\usepackage{bookmark} % for bookmarks
\usepackage{lastpage} % for getting the total number of pages
\usepackage{changepage} % for one column entries (adjustwidth environment)
\usepackage{paracol} % for two and three column entries
\usepackage{ifthen} % for conditional statements
\usepackage{needspace} % for avoiding page brake right after the section title
\usepackage{iftex} % check if engine is pdflatex, xetex or luatex

% Ensure that generate pdf is machine readable/ATS parsable:
\ifPDFTeX
    \input{glyphtounicode}
    \pdfgentounicode=1
    \usepackage[T1]{fontenc}
    \usepackage[utf8]{inputenc}
    \usepackage{lmodern}
\fi

\usepackage[default, type1]{sourcesanspro} 

% Some settings:
\AtBeginEnvironment{adjustwidth}{\partopsep0pt} % remove space before adjustwidth environment
\pagestyle{empty} % no header or footer
\setcounter{secnumdepth}{0} % no section numbering
\setlength{\parindent}{0pt} % no indentation
\setlength{\topskip}{0pt} % no top skip
\setlength{\columnsep}{0.15cm} % set column seperation
\makeatletter
\let\ps@customFooterStyle\ps@plain % Copy the plain style to customFooterStyle
\makeatother
\pagestyle{customFooterStyle}

\titleformat{\section}{
    % avoid page braking right after the section title
    \needspace{4\baselineskip}
    % make the font size of the section title large and color it with the primary color
    \Large\color{primaryColor}
}{
}{
}{
    % print bold title, give 0.15 cm space and draw a line of 0.8 pt thickness
    % from the end of the title to the end of the body
    \textbf{#1}\hspace{0.15cm}\titlerule[0.8pt]\hspace{-0.1cm}
}[] % section title formatting

\titlespacing{\section}{
    % left space:
    -1pt
}{
    % top space:
    0.3 cm
}{
    % bottom space:
    0.2 cm
} % section title spacing

% \renewcommand\labelitemi{$\vcenter{\hbox{\small$\bullet$}}$} % custom bullet points
\newenvironment{highlights}{
    \begin{itemize}[
        topsep=0.10 cm,
        parsep=0.10 cm,
        partopsep=0pt,
        itemsep=0pt,
        leftmargin=0.4 cm + 10pt
    ]
}{
    \end{itemize}
} % new environment for highlights

\newenvironment{highlightsforbulletentries}{
    \begin{itemize}[
        topsep=0.10 cm,
        parsep=0.10 cm,
        partopsep=0pt,
        itemsep=0pt,
        leftmargin=10pt
    ]
}{
    \end{itemize}
} % new environment for highlights for bullet entries


\newenvironment{onecolentry}{
    \begin{adjustwidth}{
        0.2 cm + 0.00001 cm
    }{
        0.2 cm + 0.00001 cm
    }
}{
    \end{adjustwidth}
} % new environment for one column entries

\newenvironment{twocolentry}[2][]{
    \onecolentry
    \def\secondColumn{#2}
    \setcolumnwidth{\fill, 4.5 cm}
    \begin{paracol}{2}
}{
    \switchcolumn \raggedleft \secondColumn
    \end{paracol}
    \endonecolentry
} % new environment for two column entries

\newenvironment{threecolentry}[3][]{
    \onecolentry
    \def\thirdColumn{#3}
    \setcolumnwidth{1 cm, \fill, 4.5 cm}
    \begin{paracol}{3}
    {\raggedright #2} \switchcolumn
}{
    \switchcolumn \raggedleft \thirdColumn
    \end{paracol}
    \endonecolentry
} % new environment for three column entries

\newenvironment{header}{
    \setlength{\topsep}{0pt}\par\kern\topsep\centering\color{primaryColor}\linespread{1.5}
}{
    \par\kern\topsep
} % new environment for the header

\newcommand{\placelastupdatedtext}{% \placetextbox{<horizontal pos>}{<vertical pos>}{<stuff>}
  \AddToShipoutPictureFG*{% Add <stuff> to current page foreground
    \put(
        \LenToUnit{\paperwidth-2 cm-0.2 cm+0.05cm},
        \LenToUnit{\paperheight-1.0 cm}
    ){\vtop{{\null}\makebox[0pt][c]
    }}}%
  }%


% save the original href command in a new command:
\let\hrefWithoutArrow\href

% new command for external links:
\renewcommand{\href}[2]{\hrefWithoutArrow{#1}{\ifthenelse{\equal{#2}{}}{ }{#2 }\raisebox{.15ex}{\footnotesize \faExternalLink*}}}


\begin{document}
    \newcommand{\AND}{\unskip
        \cleaders\copy\ANDbox\hskip\wd\ANDbox
        \ignorespaces
    }
    \newsavebox\ANDbox
    \sbox\ANDbox{}

    \placelastupdatedtext
    \begin{header}
        \fontsize{30pt}{30 pt} 
      {\textbf{
ARYAN YADAV
}}
        \vspace{0.2 cm}
          \begin{onecolentry}
\subsubsection{     ( Data Analytics|Data Scientist|Business Analyst)}
      \end{onecolentry}
      
        \vspace{0.3 cm}

        \normalsize
        \mbox{{\footnotesize\faMapMarker*}\hspace*{0.13cm}Varanasi,UP}%
        \kern 0.25 cm%
        \AND%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{https://Aryanyadv181@gmail.com}{{\footnotesize\faEnvelope[regular]}\hspace*{0.13cm}Aryanyadv181@gmail.com}}%
        \kern 0.25 cm%
        \AND%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{tel:+91-7310210707}{{\footnotesize\faPhone*}\hspace*{0.13cm}7310210707}}%
        \kern 0.25 cm%
        \AND%
        \kern 0.25 cm%
        \AND%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{https://www.linkedin.com/in/aryan-yadav-2312res181}{{\footnotesize\faLinkedinIn}\hspace*{0.13cm}aryan-yadav-2312res181}}%
        \kern 0.25 cm%
        \AND%
        \kern 0.25 cm%
        \mbox{\hrefWithoutArrow{https://github.com/aryan-181}{{\footnotesize\faGithub}\hspace*{0.13cm}aryan-181}}%
    \end{header}

    \vspace{0.3 cm - 0.3 cm}

    \section{Profile}
  
        \begin{onecolentry}
            Passionate about Data Analytics with a strong foundation in Computer Science and Data Analytics. Looking for opportunities to apply analytical and technical skills to solve real-world data challenges and drive impactful insights.
        \end{onecolentry}

        \vspace{0.2 cm}
         \section{Education}
        \begin{threecolentry}{\textbf{BS}}{
            july 2023 – Present
        }
            \textbf{Indian Institute of Technology, Patna}, Computer Science \& Data Analytics
             
        \end{threecolentry}
        
        
 \section{Technologies}
 
        \begin{onecolentry}
            \textbf{Languages:}Python, Java, SQL, HTML
        \end{onecolentry}
\begin{onecolentry}
            \textbf{Database :} MySQL \end{onecolentry}
        \begin{onecolentry}
            \textbf{Data Visualization  :} Power Bi, MS-Excel,Pandas, NumPy, Seaborn,Matplotlib,Jupyter Notebook \end{onecolentry}
\begin{onecolentry}
            \textbf{Machine Learning :} Machine Learning Library(Scikit-Learn,BeautifulSoup ,NLTK ) \end{onecolentry}
    \section{Project}

    \begin{onecolentry}
    
 \textbf{IPL 2022 Data Analysis \& Visualization}
\begin{itemize}
\textbf{Tools Used: Python, Pandas, Plotly, Data Visualization}

 \item  Analyzed team performances by creating bar charts showing matches won, winning margins, and best bowling performances.
 \item Created bar graphs, pie charts, and stacked bar graphs to track the top scorers, the best bowlers, and the match winners.
 \item Processed and cleaned cricket data, converting categorical values into structured formats for better insight.
 \item Strengthened data storytelling through visualization and pattern recognition.
 
\end{itemize}

         \textbf{Insights for Ride-Hailing Analytics}
         
         \textit{\textbf{Tool Used:Power Bi }}
\begin{itemize}
\item Interactive Dashboards: Designed real-time dashboards to visualize trip demand, driver supply, and peak hours.
 \item  Used Power BI DAX to calculate and highlight optimal hours for adding drivers.
 \item Automated Data Processing: Integrated Power Query for ETL, handling missing values and time formatting for accurate reporting.
  \end{itemize}

      \textbf{{Sentiment Stock Data Analysis}}
\begin{itemize}
 \item  Developed an NLP-driven stock analysis model to extract financial insights from tweets, leveraging Named Entity Recognition (NER), sentiment analysis, and semantic relationships. Utilized Machine Learning for stock trend prediction. 
 \item   Engineered text \& sentiment-based features and applied TF-IDF \& Sentence Transformer 
                      embeddings.
 \item  Used the RandomForestClassifier to improve the prediction accuracy.
 \item  Generated pairplots \& relationship graphs to explore stock sentiment trends.
 \item Analyzed financial events affecting market movement using data-driven insights.
 \item 
Generated pairplots \& relationship graphs to explore stock sentiment trends.

 
 \end{itemize}

    \end{onecolentry}

      \vspace{0.4cm}
      
    \section{Experience}
        \begin{twocolentry}{
        march 2024 – April 2024
        }
            \textbf{Code Soft},\textbf{ Data Scientist(Intern})
            \begin{highlights}
                \item Data Preprocessing \& Feature Engineering for Titanic Dataset 
                \item Cleaned and preprocessed Titanic dataset by handling missing values 
                \item Optimized performance through feature engineering, handling missing data, and encoding 
                       categorical variables. 
                \item Implement Machine Learning Algorithm(Logistic Regression model) on the Titanic dataset, 
                  achieving \textbf{78\% accuracy} 
            \end{highlights}
        \end{twocolentry}
        
        \vspace{0.2 cm}
    
    \section{Certificate\&Achievements }
        \begin{samepage}
            \begin{twocolentry}{
                March-2025
            }
                 \item {Finalist in Techanalytics Hackathon in Technex’25(IIT BHU Varanasi) 
                 \item{Data Science Workshop certificate from IIT Hydrabad.}
               \item  { AI ML With Data Science Workshop from IIT Ropar.}
             \item{Participate in Hackfest’25 (IIT(ISM)Dhanbad)} 
               \vspace{0.2 cm}
           }
           \end{twocolentry}
        \end{samepage}  

\end{document}
<!---
Aiizzen/Aiizzen is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
