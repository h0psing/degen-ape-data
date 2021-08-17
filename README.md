du -a | grep json$ | cut -f 2 | xargs -I {} sh -c '( printf {}\, ; jq .Properties.attributes {} | grep "No Traits" | wc -l) | cat' | tee /tmp/results.csv
cat /tmp/results.csv | grep 5$ | cut -f 1 -d, | xargs -I {} sh -c 'cat {} | jq .Properties.attributes {}' | grep value | grep -v No | sort | cut -f 2 -d :

cat trait_count.csv| cut -f 2 -d \, | sort | uniq -c

 218 0
2270 1
4415 2
2541 3
 526 4
  35 5


coffee money DhPr5jch2CgJpbVxLKhaQHZt4uJ1GVVhpFQ9Wd9WQmYN