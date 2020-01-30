```bash
for i in `ls *.csv` ; do cat $i | grep -v 'source: BNO @' | grep -v '# update:'| sed 's/# //g' | sponge $i ; done
for i in `ls *.csv` ; do csvformat -d '|' -D ',' $i ; done
for i in `ls *.csv` ; do csvformat -d '|' -D ',' $i | sponge $i; done
for i in `ls *.csv`; do csvclean $i ; done
```
