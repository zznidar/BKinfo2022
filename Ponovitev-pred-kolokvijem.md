Blast: kje vidiš velikosti zbirk: pri Search Summary nekje.  
Kjer izbiraš podatkovno bazo (pri iskanju), ti vprašajček izpiše, koliko sekvenc je v bazi.   
Število nt pa je v search summary ("**Number of letters**")  

Query subrange: če iščeš samo del zaporedja

Na UniProtu: če pri domeni Blastaš, ti išče samo to domeno.

Če se ti kje zatakne, je dovoljeno iti pod Help. Tudi na Pavšičevo une. Google je tudi dovoljen. Kolokvij traja 1 uro.

Cytoscapa najverjetneje ne pričakovati (ni pa ziher).  


# PubMed
Na levem delu filtriraš variante (clinical trial, free access, review ...)

# GenBank
Ekson je anotiran; na 3'-koncu je poli-A signal, zato je največ A-ja  
Na kolokviju so baje dost podobna vprašanja  
tRNA nima zgolj običajnih nt (tudi to je anotirano)  
mRNA: 3' netransliran del je daljši kot 5'
* stabilnost in vezavna mesta za miRNA (regulacija)

Najdaljše zaporedje: advanced search, organisem: human -> filter: mRNA -> Sort by seq len => titin.  
Smiselno je gledati referenčna zaporedja; ref protein: xy aa  

# UniProt
trans-mb regije: v topologiji  
disulfidi: post-transl.  
lokacija: tudi v nekem subheadingu

**cistin** === disulfidna vez  
also, 2 cisteina se povežeta, nastane 1 cistin.  
EPCAM: so navedene S-S vezi; 6 zunajcel (24–265). disulfidnih vezi, ki povezujejo 12 cisteinov.  
Miraculin: ima še 1 interchain S-S vez, torej ima 7 oksidiranih cisteinov (6 davon: intramol.; 1 intermol.)

### Kako pokvariti neraziskan encim (konjska triptaza)?  
tryptase organism:horse -> Tryptase gamma 1 (ni anotirana) => poiščemo sorodne iz drugih organizmov, ki so anotirani.  
Tryptase gamma (npr. človeška, mišja ...): so označeni active site.  
Oba dodamo v basket, ju alignamo kar v Uniprotu (_lahko potem vključiš anotacije od UniProta_) -> Highlight: Active Site. Pobarva samo človeško. 

Katalitična triada: histidin, aspartat, serin (nukleofil, napade peptidno vez) => serin zmutiramo v alanin.

### Adam28: podobno
le da je ta dobro anotiran (ak 340); kofaktor: cink; topnost: Extracellular domain; za aktivnost zadostuje peptidaza.  
Ekspresijski sistem: post-transl. mod. => **insekti primernejši** [^1]

[^1]: Bakterije ne vršijo disulfidnih vezi, glikozilacije ... 

# ProtParam
pI, naboj, M, deleži ak, $\varepsilon_0$ ...  
pI = 5,39; protein bo pri pH 8 negativno nabit => anionski izmenjevalec

# Dotplot
Emboss DotMatcher  
myotilin, porvnava samega s sabo; window size mal povečaš (40)

Zanima nas, v katerih delih se pojavijo črtice (podobne domene)

# Poravnave
Podobna zaporedja (izooblike): globalna (prbl. enako dolge seq, homologna)  
lokalne: za domene iz zelo evolucijsko oddaljenih proteinov.

# Blastx
nt-zaporedje -> protein, v vseh 6 bralnih okvirjih

Homologi: vnparej definiraš ogranizem

Kratka zaporedja imajo velik E-value (ujemanje je posledica naključnosti)

# Ortologi (miška)
Kako veš, da si našel ortolog? Reverse blast.  
Protein A v 1, not v 2, uporabiš za iskanje ortologov v 2. Najdeš 3 proteine, ki so si med sabo homologi. But are they ortologs to A?   
* Vzameš katergakoli od teh 3 in ga daš v Blast
* Zdej najdeš nek drug protein != A iz 1 (najnižji E-value), torej nista ortologa. 
    * Should you find A, bi bila ortologa.

E < 10^-50: skoraj identično  
10^-30 < E < 10^-50: najbrž homologa (preveri bio-relevantnost)  
E > 10^-6: ni povezave

Za iskanje homologov je bolj smiselno ak-seq, ker bolje ohranjeno.

# Virusni genom
daš v blast. Je koronavirus. Poiščeš genom v GenBanku

# PSI-BLAST $\varPsi$
3x  
ne najdemo nič pametnega, dobimo 2 kandidata nad thresholdom -> blast pripravi poravnavo, matriko substitucij ... -> repeat, nova 2 -> 3. iteracija z 200 zadetki

# Grafi
we found clusters!  
geneOntology: clustri so udeleženi v podobnih bio-procesih.

# Strukture, blastp
ak -> podobne ak iz zbirke pdb  

# homologija: swiss-model
primerjava z alpha-foldom ali experimentom