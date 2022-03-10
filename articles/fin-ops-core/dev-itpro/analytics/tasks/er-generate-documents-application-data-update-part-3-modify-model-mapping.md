---
title: Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määritysten suunnittelua sähköisen asiakirjan luontia ja sovellustietojen päivitystä varten. (Osa 2 – Asiakirjojen luonti).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d7df46bab244d11509b86a27eeed3c2725400b5eb4d0fbf50af1750e7de45d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745885"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a>Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja

[!include [banner](../../includes/banner.md)]

Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 2: asiakirjojen luominen) -menettely on suoritettu. 

Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten. Tässä menettelyssä muokataan ER-konfiguraatioita ja aloitetaan niiden käyttäminen sähköisten asiakirjojen luomista ja sovellustietojen päivitystä varten. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.


## <a name="modify-data-model"></a>Tietomallin muokkaaminen
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Valitse puussa Intrastat (model).
    * Voit laajentaa tietomallin käyttötapaa. Tietomallia käytetään Intrastat-raportin luonnissa käytettävänä tietolähteenä sekä Intrastat-raportointiprosessin tietojen keräämisessä. Tietoja käytetään tämän jälkeen sovellustietojen päivityksessä.   
3. Valitse Suunnittelutoiminto.
4. Avaa valintaikkuna valitsemalla Uusi.
5. Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".
6. Kirjoita Nimi-kenttään Sovellustietojen päivitystä varten.
    * Sovellustietojen päivitystä varten  
7. ValitseLisää.
8. Valitse puussa For application data update.
    * Tämä uusi juurinimike lisätään määrittämään tietovirta, jota käytetään (tietolähteenä käytettävän) Intrastar-raportin tietojen siirtämiseen sovellustauluihin (päivityskohde). Huomaa, että lähtevään asiakirjaan kirjattujen tietojen ja sovellustietojen päivityksessä käytettävän asiakirjan tietojen haussa on käytettävä eri juurinimikkeitä.   
9. Avaa valintaikkuna valitsemalla Uusi.
10. Syötä Nimi-kenttään Arkiston otsikko.
    * Arkiston otsikko  
11. Valitse Nimiketyyppi-kentässä Tietueluettelo.
12. ValitseLisää.
    * Koska luot jokaiselle luodulle Intrastat-raportille tietueen, raportille on luotava uusi nimike.  
13. Avaa valintaikkuna valitsemalla Uusi.
14. Kirjoita Nimi-kenttään "Tiedoston nimi".
    * Tiedostonimi  
15. Valitse Nimiketyyppi-kentässä Merkkijono.
16. ValitseLisää.
17. Avaa valintaikkuna valitsemalla Uusi.
18. Syötä Nimi-kenttään Rivien määrä.
    * Rivien määrä  
19. Valitse Nimiketyyppi-kentässä Kokonaisluku.
20. ValitseLisää.
    * Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien määrää.  
21. Avaa valintaikkuna valitsemalla Uusi.
22. Syötä Nimi-kenttään Arkiston rivit.
    * Arkiston rivit  
23. Valitse Nimiketyyppi-kentässä Tietueluettelo.
24. ValitseLisää.
    * Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien luetteloa.  
25. Avaa valintaikkuna valitsemalla Uusi.
26. Syötä Nimi-kenttään Summa.
    * Määrä  
27. Valitse Nimiketyyppi-kentässä Reaaliluku.
28. ValitseLisää.
29. Avaa valintaikkuna valitsemalla Uusi.
30. Kirjoita Nimi-kenttään Kauppatavaratietueen tunnus.
    * Kauppatavaratietueen tunnus  
31. Valitse Nimiketyyppi-kentässä Int64.
32. ValitseLisää.
33. Avaa valintaikkuna valitsemalla Uusi.
34. Syötä Nimi-kenttään Nimiketunnus.
    * Nimiketunnus  
35. Valitse Nimiketyyppi-kentässä Merkkijono.
36. ValitseLisää.
37. Valitse Tallenna.
38. Sulje sivu.

## <a name="modify-model-mapping"></a>Mallin yhdistämismäärityksen muokkaaminen
1. Laajenna puussa Intrastat (model).
2. Valitse puussa Intrastat (model)\Intrastat (mapping).
    * Muokkaa aiemmin määritettyä mallin yhdistämismääritystä, kun haluat aloittaa sen käytön sovellustietojen päivityksessä ja Intrastat-raportoinnin tietojen arkistoinnissa.  
3. Valitse Suunnittelutoiminto.
4. Valitse Uusi.
5. Syötä Nimi-kenttään Päivitä arkisto.
    * Arkiston päivittäminen  
6. Valitse Suunta-kentässä Kohteeseen.
7. Valitse Tallenna.
    * Tämä uusi yhdistämismääritys määrittää tietovirran, jota käytetään tietojen (Intrastat-raportoinnin tietojen) siirtämisessä tietomallista sovellustauluihin (päivityskohde). Ota huomioon, että raportointiprosessin sovelluksen tietojen haussa ja sovellustietojen päivityksen tietomallin tietojen käytössä on käytettävä eri mallin juurinimikkeitä.   
8. Valitse Suunnittelutoiminto.
9. Valitse puussa Data model\Data model.
    * Lisää vaadittu tietolähde. Tämä on tietomalli, joka sisältää raportoitujen ja arkistoitavien Intrastat-tapahtumien tiedot.  
10. Valitse Lisää juuri.
11. Kirjoita Nimi-kenttään malli.
    * malli  
12. Syötä tai valitse Määritelmä-kenttään Sovellustietojen päivitystä varten -arvo.
    * Sovellustietojen päivitystä varten  
13. Valitse OK.
14. Laajenna puussa solmu model.
15. Valitse puussa solmu Functions\Calculated field.
16. Valitse puussa model\Archive header.
17. ValitseLisää.
    * Koska haluat luetteloida raportoidut Intrastat-tapahtumat arkistointia varten, soveltuva tietolähde on lisättävä.  
18. Syötä Nimi-kenttään Luetteloidut rivit.
    * Luetteloidut rivit  
19. Valitse Muokkaa kaavaa.
20. Valitse puussa List\ENUMERATE.
21. Valitse Lisää toiminto.
22. Laajenna puussa solmu model.
23. Laajenna puussa model\Archive header.
24. Valitse puussa model\Archive header\Archive lines.
25. Valitse Lisää tietolähde.
26. Syötä Kaava-kenttään ENUMERATE(model.'Archive header'.'Archive lines').
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. Valitse Tallenna.
28. Sulje sivu.
29. Valitse OK.
30. Valitse Lisää kohde.
    * Lisää sovellustaulut pakollisina kohteina, jotka vaativat päivitykset raportoitujen Intrastat-tapahtumien tietojen arkistointia varten.  
31. Kirjoita Nimi-kenttään Arkisto.
    * Arkistoi  
32. Kirjoita Taulun nimi -kenttään IntrastatArchiveGeneral.
    * IntrastatArchiveGeneral  
    * Säilytä tietueen lisäystoiminto, jotta voit lisätä tietueita kunkin Intrastat-raportointiprosessin tietojen arkistoinnin aikana.  
33. Valitse Tietueen infoloki -kentässä Kyllä.
    * Valitse Kyllä, kun haluat hakea sovellustietojen päivityksen ongelmien tiedot.  
34. Valitse Ohita tietueen toiminnon tarkistus -kentässä Kyllä.
    * Valitse Kyllä, jos haluat piilottaa tyhjän Intrastat-arkiston tunnus -kentän tarkistusvirheet. Tämä tehdään tietueiden lisäämisen jälkeen tälle taululle ulkomaankaupan parametrilomakkeessa määritettyjen järjestysnumeroiden asetusten perusteella.  
35. Valitse OK.
    * Sido lisätyn tietolähteen (suodatettu malli, joka perustuu valittuun juurinimikkeeseen) elementit lisätyn kohteen elementtien kanssa.  
36. Laajenna puussa Archive.
37. Laajenna puussa Archive\<Relations.
38. Laajenna puussa Archive\<Relations\IntrastatArchiveDetail.
39. Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).
40. Laajenna puussa model\Archive header\Enumerated lines.
41. Laajenna puussa model\Archive header\Enumerated lines\Value.
42. Valitse puussa model\Archive header\Enumerated lines\Value\Amount.
43. Valitse Sido.
44. Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).
45. Valitse puussa model\Archive header\Enumerated lines\Value\Commodity rec id.
46. Valitse Sido.
47. Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).
48. Valitse puussa model\Archive header\Enumerated lines\Value\Item number.
49. Valitse Sido.
50. Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).
51. Valitse puussa model\Archive header\Enumerated lines\Number.
52. Valitse Sido.
53. Valitse puussa Archive\<Relations\IntrastatArchiveDetail.
54. Valitse puussa model\Archive header\Enumerated lines.
55. Valitse Sido.
56. Valitse puussa Archive\File name(FileName).
57. Valitse puussa model\Archive header\File name.
58. Valitse Sido.
59. Valitse puussa Archive\Number of lines(NumberOfLines).
60. Valitse puussa model\Archive header\Number of lines.
61. Valitse Sido.
62. Valitse puussa Archive.
63. Valitse puussa model\Archive header.
64. Valitse Sido.
65. Valitse Tallenna.
66. Sulje sivu.
67. Sulje sivu.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]