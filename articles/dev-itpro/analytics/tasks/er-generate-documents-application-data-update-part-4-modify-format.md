--- 
title: "Sovellustietoja sisältävien asiakirjojen luominen muokkaamalla muotoa"
description: "Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 3 – mallin ja yhdistämismäärityksen muokkaaminen) -menettely on suoritettu."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6c7455e4293993f297aeede4d9d6a50f25ca6c07
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="modify-format-to-generate-documents-with-application-data"></a>Sovellustietoja sisältävien asiakirjojen luominen muokkaamalla muotoa

[!include [task guide banner](../../includes/task-guide-banner.md)]

Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 3: mallin ja yhdistämismäärityksen muokkaaminen) -menettely on suoritettu.

Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten. Tässä menettelyssä muokataan ER-konfiguraatioita, jotta niitä voidaan käyttää sekä sähköisten asiakirjojen luomisessa että sovellustietojen päivityksessä. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.


## <a name="modify-format-to-collect-details-of-reporting"></a>Muodon muokkaaminen raportoinnin tietojen keräämistä varten
1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
2. Laajenna puussa Intrastat (model).
3. Valitse puussa Intrastat (model)\Intrastat (format).
4. Valitse Suunnittelutoiminto.
5. Laajenna puussa File.
6. Laajenna puussa File\Declaration.
7. Valitse puussa File\Declaration\Data.
8. Valitse Monimuotoisuus-kentässä Yksi tai useita.
    * Määritä tämä muotoelementti, kun arkistoit Intrastat-raportointiprosessin tiedot. Tämä nimike edustaa arkiston otsikkotietuetta.  
9. Laajenna puussa File\Declaration\Data.
10. Valitse puussa File\Declaration\Data\Item.
11. Valitse Monimuotoisuus-kentässä Nolla, yksi tai useita.
    * Määritä tämä muotoelementti, kun arkistoit Intrastat-raportointiprosessin tiedot. Tämä nimike edustaa arkistoitujen rivien luetteloa.  
12. Valitse puussa File\Declaration\Data\Item.
13. Valitse puussa File\Declaration\Data\Item\Dim1.
14. Valitse Poissuljettu-kentässä Kyllä.
    * Näitä tietoja ei arkistoida, joten voit sulkea pois tämän muotoelementin Intrastat-raportoinnin tietojen tietolähteestä.  
15. Valitse puussa File\Declaration\Data\Item\Dim1.
16. Valitse puussa File\Declaration\Data\Item\Dim1\property.
17. Valitse Poissuljettu-kentässä Kyllä.
18. Valitse puussa File\Declaration\Data\Item\Dim1\date.
19. Valitse Poissuljettu-kentässä Kyllä.
20. Valitse puussa File\Declaration\Data\Item\Dim2.
21. Valitse Poissuljettu-kentässä Kyllä.
22. Laajenna puussa File\Declaration\Data\Item\Dim2.
23. Valitse puussa File\Declaration\Data\Item\Dim2\property.
24. Valitse Poissuljettu-kentässä Kyllä.
25. Valitse puussa File\Declaration\Data\Item\Dim2\code.
26. Valitse Poissuljettu-kentässä Kyllä.
27. Valitse puussa File\Declaration\Data\Item\Dim3.
    * Muotoelementeillä voi olla sama nimi. Esimerkiksi Dim. Näitä ei voi tunnistaa eksplisiittisesti, kun tätä muotoa käytetään tietolähteenä Intrastat-raportoinnin tietojen arkistoinnissa. Määritä siis näille muotoelementeille vaihtoehtoiset nimet.   
28. Syötä Nimi-kenttään Summa.
    * Määrä  
29. Valitse Monimuotoisuus-kentässä Tasan yksi.
30. Valitse puussa File\Declaration\Data\Item\Dim4.
31. Syötä Nimi-kenttään Nimike.
    * Nimike  
32. Valitse Monimuotoisuus-kentässä Tasan yksi.
    * Rakenteen muotoelementtien lisäksi on arkistoitava seuraavat Intrastat-raportoinnin tiedot: kunkin raportoidun kauppatavaranimikkeen ja luodun tiedoston nimen yksilöllinen tietuetunnus. Koska näitä tietoja ei täytetä Intrastat-raporttiin, sinun on lisättävä näihin tietoelementteihin liittyvä muoto tietolähteen nimikkeinä.  
33. Valitse puussa File\Declaration\Data.
34. Avaa valintaikkuna valitsemalla Lisää.
35. Valitse puussa Data source\Item.
36. Kirjoita Nimi-kenttään "Tiedoston nimi".
    * Tiedostonimi  
37. Valitse Tietotyyppi-kentässä Merkkijono.
38. Valitse OK.
39. Valitse puussa File\Declaration\Data\Item.
40. Valitse Lisää nimike.
41. Kirjoita Nimi-kenttään Kauppatavaratietueen tunnus.
    * Kauppatavaratietueen tunnus  
42. Valitse Tietotyyppi-kentässä Int64.
43. Valitse OK.
44. Valitse Yhdistämismääritys-välilehti.
45. Valitse puussa File\Declaration\Data\File name.
46. Valitse Sido.
47. Laajenna puussa solmu model.
48. Laajenna puussa model\Transactions.
49. Valitse puussa File\Declaration\Data\Item = model.Transactions\Commodity rec id.
50. Valitse puussa model\Transactions\Commodity rec id.
51. Valitse Sido.
52. Valitse Tallenna.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Muodon muokkaaminen raportoinnin tietojen tallentamista varten
1. Valitse Yhdistä muoto malliin.
2. Valitse Uusi.
3. Syötä tai valitse Määritelmä-kenttään Sovellustietojen päivitystä varten -juurinimike.
    * Sovellustietojen päivitystä varten  
4. Kirjoita Nimi-kenttään Yhdistämismääritys tietojen päivitystä varten.
    * Yhdistämismääritys tietojen päivitystä varten  
5. Valitse Tallenna.
    * Tämä yhdistämismääritys määrittää, miten Intrastat-raportin tiedot kerätään tietomalliin ja valitun Sovellustietojen päivitystä varten -juurinimikkeen määrittämän rakenteen. Näitä tietoja, saman Sovellustietojen päivitystä varten -juurinimikkeen mallin yhdistämismääritystä ja Kohteeseen -suuntaa käytetään sovellustietojen päivityksessä. Sovellustietojen päivitys alkaa heti, kun lähtevä Intrastat-raportti on luotu. Ota huomioon, että sovellustietojen päivitys voidaan ohittaa suorituksen aikana, mutta tietomallin on oltava tyhjä (sisältää tyhjän tietueluettelon).   
6. Valitse Suunnittelutoiminto.
    * Ota huomioon, että lähtevän Intrastat-raportin muoto lisätään oletusarvoisesti tämän mallin yhdistämismäärityksen tietolähteeksi.  
    * Sido määritetyn raportin (esitetään tietolähteenä) elementit sen tietomallin elementteihin, joka on suodatettu valitun mallin juurinimikkeen perusteella.  
7. Laajenna puussa Archive header.
8. Laajenna puussa Archive header\Archive lines.
9. Laajenna puussa format.
10. Laajenna puussa format\Declaration: XML Element(Declaration).
11. Laajenna puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
12. Laajenna puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.
13. Laajenna puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount).
14. Laajenna puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item).
15. Laajenna puussa Archive header\Number of lines.
16. Valitse Muokkaa.
17. Valitse puussa List\COUNT.
18. Valitse Lisää toiminto.
19. Laajenna puussa format.
20. Laajenna puussa format\Declaration: XML Element(Declaration).
21. Laajenna puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
22. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item).
23. Valitse Lisää tietolähde.
24. Syötä Kaava-kenttään COUNT(format.Declaration.Data.Item).
    * COUNT(format.Declaration.Data.Item)  
25. Valitse Tallenna.
26. Sulje sivu.
27. Valitse puussa Archive header\File name.
28. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name).
29. Valitse Sido.
30. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number).
31. Valitse puussa Archive header\Archive lines\Item number.
32. Valitse Sido.
33. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value).
34. Valitse puussa Archive header\Archive lines\Amount.
35. Valitse Sido.
36. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id).
37. Valitse puussa Archive header\Archive lines\Commodity rec id.
38. Valitse Sido.
39. Valitse puussa Archive header\Archive lines.
40. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item).
41. Valitse Sido.
42. Valitse puussa Archive header.
43. Valitse puussa format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data).
44. Valitse Sido.
45. Valitse Tallenna.
46. Sulje sivu.
47. Sulje sivu.
48. Sulje sivu.


