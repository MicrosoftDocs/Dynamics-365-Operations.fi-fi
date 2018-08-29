---
title: "Yritysten väliset tietolähteet sähköisessä raportoinnissa (ER)"
description: "Tässä ohjeaiheessa kerrotaan yritystenvälisten tietolähteiden käytöstä sähköisessä raportoinnissa (ER)."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 201d0f1e3fddd662748008c7304d67ef6003ef02
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="cross-company-data-sources-in-electronic-reporting-er"></a>Yritysten väliset tietolähteet sähköisessä raportoinnissa (ER)

[!include[banner](../includes/banner.md)]

Voit suunnitella sähköisen raportoinnin (ER) muotoja luodaksesi lähteviä tiedostoja eri muodoissa. Kun asiakirja luodaan, ER-muoto kutsuu tietolähteitä, jotka määritettiin vastaavassa ER-mallin määrityksessä. Voit määrittää tietojen noutamisen käyttöoikeudet sovelluksen tauluihin käyttämällä ER-tietolähteitä, joiden tyyppi on **Taulukkotietueet**. Tietolähde palauttaa kaikki tietueet käytettäessä taulua, joka on jaettu taulu (toisin sanoen taulu, johon tiedot tallennetaan ilman yrityksen tunnusta). Käytettäessä yrityksestä riippuvaa taulukkoa (toisin sanoen taulu, johon tiedot tallennetaan yrityskohtaisesti) tietolähde palauttaa vain tietueet, jotka on tallennettu nykyiselle yritykselle (toisin sanoen yrityskonteksti, jossa ER-muotoa suoritetaan).

Mallimäärityksen jokainen tietolähde, jonka tyyppi on **Taulukkotietueet**, voidaan nyt merkitä yritystenväliseksi tietolähteeksi. Siksi voit käyttää sovelluksen taulujen yritystenvälisiä tietoja käyttämällä tietolähteitä, joiden tyyppi on **Taulukkotietueet**. 

Jos merkitset tietolähteen yritystenväliseksi, tapahtuu seuraavaa:

- Tietolähde, joka viittaa mihin tahansa jaettuun tauluun paitsi CompanyInfo-tauluun, palauttaa kaikki viitatun taulun tietueet. 
- Tietolähde, joka viittaa CompanyInfo-tauluun, vaikka CompanyInfo on jaettu taulu, palauttaa tietueet, jotka sisältävät määritetyn vaikutusalueen yrityksen tunnuksen.
- Yrityksestä riippuvalle taululle tietolähde palauttaa viitatun taulun tietueet, jotka sisältävät määritetyn vaikutusalueen yrityksen tunnuksen.

Kun järjestelmäkyselyn valintaikkunassa **Kysy kyselyä** -vaihtoehto on valittuna kaikille tietolähteille, jotka on merkitty yritystenväliseksi, voit sisällyttää yhden tai useita yrityksiä manuaalisesti **Yritysalue**-välilehdessä.

> [!IMPORTANT]
> Kuten muutkin suodattimet, yrityssuodatin säilytetään kyselyiden viimeksi käytettynä arvona suoritettaessa ER-muotoa. Suodatinta ei automaattisesti muuteta, jos muutat tietolähteen yritystenvälistä arvoa. Voit käyttää eri yritystenvälistä arvoa toiseen tietolähteeseen poistamalla vastaavan käyttäjäkohtaisen valinnan.

Jokaiselle tietolähteelle, joka on merkitty yritystenväliseksi, voit valita haluamasi tietueet käyttämällä ER-lausekkeiden **FILTER**- ja **WHERE**-toimintoja. **dataAreaID**-kenttää voidaan käyttää myös yrityksen tunnuksena. Tällä hetkellä **dataAreaID**-kenttä koskee vain seuraavia ehtotyyppejä, joissa käytetään **FILTER**-toimintoa: 

- Vain ehtoja, joissa on yksi **dataAreaID**-kenttävertailu, tuetaan.
- Sallitaan vain vertailut, joissa on lausekkeita, jotka eivät ole riippuvuussuhteessa tietueluettelon kohteisiin.

Siksi seuraava lauseke on kelvollinen.

    FILTER (MyTable, MyTable.dataAreaID = $StringUserInputParameter)
    While shown below expressions will not pass the validation:
    FILTER (MyTable, MyTable.dataAreaID = MyTable2RecordsList.MyField)
    FILTER (MyTable, 
        OR(
            MyTable.dataAreaID = $StringUserInputParameter1,
            MyTable.dataAreaID = $StringUserInputParameter2
        )
    )

Oletusarvon mukaan vaikutusalue sisältää nykyisen sovelluksen kaikki yritykset. Tätä voidaan kuitenkin rajoittaa. Määritä tietty organisaatiohierarkia muotoon rajoittaaksesi yritystenvälisten tietojen käyttöoikeuksia yhdelle ER-muodolle. Kun hierarkia määritetään ER-muodolle, vain yritysten määritetyssä hierarkiassa esiintyvät tietueet palautetaan, vaikka muoto kutsuu yritystenvälisiä tietolähteitä. Kun ER-muodolle määritetään hierarkiaviite, jota ei enää ole, käytetään oletusarvoista vaikutusaluetta ja muoto kutsuu yritystenvälisiä tietolähteitä. Tässä tilanteessa sovelluksen kaikien yritysten tietueet palautetaan. 

Huomaa, että kun **Käytä luonnosta** -vaihtoehto on valittuna määritetylle yksittäiselle ER-muodon organisaatiohierarkialle, käytetään yrityksiä tämän hierarkian luonnosversiosta, jotta voidaan tunnistaa yritystenvälisten tietolähteiden vaikutusalue. Jos luonnosversiota ei ole, tähän käytetään tämän organisaatiohierarkian viimeksi julkaistun version yrityksiä.

Huomaa, että kun **Käytä luonnosta** -vaihtoehto ei ole valittuna määritetylle yksittäiselle ER-muodon organisaatiohierarkialle, käytetään yrityksiä tämän organisaatiohierarkian viimeksi julkaistusta versiosta, jotta voidaan tunnistaa yritystenvälisten tietolähteiden vaikutusalue. Organisaatiohierarkioiden voimassaolopäivämääriä ei tueta vielä ER-kehyksessä.

Hierarkia voidaan määrittää muodolle tietyllä sivulla, jota voidaan käyttää ER-työtilasta tai käyttämällä valikkokohdetta **Organisaation hallinto -> Sähköinen raportointi -> Muotojen yrityssuodatin**. Sivun käyttö edellyttää, että käyttäjälle on myönnetty **Ylläpidä muotojen yrityssuodattimia** -oikeus (ERMaintainFormatMappingLegalEntityFilters). Muodon hierarkiaan perustuvien yritysten vaikutusalueen rajoitusta käytetään sen rajoituksen lisäksi, että käyttäjä voi määrittää manuaalisesti järjestelmän kyselyvalintaikkunassa. Muotoa suoritettaessa käytetään näiden rajoitusten leikkausta.

Lisätietoja tästä toiminnosta saat toistamalla tehtäväoppaan **ER – Yrityksestä riippuvaisten taulukoiden tietueiden käyttö yritystenvälisessä tilassa**, joka on osa 7.5.4.3 Hanki/Kehitä IT-palvelu/ratkaisukomponentit (10677) -liiketoimintaprosessia, jonka voi ladata [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684). Tässä tehtäväoppaassa viedään läpi prosessin, jossa määritetään ER-mallimääritys ja ER-muoto, jotta voidaan käyttää sovelluksen tauluja yritystenvälisessä tilassa.

Lataa seuraavat tiedostot suorittaaksesi tehtäväoppaan:

- [ER-mallin määritys - CrossCompanyDataAccessModel.xml](https://go.microsoft.com/fwlink/?linkid=874111)
- [ER-muodon määritys - CrossCompanyDataAccessFormat.xml](https://go.microsoft.com/fwlink/?linkid=874111)

