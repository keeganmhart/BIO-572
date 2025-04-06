# Keegan Hart BIO 572 Problem Set 
Partners were Cass and Olivia.
## Problems
### 1. Let's imagine a 5 bp section of a genome, and that there is a SNP (A/G) in basepair 3. Assume that we are genotyping one heterozygous individual (50% chance of sequencing either allele). Please calculate the probability for the following sequencing reads:

**Set 1**
    
    ```
    AAATG
    AAATG
    AAATG
    ```
**Answer Set 1**


The probability of having A at basepair 3 in all 3 reads of a heterozygous individual is:
 $\frac{1}{2} *\frac{1}{2} * \frac{1}{2} = \frac{1}{8}$

 **Set 2**

    ```
    AAATG
    AAATG
    AAATG
    AAATG
    AAATG
    ```
**Answer Set 2**

The probability of having A at basepair 3 in all 5 reads of a heterozygous individual is:
$\frac{1}{2}  * \frac{1}{2} * \frac{1}{2} * \frac{1}{2} * \frac{1}{2} = \frac{1}{32}$


 **Set 3**

    ```
    AAATG
    AAGTG
    AAATG
    AAATG
    AAATG
    ```
**Answer Set 3**

The probability of having 4 reads with A in basepair 3 and one read with G in basepair 3 is: 
$  P_x = \frac {5!}{(5-4)!* 4!} * \frac{1}{2}^4 * \frac{1}{2}^1 = \frac{5}{32}$

### 2. Way back in old 1993, Spitze reported the following number of genotypes at the *PGI* allozyme locus in the *Daphnia* population in Nothing Pond:

|Genotype|Count|
|--------|-----|
|*SS*| 10|
|*SS-*|56|
|*S-S-*|60|

### A. What are the observed genotype and allele frequencies?
### B. Given the observed allele frequencies, what are the genotypic frequencies expected under Hardy-Weinberg?  Using a chi-square test, how well do the observed genotype frequences agree with the HWE expecations?
### C. What is the observed heterozygosity in this population and what is the expected heterozygosity?
\
 **Answer Set A**
 
genotype frequency :

$SS = \frac{10}{126} = 0.08$

$SS^- = \frac{56}{126} = 0.44$

$S^-S^- = \frac{60}{126} = 0.48$

allelic frequency: 

$S = \frac{2(10) + 56}{2(126)} = 0.3$

$S^- = \frac {2(60) + 56}{2(126)} = 0.7$

 **Answer Set B**

 genotypic frequencies under Hardy-Weinberg:
 
 
|Genotype|Freq|Count|
|--------|-----|----|
|*SS*|$$0.3^2 = .09$$|$$.09^2 * 126= 11.34$$|
|*SS-*|$$2(.3)(.7) = 0.42$$|$$(2)(.3)(.7) * 126  = 52.92$$|
|*S-S-*|$$(.7)^2 = 0.49$$|$$7^2 * 126 = 61.74$$|


   Chi square: There is 1 degree of freedom due to the 3 genotypes and 2 alleles
$x^2 = \frac{(10-11.34)^2}{11.34} + \frac{(60-61.74)^2}{61.74} + \frac{(56-52.92)^2}{52.92} = 0.159 + 0.049 + 0.179 = 0.387$
    0.387 < 3.84 so observed frequencies agree with HWE expectations

 **Answer Set C**
\
    expected heterozygosity:
He = $1 - (p^2 + q^2)$ 
He = $1 - (0.3)^2 + (0.7)^2$
He = $1 - 0.58$
He = 0.42
\
    observed heterozygosity:
Ho = the genotype frequency of $SS^- = 0.44$

### 3.  Let's imagine another small population with the following genotype counts at a single SNP:

|Genotype|Count|
|--------|-----|
|A/A|0|
|A/G|10|
|G/G|0|

### A. What are the observed genotype and allele frequencies?
### B. Given the observed allele frequencies, what are the genotypic frequencies expected under Hardy-Weinberg?  Using a chi-square test, how well do the observed genotype frequences agree with the HWE expecations?
### C. Simulate one generation of random mating (you don't need to code this simulation; it can be by hand):
        * Pair off the ten indivduals into mating pairs
        * Randomly pick two expected offspring genotypes per pair (10 offspring genotypes)
        * Create a new genotype table from the offsrping only (should only be 10 genotypes)
        * Repeat subqestions A and B on the new genotype table

**Answer Set A**
\
 observed genotypic frequency:
|Genotype|Frequency|
|--------|-----|
|A/A|$\frac{0}{10} = 0$|
|A/G|$\frac{10}{10} = 1$|
|G/G|$\frac{0}{10} = 0$|


allele frequency:
$A = \frac{(2 * 0) + 10}{20} = 0.5$
$G = \frac{(2 * 0) + 10}{20} = 0.5$

**Answer Set B**

genotypic frequencies expected under Hardy-Weinberg:

|Genotype|Frequency|Count|
|--------|-----|--------|
|A/A|$0.5^2 = 0.25$|$10*0.25 = 2.5$|
|A/G|$2 * 0.5 * 0.5 = 0.5$|$10*0.5 = 5$|
|G/G|$0.5^2 = 0.25$|$10*0.25 = 2.5$|

 Chi square: There is 1 degree of freedom due to the 3 genotypes and 2 alleles
$x^2 = \frac{(0-2.5)^2}{2.5} + \frac{(10-5)^2}{5} + \frac{(0-2.5)^2}{2.5} = 2.5 + 5 + 2.5 = 10$
    10 > 3.84 (value for 1 degrees of freedom) so observed frequencies DO NOT agree with HWE expectations

 
**Answer Set C**

    
|   	|   A	|  G 	|
|---	|---	|---	|
|   A	|  AA 	|   AG	| 
|   G	|  AG 	|   GG	| 


|Genotype|Count|
|--------|-----|
|A/A|4|
|A/G|3|
|GG|3|

observed genotype frequencies:

|Genotype|Frequency|
|--------|---------|
|AA|$\frac{4}{10} = 0.4$|
|AG|$\frac{3}{10} = 0.3$|
|GG|$\frac{3}{10} = 0.3$|

 allele frequencies:
$A = \frac{(2 * 4) + 3}{20} = \frac{11}{20} = 0.55$
$G = \frac{(2 * 3) + 3}{20} = \frac{9}{20} = 0.45$

 genotypic frequencies under HWE:
 
|Genotype|Expected Frequency|Expected Count|
|--------|---------|-----|
|AA|$(0.55)^2 = 0.3025$|$0.55^2 * 10 = 3.025$|
|AG|$2(0.55)(0.45) = 0.495$|$2 * 0.55 * 0.45 *10 = 4.95$|
|GG|$(0.45)^2 = 0.2025$|$0.45^2 * 10 = 2.025$|


Chi square: There are 1 degrees of freedom due to their being 3 genotypes and 2 alleles
$x^2 = \frac{(4-3.025)^2}{3.025} + \frac{(3-4.95)^2}{4.95} + \frac{(3-2.025)^2}{2.025} = 0.314 + 0.768 + 0.469 = 1.551$
1.551 < 3.84 so observed frequencies agree with HWE expectations

<br>

### 4. Take a look at Gel C below:


![img](./img/February%209%2C%202023/IMG_0524.jpeg)


Gel C is the banding pattern from two AFLP markers (the upper and lower sets of bands). These are presence/absence markers. So, there is a band or a null allele.

You could also read this as a table:

|Individuals|Genotype Upper Marker|Genotype Lower Marker|
|----------|-----------------------|--------------------|
|6|Absent|Present|
|101|Present|Absent|
|39|Present|Present|
|14|Absent|Absent|
    
    A. Estimate the frequency (q) of the null allele of each of the two AFLP markers assuming HWE.
    
    B. Estimate the percentage of *band-present* individuals (not the overall frequencies) that are heterozygous at each of the two markers.  What biological principle does the difference between these two percentages illustrate?

**Answer Set A**
\

|Genotypes| |
|-------------|-|
|BB|Band present|
|Bnb|Band present|
|nbnb|No Band Present|

Genotype frequencies for Bottom band:
|Genotype|Count|Frequency|Expected|
|--------|-----|--------|------------|
|BB, Bnb|$6 + 39 = 45$|$45/160 = 0.28$|$p^2 + 2pq$
|nbnb|$ 101+ 14 = 115$|$115/160 = 0.72$|$q^2$|


Genotype frequencies for Top band:
|Genotype|Count|Frequency|Expected|
|--------|-----|--------| ----------|
|BB, Bnb|$101 + 39 = 140$|$140/160 = 0.875$|$p^2 + 2pq$|
|nbnb|$6+ 14 = 20 $|$20/160 = 0.125$|$q^2$|


frequency of null alleles:
Bottom Band: $q = \sqrt{0.72} = 0.85$
Top Band: $q = \sqrt{0.125} = 0.354$

**Answer Set B**

$x^2 = \frac{(4-3.025)^2}{3.025} + \frac{(3-4.95)^2}{4.95} + \frac{(3-2.025)^2}{2.025} = 0.314 + 0.768 + 0.469 = 1.551$

Bottom band:
$ band present indivs = \frac{2pq}{p^2+2pq} = \frac{2* (1-0.85) *0.85}{0.28} = 0.910$


Top band:
$\frac{2pq}{p^2+2pq} = \frac{2* (1-0.354) *0.354}{0.875} = 0.522$

> The difference between these two percentages illustrates that as the band-present allele becomes rarer, a greater proportion of them are heterozygotes at HWE.

### 5.  A highly isolation colony of the month *Panaxia dominula* near Oxford, England has been instenstively studied by Ford and collaborators over the period of 1928-1968 (Ford and Sheppard 1969).  This speices has one generation per year, and estimates of the population size were caried out yearly begnining in 1941.  For the years 1950-1961, inclusive, estimates of the population size were: 

|Year| Individuals|
|------|----------|
| 1950 | 4100 |
| 1951 | 2250 |
| 1952 | 6000 |
| 1953 | 8000 |
| 1954 | 11000 |
| 1955 | 2000 |
| 1956 | 11000 |
| 1957 | 16000 |
| 1958 | 15000 |
| 1959 | 7000 |
| 1960 | 2500 |
| 1961 | 1400 | 
   * Assuming that the actual size of the population in any year equals the effective population size in that year, estimate the average effective number over the entire 12-year period.
  
**Answer Set 5**

$N_e = \frac{t}{\sum (\frac{1}{N_i})}$
$N_e = \frac{12}{\frac{1}{4100}+\frac{1}{2250}+\frac{1}{6000}+\frac{1}{8000}+\frac{1}{11000}+\frac{1}{2000}+\frac{1}{11000}+\frac{1}{16000}+\frac{1}{15000}+\frac{1}{7000}+\frac{1}{2500}+\frac{1}{1400}}$
$N_e = 3936$

### 6. A dairy farmer has a herd consisting of 200 cows and 2 bulls. What is the effective population size?

**Answer Set 6**
$N_e = \frac {4N_fN_m}{N_f + N_m}$
$N_e = \frac{4 * 200 * 2}{200 + 2} = \frac{1600}{202}=7.92$

### 7.  A rare triggerplant from Australia (*Stylidium coroniforme*) has only five known populations (Coates 1992).  One of these populations has been monitored for several years, and over five years in the early 1980s: 2, 3, 25, 32, and 86 plants were recoreded.  Assuming *N<sub>e</sub>* = *N<sub>c</sub>* in that year, estimate *N<sub>e</sub>* as well as the average *N<sub>c</sub>* over this period.  What biological principle is illustrated by this example?

$N_e = \frac{5}{\frac{1}{2}+\frac{1}{3}+\frac{1}{25}+\frac{1}{32}=\frac{1}{86}} = 5.46$

>The biological principle exhibited by this example is the bottleneck effect which shows that "a rapid expansion in numbers does not affect the previous loss of genetic varation; it merely reduces the current rate of loss" pg 139 in book

### 8.  You genotype a species of grasshopper along a transect in the European Alsp.  Near Munich, Germany, you sample 120 individuals; near Inssbruck, Austria, you sample 122 individuals;  near Verona, Italy you sample 118 individuals. You find the following genotypes:

| Locality| A<sub>1</sub>A<sub>1</sub> | A<sub>1</sub>A<sub>2</sub> | A<sub>2</sub>A<sub>2</sub>|
|---------|--------------|---------|---------|
|Munich| 6|33|81|
|Innsbruck| 20|59|43|
|Verona|65|39|14|

* Calculate the frequencies of the two alleles in each population
* Do any populations have excess heterozygotes?
* Do any populations have a deficit of heterozygotes?
* Calculate *F<sub>IS</sub>* for each of the populations and how does this related to B and C?
   * Hint: this the equation $F_{IS} = \frac{H_S - H_I}{H_S}$
   * I suggest looking it up, but you can likely figure it out from context
   
* Calculate the frequencies of the two alleles in each population

Total individuals per population:
Munich: 120
Innsbruck: 122
Verona: 118

Genotype Frequencies:

|Locality|A<sub>1</sub>A<sub>1</sub> | A<sub>1</sub>A<sub>2</sub> | A<sub>2</sub>A<sub>2</sub>|
|---------|--------------|---------|---------|
|Munich|$\frac{6}{120} = 0.05$|$\frac{33}{120} = 0.275$|$\frac{81}{120} = 0.675$|
|Innsbruck|$\frac{20}{122} = 0.164$|$\frac{59}{122} = 0.484$|$\frac{43}{122} = 0.352$|
|Verona|$\frac{65}{118} = 0.551$|$\frac{39}{118} = 0.331$|$\frac{14}{118} = 0.119$|

Allele Frequencies:

|Locality|A<sub>1</sub>|A<sub>2</sub>|
|---------|--------------|---------|
|Munich|$\frac{2*6 + 33}{2*120} = 0.188$|$\frac{2*81 + 33}{2*120} = 0.275 = 0.813$|
|Innsbruck|$\frac{2*20 + 59}{2* 122} = 0.406$|$\frac{2*43 + 59}{2*122} = 0.594$|
|Verona|$\frac{2*65 + 39}{2*118} = 0.716$|$\frac{2*14 + 39}{2* 118} = 0.284$|

* Do any populations have excess heterozygotes?

Expected genotype frequencies: 

|Locality|A<sub>1</sub>A<sub>1</sub> | A<sub>1</sub>A<sub>2</sub> | A<sub>2</sub>A<sub>2</sub>|
|--------|-------------|-------------|--------------|
|Munich|$0.188^2 = 0.035$|$2 * 0.188 * 0.813 = 0.305$|$0.813^2 = 0.661$|
|Innsbruck|$0.406^2 = 0.165$|$2 * 0.406 * 0.594 = 0.482$|$0.594^2 = 0.353$|
|Verona|$0.716^2 = 0.513$|$2 * 0.716 * 0.284 = 0.407$|$0.284^2 = 0.081$|

Expected Genotype Counts
|Locality|A<sub>1</sub>A<sub>1</sub> | A<sub>1</sub>A<sub>2</sub> | A<sub>2</sub>A<sub>2</sub>|
|--------|---------------------------|----------------------------|---------------------------|
|Munich|$0.035 * 120 = 4.2$|$0.305 * 120 = 36.6$|$0.661 * 120 = 79.32$|
|Innsbruck|$0.165 * 122 = 20.13$|$0.482 * 122 = 58.84$|$0.353 * 122 = 43.07$|
|Verona|$0.513 * 118 = 60.53$|$0.407 * 118 = 48.03$|$0.081 * 118 = 9.56$|

|Locality|$H<sub>o</sub> - H<sub>e</sub>$|
|--------|--------|
|Munich|$33-36.6 = -3.6$|
|Innsbruck|$59-58.84 = 0.16$|
|Verona|$39-48.03 = -9.03$|

* Do any populations have excess heterozygotes?
>  Innsbruck has a very slight excess of heterozygotes

* Do any populations have a deficit of heterozygotes?
> Yes, Verona has a significant deficit of heterozygotes and Munich has a slight deficit of heterozygotes 

* Calculate *F<sub>IS</sub>* for each of the populations and how does this related to B and C?
   * Hint: this the equation $F_{IS} = \frac{H_S - H_I}{H_S}$
   * I suggest looking it up, but you can likely figure it out from context
   
Locality|F<sub>IS|
|-------|-------|------|
|Munich|$1-\frac{0.275}{0.305} = 0.098$|
|Innsbruck|$1-\frac{0.484}{0.482} = -0.004$|
|Verona|$1-\frac{0.331}{0.407} = 0.187$|   

> F<sub>IS</sub> < 0 indicates a deficit of heterozygotes/excess of homozygotes therefore Innsbruck has a deficit of heterozygotes. F<sub>IS</sub> > 0 indicates a deficit of heterozygotes/excess of homozygotes so Verona and Munich have a heterozygote deficit. Verona has twice the heterozygote deficit of Munich.  

### 9.  The fly *Eurosta solidaginis* forms galls (enlarged areas) on goldenrod plants within which the fly larvae feed and develop.  A study of allozyme frequencies in 21 subpopulations of *E. solidaginis* on two different species of goldenrod distributed from Minnesota to Maine (Waring et al. 1990) produced the following estimates of *F<sub>ST</sub>*:

>* Calculate the expected number of migrants per generation for each locus.  What is your interpretation of these data?  Do you think the differentiation at these loci is caused soley by a balance between migration and drift?  Why or why not?

>* Most of the differentiation at *HBDH-1* show in the data occurs btween the two species of host plants; nine of the subpopulations occured on *Solidago altissima* and the other 12 subpops were on *S. gigantean*.  The frequency of one of the two *HBDH* alleles is 0.84 on *S. altissima* and 0.13 on *S. gigantea*.  How does this affect your interpretation of the results?

|Locus | *F<sub>ST</sub>* |
|------|------------------|
| *GAP-1*| 0.10|
| *TPI-1*| 0.11|
| *IDH-1*| 0.02|
| *HBDH-1*| 0.62|
| *GPD-1*| 0.11|
| *PGM-1*| 0.14|


* Calculate the expected number of migrants per generation for each locus.  What is your interpretation of these data?  Do you think the differentiation at these loci is caused soley by a balance between migration and drift?  Why or why not?

$mN= \frac{1-F_{ST}}{4F_{ST}}$

|Locus | *F<sub>ST</sub>* |mN|
|------|------------------|----|
| *GAP-1*| 0.10|$\frac{1-.1}{4(.1)}= 2.25$|
| *TPI-1*| 0.11|$\frac{1-.11}{4(.11)}= 2.02$|
| *IDH-1*| 0.02|$\frac{1-.02}{4(.02)}= 12.25$|
| *HBDH-1*| 0.62|$\frac{1-.62}{4(.62)}= 0.153$|
| *GPD-1*| 0.11|$\frac{1-.11}{4(.11)}= 2.02$|
| *PGM-1*| 0.14|$\frac{1-0.14}{4(.14)}= 1.54$|

>  I believe that the differentiation found at all loci except for IDH-1 and HBDH-1 appear to be due to a balance between migration and drift. IDH-1 has a comparatively low F<sub>ST</sub and high mN and HBDH-1 has a comparatively high F<sub>ST</sub and very low mN. Because all other loci have ~2 for mN it is clear that these loci are likley not selectively neutral.  

* Most of the differentiation at *HBDH-1* show in the data occurs between the two species of host plants; nine of the subpopulations occured on *Solidago altissima* and the other 12 subpops were on *S. gigantean*.  The frequency of one of the two *HBDH* alleles is 0.84 on *S. altissima* and 0.13 on *S. gigantea*.  How does this affect your interpretation of the results?

> This result indicates that the *Solidago altissima* allele is experiencing positive directional selection and that the HBHD- 1 locus is correlated with a local adaptation. 

### 10. Levin (1978) studied allele frequencies at the 6-*pgd* allozyme locus in 73 sub-populations of the self-incompatible species *Phlox drummondi*. Of these 73 subpopulations, **66 were fixed for the a allele**, with allele frequencies and observed heterozygosities at the other loci given below (Levin's original subpopulation numbering altered for simplicity):

|Subpopulation |*p* |*H<sub>O</sub>* |
|--------------|----|----------------|
|1-66|1|0|
|67|0.86|0.06|
|68|0.80|0.12|
|69|0.70|0.20|
|70|0.96|0.03|
|71|0.96|0.09|
|72|0.73|0.15|
|73|0.91|0.06|

* Calculate the three F-statistics for these data and check to make sure they have the correct mathematical relationship. 

>Necessary equations:
>$$F_{ST} = 1 - \frac{H_S}{H_T}$$
>$$F_{IS} = 1 - \frac{H_I}{H_S}$$
>$$F_{IT} = 1 - \frac{H_I}{H_T}$$
>H<sub>I</sub> = average observed heterozygosity across subpops\
>H<sub>S</sub> = average expected heterozygosity across subpops\
>H<sub>T</sub> = average expected heterozygosities for overall total population

>|Subpopulation |*p*|*q*|*H<sub>E</sub>(2pq)*|*H<sub>O</sub>* |
>|--------------|----|-------|---------|---|
>|1-66|1|0|0|0|
>|67|0.86|0.14|0.24|0.06|
>|68|0.80|0.2|0.32|0.12|
>|69|0.70|0.3|0.42|0.20|
>|70|0.96|0.04|0.08|0.03|
>|71|0.96|0.04|0.08|0.09|
>|72|0.73|0.27|0.39|0.15|
>|73|0.91|0.09|0.16|0.06|

>|Subpopulation|*$$\bar{p}$$*|*$$\bar{q}$$*|*$$H_T$$*|
>|---|---|---|---|
>|all|0.985|0.015|0.03|

>$$H_I=\frac{(66*0) +0.06 + 0.12 + 0.20 + 0.03 + 0.09 + 0.15 + 0.06}{73}= 0.0097$$
>$$H_S=\frac{(66*0)+0.24+0.32+0.42+0.08+0.08+0.39+0.16}{73}=0.0232$$
>$$H_T=2\bar{p}\bar{q} = 2(0.985)(0.015)=0.0296$$

>$$F_{IS} = 1 - \frac{H_I}{H_S}=1-\frac{0.0097}{0.023}= 0.582$$
>$$F_{ST} = 1 - \frac{H_S}{H_T} = 1-\frac{0.023}{0.03}= 0.233$$
>$$F_{IT}= 1- \frac{H_I}{H_T}=1-\frac{0.0097}{0.03} = 0.677$$

* Do these comparisons fit your expectations based on the mating systems of this species? Why or why not? If not, do you have a possible explanation for the lack of fit?

 > F<sub>IS</sub> in this example is relatively high at 0.582 which indicates a significant deficit of heterozygotes. As indicated in the problem description this species is self-incompatible which makes a high F<sub>IS</sub> value like this unlikely. A likely explanation for this results is the Wahlund effect which occurs if there are multiple demes in a subpoopulation that was not previously accounted for. 

* Calculate *N<sub>e</sub>m* from these data.  If the migration rate *m* was found to be 0.1, what would the estimate of *N<sub>e</sub>* be?
>$$N_em = \frac{1-F_{ST}}{4F_{ST}} =\frac{1-0.23}{4(0.23)} = 0.84$$
>$$N_e = \frac{0.84}{.1}=8.4$$

* Now assume that *N<sub>e</sub>* is very large, 6-*pgd* is neutral in these subpopulations, and the migration rate is still 0.1. What would the frequencies of the *a* allele in subpopulations 68 and 69 after 10 generations be? After 25 generations? What biological principle is illustrated by these results?
>We would need to use the following equation:
$$p_t = \bar{p} + (p_0 - \bar{p}) (1 - m)^t$$
$$m = 0.1$$
$$\bar{p} = 0.985$$
for population 68: $$p_0 = 0.8$$
for population 69: $$p_0 = 0.7$$

|Subpopulation|10 generations|25 generations|
|-------------|--------------|--------------|
|68|$$p_10 = 0.985 + (0.8-0.985)(1-0.1)^10)= 0.92$$|$$p_25 = 0.985 + (0.8-0.985)(1-0.1)^25)= 0.97$$|
|69|$$p_10 = 0.985 + (0.7-0.985)(1-0.1)^10)= 0.88$$|$$p_25 = 0.985 + (0.7-0.985)(1-0.1)^25)= 0.96$$|

> This example shows that over the course of 25 generations that migration would reduce the genetic differentiation of the subpopulations as both populations are headed toward fixation for the same allele. 

### 11. In *D. melanogaster*, curly wings is due to a dominant allele C<sub>*y*</sub> that is lethal when homozygous. A population is established with an initial frequency of C<sub>*y*</sub> equal to 0.168. Calculate the expected frequency in the next generation, assuming.

* The relative fitness of +/+ : C<sub>*y*</sub>/+ is 1:1.
$$w_Cy_Cy = 0$$
$$w_Cy+ = 1$$
$$w_++ = 1$$

$$q = 0.168$$
$$p = 0.832$$

Need the equation: 
$$p^\prime= \frac {p^2w_{11} + pqw_{12}}{p^2w_{11}+2pqw_{12} + q^2w_{22}}$$


$$p^\prime =\frac {0.168^2*0 + 0.168*(1-0.168)*1}{0.168^2*0 +2*0.168*(1-0.168)*1 + (1-0.168)^2*1} = 0.144$$
      
* The relative fitness of +/+ : C<sub>*y*</sub>/+ is 1:0.5.

$$w_11 = 0$$
$$w_12 = 0.5$$
$$w_22 = 1$$

Need the equation: 
$$p^\prime= \frac {p^2w_{11} + pqw_{12}}{p^2w_{11}+2pqw_{12} + q^2w_{22}}$$

$$p^\prime =\frac {0.168^2*0 + 0.168*(1-0.168)*0.5}{0.168^2*0 +2*0.168*(1-0.168)*0.5 + (1-0.168)^2*1} = 0.084$$


### 12. If the fitnesses of the genotypes A<sub>1</sub>A<sub>1</sub>, A<sub>1</sub>A<sub>2</sub>, and A<sub>2</sub>A<sub>2</sub> are 1.5, 1.1, and 1.0, respectively, what are the values of the selection coefficient and the heterozygous effect?

|Genotype|Fitness|Relative Fitness|
|--------|--------|--------|
|A<sub>1</SUB>A<sub>1|1.5|$$1.5/1.5 = 1$$|
|A<sub>1</SUB>A<sub>2|1.1|$$1.1/1.5 = 0.73 = 1-hs$$|
|A<sub>2</SUB>A<sub>2|1.0|$$1/1.5 0.66 = 1-s$$|

$$s = 1-0.66 = 0.34$$ 
$$h=\frac{0.27}{0.34}=0.79$$

### 13. Industrial melanism refers to the dark pigmentation that evolved in some insects, giving them protective coloration on vegetation darkened by soot in heavily industrialized areas prior to the requirement for smokestack filtration. In one heavily polluted area near Birmingham, England in 1956, 87% of moths of the species *Biston betularia* had black bodies due to the presence of a dominant gene for melanism (Kettlewell 1956). 

* Estimate the frequency of the dominant allele in this population and the frequency of melanics that are heterozygous.
>$$p^2 +2pq = 0.87$$
>$$q^2 = 0.13$$
>$$q=\sqrt{0.13}=0.36$$
>$$p=1-0.36=0.64$$
>$$2pq = H_O = 2(0.36)(0.64)=0.46$$

Melanics that are heterozygous: 
$$\frac{2pq}{p^2 + 2pq} = \frac{0.46}{0.87} = 0.539$$ 

* In this species, the frequency of melanic moths increased from a value of 1% in 1848 to a value of 95% in 1898.  The species has one generation per year.
  * Estimate the approximate value of the selection coeffecient *s* against non-melanics that would be necessary to account for the change in the frequency of the melanic forms.

> The melanic moth color is due to dominant allele. Therefore...
> $q_{0} = \sqrt{1-0.01} = \sqrt{0.99}= 0.995$

> $p_{0} = 1 - 0.995 = 0.005$

> $q_{50} = \sqrt{1-0.95} = 0.224$

> $p_{50} = 1 - 0.224 = 0.776$

 > $st = \ln{\frac{p_{t}}{q_{t}}} + \frac{1}{q_{t}} - \ln{\frac{p_{0}}{q_{0}}} - \frac{1}{q_{0}}$ 

 > $st=\ln{\frac{0.776}{0.224}} + \frac{1}{0.224} - \ln{\frac{0.005}{0.995}} - \frac{1}{0.995} = 9.98$   

 >$s = \frac{6.81}{50} = 0.2$
         
* How many generations would be required for the same change in frequency of melanic forms in a hypothetical case in which the allele for melanism is recessive, assuming the same value of *s* against nonmelanics

> $p_{0} = \sqrt{0.01} = 0.1$

> $q_{0} = 1- 0.1 = 0.9$

> $p_{50} = \sqrt{0.95} = 0.97$

> $q_{50} = 1- 0.97 = 0.03$

> $st = \ln{\frac{p_{t}}{q_{t}}} + \frac{1}{p_{t}} - \ln{\frac{p_{0}}{q_{0}}} - \frac{1}{p_{0}}$

> $st = \ln{\frac{0.97}{0.03}} + \frac{1}{0.97} - \ln{\frac{0.1}{0.9}} - \frac{1}{0.1}$

> $st = 3.48 + 1.03 + 2.19 - 10 = -3.3 $

> $t = \frac{-3.3}{0.2} = -9.8$

This does not make sense biologically but I believe the math is correct

### 14. Cross and Birley (1986) studied restriction site variation in the region of alccohol dehydrogenase (*Adh*)gene of *D. melanogaster* in a  population descended from flies trapped at a Dutch fruit market in Groningen.  The following data was collected:

| *Adh* Allele | *Eco*RI Allele| Individuals|
|-------------|----------------|------------|
*Adh<sup>F</sup>*| *Eco*RI<sup>+</sup> | 22|
*Adh<sup>S</sup>*| *Eco*RI<sup>+</sup> | 4|
*Adh<sup>F</sup>*| *Eco*RI<sup>-</sup> | 3|
*Adh<sup>S</sup>*| *Eco*RI<sup>-</sup> | 5|

Where *Adh<sup>F</sup>* and *Adh<sup>S</sup>* are the allozyme alleles of *Adh* and *Eco*RI<sup>+</sup> and *Eco*RI<sup>-</sup> indicate the presence or absence of an *Eco*RI restriction site 3.5 kb downstream
   * Test for the presence of linkage disequilibrium
   * If significant, express *D* relative to its theoretical maximum or minimum.

>| *Adh* Allele | *Eco*RI Allele| Individuals|G|
>|-------------|----------------|------------|--|
>*Adh<sup>F</sup>*| *Eco*RI<sup>+</sup> | 22|$\frac{22}{34}=0.647$|
>*Adh<sup>S</sup>*| *Eco*RI<sup>+</sup> | 4|$\frac{4}{34}=0.118$|
>*Adh<sup>F</sup>*| *Eco*RI<sup>-</sup> | 3|$\frac{3}{34}=0.088$|
>*Adh<sup>S</sup>*| *Eco*RI<sup>-</sup> | 5|$\frac{5}{34}=0.147$|

>$$D = G_1G_4 - G_2G_3$$
>$$D = (0.647)(0.147)-(0.118)(0.088)=0.095-0.010 = 0.085$$

> The allele frequency of $Adh^F = p_1 = \frac{(22 + 3)}{34} = \frac{25}{34} = 0.735$

> The allele frequency of $Adh^S = q_1 = 1 - 0.735 = 0.265$

> The allele frequency of $EcoRI^+ = p_2 = \frac{(22 + 4)}{34} = 0.765$

> The allele frequency of $EcoRI^- = q_2 = 1 - 0.765 = 0.235$

>| *Adh* Allele | *EcoRI* Allele | Observed |Expected Frequency (linkage equilibrium) |Chi Square|
>|-------------|----------------|----------|--------------------|------|
>| *Adh<sup>F</sup>* | *EcoRI<sup>+</sup>* |22|$0.735 *  0.765 *  34 = 19.07$| $\frac{(22 - 19.07)^2}{19.07} = 0.45$|
>| *Adh<sup>S</sup>* | *EcoRI<sup>+</sup>* |4 |$ 0.265 * 0.765 * 34 = 6.87 $ |$\frac{(4 - 6.87)^2}{6.87} = 1.2$|
>| *Adh<sup>F</sup>* | *EcoRI<sup>-</sup>* | 3|$ 0.735 * 0.235 * 34 = 5.84 $ |$\frac{(3 - 5.84)^2}{5.84} = 1.38$|
>| *Adh<sup>S</sup>* | *EcoRI<sup>-</sup>* | 5|$ 0.265 * 0.235 * 34 = 2.22 $ |$\frac{(5 - 2.22)^2}{2.22} = 3$|

> $x^2 = 0.45 + 1.2 + 1.38 + 3 =4.77$

> In this case we have one degree of freedom so $4.77 > 3.84 $ therefore there is a presence of linkage disequilibrium

>  $ D' = \frac{D}{Dmax}$

> $D_{max} = min(p_1q_2,p_2q_1) = min(0.735*0.235, 0.265*0.765) = min(0.173,0.202)$

> $D' = \frac{0.085}{0.173} = 0.49$

> There is a significant effect of linkage disequilibrium between Adh and EcoRI loci in this population

### 15. Three linked loci in a random mating population have the gametic frequencies shown in the table below. Calculate the linkage disequilibrium *D*/*D<sub>max</sub>* between each pair of genes. Explain why the results seem paradoxical.

|Genotype | Frequency|
|---------|------|
| *ABC*| 0.25|
| *ABc*| 0|
| *AbC*| 0.25|
|*Abc*| 0|
|*aBC* | 0|
|*aBc* | 0.25|
|*abC* | 0|
|*abc*|0.25|

>From looking at the table it is clear to me that there is linkage between the a and c loci and no clear linkage between b and a or b and c 

>|Allele|Frequency|
>|-----|----------|
>|A|0.5|
>|a|0.5|
>|B|0.5|
>|b|0.5|
>|C|0.5|
>|c|0.5|


LD between A and B:

>$D_{AB} = f(AB)f(ab) - f(Ab)f(aB)$

>$D_{AB} = (f(ABC) + f(ABc))(f(abc) + f(aBc)) - (f(AbC) + f(Abc))(f(aBC) + f(aBc))$

>$D_{AB} = (0.25 + 0)(0 + 0.25) - (0.25 + 0)(0 + 0.25) = 0$


LD between A and C:
> $D_{AC} = f(AC)f(ac) - f(Ac)f(aC)$

> $D_{AC} = (f(ABC) + f(AbC))(f(abc) + f(aBc)) - (f(ABc) + f(Abc))(f(aBC) + f(abC))$

>$D_{AC} = (0.25 + 0.25)(0.25 + 0.25) - (0 + 0)(0 + 0) = 0.25$


LD between B and C:
> $D_{BC} = f(BC)f(bc) - f(Bc)f(bC)$

> $D_{BC} = (f(ABC) + f(aBC))(f(abc) + f(Abc)) - (f(ABc) + f(aBc))(f(abC) + f(AbC))$

> $D_{BC} = (0.25 + 0)(0+ 0.25) - (0 + 0.25)(0 + .25) = 0$

get $D'$

> $D_{max} = 0.25$

>$D'_{AB} = \frac{D_{AB}}{D_{max}} = \frac{0}{0.25} = 0$

>$D'_{AC} = \frac{D_{AC}}{D_{max}} = \frac{0.25}{0.25} = 1$

>$D'_{BC} = \frac{D_{BC}}{D_{max}} = \frac{0}{0.25} = 0$

> The results seem paradoxical because you would assume that all loci are in  disequilibrium due to their only being 4 gamete types, but in reality AB and BC are in equilibrium and only AC are in gametic disequilibrium.

### 16. Two populations are examined for the same pair of loci with the following results in terms of two-locus gamete numbers:

> N of Pop 1 = 1000

> N of Pop 2 = 10,000

> N of Pop 3 = 11,000

|Population|Gamete| Count|G|
|----------|------|-------|---|
| Pop 1| AB | 720|G1 = 0.72|
| Pop 1| Ab | 180|G2 = 0.18|
| Pop 1| aB | 80|G3 = 0.08|
| Pop 1| ab | 20|G4 = 0.02|
| Pop 2| AB | 300|G1 = 0.03|
| Pop 2| Ab | 2700|G2 = 0.27|
| Pop 2| aB | 700|G3 = 0.07|
| Pop 2| ab | 6300|G4 = 0.63|


These two populations are now combined to form a third:

|Population|Gamete| Count|G|
|----------|------|-------|---|
| Pop 3| AB | 1020|G1 = 0.093|
| Pop 3| Ab | 2880|G2 = 0.262|
| Pop 3| aB | 780|G3 = 0.071|
| Pop 3| ab | 6320|G4 = 0.575|


Calculate the two-locus gamete frequencies for each population and the gameticphase imbalance (linkage disequilibrium). Is any population out of linkage equilibrium?
> Pop 1:$$ D = G_1G_4 - G_2G_3 = (0.72)(0.02)-(0.18)(0.08)$$
>$$D = 0.0144 - 0.0144$$
>$$D = 0$$

> Pop 2:$$ D = G_1G_4 - G_2G_3 = (0.03)(0.63)-(0.27)(0.07)$$
>$$D = 0.0189 - 0.0189$$
>$$D = 0$$

>Both populations are in linkage equilibrium 

What is the effect of pooling of the two populations on linkage equilibrium?
> Pop 3:$$ D = G_1G_4 - G_2G_3 = (0.093)(0.262)-(0.071)(0.575)$$
>$$D = 0.053 - 0.0186$$
>$$D = 0.034$$

> Population 3 is not in linkage equilibrium which shows the Wahlund Effect where distinct genetic subpopulations lead to LD 

Suppose that the recombination rate between loci A/a and B/b is 0.1. What is the expected disequibrium in the offspring of population 3 (the parental gene pool), assuming random mating? In the second generation?

   >1. Disequilibrium in offspring of parental gene pool:
   >$$D'=D(1-r)$$
   >$$D'=0.034(0.9)=0.031$$
   >2. Disequilibrium in second generation: 
   >$$D_t=D_0(1-r)^t$$
   >$$D_t=0.034(0.9)^2=0.028$$

 Can this single episode of admixture be detected in the population established from population 3 after two generations of random mating?

>The episode of admixture can be still be detected from the second generation due ot the fact that the population is still in some level of disequilibrium (0.0281)

 Can it be detected in the genotype frequencies at the A/a locus after two generations of random mating? 
 Can it be detected in the genotype frequencies at the B/b locus after two generations of random mating?
 
 Allele Frequencies at t = 0: 

>$$p_1 = A = \frac{1020+2880}{11000} = 0.035$$
>$$q_1 = a = 1-0.035 =0.65$$

>$$p_2 = B = \frac{1020+780}{11000} = 0.164$$
>$$q_2 = b = 1-0.1636=0.836$$

Genotype Frequencies:
> $f(AB)_2 = p_1 p_2 + D_2$ = $(.035)(.164) + 0.028 = 0.034$

> $f(Ab)_2 = p_1 q_2 - D_2$ = $(.035)(.836) - 0.028 = 0.001$

> $f(aB)_2 = q_1p_2 - D_2$ = $(.65)(.164) - 0.028 = 0.079$

> $f(ab)_2 = q_1q_2 + D_2$ = $(.65)(.836) + 0.028 = 0.571$

> This confirms that yes you can detect linkage disequilibrium in the genotype frequences after two generations of random mating. 


 ### 17.  A continuous trait is distributed approximately according to a normal distribution with mean 100 and standard deviation of 15. What proportion of the population is expected to have a phenotypic value above 130? Below 85? Above 85

 Using https://homepage.divms.uiowa.edu/~mbognar/applets/normal.html

>1. 2.28% of the population is expected to have a phenotypic value above 130
>2. 15.87% of the population is expected to have a phenotypipic value below 85
>3. 84.13% of the population is expected to have a phenotypipic value above 85

### 18. A genetically heterogeneous population of wheat has a variance in the number A days to maturation of 40, whereas two inbred populations derived from it have a variance in the number of days to maturation of 10.  
   * What is the genotypic variance (V<sub>G</sub> or $\sigma_{g}^2$), the environmental variance (V<sub>E</sub> or $\sigma_{e}^2$), and the broad sense heritablilty *H*<sup>2</sup>, of days to maturation in this population?
      > * $V_P: 40 = V_G + V_E$ 

      for inbred population: no genetic variance $ V_P = V_E = 10$
      > * $V_G = 40 - 10 = 30$
      > * $V_E = 10$
      > * broad sense heritability: $\frac{V_G}{V_P} = \frac{30}{40} = 0.75$

   * If the inbred lines were crossed, what would be the predicted variance in days to maturation of the F<sub>1</sub> generation?
      > * the predicted variance in days to maturation of the F<sub>1</sub> would be 10 because the F<sub>1</sub> would have no genetic variance 

### 19. In comparing a quantitative trait in the F<sub>1</sub> and F<sub>2</sub> generations obtained by crossing two highly inbred strains:

* Which set of progeny provides an estimate of the environmental variance?

>The F1 generation provides a better estimate of the environmental variance because each inbred line has essentially no genotypic variance so when crossed there are little genetic differences between offspring

* What determines the variance of the other set of progeny?

>the variance of the F2 generation is determined by the genotypic and environmental variance

### 20. In a cross between two cultivated inbred varieties of tobacco, the variance in leaf number per plant in the F<sub>1</sub> generation is 1.46 and in the F<sub>2</sub> generation it is 5.97. 

What are the genotypic and environmental variances? What is the broad-sense heritability in leaf number?

   > * F1 genotypic variance: $0$ (offspring are all ~ genetically identical)
   > * F1 environmental variance: $1.46$


   > * F2 genotypic variance: $5.97-1.46=4.51$
   > * F2 environmental variance: $ 1.46 $ (environment is same as F1)
   > * Broad sense hertitability: $\frac{4.51}{5.97}=0.755$











   

