---
date: "2022-03-23"
title: "About"
---

With FPGAs becoming increasingly widespread, there is huge demand for tools that make them easier to
program. High-level synthesis (HLS) is a particularly compelling solution, as it promises to make
the computational power and energy efficiency of FPGAs available to software engineers without a
background in hardware design. There has, accordingly, been a huge amount of HLS research in recent
years, much of which has been presented at FCCM and the other F-conferences.

We believe that there is a considerable opportunity to improve the reliability of HLS tools, as well
as the quality of the hardware designs they produce, through the application of formal
methods. Formal methods include tools such as proof assistants, static analysers, and automatic
verifiers, and also techniques such as formal semantics for specifying the source/target languages.

Work presented at FCCM in recent years indicates a substantial number of researchers in the
community with interests at the intersection of HLS and formal methods. For instance, Cheng et
al. [1] formalised hardware circuits as Petri nets and used static analysis on those nets to
determine initiation intervals for pipelines; Herklotz et al. [2] used fuzzing methods to test HLS
tools, motivating the need to formally verify the HLS process; and Faissole et al. [3] used the Coq
proof assistant to verify that HLS optimisations respect dependencies in the source code. More
generally, “translation validation” and “formal verification” have long been popular topics in FCCM
papers.

We intend this workshop to provide a forum to bring these people together to share ideas. We hope
that it will be valuable both to HLS experts who are interested in how formal methods could improve
the correctness and efficiency of HLS tools, and to formal methods experts who would like to learn
about how HLS as an interesting and worthwhile application domain for their techniques.

[1] Jianyi Cheng, John Wickerson, and George A. Constantinides: “Probabilistic Scheduling in
High-Level Synthesis”, FCCM 2021. https://ieeexplore.ieee.org/document/9444048

[2] Yann Herklotz, Zewei Du, Nadesh Ramanathan, and John Wickerson: “An Empirical Study of the
Reliability of High-Level Synthesis Tools”, FCCM 2021. https://ieeexplore.ieee.org/document/9444067

[3] Florian Faissole, George A. Constantinides, and David Thomas: “Formalizing Loop-Carried
Dependencies in Coq for High-Level Synthesis”,
FCCM 2019. https://ieeexplore.ieee.org/document/8735537
