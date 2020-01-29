  568  for i in `ls *.csv` ; do cat $i | grep -v 'source: BNO @' | grep -v '# update:'| sed 's/# //g' | sponge $i ; done
  576  for i in `ls *.csv` ; do csvformat -d '|' -D ',' $i ; done
  579  for i in `ls *.csv` ; do csvformat -d '|' -D ',' $i | sponge $i; done
  583  for i in `ls *.csv`; do csvclean $i ; done

