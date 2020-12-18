Templatka jest poprawioną wersją https://github.com/gskornowicz/latex-szablon-praca-inz. Wprowadzone zostały istotne zmiany oraz templatka jest dedykowana tylko i wyłącznie na Overleaf.com (tam została przetestowana).

Listening robimy za pomocą
```sh
\begin{lstlisting}[caption=Nazwa listeningu , label=listing:labelka-listeningu]
network:
  ethernets:
    eth0:
      addresses:
        - 192.168.1.20/24
      dhcp4: false
      gateway4: "192.168.1.254"
      nameservers:
        addresses:
          - "8.8.8.8"
          - "8.8.4.4"
  renderer: networkd
  version: 2
\end{lstlisting}
```

Zdjęcia wrzucamy:
```sh
\begin{figure}[ht]
        \centering
        \includegraphics[width=16cm]{./img/image1.png} % width zmienia wielkość zdjęcia i 16cm to maksymalny rozmiar.
        \caption{przykladowy opis - opracowanie własne} %ewentualeni można dodać \cite{} do przypisu harwardzkiego
        \label{fig:sample-label}
\end{figure}
```

Tabele wrzucamy:
```sh
\begin{table}[htb]
	\centering
	\caption{Przykładowa tabela}
	\label{table:przykladowa-tabela}

    \begin{tabular}{| l | l |}
    \hline
    Nazwa komponentu & Licencja \\ \hline
    Graylog 2.5 & GNU General Public License v3 \\ \hline
    MongoDB 3.4 & GNU Affero General Public License v3 \\ \hline
    Elasticsearch 6.5.1 & Elastic License \cite{elastic-license} \\ \hline
    rsyslog 8.24.0 & GNU General Public License v3  \\ \hline
    NXLog CE 2.10.2150& NXLog Public License  \\ \hline
    Docker 18.09.1 & Apache License 2.0  \\
    \hline
    \end{tabular}
\end{table}
```

Przypis harwardzki tworzy się poprzez użycie \cite{example}, gdzie example odnosi się do bibitem w bibliografia.tex
