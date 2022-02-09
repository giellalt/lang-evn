# The Evenki morphophonological/twolc rules file 

This file documents the [phonology.twolc file](http://github.com/giellalt/lang-evn/blob/main/src/fst/phonology.twolc) 

## Alphabet

*  а б в г д е ё ж з и й к л м н ӈ о п р с т у ф х ц ч ш щ ъ ы ь э ю я  
*  А Б В Г Д Е Ё Ж З И Й К Л М Н Ӈ О П Р С Т У Ф Х Ц Ч Ш Щ Ъ Ы Ь Э Ю Я  

*  %{ː%}:̄  

*  %{L%}:л %{L%}:р							     
*  %{G%}:г %{G%}:к %{G%}:ӈ						     
*  %{D%}:д %{D%}:т 							     
*  %{A%}:а %{A%}:э %{A%}:о  						     
*  %{Я%}:я %{Я%}:е %{Я%}:ё %{Я%}:а %{Я%}:э %{Я%}:о     			     
*  %{V%}:в %{V%}:м							     
*  %{R%}:р %{R%}:0 %{R%}:т %{R%}:л %{R%}:н 				     

*  %{j%}:0  %{j%}:ъ		
*  %{i%}:0 %{i%}:и %{i%}:ы        
*  %{U%}:и %{U%}:у  %{U%}:0  	
*  %>  ;       	  		

Sets

* Vow = а е ё и о у ы э ю я 						       
*       А Е Ё И О У Ы Э Ю Я 						       
*       а̄ е̄ ӣ э̄ ӯ о̄							       
*       А̄ Е̄ Ӣ ¯Э Ӯ О̄ ;						       

* Cns = б в г д ж з й к л м н ӈ п р с т ф х ц ч ш щ      
*       Б В Г Д Ж З Й К Л М Н Ӈ П Р С Т Ф Х Ц Ч Ш Щ ;    
* ArchiCns = %{D%} %{G%} %{L%} %{R%} %{V%} ;			       
* Nasal = м н ӈ									       
*         М Н Ӈ ; 								       

* NonLN = б в г д ж з й к м ӈ п р с т ф х ц ч ш щ        
*         Б В Г Д Ж З Й К М Ӈ П Р С Т Ф Х Ц Ч Ш Щ ;      

* UnvoicedCns = к с т п ;    
* VoicedCns1 = б в г д щ з й р ; 

## Rules

### Assimilation rules

**Remove suffix vowel with vowel-ending stem**  

**Realise suffix vowel as y after t**  

**Realise suffix vowel as i after non-t**  

**Assimilate possessive to plural**  

**Consonant assimilation in suffixes**  

**Unvoicing assimilation**  

* *дэт>{D}ук*
* *дэт>тук*

**Voicing assimilation**  

* *орон>{D}у{ː}*
* *орон>дӯ*

* *ю{ː}>{D}*
* *ю̄>д*

* *урэ>{D}ук*
* *урэ>дук*

**Nasal assimilation of V**  

**Default realisaton of V **  

* *урэ>{i}л>{V}{A}*
* *урэ>0л>вэ*

* *орон>{V}{A}*
* *орор>во*

### Palatalisation

**Not realising hard sign after vowel or n**  

* *дю{ː}>{j}{A}>{i}в*
* *дю̄>0я>0в*

* *урэ>{i}л>{A}*
* *урэ>0л>э*

**Realising hard sign**  

* *урэ>{j}{A}*
* *урэ>0е*

* *бэр>{j}{A}*
* *бэр>ъе*

* *бэр>{V}{A}*
* *бэр>вэ*

* *урэ>{V}{A}*
* *урэ>вэ*

* *дю{ː}>{V}{A}>{i}в*
* *дю̄>ва00в*

* *дю{ː}>{D}у{ː}>{i}в*
* *дю̄>дӯ>0в*

### Other vowel rules

## Consonant rules

### Other cns

* *са{ː}>{R}{A}>н*
* *са̄>ра0н*

* *ис>{R}{A}>н*
* *ис>та0н*

* *мел>{R}{A}>н*
* *мел>ла>н*

* *уӈ>{R}{A}>н*
* *уӈ0нэ>н*

* *гун>{R}{A}>н*
* *гун>0э>н*

## Vowel rules

### Vowel harmony for а

**Vowel harmony for A to а, main rule**  (note е->а)

**Vowel harmony for {A} following i**  

**Vowel harmony for A following long o**  long o gives a

**Vowel harmony for A to о, main rule**  (note е->а)

**Palatalised short vowel harmony for A**  

* *орон>{j}{A}*
* *орон>0о*

**Vowel harmony for A to э, main rule**  (note е->а)

* *урэ>{i}кл{A}{ː}*
* *урэ>0клэ̄*

* *урэ>{i}л>{D}ул{A}{ː}*
* *урэ>0л>дулэ̄*

* *бэр>{D}ул{A}{ː}*
* *бэр>дулэ̄*

* *тэтыврэв*
* *тэтыврэв*

* *урэ>{i}л>{A}*
* *урэ>0л0э*

* *урэ>{V}{A}*
* *урэ>вэ*

* *орон>{V}{A}*
* *орон>мо*

* *орон>р{V}{A}*
* *оро0>рво*

* *test*
* *fail*

* * *

<small>This (part of) documentation was generated from [src/fst/phonology.twolc](https://github.com/giellalt/lang-evn/blob/main/src/fst/phonology.twolc)</small>

---

