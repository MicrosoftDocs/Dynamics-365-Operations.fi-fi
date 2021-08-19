---
title: ER Tarvittavien määritysten luonti tietojen tuontiin ulkoisesta tiedostosta
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määrityksen suunnittelua tuomaan tietoja Microsoft Dynamics 365 Finance -sovellukseen ulkoisesta tiedostosta.
author: NickSelin
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eaa35baae8e030d8a8b7ce903554c4876c874b48cfd72d6ac278cf4c0e8a6e8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720853"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER Tarvittavien määritysten luonti tietojen tuontiin ulkoisesta tiedostosta

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella sähköisen raportoinnin (ER) konfiguraatioita tuomaan tietoja sovellukseen ulkoisesta tiedostosta. Tässä esimerkissä luodaan pakollisia ER-määrityksiä malliyritykselle Litware, Inc. Näitä vaiheita varten on suoritettava ensin ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -tehtäväoppaan vaiheet. Nämä vaiheet voidaan suorittaa USMF-tietojoukon avulla. Seuraavat tiedostot täytyy myös ladata ja tallentaa paikallisesti: 

| Sisällön kuvaus                       | Tiedostonimi                                     |
|-------------------------------------------|-----------------------------------------------|
| ER-tietomallin konfigurointi – 1099 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| ER-muodon konfigurointi – 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| Saapuvan asiakirjan XML-muotoinen näytetiedosto                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Saapuvan asiakirjan tietojen hallinnan työkirjamalli                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

Sähköisen raportoinnin (ER) ansiosta yrityskäyttäjät voivat määrittää prosessin, jolla ulkoiset datatiedostot tuodaan tauluihin .XML- tai .TXT-muodossa. Ensimmäiseksi on suunniteltava tuotavia tietoja vastaava abstraktin tietomallin ja ER-tietomallin määritys. Seuraavaksi on määritettävä tuotavan tiedoston rakenne ja menetelmä, jolla tiedot siirretään tiedostosta abstraktiin tietomalliin. Kyseiselle abstraktille tietomallille on luotava suunniteltuun tietomalliin yhdistävä ER-muotomääritys. Tietomallimääritystä on sitten laajennettava yhdistämismäärityksellä, joka ilmaisee, miten tuodut tiedot säilytetään abstraktina tietomallin tietoina ja miten taulut päivitetään sen avulla.  ER-tietomallimääritykseen on liitettävä uusi malliyhdistämismääritys, joka ilmaisee, miten tietomalli sidotaan sovelluksen kohteisiin.  

Seuraavassa skenaariossa esitellään ER-tietojen tuontiominaisuuksia. Niitä ovat esimerkiksi toimittajatapahtumat, joita seurataan ulkoisesti ja jotka sitten tuodaan, jotta ne voidaan myöhemmin raportoida toimittajan valmisteveron tilityksenä.   

## <a name="add-a-new-er-model-configuration"></a>Uuden ER-mallimäärityksen lisääminen
1. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.

    Varmista, että esimerkkiyrityksen Litware Inc. konfiguraation tarjoaja on käytettävissä ja merkitty aktiiviseksi. Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.   

2. Valitse Raportointikonfiguraatiot.

    Lataa tietojen tuontia tukevan uuden mallin luomisen sijaan aiemmin lataamasi tiedosto, 1099model.xml. Tässä tiedostossa on toimittajien tapahtumien mukautettu tietomalli. Tämä tietomalli yhdistetään AOT-tietoyksikössä oleviin tieto-osiin.   

3. Valitse Vaihto.
4. Valitse Lataa XML-tiedostosta.

    Valitse Selaa ja siirry aiemmin ladattuun 1099model.xml-tiedostoon.  

5. Valitse OK.
6. Valitse puussa 1099-maksumalli.

## <a name="review-data-model-settings"></a>Tietomallin asetusten tarkasteleminen
1. Valitse Suunnittelutoiminto.

    Tämä malli on suunniteltu vastaamaan toimittajien tapahtumia yrityksen näkökulmasta. Se on myös erillään toteutuksesta.   

2. Laajenna puussa 1099-MISC.
3. Valitse puussa 1099-MISC\Tapahtumat.
4. Laajenna puussa 1099-MISC\Tapahtumat.

    Tämän mallin Tapahtumat-elementti vastaa yksittäisiä tapahtumia. Alielementtien avulla määritetään kunkin tapahtuman pakolliset tiedot, kuten toimittajan tili ja tapahtumapäivä.   

5. Sulje sivu.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Tietojen tuontia tukevan uuden ER-muodon konfiguraation lisääminen
Tämä alitehtävän ohjeiden avulla osaat luoda uuden muotomäärityksen, jolla voidaan hallita tietojen tuontia ulkoisista tiedostoista.   
1. Avaa valintaikkuna napsauttamalla Luo konfigurointi.
2. Anna Uusi-kenttään Muoto perustuu tietomalliin 1099-maksumalli.
3. Valitse Tukee tietojen tuontia -kentässä Kyllä.
4. Sulje sivu painamalla ESC-näppäintä.

    Lataa tietojen tuontia tukevan uuden muodon luomisen sijaan aiemmin lataamasi tiedosto, 1099format.xml. Tässä tiedostossa on tuotavan tiedoston määritetty rakenne ja rakenteen yhdistämismääritys toimittajien tapahtumien mukautettuun tietomalliin.   
5. Valitse Vaihto.
6. Valitse Lataa XML-tiedostosta.
    Valitse Selaa ja siirry aiemmin ladattuun 1099format.xml-tiedostoon.  
7. Valitse OK.
8. Laajenna puussa 1099-maksumalli.
9. Valitse puussa 1099-maksumalli\Toimittajien tapahtumien tuontimuoto.

## <a name="review-format-settings"></a>Muotoasetusten tarkasteleminen
1. Valitse Suunnittelutoiminto.
2. Vaihda Näytä tiedot käyttöön
3. Valitse Laajenna tai tiivistä.
4. Valitse Laajenna tai tiivistä.

    Suunniteltu muoto vastaa ulkoisen tiedoston odotettua rakennetta. Tämän tiedoston on oltava XML-muotoinen ja siinä on oltava tilityksen päätason elementti. Kutakin toimittajan tapahtumaa vastaa tapahtumaelementti, jonka monimuotoisuudeksi on määritetty nollasta moneen. Tämä tarkoittaa sitä, että saapuvan tiedoston tapahtumien määrä voi vaihdella nollasta moneen tapahtumaan. Tapahtumaelementin sisäkkäiset elementit vastaavat yksittäisen tapahtuman määritteitä. Huomaa, että maata lukuun ottamatta kaikki tapahtumat on merkitty pakolliseksi. Tämä tarkoittaa sitä, että niiden on sisällyttävä tuotavaan tiedostoon.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>Tietomalliin tehtävän muodon yhdistämismäärityksen asetusten tarkasteleminen
1. Valitse Yhdistä muoto malliin.

    Toimittajien tapahtumien yhdistämismääritys sisältää tiedonsiirtosäännöt, jotka koskevat saapuvasta XML-tiedostosta mukautetun tietomallin valittuun osaan tapahtuvaa siirtoa ja joka on määritetty valitsemalla 1099-MISC-määritys.  

2. Valitse Suunnittelutoiminto.
3. Vaihda Näytä tiedot käyttöön
4. Laajenna puussa muoto: Tietue.
5. Valitse puussa muoto: Tietue.

    Huomaa, että suunniteltu muoto esitellään tässä tietolähdeosana.  

6. Laajenna puussa kohde `format: Record\*settlement: XML Element 1..1 (settlement): Record`.
7. Laajenna puussa kohde `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list`.
8. Laajenna puussa kohde `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.
9. Laajenna puussa kohde `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record`.
10. Valitse puussa `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.

    Huomaa, että pakollisten ja valinnaisten muotoelementtien esittely on erilainen ennalta määritetyssä muodon tietolähdeosassa.  
11. Laajenna puussa Tapahtumat: Tietueluettelo= format.settlement.'$enumerated'.

    Huomaa, että tuodun tiedoston rakennetta määrittävät muotoelementit on sidottu mukautetun tietomallin elementteihin. Tuodun XML-tiedoston sisältö tallennetaan näiden sidontojen perusteella ajonaikaisesti aiemmin luotuun tietomalliin. Maaelementin sidontaan kannattaa kiinnittää huomiota. Jos kyseistä elementtiä ei ole saapuvan tiedoston tapahtumaelementissä, tietomallissa käytetään oletusmaakoodia USA.  

12. Valitse Vahvistukset-välilehti.

    Tässä muodon yhdistämismäärityksessä voi olla käyttäjän määrittämä logiikka, jolla tarkistetaan tuotujen tietojen oikeellisuus yrityksen näkökulmasta. Asetuksen perusteella esimerkiksi infolokiin voidaan luoda varoitusviesti kaikista tuotavan tiedoston tapahtumista, joissa ei ole maakoodia. Käyttäjä saa viestin avulla asiasta tiedon. Lisäksi viestissä on tapahtuman järjestysnumero.  

13. Sulje sivu.

## <a name="run-the-format-mapping-to-the-data-model"></a>Muodon yhdistämismäärityksen suorittaminen tietomalliin
Testaa muodon yhdistämismääritys suorittamalla se. Käytä aiemmin ladattua 1099entries.xml-tiedostoa. Voit viedä tämän tiedoston toimittajan tapahtumien hallintaan käytettävästä 1099entries.xlsx-työkirjasta. Luodut tiedot tuodaan valitusta XML-tiedostosta ja niillä täytetään mukautetun tietomallin tiedot varsinaisen tuonnin yhteydessä.  

1. Valitse Suorita.

    Valitse Selaa ja siirry aiemmin ladattuun 1099entries.xml-tiedostoon.  

2. Valitse OK.

    Huomaa varoitussanoma, joka ilmoittaa puuttuvasta maakoodista tuodun tiedoston tapahtumassa.  
    
    Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin.   

3. Sulje sivu.
4. Sulje sivu.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>Kohteisiin tehtävän mallin yhdistämismäärityksen asetusten tarkasteleminen
1. Valitse puussa 1099-maksumalli.
2. Valitse Suunnittelutoiminto.
3. Valitse Yhdistä malli tietolähteeseen.

    Manuaalisten 1099-tapahtumien tuonnin yhdistämismääritykset on määritetty Kohteeseen-suuntatyypillä. Se on siis annettu tukemaan tietojen tuontia ja se sisältää sellaisten sääntöjen asetukset, joilla määritetään ulkoisten tiedostojen tuonti ja säilyttäminen abstraktina tietomallina ja miten niillä päivitetään sovelluksen taulut.  

4. Valitse Suunnittelutoiminto.
5. Laajenna puussa malli: Tietomalli 1099-maksumalli.
6. Laajenna puussa malli: Tietomalli 1099-maksumalli\Tapahtumat: Tietueluettelo.

    Huomaa, että suunniteltu malli esitellään tässä tietolähde-elementtinä. Ajonaikana se sisältää ulkoisesta tiedostosta tuodut tiedot. Useita tauluja lisättiin tietolähde-elementteinä. Tämä varmistaa, että tuodut tiedot ovat yhteensopivia nykyisen sovelluksen tietojen kanssa. Näin varmistetaan esimerkiksi, että tuotavan tapahtuman toimittajatili on käytettävissä järjestelmässä ja tuotavien maa- ja osavaltiokoodien yhdistelmä on olemassa.  

7. Valitse puussa malli: Tietomalli 1099-maksumalli\Tapahtumat: Tietueluettelo\$failed: Laskettu kenttä = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean.
8. Valitse Muokkaa.
9. Valitse Muokkaa kaavaa.

    Kun vähintään yksi yksittäisen tuodun tapahtuman tarkistus epäonnistuu, tietolähdemäärite $failed merkitsee kyseisen tapahtuman epäonnistuneeksi.  

10. Sulje sivu.
11. Valitse Peruuta.
12. Valitse puussa tax1099trans: Taulu VendSettlementTax1099 tietueet= model.Validated.
13. Valitse Muokkaa kohdetta.

    Tämä ER-kohde lisättiin määrittämään, miten tuodut tiedot päivitetään sovellustauluissa. Tässä tapauksessa on valittu tietotaulun VendSettlementTax1099. Koska tietuetoiminto Lisää on valittu, tuodut tapahtumat lisätään tauluun VendSettlementTax1099. Huomaa, että yhdellä mallin yhdistämismäärityksellä voi olla useita kohteita. Niinpä tuoduilla tiedoilla voidaan päivittää samalla kertaa useita sovelluksen tauluja. Tauluja, näkymiä ja tietoyksiköitä voidaan käyttää ER-kohteina.   

    Jos yhdistämismääritys kutsutaan sovelluksen toimintoa varten suunnitellusta pisteestä (kuten painikkeesta tai valikkokohteesta), ER-kohde on merkittävä integrointipisteeksi. Tässä esimerkissä se on ERTableDestination#VendSettlementTax1099-piste.  

14. Valitse Peruuta.
15. Valitse Näytä kaikki.
16. Valitse Näytä vain yhdistetyt.
17. Laajenna puussa tax1099trans: Taulu VendSettlementTax1099 tietueet= model.Validated.

    Huomaa, että vain tarkistettuja tapahtumia sisältävä tietolähde-elementti on sidottu luotuun kohteeseen. Voit suodattaa tuodut tapahtumat ohittamaan kohteet, jotka eivät ole yhteensopivia sovelluksen tietojen kanssa.  

18. Valitse puussa epäonnistui: Taulu VendSettlementTax1099Entity tietueet= model.Failed.
19. Valitse Vahvistukset-välilehti.

    Tässä mallin yhdistämismäärityksessä voi olla käyttäjän määrittämä logiikka, jolla tarkistetaan aiemmin luoduista sovellustiedoista tuotujen tietojen oikeellisuus. Ennalta määritetyn asetuksen perusteella esimerkiksi voidaan luoda varoitussanoma kaikista tuotavan tiedoston tapahtumista, joiden toimittaja tili ei ole järjestelmässä. Käyttäjä saa sanoman avulla tiedon virheellisestä toimittajatilin koodista.  

    Huomaa, että Tarkistuksen jälkeinen toiminto -asetuksella voi määrittää jokaisessa tarkistuksessa, jatketaanko tuontiprosessia vai pysäytetäänkö se. Lisäksi sillä voi määrittää, säilytetäänkö vai peruutetaanko jo suoritetut lisäykset tai päivitykset.  

20. Valitse Näytä vain yhdistetyt.
21. Valitse Näytä kaikki.
22. Sulje sivu.

    Testaa suunniteltua mallia ja mallin yhdistämismäärityksiä suorittamalla tämä mallin yhdistämismääritys. Käytä 1099entries.xml-tiedostoa. Valitun tiedoston tiedot tuodaan järjestelmään.  

23. Valitse Suorita.

    Huomaa, että tässä valintaikkunassa ei ole lisäkysymyksiä, jotka koskevat muodon yhdistämismääritystä, jota on käytettävä tuodun tiedoston jäsentämiseen ja tietojen siirtämiseen tietomalliin. Tämä johtuu siitä, että vain yksi muoto käyttää tätä mallia, joka on merkitty tietojen tuontia varten suunnitelluksi.  
    
    Määritä tositetunnus erottamaan tuodut tapahtumat muista mahdollisista manuaalisesti annetuista tai tuoduista tapahtumista.  

24. Kirjoita Anna tositetunnus -kenttään IMPORT-001.

    Siirry 1099entries.xml-tiedostoon.  

25. Valitse OK.

    Luotujen varoitusten luettelossa on tietoja esimerkiksi virheellisistä toimittajatileistä, virheellisestä valmisteverolomakkeen ruutukoodista ja puuttuvista maakoodeista. Vertaa tätä varoitusluetteloa suoritettavaan XML-tiedostoon sisältyvään luetteloon.  

26. Sulje sivu.
27. Sulje sivu.
28. Sulje sivu.
29. Sulje sivu.
30. Valitse Ostoreskontra > Kausittaiset tehtävät > Valmistevero (1099) > Toimittajien tilitykset valmisteveroja (1099) varten.

    Tax1099Summary-taulun kumulatiiviset tapahtumat näkyvät tässä lomakkeessa. Nämä tapahtumat on luotu tuotujen tapahtumien perusteella.  

31. Syötä Päivämäärästä-kenttään päivämäärä 1.1.2000.
32. Valitse Manuaaliset 1099-tapahtumat.

    Tässä lomakkeessa on luettelo manuaalisesti lisätyistä ja tuoduista tapahtumista.  

33. Avaa Tosite-sarakkeen suodatin.
34. Anna suodattimen arvo IMPORT-001 Tosite-kentässä käyttämällä alkaa-suodatinoperaattoria.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>Mallin ja muodon yhdistämismääritysten suhteen tarkasteleminen
1. Sulje sivu.
2. Sulje sivu.
3. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
4. Valitse Raportointikonfiguraatiot.
5. Valitse puussa 1099-maksumalli.

    Oletetaan, että haluat tukevat samojen tietojen tuontia, mutta tuonti tapahtuu .TXT-tiedostomuodosta.   

6. Avaa valintaikkuna valitsemalla Luo konfigurointi. 
7. Anna Uusi-kenttään Muoto perustuu tietomalliin 1099-maksumalli.
8. Kirjoita Nimi-kenttään tuo TXT-tiedoston tiedot.
9. Valitse Tukee tietojen tuontia -kentässä Kyllä.
10. Valitse Luo konfiguraatio.
11. Valitse Suunnittelutoiminto.
12. Valitse Yhdistä muoto malliin.
13. Valitse Uusi.
14. Anna tai valitse Määritys-kentän arvo.

    Valitse vaihtoehto 1099-MISC.  

15. Kirjoita Nimi-kenttään tuo TXT-tiedoston tiedot.
16. Kirjoita Kuvaus-kenttään tuo TXT-tiedoston tiedot.
17. Valitse Tallenna.
18. Sulje sivu.
19. Sulje sivu.
20. Valitse Muokkaa.

    Jos olet asentanut hotfix-korjauksen KB 4012871 GER-mallien yhdistämismääritysten tuki erillisinä määrityksenä sekä mahdollisuus määrittää erilaiset ennakkoedellytykset niiden käyttöönottamiseksi Dynamics 365 Financen eri versioissa ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), suorita annetulle muotomääritykselle seuraava vaihe, Mallin määrityksen oletusarvo -merkinnän ottaminen käyttöön. Ohita seuraava vaihe muussa tapauksessa.  

21. Valitse Mallin määrityksen oletusarvo -kentässä Kyllä.
22. Valitse puussa 1099-maksumalli.
23. Valitse Suunnittelutoiminto.
24. Valitse Yhdistä malli tietolähteeseen.
25. Valitse Suorita.

    Jos olet asentanut hotfix-korjauksen KB 4012871, GER-mallien yhdistämismääritysten tuki, erillisinä määrityksinä ja valmiudella määrittää erilaiset ennakkoedellytykset niiden käyttöönottamiseksi eri versioissa ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)), valitse hakukentästä ensisijainen mallin yhdistämismääritys. Jos et ole vielä asentanut hotfix-korjausta, ohita seuraava vaihe, sillä oletusmuotomäärityksen määritelmä on jo valinnut yhdistämismäärityksen.  
    
    Jos et ole vielä asentanut hotfix-korjausta KB 4012871, huomaa, että valintaikkunassa mallin yhdistämismääritystä koskeva lisäkysymys, jonka avulla tuotava tiedosto jäsennetään. Tiedot siirretään sitten valintaikkunasta tietomalliin. Käytettävä muodon yhdistämismääritys voidaan tällä hetkellä valita sen mukaan, minkä tyyppinen tiedosto aiotaan tuoda.  
    
    Jos aiot kutsua tämän mallin yhdistämismäärityksen toimintoa varten suunnitellusta sovelluksen pisteestä, ER-kohde ja muodon yhdistämismääritys on merkittävä integraation osaksi.  

26. Valitse Peruuta.
27. Sulje sivu.
28. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
