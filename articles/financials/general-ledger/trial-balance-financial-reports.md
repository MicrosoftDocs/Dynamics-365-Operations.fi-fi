---
title: "Pääkirjan talousraportit"
description: "Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a61369033202bdb99fe4b36b24051c64cb9ca4b1
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="trial-balance-financial-reports"></a>Pääkirjan talousraportit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan. 

<a name="default-trial-balance-reports"></a>Pääkirjan oletusraportit
-----------------------------

Microsoft Dynamics 365 for Finance and Operationsin talousraportointi sisältää kolme pääkirjan raporttia..

| Oletusraportti                                 | Toiminnot                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Yksityiskohtainen pääkirja – oletus               | Määrittää kaikkien tilien saldotiedot ja sisältää debet- ja kreditsaldot ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.                  |
| Pääkirjan yhteenveto – oletus                | Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden nettoeron.                                        |
| Pääkirjan yhteenveto vuosittain – oletus | Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron. |

## <a name="building-blocks"></a>Rakenneosat
Pääkirjan talousraporteissa käytetään seuraavia rakenneosia.

| Oletusraportti                                 | Rivimääritys          | Sarakemääritys                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Yksityiskohtainen pääkirja – oletus               | Pääkirja - oletusarvo | Yksityiskohtainen pääkirja – oletus               |
| Pääkirjan yhteenveto – oletus                | Pääkirja - oletusarvo | Pääkirjan yhteenveto - oletusarvo                |
| Pääkirjan yhteenveto vuosittain – oletus | Pääkirja - oletusarvo | Pääkirjan yhteenveto vuosittain - oletusarvo |

### <a name="row-definition"></a>Rivimääritys

Rivimääritys, Pääkirja – Oletusarvo, sisältää yhden rivin, joka hakee kaikki päätilit. Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä. Voit siirtyä raporttia tarkastellessasi yhdelle riville, kun haluat nähdä kunkin tilin tiedot. Voit muokata rivimääritystä niin, että se sisältää enemmän tietoja. Pääkirjan muokkaaminen - oletusrivimääritys, joka sisältää kaikkien tilien rivit. Noudata seuraavia ohjeita.

1.  Valitse **Muokkaa** ja valitse sitten **Lisää rivejä dimensioista**. **Lisää rivejä dimensioista** -komennon avulla voit valita rivimääritykseen haluamasi dimensiot. Tässä rivimäärityksessä käytetään **päätiliä**.
2.  Varmista, että **päätili** sisältää kaikki et-merkit (&) ja valitse sitten **OK**.

Rivimääritys sisältää nyt kaikki oletusyrityksen päätilit.

### <a name="column-definition"></a>Sarakemääritys

Jokaisessa pääkirjan raportissa käytetään eri sarakemääritystä. Nämä sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.

-   **Yksityiskohtainen pääkirja – oletussaraketyypit:**
    -   **DESC** – rivimäärityksen kuvaus
    -   **ACCT** – tilikoodit
    -   **ATTR (3)** – määritteet:
        -   Tapahtumapäivä
        -   Tosite
        -   Kirjauskansion kuvaus
    -   **FD** – vain debet-tiedot sisältävät taloushallinnon tiedot
    -   **FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot
    -   **CALC** – nettoerotus
-   **Pääkirjan yhteenveto – oletussaraketyypit:**
    -   **ACCT** – tilikoodit
    -   **DESC** – rivimäärityksen kuvaus
    -   **ATTR** – määrite:
        -   Tosite
    -   **FD** – alkusaldon taloushallinnon tiedot
    -   **FD** – vain debet-tiedot sisältävät taloushallinnon tiedot
    -   **FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot
    -   **CALC** – nettoerotus
    -   **CALC** – loppusaldo
-   **Pääkirjan yhteenveto vuosittain – oletusarvo**
    -   **ACCT** – tilikoodit
    -   **DESC** – rivimäärityksen kuvaus
    -   **ATTR** – määrite
        -   Tosite
    -   **FD** – kuluvan vuoden alkusaldon taloushallinnon tiedot
    -   **FD** – vain kuluvan vuoden debet-tiedot sisältävät taloushallinnon tiedot
    -   **FD** – vain kuluvan vuoden kredit-tiedot sisältävät taloushallinnon tiedot
    -   **CALC** – nettoerotus
    -   **CALC** – loppusaldo
    -   **FD** – vain edellisen vuoden debet-tiedot sisältävät taloushallinnon tiedot
    -   **FD** – vain edellisen vuoden kredit-tiedot sisältävät taloushallinnon tiedot



<a name="additional-resources"></a>Lisäresurssit
--------

[Talousraportointi](financial-reporting-getting-started.md)

[Raporttien näyttäminen](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)




