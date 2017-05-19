---
title: "Pääkirjan talousraportit"
description: "Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ff868bcc202d74f94b6e2f9047a34d83e2ac149f
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="trial-balance-financial-reports"></a>Pääkirjan talousraportit

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan. 

<a name="default-trial-balance-reports"></a>Pääkirjan oletusraportit
-----------------------------

Microsoft Dynamics AX 7:n Talousraportointi-osa sisältää kolme pääkirjan raporttia.

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

 

<a name="see-also"></a>Lisätietoja
--------

[Taloushallinnan raportointi](financial-reporting-getting-started.md)

[Näytä raportit](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)




