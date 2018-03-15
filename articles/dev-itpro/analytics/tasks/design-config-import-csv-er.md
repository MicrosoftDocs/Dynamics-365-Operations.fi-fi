--- 
title: Konfiguraation suunnitteleminen tietojen tuomiseksi ulkoisesta tiedostosta CSV-muotoon (ER)
description: "Voit suunnitella tämän menettelyn avulla sähköisen raportoinnin (ER) konfiguraatioita, joilla tuodaan tietoja ulkoisesta tiedostosta CSV-muodossa Dynamics 365 for Finance and Operations, Enterprise edition -sovellukseen."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 5c1766992531ee272ea156bc33c4c0ea8dfac27a
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="design-a-configuration-to-import-data-from-an-external-file-in-csv-format-er"></a>Konfiguraation suunnitteleminen tietojen tuomiseksi ulkoisesta tiedostosta CSV-muotoon (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voit suunnitella tämän menettelyn avulla sähköisen raportoinnin (ER) konfiguraatioita, joilla tuodaan tietoja ulkoisesta tiedostosta CSV-muodossa Dynamics 365 for Finance and Operations, Enterprise edition -sovellukseen. Tällä menettelyllä luodaan pakollisia ER-määrityksiä malliyritykselle Litware, Inc. Näitä vaiheita varten on suoritettava ensin ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet. 

Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla. 

Lataa ja tallenna paikallisesti myös seuraavat tiedostot: (https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Voit määrittää prosessin, jolla XML-, TXT- tai CSV-muotoisia ulkoisia tiedostoja tuodaan Dynamics 365 for Finance and Operations, Enterprise edition -sovelluksen tauluihin. Luo liiketoiminnan kannalta tuotuja tietoja varten ensin abstrakti tietomalli – tätä varten luodaan ER-tietomallin konfiguraatio. Määritä seuraavaksi suunniteltuun tietomalliin yhdistettävän tuodun tiedoston rakenne tavaksi, jolla tiedoston tiedot voidaan siirtää abstraktiin tietomalliin – tätä varten luodaan ER-muotokonfiguraatio. ER-tietomallin konfiguraatiota on sitten laajennettava uudella mallin yhdistämismäärityksellä, joka ilmaisee, miten sovelluksen taulut tai tietoyksiköt päivitetään tuodun tiedoston tietojen ja abstraktin tietomallin pysyvien tietojen avulla.  
    * Seuraavissa vaiheissa näytetään, miten ulkoisesti seuratut toimittajien tapahtumat tuodaan ulkoisesta CSV-tiedostosta toimittajan 1099-lomakkeiden tilitysten myöhempää käyttöä varten.   
    * Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.  
2. Valitse Raportointikonfiguraatiot.
3. Käytä 1099-maksumalli-suodatinta. Jos olet jo suorittanut menettelyn ER Luo vaaditut konfiguraatiot tietojen tuomiseksi ulkoisesta tiedostosta sähköistä raportointia varten ja 1099-maksumalli-konfiguraatio on käytettävissä konfiguraatiopuussa, ohita kaikki seuraavan alitehtävän vaiheet.   

## <a name="add-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen lisääminen
1. Lataa tietojen tuontia tukevan uuden mallin luomisen sijaan aiemmin lataamasi tiedosto, 1099model.xml. Tässä tiedostossa on toimittajien tapahtumien mukautettu tietomalli. Tämä tietomalli on jo yhdistetty tarvittaviin tieto-osiin.  
2. Valitse Vaihto.
3. Valitse Lataa XML-tiedostosta.
4. Valitse Selaa ja siirry aiemmin ladattuun 1099model.xml-tiedostoon.  
5. Valitse OK.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Tietojen tuontia tukevan uuden ER-muodon konfiguraation lisääminen
1. Valitse puussa 1099-maksumalli.
2. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
3. Anna Uusi-kenttään Muoto perustuu tietomalliin 1099-maksumalli.
4. Valitse Tukee tietojen tuontia -kentässä Kyllä.
5. Sulje sivu painamalla ESC-näppäintä.
    * Lataa tietojen tuontia tukevan uuden ER-muodon luomisen sijaan aiemmin lataamasi tiedosto, 1099formatcsv.xml. Tässä tiedostossa on pakollinen ER-muoto, joka määrittää saapuvan CSV-tiedoston rakenteen ja tämän rakenteen yhdistämismäärityksen toimittajien tapahtumien tietomalliin.   
6. Valitse Vaihto.
7. Valitse Lataa XML-tiedostosta.
    * Valitse Selaa ja siirry aiemmin ladattuun 1099formatcsv.xml-tiedostoon.  
8. Valitse OK.
9. Laajenna puussa 1099-maksumalli.
10. Valitse puussa 1099-maksumalli\Toimittajien tapahtumien tuominen (CSV).

## <a name="review-format-settings"></a>Muotoasetusten tarkasteleminen
1. Valitse Suunnittelutoiminto.
2. Valitse Laajenna tai tiivistä.
3. Vaihda Näytä tiedot käyttöön.
    * Suunniteltu muoto vastaa ulkoisen tiedoston odotettua rakennetta CSV-muodossa.  
4. Valitse puussa Incoming: File\Root: Sequence.
    * Tyypin SEQUENCE juurielementin vaihtoehto Uusi rivi - Windows (CR LF) on valittu Erikoismerkit-kentässä. Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään erillisenä tietueena.   
5. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..*.
    * Tyypin SEQUENCE Root\Line-elementille on valittu vaihtoehto Yksi tai useita Monimuotoisuus-kentässä. Tämän asetuksen perusteella jäsennystiedostossa on vähintään yksi rivi.   
6. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case.
    * Ota huomioon, että tyypin CASE Root\Line\Types-elementti on lisätty Root\Line-järjestyksen sisäkkäisenä elementtinä. Koska tämä CASE-elementti sisältää 3 sisäkkäistä järjestyselementtiä, tämä asetus olettaa, että jäsennystiedostossa odotetaan olevan 3 erilaista rivityyppiä.   
7. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Header: Sequence 1..1.
    * Tyypin SEQUENCE Root\Line\Types\Header-elementti sisältää sisäkkäisen STRING-elementin, jonka arvo on määritetty vakiopituiseksi merkkijonoksi. Tämä järjestys jäsentää jäsennystiedoston otsikkorivin.   
8. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,).
    * Tyypin SEQUENCE Root\Line\Types\Record-elementti jäsentää tapahtumarivit. Huomaa, että Mukautettu erotin -valinta on määritetty pilkuksi. Tämä tarkoittaa sitä, että pilkkua käytetään kenttien erottimena jäsennystiedoston tämän tyyppisessä rivissä.   
    * Huomaa, että erilaisten tietotyyppien useita sisäkkäisiä elementtejä on lisätty Root\Line\Types\Record-elementtiin, jotta tapahtuman rivit voidaan jäsentää erillisinä kenttinä. Huomaa, että Tarjoussovellus-valinnan arvoksi on määritetty Ei mitään. Tämä tarkoittaa sitä, että tiedoston jäsennyksessä millään tämän tyyppisellä kentällä ei katsota olevan kehystettyjä merkkejä.   
9. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\TransactionDate: DateTime.
    * Esimerkiksi tyypin DATETIME Root\Line\Types\Record\TransactionDate-elementti hakee tapahtuman päivämäärän ja aika-arvon jäsennystiedostosta muodossa K/p/vvvv.   
10. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\CountryCode: String 0..1.
    * Huomaa, että tyypin STRING Root\Line\Types\Record\CountryCode-elementti on määritetty niin, että Monimuotoisuus-kentän arvo on Nolla tai yksi. Tämä asetus määrittää jäsennysrivin CountryCode-kentän arvoksi valinnaisen arvon.   
11. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Record: Sequence 1..1 (,)\Remark: Sequence 1..1 (,).
    * Huomaa, että tyypin SEQUENCE Root\Line\Types\Record\Remark-elementti on määritetty niin, että Tarjoussovellus-kentän arvo on Kaikki ja Lainausmerkki-kentän arvo on Lainausmerkit. Tällöin jäsennystiedoston kaikkien tämän tyyppisten rivien kenttien (kuvataan sisäkkäisillä elementeillä: STRING-tyyppinen teksti) ajatellaan olevan lainausmerkkien sisässä.  
12. Valitse puussa Incoming: File\Root: Sequence\Line: Sequence 1..* \Types: Case\Unparsed: Sequence 1..1.
    * Tyypin SEQUENCE Root\Line\Types\Unparsed-elementti jäsentää sen rakenteen tapahtumarivit, joka ei vastaa CASE-pääelementissä kuvattua rakennetta.   

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Tietomalliin tehtävän muodon yhdistämismäärityksen asetuksen tarkasteleminen
1. Valitse Yhdistä muoto malliin.
    * Yhdistämismääritys malliin CSV-muodosta -mallin yhdistämismääritys kuvaa tietojen siirron tietovirtaa saapuvasta CSV-tiedostosta tietomalliin.   
2. Valitse Suunnittelutoiminto.
3. Laajenna puussa format.
    * Huomaa, että suunniteltu muoto esitellään tässä tietolähdeosana.  
4. Laajenna puussa format\Incoming: File(Incoming).
5. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root).
6. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line).
7. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types).
8. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record).
9. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data.
10. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\CountryCode: String 0..1 (CountryCode).
11. Laajenna puussa format\Incoming: File(Incoming)\Root: Sequence(Root)\Line: Sequence 1..* (Line)\Types: Case(Types)\Record: Sequence 1..1 (,)(Record)\Data\TransactionDate: DateTime(TransactionDate).
    * Huomaa, että pakolliset ja valinnaiset muotoelementit, kuten TransactionDate ja CountryCode, ovat erilaisia ennalta määritetyn muodon tietolähdeosassa.   
12. Laajenna puussa 'Transactions = '$both''.
    * Huomaa, että tuodun tiedoston rakennetta määrittävät muotoelementit on sidottu tietomallin elementteihin. Tuodun CSV-tiedoston sisältö tallennetaan näiden sidontojen perusteella ajonaikaisesti aiemmin luotuun tietomalliin. CountryRegion-elementin sidontaan kannattaa kiinnittää huomiota. Jos saapuvan tiedoston tapahtumaelementissä ei ole määritettyä maakoodin arvoa, tietomallissa käytetään oletusmaakoodia USA.   
13. Vaihda Näytä tiedot käyttöön.
14. Valitse Vahvistukset-välilehti.
15. Valitse Haku.
16. Kirjoita Etsi-kenttään "toim".
17. Valitse Etsi seuraava.
    * Tässä muodon yhdistämismäärityksessä voi olla käyttäjän määrittämä logiikka, jolla tarkistetaan tuotujen tietojen oikeellisuus yrityksen näkökulmasta. Jos esimerkiksi asetuksen perusteella tuotavan tiedoston minkä tahansa rivin rakenne ei vastaa otsikkorivin tai tapahtumarivin rakennetta, infolokiin tulee varoitussanoma, jossa käyttäjälle kerrotaan tapauksesta. Tiedoissa on myös tapahtuman järjestysnumero tiedostossa.   
18. Sulje sivu.

## <a name="run-the-format-mapping"></a>Muodon yhdistämismäärityksen suorittaminen
Testausta varten voit suorittaa muodon yhdistämismäärityksen käyttämällä aiemmin ladattua 1099entriescsv.csv-tiedostoa. Luodut tiedot vastaavat tietoja, jotka tuodaan valitusta CSV-tiedostosta ja joilla täytetään mukautetun tietomallin tiedot varsinaisen tuonnin yhteydessä.   
1. Valitse Suorita.
    * Valitse Selaa ja siirry aiemmin ladattuun 1099entriescsv.csv-tiedostoon.  
2. Valitse OK.
    * Kiinnitä huomioita varoituksiin riveistä, joita ei hyväksytä. Rivi 4 sisältää tulojen arvon, joka esitetään hyväksymättömässä muodossa. Rivillä 7 taas tapahtuman huomautusteksti ei ole lainausmerkeissä.   
    * Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin. Huomaa, että kaikki 7 tuodun CSV-tiedoston riviä on käsitelty. Sisältyvien kenttien otsikoista 1 ohitettiin, 4 tapahtumaa jäsennettiin oikein ja 2 tapahtumaa todettiin virheellisiksi.   
3. Sulje sivu.
4. Sulje sivu.


