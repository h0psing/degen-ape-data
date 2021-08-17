

All Apes have at least 2 traits (background and fur/skin). Listed in order of rarity:


| Total Apes | Traits | Example Img |
| --- | --- | --- |
| 35 | 2 (Bare) | <img src="https://e3rgq4zucds77kvdugl45obtgc5cctaota4tghfyqmmg5niyko2a.arweave.net/JuJoczQQ5f-qo6GXzrgzMLohTA6YOTMcuIMYbrUYU7Q" width="100" height="100"> |
| 218 | 7 (Fully Loaded) | <img src="https://6hvdkhi4hquv2l73hkin2nfy2qyly6btcrgrt4cz5ddq2ii27kda.arweave.net/8eo1HRw8KV0v-zqQ3TS41DC8eDMUTRnwWejHDSEa-oY" width="100" height="100"> |
| 526 | 3 | <img src="https://4u4zed4z6fl4ajtisoxon65c66vhq2vno3yndnxhmbhtketaxhhq.arweave.net/5TmSD5nxV8AmaJOu5vui96p4aq128NG252BPNRJguc8" width="100" height="100"> |
| 2270 | 6 | <img src="https://3fr6fikvp7ml2glpg2i6huhrpo6zayaiw6omp2ddz3bt3rt64tia.arweave.net/2WPioVV_2L0ZbzaR49Dxe72QYAi3nMfoY87DPcZ-5NA" width="100" height="100"> |
| 2541 | 4 | <img src="https://oxesepcjch44bnx5d4xqztybulmhr4yac5mjh5wtrtyz5vlo7g5q.arweave.net/dckiPEkR-cC2_R8vDM8Both48wAXWJP204zxntVu-bs" width="100" height="100"> |
| 4415 | 5 | <img src="https://vaxytko5jnyl4gku57khgspxrd2jwmgic36fmrb3l2wdx4ncrlta.arweave.net/qC-Jqd1LcL4ZVO_Uc0n3iPSbMMgW_FZEO16sO_GiiuY" width="100" height="100"> |


:pray: coffee money to DhPr5jch2CgJpbVxLKhaQHZt4uJ1GVVhpFQ9Wd9WQmYN and support degen ape community development

feature requests and community contrib welcome. DM empires on discord or Twitter: https://twitter.com/0xempires

# Looking For A Specific Trait?

Type in the search box above ^ (ex. "Halo" -- https://github.com/0xempires/degen-ape-data/search?q=halo) and GitHub presents total number in search results. Careful with overloaded queries like "Gold"

# Technically Inclined?

Explore the data/ dir to see .json file per token address.

Example:
```bash
du -a | grep json$ | cut -f 2 | xargs -I {} sh -c '( printf {}\, ; jq .Properties.attributes {} | grep "No Traits" | wc -l) | cat' | tee /tmp/results.csv
cat /tmp/results.csv | grep 5$ | cut -f 1 -d, | xargs -I {} sh -c 'cat {} | jq .Properties.attributes {}' | grep value | grep -v No | sort | cut -f 2 -d :
```
See token addrs per trait counts (presented as num traits MISSING from total 7):
```
cat trait_count.csv| cut -f 2 -d \, | sort | uniq -c
```

