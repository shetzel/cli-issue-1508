Repro Steps:
1. `sfdx force:mdapi:deploy -d src-converted -w 10`

I was also using the `src-converted2` dir to play around with metadata deploy sizes:
1. `rm -rf src-converted2`
2. `sfdx force:source:convert --rootdir force-app --outputdir src-converted2`
3. `du -hs src-converted2`  (note the size)
4. `sfdx force:mdapi:deploy -d src-converted2 -w 10`

Modify the amount and size of static resources by copying them from the `static_resources` dir.