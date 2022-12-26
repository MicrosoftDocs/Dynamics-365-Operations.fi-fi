---
title: Kirjanpitotapahtuman selvityskysely
description: Tässä artikkelissa käsitellään Kirjanpitotapahtuman selvityskysely -ikkunaa
author: kweekley
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ae49d9503c0a83bda7e0093ab6ef69fb4aef0a
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853125"
---
# <a name="ledger-settlement-inquiry"></a>Kirjanpitotapahtuman selvityskysely

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **Kirjanpitotapahtuman selvityskysely** -ikkunaa, jossa voidaan tarkastella tilakauden selvitettyjä, selvittämättömiä tai sekä selvitettyjä että selvittämättömiä kirjanpitotapahtumia.

## <a name="view-ledger-settlement-transactions"></a>Kirjanpidon selvitystapahtumien näyttäminen
1.  Valitse **Kirjanpito > Kyselyt ja raportit > Kirjanpitotapahtuman selvityskysely**.
2.  Määritä päivämääräalue **Päivämäärästä**- ja **Päivämäärään**-kenttien tai **Päivämääräväli**-kentän avulla. Pääkirjan osalta päivämääräalueen on oltava yhden tilikauden sisällä.
3.  Valitse **Päätilit**-kentässä tarkasteltavaksi ainakin yhden päätilin kirjanpitotapahtumat. Avattavassa luettelossa ovat vain ne päätilit, jotka on määritetty tapahtuman tilitystä varten **Kirjanpitoparametrit**-sivulla.
4.  Ruudukossa olevat taloushallinnon dimensiot saadaan näkyviin **Taloushallinnon dimensioyhdistelmä** -kentän avulla. Koska päätili on pakollinen, **Päätili**-kentän arvo näkyy aina ensimmäisenä sarakkeena, vaikka valittu taloushallinnon dimensioyhdistelmä ei sisältäisi päätiliä.
5.  Valitse **Tila**-kentässä:
-   **Kaikki**, jos haluat tarkastella sekä selvitettyjä että selvittämättömiä tapahtumia.
-   **Selvittämätön**, jos haluat tarkastella vain selvittämättömiä tapahtumia. 
-   **Selvitetty**, jos haluat tarkastella vain selvitettyjä tapahtumia.
6.  Valitse **Näytä tapahtumat**. Kirjanpitotapahtumat näkyvät ruudukossa annettujen ehtojen perusteella. Kyselyn tulokset voidaan viedä Microsoft Exceliin lisäanalyysia varten. Tee ruudukossa valinta ja pidä valittuna (tai napsauta hiiren kakkospainikkeella).

### <a name="column-details"></a>Sarakkeen tiedot
**Kirjanpitotapahtuman selvityskysely** -sivun ruudukossa on seuraavat sarakkeet:
-   **Päätili** – tämä kenttä on pakollinen ja aina näkyvissä.
-   **Taloushallinnon dimensiot** – taloushallinnon dimensiot näytetään valitun taloushallinnon dimensioyhdistelmän perusteella.
-   **Tapahtumapäivä** – kirjanpitotapahtuman kirjauspäivä.
-   **Alkuperäinen tapahtumapäivä** – Jos tilikauden lopetus on suoritettu ja tapahtuman selvitys on määritetty säilyttämään päätilin tiedot, selvittämättömän tapahtumat tuodaan eriteltyinä alkusaldoksi. Kirjanpitotapahtuman alkuperäinen kirjauspäivä säilytetään **Alkuperäinen tapahtumapäivä** -kentässä.
-   **Tapahtuman ikä** – Kaikkien selvitettyjen tapahtumien arvo on 0 (nolla). Selvittämättömien tapahtumien arvo lasketaan päivien määränä joko alkuperäisestä tapahtumapäivästä tai tapahtumapäivästä kyselyn suorituspäivään.
Esimerkki: Kirjanpitotapahtuman tapahtumapäivä on 1. tammikuuta 2022 (1.1.2022) ja alkuperäinen tapahtumapäivä on 30. joulukuuta 2021 (30.12.2021). Jos kysely suoritetaan 2. tammikuuta 2022 (2.1.2022) tilikaudelle 2022, **tapahtuman ikä** on 4. Tämä arvo lasketaan alkuperäisen tapahtumapäivän (30.12.2021) ja 2.1.2022 välisenä päivien määränä.

Jos alkuperäistä tapahtumapäivää ei ole, sen tilalla käytetään tapahtumapäivää.
-   **(Muut tapahtuman tiedot)** – lisäsarakkeissa on tietoja, kuten tositteen numero, kuvaus sekä debet- ja kredit-summat kolmena valuuttana (tapahtuma-, kirjanpito- ja raportointivaluutta).
-   **Tila** – tämä arvo joko **Selvitetty** tai **Selvittämätön**.
-   **Tilitystunnus** – selvitetyille tapahtumille määritetty tunnus.

[![Kirjanpitotapahtuman selvityskysely -sivu](./media/Inquiry1.png)](./media/Inquiry1.png)

 
Summat voidaan näyttää ruudukon alapuolella.
1.  Valitse kolme pistettä (…) ruudukon oikealla puolella ja valitse sitten **Näytä alatunniste**.
2.  Valitse kukin sarakkeen summa ja pidä se valittuna (tai napsauta sitä hiiren kakkospainikkeella) ja tuo sitten summat näkyviin valitsemalla **Ryhmittele tämän sarakkeen mukaan**. Summat näytetään alatunnisteessa. Jos kysely on suodatettu näyttämään vain selvittämättömät tapahtumat, kokonaissummia voi käyttää summien täsmäyttämiseen pääkirjaan.







