# Diagrama contract process

By Robert Bermudez

```mermaid
flowchart TD

%% Nodos %%
A((Job searching))
B[job found]
C{met qualifications?}
C.1[No]
C.2((Start Over))
C.3[Yes]
D[Applying for the job]
E{Did the applicant get positive feedback?}
E.1[Yes]
E.2[No]
E.3((Start Over))
F[complete the video task requested]
F.1{Did the applicant get positive feedback?}
F.2[Yes]
F.3[No]
F.4((Start Over))
G[Interview stage]
G.1{will the interviewed go to the next stage?}
G.2[Yes]
G.3[No]
G.4((Start Over))
G.5(Documentation requested)
H[CEO interview]

%% Conexiones %%
A --> B
B ---> C
C ---x C.1 --> C.2
C --- C.3 --> D
D --- E
E --- E.1 --> F
E ---x E.2 --> E.3
F --- F.1 --- F.2 --> G
F.1 ---x F.3 --> F.4
G --> G.1
G.1 --- G.2 --> H
G.1 --- G.3 --> G.4
G.1 ---o G.5

%% Enlaces externos %%
click A "https://www.linkedin.com/jobs"
click F "https://www.loom.com/"
click B "https://www.linkedin.com/jobs/view/customer-success-representative-e-commerce-at-panda-music-4028681338/"
click H "https://us06web.zoom.us/j/88935512094?pwd=MInYAPt1Ufpil2v3h7zt3AyoCaXSNa.1"

%% Estilo de Nodos %%
style A fill:#87CEEB,stroke:#000,stroke-width:1px
style F fill:#87CEEB,stroke:#000,stroke-width:1px
style B fill:#87CEEB,stroke:#000,stroke-width:1px
style H fill:#87CEEB,stroke:#000,stroke-width:1px