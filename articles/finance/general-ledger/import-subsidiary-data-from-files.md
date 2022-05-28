---
title: Tytäryhtiöiden tietojen tuominen tiedostoista
description: Tässä aiheessa kerrotaan, kuinka tiedot ulkoisista järjestelmistä valmistellaan niin, että ne voidaan tuoda Microsoft Dynamics 365 Financeen.
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 045ecd6dfb95ccf38773293d44834531668ac1ff
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8733816"
---
# <a name="import-subsidiary-data-from-files"></a>Tytäryhtiöiden tietojen tuominen tiedostoista

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, kuinka tiedot ulkoisista järjestelmistä valmistellaan niin, että ne voidaan tuoda Microsoft Dynamics 365 Financeen. **Konsolidoi tuonnin kanssa** -sivun (**Konsolidoinnit \> Konsolidoi tuonnin kanssa**) avulla voit valmistella tytäryhtiöiden tietojen siirtämisen ulkoisista järjestelmistä.

1. Luo tytäryhtiön yritys konsolidointia varten. Lisätietoja yritysten luomisesta on kohdassa [yrityksen luominen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Lisätietoja on kohdissa [Valmistele yritys, jota voidaan käyttää konsolidoinnissa](prepare-company-for-consolidation.md) ja [Määritä tytäryhtiö konsolidointia varten](set-up-subsidiary-company-for-consolidation.md).

2. Valmistele tiedosto, joka sisältää tuodut tiedot. Lisätietoja tietojen tuontiprosessita on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Vie tiedot tiedostoon noudattamalla tietojen tuonti- ja vientiprosessin vaiheita ohjeessa [Tietojen tuonti- ja vientityöt – yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Tämän menetelmän avulla voit konsolidoida tietoja joko toisesta Dynamics 365 Finance -esiintymästä tai Dynamics 365 Business Centralista. Jos tuot tietoja ulkoisista järjestelmistä, tietojen on oltava muodossa, joka on kuvattu kohdassa [Vie tytäryhtiön tiedot tiedostoihin](export-subsidiary-data-to-file.md).
4. Valitse **Konsolidoinnit \> Konsolidoi tuonnin kanssa**. Määritä **Konsolidoi tuonnin kanssa** -sivun **Ehdot**-välilehdessä raportin ja/tai tuonnin tiedot määrittämällä seuraavat kentät.

    | Kenttä                                 | Arvo raporttia varten | Arvo tuontia varten |
    |---------------------------------------|----------------------|----------------------|
    | kuvaus                           | Ei käytettävissä | Kirjoita tuonnin tunnuksena käytettävä kuvaus. |
    | Päätili                          | Määritä raporttiin sisällytettävä tilialue. Jos et määritä aluetta, kaikki tilit sisällytetään mukaan. | Määritä tuontiin sisällytettävä tilialue. Jos et määritä aluetta, kaikki tilit sisällytetään mukaan. |
    | Konsolidointikausi                  | Määritä konsolidoitavat päivämäärävälit. | Määritä konsolidoitavat päivämäärävälit. |
    | Sisällytä todelliset summat                | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää todelliset arvot. | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää todelliset arvot. |
    | Sisällytä budjettisummat                | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää budjettisummat konsolidoinneissa. | Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat sisällyttää budjettisummat konsolidoinneissa. |
    | Saldojen muodostaminen uudelleen konsolidoinnin aikana | Valitse tämän vaihtoehdon arvoksi **Kyllä**, jos uudelleenrakentaminen poistaa saldon ja uudet tietueet kokonaan ja luo saldon uudelleen alusta lähtien. | Valitse tämän vaihtoehdon arvoksi **Kyllä**, jos uudelleenrakentaminen poistaa saldon ja uudet tietueet kokonaan ja luo saldon uudelleen alusta lähtien. |
    | Budjettimallit                         | Ei käytettävissä | Jos olet valinnut tuoda budjettisummia, syötä konsolidoitavat budjettimallit. |
    | Budjettikurssin tyyppi                      | Ei käytettävissä | Anna budjetin vaihtokurssin tyyppi. |

6. Jos käytössä on eri kirjanpitovaluutat, konfiguroi konsolidoinnin aikana tehtävä käännös **Valuutan muuntaminen** -välilehden kenttien avulla.

    | Kenttä                      | kuvaus |
    |----------------------------|-------------|
    | Lähdeoikeushenkilö        | Valitse yritys, josta olet tuomassa. |
    | Kirjanpidon lähdevaluutta | Tämä oletusvaluutta on valuutta, joka liittyy **Lähdeyritys**-kentässä valittuun lähdeyritykseen. |
    | Lähde- ja Kohde-tilit       | Määritä lähdeyrityksestä tuotavien tilien alue. |
    | Vaihtokurssin tyyppi         | Valitse vaihtokurssin tyyppi. Vaihtokurssityypit määritetään, kun luot päätilin. Lisätietoja on ohjeaiheessa [Päätilin luominen](tasks/create-main-account.md). |
    | Käytä vaihtokurssia kohteesta   | Määritä päivämäärä, jolloin tuolloin voimassa ollutta vaihtokurssia käytetään. Voit myös määrittää arvon, jota käytetään vaihtokurssina. |
    | Vaihtokurssi              | Oletusarvo riippuu **Vaihtokurssin tyyppi** kentässä valitusta vaihtokurssin tyypistä. Jos olet määrittänyt käyttäjän määrittämän vaihtokurssin, voit määrittää kurssin. |

7. Määritä **Suorita taustalla** -asetuksen arvoksi **Kyllä**, jos haluat ottaa tuontiprosessin käyttöön taustalle suoritettavaksi.
8. Määritä **Eräkäsittely**-asetuksen arvoksi **Kyllä**, jos haluat suorittaa konsolidoinnin erätyönä tiettynä aikana. Jos haluat suorittaa konsolidoinnin heti, valitse **OK**. 

Konsolidoitaviksi määritetyt tytäryhtiöiden tapahtumat ja saldot lisätään konsolidointiyrityksen tileille.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
