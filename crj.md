


















* Sets for POS sub-categories





* Sets for Semantic tags





* Sets for Morphosyntactic properties






































































































































































* Sets for verbs


    - V is all readings with a V tag in them, REAL-V should
be the ones without an N tag following the V.  
The REAL-V set thus awaits a fix to the preprocess V ... N bug.



* The set COPULAS is for predicative constructions







* NP sets defined according to their morphosyntactic features







* The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.












The set **NOT-NPMOD** is used to find barriers between NPs.
Typical usage: ... (*1 N BARRIER NPT-NPMOD) ...
meaning: Scan to the first noun, ignoring anything that can be
part of the noun phrase of that noun (i.e., "scan to the next NP head")






* Miscellaneous sets





















* Border sets and their complements













* Syntactic sets




These were the set types.



## HABITIVE MAPPING


* **hab1** 


* **hab2** 

* **hab3** (<hab> @ADVL>) for hab-actor and hab-case; if leat to the right, and Nom to the right of leat. Lots of restrictions.



* **habNomLeft** 


* **hab4** 	



* **hab6** 

* **hab7** 

* **hab8** This is not HAB
* **hab5**  This is not HAB



* **habDain** (<hab> @ADVL>) for (Pron Dem Pl Loc) if leat followed by Nom to the right




* **habGen** (<hab> @<ADVL) hab for Gen; if Gen is located in the end of the sentence and Nom is sentence initial










































































* **spred<obj** (@SPRED<OBJ) for Acc; the object of an SPRPED. Not to be mistaken with OPRED. If SPRED is to the left, and copulas is to the left of it. Nom or Hab are found sentence initially.


* **Hab<spred** (@<SPRED) for Nom; if copulas, goallut or jápmit is FMAINV and habitive or human Loc is found to the left. OR: if Ill or @Pron< followed by HAB are found to the left.

* **Hab>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween HAB and <ext>.

* **Nom>Advlcase<spred** (<ext> @<SUBJ) for Nom; it allows adverbials with Ill/Loc/Com/Ess to be found inbetween Nom and <ext> @<SUBJ.

* **<spred** (<ext> @<SUBJ) for Nom; if copulas to the left, and some kind of adverb, N Loc, time related word or Po to the left of it. OR: if Ill or @Pron< to the left, followed by copulas and the before mentioned to the left of copulas. 

* **<spred** (<ext> @<SUBJ) for Nom, but not for Pers. To the left boahtit or heaŋgát as MAINV, and futher to the left is some kind of place related word, or time related word


* **<spredQst1** (<ext> @<SUBJ) for Nom in a typically question sentence; if A) Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. B) same as a, only the Qst-pcle is attached to copulas. C) Qst to the left, with copulas to its left, but not if two Nom:s are found somewhere to the right. D) copulas to the left, and BOS to the left. E) Loc or Ill to the left, and Loc or Hab to the left of this, Qst and copulas to the left. F) Num @>N to the left, Hab, some kind of place word, Po or Nom to the left, and Qst followed by copulas to the left. NOTE) for all these rules; human, Loc or Sem/Plc not allowed to the right.

* **<spredQst2** (@<SPRED) for Nom; in a typically question sentence; differs from <spredQst1 by not beeing as restricted to the right. Though you are not allowed to be Pers or human.

* **Nom<spredQst** (@<SPRED) for Nom; in a typically question sentence. Differs from <spredQst2 by letting Nom be found between SPRED and copulas



* **<spred** (@<SPRED) for A Nom or N Nom if; the subject Nom is on the same side of copulas as you: on the right side of copulas

* **<spredVeara** (@<SPRED) for veara + Nom; if genitive immediately to the right, and intransitive mainverb to the right of genitive

* **leftCop<spred** (@<SPRED) for Nom; if copulas is the main verb to the left, and there is no Ess found to the left of cop (note that Loc is allowed between target and cop). OR: if you are Coll or Sem/Group with copulas to your left. 

* **<spredLocEXPERIMENT** (@<SPRED) for material Loc; if you are to the right of copulas, and the Nom to the left of copulas is not a hab-actor


* **NumTime** (@<SPRED) for A Nom

* **<spredSg** (@<SPRED) for Sg Nom	

* **<spredPg** (@<SPRED) for Pl Nom	

* **<spred** (@<SPRED) for Nom; if copulas to the left, and Nom or sentence boundary to the left of copulas. First one to the right is EOS.

* **<spred** (@<SPRED) for N Ess

* **spredEss>** (@SPRED>) for N Ess; if copulas to the right of you, and if an NP with nom-case first one to your left.

* **HABSpredSg>** (@SPRED>) for Nom; if habitive first one to the left, followed by copulas.

* **GalleSpred>** (@SPRED>) for Num Nom; if sentence initial

* **spredSgMII>** (@SPRED>)

* **r492>** (@SPRED>) for Interr Gen; consisting only of negations. You are not allowed to be MII. You are not allowed to have an adjective or noun to yor right. You are not allowed to have a verb to your right; the exception beeing an aux.



* **AdjSpredSg>** (@SPRED>) for A Sg Nom; if copulas to the right, but not if A or @<SPRED are found to the right of copulas

* **SpredSg>Hab** (@SPRED>) for Nom; if you are sentence initial, copulas is located to the right, and there is a habitive to the right of copulas



* **Spred>SubjInf** (@SPRED>) for Nom; if copulas to the right, and the subject of copulas is an Inf to the right

* **spredCoord** (@<SPRED) coordination for Nom; only if there already is a SPRED to the left of CNP. Not if there is some kind of comparison involved.






* **subj>Sgnr1** (@SUBJ>) for Nom Sg, including Indef Nom if; VFIN + Sg3 or Pl3 to the right (VFIN not allowed to the left) 

* **subj>Du** (@SUBJ>) for dual nominatives, including Coll Nom. VFIN + Du3 to the right. 
* **subj>Pl** (@SUBJ>) for plural nominatives, including Coll and Sem/Group. VFIN + Pl3 to the right.

* **subj>Pl** (@SUBJ>) for plural nominatives


* **subj>Sgnr2** (@SUBJ>) for Nom Sg; if VFIN + Sg3 to the right.

* **<subjSg** (@<SUBJ) for Nom Sg; if VFIN Sg3 or Du2 to the left (no HAB allowed to the left).




















* **f<advl** (@-F<ADVL) for infinite adverbials

* **f<advl** (@-F<ADVL) for infinite adverbials



* **s-boundary=advl>** (@ADVL>) for ADVL that resemble s-booundaries. Mainverb to the right.




* **-fobj>** (@-FOBJ>) for Acc 

* **-fobj>** (@-FOBJ>) for Acc




* **advl>mainV** (@ADVL>) if; finite mainverb not found to the left, but the finite mainverb is found to the right.


* **<advl** (@<ADVL) if; finite mainverb found to the left. Not if a comma is found immediately to the left and a finite mainverb is located somewhere to the right of this comma.




* **<advlPoPr** (@<ADVL) if mainverb to the left.
* **advlPoPr>** (@<ADVL) if mainverb to the right.



* **advlEss>** (@<ADVL) for weather and time Ess, if FMAINV to the left.






* **advl>inbetween** (@ADVL>) for Adv; if inbetween two sentenceboundaries where no mainverb is present.

* **comma<advlEOS** (@<ADVL) if; comma found to the left and the finite mainverb to the left of comma. To the right is the end of the sentence.



* **advlBOS>** (@ADVL>) if; you are N Ill and found sentnece initially. First one to your right is a clause.


* **<advlPoEOS** (@<ADVL) for Po; if you are found at the very end of a sentence. A mainverb is needed to the right though.



* **cleanupILL<advl** (@<ADVL) for N Ill if; there are no boundarysymbols to your left, if you arent already @N< OR @APP-N<, and no mainverb is to yor left.











* **<opredAAcc** (@<OPRED) for A Acc; if an other accusative to the left, and a transtive verb to the left of it. OR: if a transitive verb to the left, and an accusative to the left of it.


### sma object









* **<advlEss** (@<ADVL) for ESS-ADVL if; FMAINV to the left
* **<spredEss** (@<SPRED) for N Ess if; FMAINV to the left is intransitive or bargat





## SUBJ MAPPING - leftovers

## OBJ MAPPING - leftovers


## HNOUN MAPPING
















# South East Cree noun stems                           


STEMS adds an affixmark and redirects to STEMLIST


# South East Cree numerals                           

## The file for numerals

 * LEXICON Numerals 


 * LEXICON NUM  adds +Num+Ipc
# Verb stems


 LEXICON VERBLIST   just adds the prefix boundary

 LEXICON VERBSTEMS  here come all the verbstems \\
 mâto IACONJ "cry" ;  GG
## South Eastern Cree pronouns

There are more pronoums to be added here.

 LEXICON Pronoun 


 LEXICON Personal  \\
 niya+Pron+Pers+1Sg:niya # ; 

# Innu (Montagnais) particles                      \


The file                                                                     

 * LEXICON pcle  adds +Ipc                                             


 * LEXICON Particles  \\                                               
 * cî+Ipc+Qst:cî # ;                                                   
 * namoya+Ipc+Neg:namoya # ;                                           



=================================== !
The Southern East Cree morphophonological/twolc rules file !
=================================== !








* *primus%>s*
* *primus00*


* examples:*

* examples:*


* examples:*

* examples:*

# Symbol affixes





# South East Cree noun morphology                           


NounPrefixes redirects to AN-IN, BODY, INALIENABLE


AN-IN adds the prefixes ni-, ki-, o-. Redirects to STEMS




Now, lexc directs us to the ../stems/nouns.lexc file,
where we find all the nominal stems. The suffixes are then
found at the end of this file.



# Suffixes


## The declensions for Animates 

 * LEXICON ANDECL  for the animate declension

 * LEXICON ANABSDECL  for the animate absolute declension

South East Cree verb morphology                  



 * @U.mood.indep@ INDEPENDENT ;		 

Now, lexc directs us to the ../stems/verbs.lexc file,
where we find all the verbal stems. The suffixes are then
found in the section "Suffixes" right underneath.

 LEXICON INDEPENDENT  gives flags and prefixes for personprefix


 LEXICON IND_TENSE  gives flags and prefixes for tense 




# Suffixes

 LEXICON IACONJ  splits in 4 moods

# Southern East Cree morphological analyser
INTRODUCTION TO MORPHOLOGICAL ANALYSER OF Southern East Cree LANGUAGE.

This is copied from Plains Cree

 # Definitions for Multichar_Symbols

## Analysis symbols

The morphological analyses of wordforms of Plains Cree are presented
in this system in terms of following symbols.
(It is highly suggested to follow existing standards when adding new tags).

POS

 * +N	         
 * +V	         
 * +A	         

 * +Adv         
 * +CC	         
 * +CS	         
 * +Interj      
 * +Pron        
 * +Num         
 * +Symbol = independent symbols in the text stream, like £, €, ©

 * +Loc         Locative

 * +Dim      Diminutive

  * +Ipc		 Indeclinable Particle

 * +Dem         Demonstrative 
 * +Prox	     Demonstrative Proximate
 * +Med	     Demonstrative Medial
 * +Dist	     Demonstrative Distal



Verbal MSP
 * +Prs   
 * +Fut  

 * +Prt   
 * +Prf   
 * +Cnj   
 * +Int   This tag is for the Future Intentional
 * +Def   This tag is for the Future Definite

 * +Ind   Indicative, aka Independent
 * +Imp   Imperative, consider deleting +Imp tag
 * +Del   Delayed imperative
 * +Imm   Immediate imperative, consider deleting +Imp tag
 * +Sbj   Subjunctive, aka Conjunct mode, ê-
 * +Cond  TODO: Should Future Conditional be tagget Fut only? Conor: we will split the Future tags




 * +1Sg     first singular
 * +2Sg     etc
 * +3Sg    
 * +4Sg    3o is obviative (Wolvengrey 3’, cf. W diss. p. xi.)
 * +5Sg    5Sg is further obviative person (Wolvengrey 3’’ cf. p. xi.)

 * +1Pl     1Pl is exclusive plural (I, them, not you)
 * +2Pl    
 * +3Pl    
 * +4Pl   
 * +12Pl    12Pl is inclusive plural (I, you, ...)

 * +1SgO    objective conjugation
 * +2SgO   
 * +3SgO   
 * +SgO    
 * +4SgO   obviative with objective conjugation
 * +1PlO   
 * +P2lO   
 * +3PlO   
 * +PlO    
 * +4PlO  

 * +Inf     infinitive (infinite?)
 * +Pos     postitive
 * +Neg     negative
 * +ConNeg  accompanying negative form

Nominal MSP
 * +Sg		  singular
 * +Pl		  plural

 * +Px1Sg	  person prefixes for nouns
 * +Px2Sg	 
 * +Px3Sg	 
 * +Px4Sg	 
 * +Px1Pl	  obviative
 * +Px12Pl	  inclusive
 * +Px2Pl	 
 * +Px3Pl	 
 * +Px4Pl	 
 * +Dim/Der 

 * +IA       intransitive with animate subject, 
 * +II       intransitive with inanimate subject, 
 * +TA       transitive with animate object, and 
 * +TI       transitive with inanimate object.

 * +AN		  animate noun
 * +IN		  inanimate noun


 * +Incl     me too, etc.
 * +Qst      yes-no question particle ci

## Auxiliary symbols

These symbols either shape or govern the
morphophonological structure

 * %> 		  suffix border
 * +WAK  	  tag to keep track of -wak plurals

 * %^LOC      Locative
 * w2       mow:mov2
 * t2 		  Prefix in possessives 
 * h2 		  Prefix in possessives 
 * i2 		  Possessive element 

 * ^%EGLOT    glottal stop after e, for eh- in conjunctive mood
 * ^%EA      ê to â in 1, 2 person of ê-stems


## Usage tags

These tags distinguish different special-purpose analysers
and generators from each other. Thus, for examples, we have
normative and descriptive analysers, and generators for different purposes.

 * +Err/Orth  tag for substandard forms
 * +Use/NG   not-generate, for ped generation isme-ped.fst



Flagdiacritics 

These are documented in Chapter 8 of Beesley/Karttunen, p. 456 zB.

We have manually optimised the structure of our lexicon using following
flag diacritics to restrict morhpological combinatorics - only allow compounds
with verbs if the verb is further derived into a noun again:
 |  @P.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @D.NeedNoun.ON@ | (Dis)allow compounds with verbs unless nominalised
 |  @C.NeedNoun@ | (Dis)allow compounds with verbs unless nominalised

For languages that allow compounding, the following flag diacritics are needed
to control position-based compounding restrictions for nominals. Their use is
handled automatically if combined with +CmpN/xxx tags. If not used, they will
do no harm.
 |  @P.CmpFrst.FALSE@ | Require that words tagged as such only appear first
 |  @D.CmpPref.TRUE@ | Block such words from entering ENDLEX
 |  @P.CmpPref.FALSE@ | Block these words from making further compounds
 |  @D.CmpLast.TRUE@ | Block such words from entering R
 |  @D.CmpNone.TRUE@ | Combines with the next tag to prohibit compounding
 |  @U.CmpNone.FALSE@ | Combines with the prev tag to prohibit compounding
 |  @P.CmpOnly.TRUE@ | Sets a flag to indicate that the word has passed R
 |  @D.CmpOnly.FALSE@ | Disallow words coming directly from root.

Use the following flag diacritics to control downcasing of derived proper
nouns (e.g. Finnish Pariisi -> pariisilainen). See e.g. North Sámi for how to use
these flags. There exists a ready-made regex that will do the actual down-casing
given the proper use of these flags.
 |  @U.Cap.Obl@ | Allowing downcasing of derived names: deatnulasj.
 |  @U.Cap.Opt@ | Allowing downcasing of derived names: deatnulasj.

For indicative, there are prefixes, so here we need one
flag for each person-number combination. Note that
for the inverse objective conjugation, the flag refers to
the **prefix**, not to the subject. So *indsg1* refers to either
subject = 1Sg or object = 1Sg. The 3-3 forms are prefixless.



The conjunctive always has
the ê- prefix, and future conditional never has a prefix.

 * @U.verb.FutCon@  Future Conditional

 * @U.mood.cnj@   Conjunctive (Conjunct)
 * @U.verb.fut@   Future Conditional

Prefixes with a certain phonological content:

 * @U.perspref.NULL@   test
 * @U.perspref.NI@   test
 * @U.perspref.KI@   test


 * @U.verb.1sgindep@ 
 * @U.verb.2sgindep@ 
 * @U.verb.3osgindep@ 
 * @U.verb.1plindep@ 
 * @U.verb.12plindep@ 
 * @U.verb.2plindep@ 
 * @U.verb.3plindep@ 

 * @U.noun.1sg@ 
 * @U.noun.2sg@ 
 * @U.noun.3sg@ 
 * @U.noun.3isg@ 
 * @U.noun.3osg@ 
 * @U.noun.1pl@ 
 * @U.noun.12pl@ 
 * @U.noun.2pl@ 
 * @U.noun.3pl@ 
 * @U.noun.3ipl@ 

 * @U.noun.abs@  
 * @U.noun.dep@ 


  LEXICON Root          is where it all starts

 * NounPrefixes ;        
 * VerbPrefixes ;        
 * Pronoun ;            
 * Punctuation ;        
 * Symbols     ;        
 * Particles ;          
 * Numerals ;            




We describe here how abbreviations are in Southern East Cree are read out, e.g.
for text-to-speech systems.

For example:

 * s.:syntynyt # ;  
 * os.:omaa% sukua # ;  
 * v.:vuosi # ;  
 * v.:vuonna # ;  
 * esim.:esimerkki # ; 
 * esim.:esimerkiksi # ; 


















































% komma% :,      Root ;
% tjuohkkis% :%. Root ;
% kolon% :%:     Root ;
% sárggis% :%-   Root ; 
% násti% :%*     Root ; 


      [ L A N G U A G E ]  G R A M M A R   C H E C K E R









# DELIMITERS


# TAGS AND SETS



## Tags


This section lists all the tags inherited from the fst, and used as tags
in the syntactic analysis. The next section, **Sets**, contains sets defined
on the basis of the tags listed here, those set names are not visible in the output.




### Beginning and end of sentence
BOS
EOS



### Parts of speech tags

N
A
Adv
V
Pron
CS
CC
CC-CS
Po
Pr
Pcle
Num
Interj
ABBR
ACR
CLB
LEFT
RIGHT
WEB
QMARK
PPUNCT
PUNCT

COMMA
¶



### Tags for POS sub-categories

Pers
Dem
Interr
Indef
Recipr
Refl
Rel
Coll
NomAg
Prop
Allegro
Arab
Romertall


### Tags for morphosyntactic properties

Nom
Acc
Gen
Ill
Loc
Com
Ess
Ess
Sg
Du
Pl
Cmp/SplitR
Cmp/SgNom Cmp/SgGen
Cmp/SgGen
PxSg1
PxSg2
PxSg3
PxDu1
PxDu2
PxDu3
PxPl1
PxPl2
PxPl3
Px

Comp
Superl
Attr
Ord
Qst
IV
TV
Prt
Prs
Ind
Pot
Cond
Imprt
ImprtII
Sg1
Sg2
Sg3
Du1
Du2
Du3
Pl1
Pl2
Pl3
Inf
ConNeg
Neg
PrfPrc
VGen
PrsPrc
Ger
Sup
Actio
VAbess



Err/Orth



### Semantic tags

Sem/Act
Sem/Ani
Sem/Atr
Sem/Body
Sem/Clth
Sem/Domain
Sem/Feat-phys
Sem/Fem
Sem/Group
Sem/Lang
Sem/Mal
Sem/Measr
Sem/Money
Sem/Obj
Sem/Obj-el
Sem/Org
Sem/Perc-emo
Sem/Plc
Sem/Sign
Sem/State-sick
Sem/Sur
Sem/Time
Sem/Txt

HUMAN

HAB-ACTOR
HAB-ACTOR-NOT-HUMAN


PROP-ATTR
PROP-SUR



TIME-N-SET


###  Syntactic tags

@+FAUXV
@+FMAINV
@-FAUXV
@-FMAINV
@-FSUBJ>
@-F<OBJ
@-FOBJ>
@-FSPRED<OBJ
@-F<ADVL
@-FADVL>
@-F<SPRED
@-F<OPRED
@-FSPRED>
@-FOPRED>
@>ADVL
@ADVL<
@<ADVL
@ADVL>
@ADVL
@HAB>
@<HAB
@>N
@Interj
@N<
@>A
@P<
@>P
@HNOUN
@INTERJ
@>Num
@Pron<
@>Pron
@Num<
@OBJ
@<OBJ
@OBJ>
@OPRED
@<OPRED
@OPRED>
@PCLE
@COMP-CS<
@SPRED
@<SPRED
@SPRED>
@SUBJ
@<SUBJ
@SUBJ>
SUBJ
SPRED
OPRED
@PPRED
@APP
@APP-N<
@APP-Pron<
@APP>Pron
@APP-Num<
@APP-ADVL<
@VOC
@CVP
@CNP
OBJ
<OBJ
OBJ>
<OBJ-OTHERS
OBJ>-OTHERS
SYN-V
@X





## Sets containing sets of lists and tags

This part of the file lists a large number of sets based partly upon the tags defined above, and
partly upon lexemes drawn from the lexicon.
See the sourcefile itself to inspect the sets, what follows here is an overview of the set types.



### Sets for Single-word sets

INITIAL


### Sets for word or not

WORD
REAL-WORD
REAL-WORD-NOT-ABBR
NOT-COMMA


### Case sets

ADLVCASE

CASE-AGREEMENT
CASE

NOT-NOM
NOT-GEN
NOT-ACC

### Verb sets


NOT-V

### Sets for finiteness and mood

REAL-NEG

MOOD-V

NOT-PRFPRC


### Sets for person

SG1-V
SG2-V
SG3-V
DU1-V
DU2-V
DU3-V
PL1-V
PL2-V
PL3-V





### Pronoun sets

















### Adjectival sets and their complements




### Adverbial sets and their complements




### Sets of elements with common syntactic behaviour


### NP sets defined according to their morphosyntactic features








### The PRE-NP-HEAD family of sets

These sets model noun phrases (NPs). The idea is to first define whatever can
occur in front of the head of the NP, and thereafter negate that with the
expression **WORD - premodifiers**.





















### Border sets and their complements











### Grammarchecker sets








