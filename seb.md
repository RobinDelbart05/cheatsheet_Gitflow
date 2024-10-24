# Git Flow

```
     Λ        Λ   
     │  H2    │   
v2.1 O<─┐     O   
     │  │     Λ   
     │  │     │   
     │  O─────┤   
     │  Λ     │   
     │  │     │   
v2.0 O──┴──┐  O   
     Λ     │  Λ   
     │     │  │   
     │     O──┤   
     │     Λ  │   
     │     │  │   
     │     O  │   
     │     Λ  │   
     │     └──O<────┐
     │    R2  Λ     │
     │        │     │
     │        O<─┐  O
     │        Λ  │  Λ
     │        │  │  │
     │        │  O  O
     │        │  Λ  Λ
     │        │  │  │
     │        │  O  O
     │        │  Λ  Λ
     │        │  │  │
     │        O──┴──┘
     │        Λ F1  F2   
     │        │      
v1.0 O────────┤      
     Λ        │      
     │        │     
  master   workshop
```
Scheme inspired by V. Driessen in *A Successful Git Branching Model*. 
※F1 = feature 1; F2 = feature 2; R2 = release 2.0; H2 = hotfix for 2.0