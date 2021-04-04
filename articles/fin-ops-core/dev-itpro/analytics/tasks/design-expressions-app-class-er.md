---
title: Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)
description: Tässä aiheessa käsitellään aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin määrityksissä kutsumalla sovellusluokkien pakollisia menetelmiä.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11b4d185703731d8491ad10bdeedea40ce811f5d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564091"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)

[!include [banner](../../includes/banner.md)]

Tässä oppaassa on tietoja aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin (ER) konfiguraatioissa kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa. Luokkien kutsumisen argumenttien arvot voidaan määrittää dynaamisesti suorituksen aikana esimerkiksi jäsennysasiakirjan perusteella. Näin varmistetaan tietojen oikeellisuus. Tässä oppaassa luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware Inc. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. 

Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla. Sinun on myös ladattava ja tallennettava paikallisesti seuraava tiedosto: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.

1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.   
    * Prosessi suunnitellaan saapuvien tiliotteiden jäsennysprosessia sovellustietojen päivitys varten. Saat saapuvat tiliotteet TXT-tiedostoina, joissa on IBAN-koodeja. IBAN-koodit on tarkistettava tiliotteiden osana tuontiprosessia. Tähän tarkistukseen käytetään sisältyvää logiikkaa.   

## <a name="import-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen tuominen
1. Etsi haluamasi tietue luettelosta ja valitse se.
    * Valitse Microsoft-toimittaja-ruutu.  
2. Valitse Säilöt.
3. Valitse Näytä suodattimet.
4. Lisää suodattimen kenttä Tyyppinimi. Anna Nimi-kentässä resurssit-arvo. Valitse ensin sisältää-suodatinoperaattori ja sitten Käytä.
5. Valitse Avaa.
6. Valitse puussa solmu Maksumalli.
    * Jos Versiot-pikavälilehden Tuo-painike ei ole käytössä, olet jo tuonut version 1, joka on eräs ER-konfiguraation maksumalleista. Voit ohittaa tämän alitehtävän seuraavat vaiheet.   
7. Valitse Tuo.
8. Valitse Kyllä.
9. Sulje sivu.
10. Sulje sivu.

## <a name="add-a-new-er-format-configuration"></a>Uuden ER-muotokonfiguraation lisääminen
1. Valitse Raportointikonfiguraatiot.
    * Lisää uusi ER-muoto, jotta voit jäsentää saapuvat tiliotteet TXT-muodossa.  
2. Valitse puussa solmu Maksumalli.
3. Avaa valintaikkunan valikko valitsemalla Luo konfigurointi.
4. Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.
5. Kirjoita Nimi-kenttään Tiliotteen tuontimuoto (esimerkki).
    * Tiliotteen tuonnin muoto (esimerkki)  
6. Valitse Tukee tietojen tuontia -kentässä Kyllä.
7. Valitse Luo konfiguraatio.

## <a name="design-the-er-format-configuration---format"></a>ER-muotokonfiguraation suunnitteleminen - muoto
1. Valitse Suunnittelutoiminto.
    * Suunniteltu muoto vastaa ulkoisen tiedoston odotettua rakennetta TXT-muodossa.  
2. Avaa valintaikkunan valikko valitsemalla Lisää juuri.
3. Valitse puussa "Text\Sequence".
4. Kirjoita Nimi-kenttään "Juuri".
    * Juuri  
5. Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".
    * Vaihtoehto Uusi rivi - Windows (CR LF) on valittu Erikoismerkit-kentässä. Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään erillisenä tietueena.  
6. Valitse OK.
7. Avaa valintaikkuna valitsemalla Lisää.
8. Valitse puussa "Text\Sequence".
9. Kirjoita Nimi-kenttään Rivit.
    * Rivit  
10. Valitse Monimuotoisuus-kentässä Yksi tai useita.
    * Vaihtoehto Yksi tai useita on valittu Monimuotoisuus-kentässä. Tämän asetuksen perusteella jäsennystiedostossa odotetaan olevan vähintään yksi rivi.  
11. Valitse OK.
12. Valitse puussa Root\Rows.
13. Valitse Lisää järjestys.
14. Kirjoita Nimi-kenttään Kentät.
    * Kentät  
15. Valitse Monimuotoisuus-kentässä Tasan yksi.
16. Valitse OK.
17. Valitse puussa Root\Rows\Fields.
18. Avaa valintaikkuna valitsemalla Lisää.
19. Valitse puussa solmu Text\String.
20. Syötä Nimi-kenttään IBAN.
    * IBAN-tilinumero  
21. Valitse OK.
    * Jäsennystiedoston jokainen rivi sisältää vain yhden IBAN-koodin.  
22. Valitse Tallenna.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>ER-muotokonfiguraation suunnitteleminen - yhdistämismääritys tietomalliin
1. Valitse Yhdistä muoto malliin.
2. Valitse Uusi.
3. Kirjoita Määritys-kenttään BankToCustomerDebitCreditNotificationInitiation.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges, määritelmä.
5. Kirjoita Nimi-kenttään Yhdistämismääritys tietomalliin.
    * Yhdistämismääritys tietomalliin  
6. Valitse Tallenna.
7. Valitse Suunnittelutoiminto.
8. Valitse puussa Dynamics 365 for Operations\Class.
9. Valitse Lisää juuri.
    * Lisää uusi tietolähde, joka kutsuu aiemmin luotua sovelluslogiikkaa IBAN-koodien tarkistusta varten.  
10. Kirjoita Nimi-kenttään tarkista koodit.
    * tarkista koodit  
11. Kirjoita Luokka-kenttään ISO7064.
    * ISO7064  
12. Valitse OK.
13. Laajenna puussa format.
14. Laajenna puussa format\Root: Sequence(Root).
15. Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows).
16. Valitse Sido.
17. Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows).
18. Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields).
19. Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).
20. Laajenna puussa 'Payments = format.Root.Rows'.
21. Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount).
22. Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification.
23. Valitse puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN.
24. Valitse Sido.
25. Valitse Vahvistukset-välilehti.
26. Valitse Uusi.
    * Lisää uusi tarkistussääntö, joka näyttää virheen jokaisella virheellisen IBAN-koodin sisältävällä jäsennystiedoston rivillä.  
27. Valitse Muokkaa ehtoa.
28. Laajenna puussa 'check_codes'.
29. Valitse puussa check_codes\verifyMOD1271_36.
30. Valitse Lisää tietolähde.
31. Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36('.
    * check_codes.verifyMOD1271_36(  
32. Laajenna puussa format.
33. Laajenna puussa format\Root: Sequence(Root).
34. Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows).
35. Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields).
36. Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).
37. Valitse Lisää tietolähde.
38. Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Valitse Tallenna.
40. Sulje sivu.
    * Tarkistusehto on määritetty palauttamaan FALSE jokaisen virheellisen IBAN-koodin kohdalla. Se kutsuu sovellusluokan ISO7064 olemassa olevaa menetelmää verifyMOD1271_36. Huomaa, että IBAN-koodin arvo määritetään dynaamisesti suorituksen aikana, koska kutsumenetelmän argumentti perustuu jäsennettävän TXT-tiedoston sisältöön.   
41. Valitse Muokkaa sanomaa.
42. Syötä Kaava-kenttään 'CONCATENATE("Löytyi virheellinen IBAN-kood: ", format.Root.Rows.Fields.IBAN)'.
    * CONCATENATE("Löytyi virheellinen IBAN-koodi: ", format.Root.Rows.Fields.IBAN)  
43. Valitse Tallenna.
44. Sulje sivu.
45. Valitse Tallenna.
46. Sulje sivu.

## <a name="run-the-format-mapping"></a>Muodon yhdistämismäärityksen suorittaminen
Testausta varten voit suorittaa muodon yhdistämismäärityksen käyttämällä aiemmin ladattua SampleIncomingMessage.txt-tiedostoa. Luodut tiedot sisältävät tietoja, jotka tuodaan valitusta TXT-tiedostosta ja joilla täytetään mukautetun tietomallin tiedot varsinaisen tuonnin yhteydessä.   
1. Valitse Suorita.
    * Valitse Selaa ja siirry aiemmin ladattuun SampleIncomingMessage.txt-tiedostoon.  
2. Valitse OK.
    * Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin. Huomaa, että vain 3 tuodun TXT-tiedoston riviä on käsitelty. Rivillä 4 oleva IBAN-koodi, joka ei ole sallittu, on ohitettu. Infolokissa on virhesanoma.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]