\documentclass[12pt]{article}
\usepackage{amsmath}

\begin{document}

\section*{What is an ADC?}

An \textbf{ADC (Analog-to-Digital Converter)} is a \textbf{mixed-signal device}, meaning it works with \textbf{both analog and digital signals}.  

\begin{itemize}
    \item \textbf{Analog Input:} Takes a voltage or current signal from the real world (e.g., temperature, sound, light sensors).  
    \item \textbf{Digital Output:} Converts the analog signal into a digital value that a microcontroller or computer can understand.  
\end{itemize}

\textbf{Simplified Concept:}  
The ADC tells us \textit{what fraction of a reference voltage (or current) the input represents}. This is why it can be considered a \textbf{divider}.  

---

\section*{ADC Output Formula}

The general formula for an ADC with a binary output is:  

\begin{equation}
\text{Output} = \frac{2^n \cdot G \cdot A_{IN}}{V_{REF}}
\end{equation}

Where:  
\begin{itemize}
    \item $n$ = Number of output bits (resolution). Higher $n$ means higher precision.  
    \item $G$ = Gain factor (usually 1).  
    \item $A_{IN}$ = Analog input voltage (or current).  
    \item $V_{REF}$ (or $I_{REF}$) = Reference voltage (or current).  
\end{itemize}

\textbf{Example:}  
Suppose a 3-bit ADC ($n = 3$) with $V_{REF} = 5$V, $G = 1$, and $A_{IN} = 2.5$V.  

\begin{align*}
\text{Output} &= \frac{2^3 \cdot 1 \cdot 2.5}{5} \\
&= \frac{8 \cdot 2.5}{5} \\
&= 4
\end{align*}

This means the ADC outputs a digital word \texttt{100} (binary) representing \textbf{half of $V_{REF}$}.

---

\section*{Important Notes}

\begin{enumerate}
    \item Most ADCs convert \textbf{voltage}, but some can also convert \textbf{current}.  
    \item The reference ($V_{REF}$ or $I_{REF}$) sets the \textbf{maximum input value} the ADC can measure.  
    \item Some ADCs use \textbf{binary output}, while others may use \textbf{offset binary} or \textbf{2's complement}.  
    \item The gain factor $G$ is usually 1 but can scale the input in certain ADCs.  
\end{enumerate}

\textbf{Summary:}  
An ADC is a device that \textbf{measures a real-world voltage or current} and outputs a digital value indicating \textbf{what fraction of the reference it is}.

\end{document}
