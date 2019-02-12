## RegexAlign
RegexAlign used re.search to find exact start and end position of query sequences in following steps:

1. Fasta files were parsed into dictionary using SeqIO.parse. Sequences of reference file were reverse complemented and saved into an seperate array.
2. Sequences from query sequences were searched against reference sequences as well as their reverse complement strand using re.search. Only the first match were retained.
3. Aligned positions were extracted form re.search.start() and re.search.end() and output into bed format.

### Dependency
* Python3
* Bio.SeqIO

### Usage
python regex_align.py query.fasta reference.fasta >align.bed

### Format
* Input: [Fasta](https://en.wikipedia.org/wiki/FASTA_format)
* Output: [Bed](https://genome.ucsc.edu/FAQ/FAQformat.html)

## TODO
Add multiple-thread mode
