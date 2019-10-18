---
title: Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla
description: Tämän aiheen vaiheissa selitetään, miten Regulatory Configuration Service (RCS) -käyttäjät voivat suunnitella uuden sähköisen raportoinnin eli ER-mallin yhdistämisen käyttämällä Finance and Operationsin metatietoja.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bfe007995c894d6cc86d07ef2b52da65e32e950
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182735"
---
# <a name="access-application-metadata-by-using-er-configuration"></a>Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla

[!include [task guide banner](../../includes/task-guide-banner.md)]

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava Regulatory Configuration Service (RCS) -käyttäjä voi suunnitella uuden sähköisen raportoinnin ER-mallin yhdistämisen sovelluksen metatietojen avulla. Sovelluksen metatietoja käytetään ER-metatietokonfiguraatiolla, joka sisältää ulkomaankauppatapahtumien käyttöön tarkoitetun metatietojen näytejoukon. Näitä varten RCS-sovelluksessa on ensin suoritettava aiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet. Seuraavaksi on suoritettava vaiheet, jotka on käsitelty aiheessa [(ER) RCS:ssä käytettävien sovelluksen metatietojen valmistelu](prepare-application-metadata-rcs.md).

## <a name="prerequisites"></a>Edellytykset
1. Valitse **Kaikki työtilat** > **Sähköinen raportointi**. 
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet. 

## <a name="import-metadata-configuration"></a>Metatietokonfiguraation tuominen 
1. Valitse **metatietojen konfiguraatiot**. 
2. Tuo metatiedot sisältävä ER-metatietokonfiguraatio, joka on määritetty luomaan sähköisiä ulkomaankaupan asiakirjoja. Tämä ER-metatietokonfiguraatio on viety XML-tiedostona samalla, kun toimenpiteen [(ER) Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi](prepare-application-metadata-rcs.md) vaiheita suoritetaan. 
3. Valitse **Vaihto**. 
4. Valitse **Lataa XML-tiedostosta**. 
5. Valitse ensin **Selaa** ja sitten Ulkomaankaupan metatiedot.xml-tiedosto. 
6. Valitse **OK**. 
7. Sulje sivu. 

## <a name="create-data-model-configuration"></a>Tietomallin konfiguraation luominen
1. Valitse **Raportointikonfiguraatiot**. 
2. Avaa valintaikkuna valitsemalla **Luo konfigurointi**. 
3. Kirjoita **Nimi**-kenttään Ulkomaankauppamalli. 
4. Valitse **Luo konfiguraatio**. 
5. Valitse **Suunnittelutoiminto**. 
6. Avaa valintaikkuna valitsemalla **Uusi**. 
7. Kirjoita **Nimi**-kenttään Juuri. 
8. Valitse **Lisää**. 
9. Avaa valintaikkuna valitsemalla **Uusi**. 
10. Kirjoita **Nimi**-kenttään Tapahtuma. 
11. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**. 
12. Valitse **Lisää**. 
13. Avaa valintaikkuna valitsemalla **Uusi**. 
14. Kirjoita **Nimi**-kenttään Kauppatavarakoodi. 
15. Valitse **Nimiketyyppi**-kentässä **Merkkijono**. 
16. Valitse **Lisää**. 
17. Avaa valintaikkuna valitsemalla **Uusi**. 
18. Kirjoita **Nimi**-kenttään Laskutettu summa. 
19. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**. 
20. Valitse **Lisää**. 
21. Avaa valintaikkuna valitsemalla **Uusi**. 
22. Kirjoita **Nimi**-kenttään Päivämäärä. 
23. Valitse **Nimiketyyppi**-kentässä **Päivämäärä**. 
24. Valitse **Lisää**. 
25. Valitse **Juuriviite**. 
26. Valitse **OK**. 
27. Valitse **Tallenna**. 
28. Sulje sivu. 
29. Valitse **Muuta tila**. 
30. Valitse **Valmis**. 
31. Valitse **OK**. 

## <a name="create-model-mapping-configuration"></a>Mallin yhdistämismäärityksen luominen 
1. Avaa valintaikkuna valitsemalla **Luo konfigurointi**. 
2. Anna **Uusi**-kenttään Mallin yhdistämismääritys perustuu tietomallin ulkomaankauppamalliin. 
3. Kirjoita **Nimi**-kenttään Ulkomaankaupan yhdistäminen. 
4. Valitse **Luo konfiguraatio**. 
5. Laajenna **Edellytykset**-osa. 
6. Valitse **Muokkaa**. 
7. Valitse **Uusi**. 
8. Merkitse valittu rivi luettelossa. 
9. Valitse **Edellytysosan tyyppi** -kentässä **Konfigurointi**. 
10. Valitse **Ulkomaankaupan metatiedot** -määritys. 
11. Valitse **Tallenna**. 
12. Ulkomaankaupan metatiedot -määrityksen versioon 1 lisättiin viite. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan. 
13. Sulje sivu. 
14. Valitse **Suunnittelutoiminto**. 
15. Valitse **Suunnittelutoiminto**. 
16. Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**. 
17. Valitse **Lisää juuri**. 
18. Kirjoita **Nimi**-kenttään Intrastat. 
19. Valitse **Intrastat**-taulukkotietueet. 
20. Valitse **OK**. 

> [!NOTE]
> Valittavana on vain kaksi taulukkoa, sillä tällä hetkellä käytössä olevaan metatietosarjaan lisättiin vain kaksi taulukkoa. 

21. Valitse **Sido**. 
22. Laajenna puussa **Intrastat**. 
23. Valitse puussa **Intrastat\AmountMST**. 
24. Laajenna puussa **Tapahtuma = Intrastat**. 
25. Valitse puussa **Tapahtuma = Intrastat\Laskutettu summa**. 
26. Valitse **Sido**. 
27. Valitse puussa **Intrastat\TransDate**. 
28. Valitse puussa **Tapahtuma = Intrastat\Date**. 
29. Valitse **Sido**. 
30. Laajenna puussa **Intrastat\>Suhteet**. 
31. Laajenna puussa **Intrastat\>Relations\IntrastatCommodity**. 
32. Valitse puussa **Intrastat\>Relations\IntrastatCommodity\Code**. 
33. Valitse puussa **Tapahtuma = Intrastat\Kauppatavarakoodi**. 
34. Valitse **Sido**. 
35. Valitse **Vahvista**. 

> [!NOTE]
> Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä sovelluksen tietoja viitatuista ER-metatietokonfiguraatiosta. 
36. Valitse **Tallenna**. 
37. Sulje sivu. 
38. Sulje sivu. 
39. Laajenna aiemmin luotu metatietojoukko tarvittaessa ja vie sitten uusi ER-metatietomäärityksen valmis versio. Voit sitten tuoda sen RCS:hen ja päivittää sellaisen määritetyn mallin yhdistämäärityksen edellytykset, jotka viittaavat tuodun metatietomäärityksen uuteen versioon. 

> [!NOTE]
> Tietojen hankkiminen sovelluksen metatiedoista tällä tavoin on käytettävissä vain paikallisesti käyttöönotetuissa sovelluksissa (kun liiketoimintatietojen paikallista (LBD) käyttöönottomallia käytetään).
        
