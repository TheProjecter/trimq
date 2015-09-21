TRIMQ is a perl script that trims bases with low quality and minimum sequence length.  An input file should be in Sanger Fastq format.


USE:
  * perl trimq\_v\_0.1.1.pl [--help] [--man]
> > [--qcutoff]  [--lcutoff]
> > --in input\_file.fastq    [--out input\_file\_trimmed.fastq]

Examples:
  * perl trimq\_v\_0.1.1.pl --help
  * perl trimq\_v\_0.1.1.pl --man
  * perl trimq\_v\_0.1.1.pl --in input\_file.fastq      (Output file name will be input\_file\_trimmed.fastq)
  * perl trimq\_v\_0.1.1.pl --in input\_file.fastq.gz   (Output file name will be input\_file\_trimmed.fastq.gz)
  * perl trimq\_v\_0.1.1.pl --in input\_file.fastq --out input\_file\_trimmed.fastq
  * perl trimq\_v\_0.1.1.pl --in input\_file.fastq.gz --out input\_file\_trimmed.fastq.gz
  * perl trimq\_v\_0.1.1.pl --qcutoff 35 --lcutoff 25 --in input\_file.fastq --out input\_file\_trimmed.fastq



Options:
  * -h or --help                      print help message
  * -q or --qcutoff                   quality value for cutoff in Sanger FASTQ format
  * -l or --lcutoff                   minimum length of fragment to keep after trimming


AUTHOR
Sijung Yun (yuns@mail.nih.gov or sijungyun@gmail.com)


DATE
July 25, 2012


ALGORITHM
FOR A FRAGMENT, GET THE LONGEST CONTIGUOUS SEGMENT IN WHICH ALL THE READS HAVE THEIR QUALITY SCORES HIGHER THAN CUTOFF.  THEN, IF THE LENGTH OF THE SELECTED SEGMENT IS LONGER THAN CUTOFF LENGTH, WRITE TO THE TRIMMED OUTPUT FILE AS SANGER FASTQ FORMAT