# Team Project Name
Minor Variant Miners

List of participants and affiliations
- Team Leader - Tung H. Nguyen (tung.nguyen@nih.gov)
- Tech Leads - Stephen Panossian, Tung H. Nguyen
- Writers - Nidia S. Trovao, Cecile Viboud
- Metadata - Eneida Hatcher, Jie Lu
- SQL query for the TF-IDF - Jie Lu, Kaiyuan Sun

## Project Goals
Do SCV2 mutations have same minor allele frequencies?

## Approach
ACTION ITEM
1) Ask Ryan for the TF-IDF query for mutations he used on variant of concerns as a document. JIE, SUNKY: chat with Ryan, get coached on the best way for VCFs.
MAF of > 15%, is there a way to unrestrict, whether it makes to do that.
2) Nidia and Cecile work on the introduction. https://virological.org/t/issues-with-sars-cov-2-sequencing-data/473 https://www.biorxiv.org/content/10.1101/2023.01.30.526314v2.full.pdf
3) Stephen, make sure the software is understandable and well documented. https://github.com/NCBI-Codeathons/vcf-4-population-genomics-team-nguyen
Each person should just have separate scripts, files, folders.

CORPUS is a collection of
‘DOCUMENTS’ = place, type of sequencing (long read, short read), type of primers
On these documents are words (mutations), we’re counting these words.

Random, systematic, spike-in. Transmission. Homoplasy (convergent evolution).
Minor (??) and consensus (https://virological.org/t/issues-with-sars-cov-2-sequencing-data/473)  alleles

1) Catalog common mutations using TF-IDF; these are mutations that appear quite frequently in Texas DHS but not in other submitters.
  a) “real mutation”: appear in multiple places
2) Separately, calculate TF-IDF on places, sequencing technologies, time, primers, VOCs?, host, vaccination, treatments.
   a) LDA
3) Given the same sequencing center, where mutation x super high TF-IDF, but Midnight (long read) protocol, the mutation:
  a) Disappeared: look similarities 
  b) Stayed
4) Let’s take closer look. Investigate the relationship of mutations the document from which it was pulled.
5) Say you have high scoring hits TF-IDF: Then, taking look at clusters of mutations. Mutations next to each other, adjacent. Identity of the variant (T). Window the genome positions 30KB. You see if these mutations are closer than they should be chance.
6) Are they close to any hard to 2/3rary structures of RNA, stem loops

## Results

## Future Work
