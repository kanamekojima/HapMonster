# HapMonster
## OVERVIEW

HapMonster is a Java program that enables simultaneous variant calling and haplotype phasing for next generation sequencing data. Phased haplotypes are estimated based on phase-informative reads which span multiple heterozygous variant sites.

## INPUT

The sequence read data in SAM or BAM format (BAM file with BAQ information is recommended)

## OUTPUT

Variant calling and haplotype phasing results in VCF format

## USAGE

Example

~~~~
java -jar HapMonster.jar \  
    VariantCall \
    -r reference_genome.fasta \
    -t chr1 \
    -d average_depth \
    -il true \ 
    <SAM or BAM file> \
    <VCF file>
~~~~



## OPTIONS

| Option | Default Value | Summary |
|--------|:--------------|:--------|
| -r (--reference) | STR none | Reference genome fasta file| 
|* -d (--depth) | INT none | Read coverage |
|* -t (--target-region) | STR none | Target region for variant calling |
|* -c (--call-range-size) | INT 2500000 | Variant calling range size |
| -h (--help) | false | Print options and exit |
| -i (--iteration) | INT 20 | Iteration count |
| -il (--illumina) | [true/false] false | Use Illumina HiSeq read correction mode |
| -l (--depth-limit) | INT 500 | Depth limit |
| -m (--margin) | INT 1000 | Margin for variant calling |
| -p (--use-paired-end) | [true/false] true | Consider paired-end reads |
| -rp (--reference-prior) | DOUBLE 0.135 | Prior strength for reference allele |
| -th (--threshold) | DOUBLE 10.0 | Threshold for filtering variant calls |
| -u (--unit-id) | INT 1 | Unit ID |

 \* Required options

## DOWNLOAD
