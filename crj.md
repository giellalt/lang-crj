
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


