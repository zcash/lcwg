### Meeting Date/Time: Thursday October 16th, 2025 17:00 UTC

### Meeting Duration: 50 minutes

### Moderators: Pacu (ZecDevRel), 

Atendees: Pacu, Za, 

### Agenda: 
- Share the results of the statistical analysis of adding the transparent data into the light client protocol https://github.com/zecdev/compact-block-data-analysis/blob/main/docs/analysis/statistical_report.md
  - There is not much question whether Zaino can pull this off, although Pacu needs to review what Zaino engineers have pointed him to. It’s more a lightwalled support question and whether it’s worth the effort for ECC to cost it and deploy it there.  
    - Followed up async and ECC will develop this on LWD  
  - According to the statistical analysis the average impact throughout all NU’s is a 50% premium on the current data costs on light clients. But when it is scoped to post-NU6 blocks the impact is significantly lowered. The whole post-sapling average has high variability and therefore is not a reliable metric.   
  - If the API to include transparent data allows optional inclusion, then the server learns whether the client is interested in T stuff or not which lightwalletd currently does and, moreover it learns about subsequent calls to make up for the missing information. The API optionality it’s still “a win” in terms of intent disclosure from the caller of the API.  
  