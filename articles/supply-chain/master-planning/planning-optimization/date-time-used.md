---
title: Suunnittelun optimoinnissa käytetyt päivämäärä- ja aikaparametrit
description: Tässä aiheessa on tietoja suunnittelun optimoinnin aikana käytettävistä päivämäärä- ja aikaparametreista.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468829"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Suunnittelun optimoinnissa käytetyt päivämäärä- ja aikaparametrit

[!include [banner](../../includes/banner.md)]

Tässä aiheessa on tietoja suunnittelun optimoinnin aikana käytettävistä päivämäärä- ja aikaparametreista.

Kun sisäinen pääsuunnittelumoduuli käyttää kaikissa laskelmissa tapahtumapäivämääriä, suunnittelun optimointi käyttää päivämäärä- ja aika-arvoja, jotka muunnetaan päivämääriksi. Tämä toimintaero voi aiheuttaa tilanteita, joissa esimerkiksi pääsuunnittelun suorituspäivänä keskiyöllä luotuja ennustetapahtumia ei oteta huomioon, koska suunnittelun optimointi katsoo, että ne on luotu ennen kuluvaa päivämäärää.

## <a name="parameters-for-issue-and-demand-transactions"></a>Varasto-otto- ja kysyntätapahtumien parametrit

Seuraavassa taulukossa luetellaan parametrit, joita suunnittelun optimointi käyttää, kun se käsittelee varasto-otto- ja kysyntätapahtumia.

| Parametri | Parametrin nimi suunnittelun optimoinnissa | Kuvaus | Vastaava kenttä Microsoft Dynamics 365 Supply Chain Managementissa (ReqTrans-taulukossa) |
|---|---|---|---|
| Suunniteltu varasto-ottoaika | `PlannedIssueTime` | Päivämäärä, jolle varasto-otto on kulloinkin suunniteltuna. | **Päättymispäivä** (`FuturesDate`) ja **Lykätty aikaan** (`FuturesTime`) |
| Pyydetty varasto-ottoaika | `RequestedIssueTime` | Käyttäjän pyytämä ja Supply Chain Managementissa määritetty varasto-oton päivämäärä. Tämä parametri on sovellettavissa vain vapautettuihin tai hyväksyttyihin suunniteltuihin tilauksiin. Suunniteltujen tilausten osalta se on oletusarvoisesti tyhjä. | **Pyydetty päivämäärä** (`ReqDateDlvOrig`) |
| Vaadittava varasto-ottoaika | `RequiredIssueTime` | Vaadittava varasto-ottoaika, jonka suunnittelun optimointi oikaisee. Jos pyydetty varasto-ottoaika on ohitettu, kun suunnittelun optimointi suoritetaan, vaadituksi varasto-ottoajaksi oikaistaan ensimmäinen avoin päivä, joka ei ole kuluvaa päivää aiemmin. Jos pyydetty varasto-ottoaika on merkitty kalenteriin estetyksi, vaadituksi varasto-ottoajaksi oikaistaan ensimmäinen avoin päivä ennen kyseistä päivämäärää. | **Tarvepäivä** (`ReqDate`) ja **Tarveaika** (`ReqTime`) |
| Varasto-oton aikaviive | `IssueTimeDelay` | Suunnitellun varasto-ottoajan ja joko hyväksyttyjen ja vapautettujen tilausten pyydetyn varasto-ottoajan tai vaaditun varasto-ottoajan välinen ero. | **Viive (päivinä)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Vastaanotto- ja toimitustapahtumien parametrit

Seuraavassa taulukossa luetellaan parametrit, joita suunnittelun optimointi käyttää, kun se käsittelee vastaanotto- ja toimitustapahtumia.

| Parametri | Parametrin nimi suunnittelun optimoinnissa | Kuvaus | Vastaava kenttä Supply Chain Managementissa (ReqTrans- tai ReqPO-taulukossa) |
|---|---|---|---|
| Suunniteltu käytettävyysaika | `PlannedAvailabilityTime` | Päivämäärä, jona lähetyksen suunnitellaan olevan käytettävissä. | **Tarvepäivä** (`ReqDate`) ja **Tarveaika** (`ReqTime`) |
| Suunniteltu vastaanottoaika | `PlannedReceiptTime` | Päivämäärä, jolloin lähetys saapuu sijaintiin. | **Päättymispäivä** (`FuturesDate`), **Lykätty aikaan** (`FuturesTime`) ja **Toimituspäivämäärä** (`ReqDateDlv`) tai **Pyydetty päivämäärä** (`ReqDateDlvOrig`), jos tilausta ei vielä ole vapautettu. |
| Vaadittava käytettävyysaika | `RequiredAvailabilityTime` | Vaadittava käytettävyysaika, jonka suunnittelun optimointi oikaisee. | **Tarvepäivä** (`ReqDate`) ja **Tarveaika** (`ReqTime`) |
| Odotettu vastaanottoaika | `ExpectedReceiptTime` | Vapautetun lähetyksen odotettu vastaanottopäivä. Käyttäjä määrittää arvon Supply Chain Managementissa, eikä suunnittelun optimointi oikaise sitä. Tämä parametri koskee vain vapautettuja lähetyksiä. | **Pyydetty päivämäärä** (`ReqDateDlvOrig`) |
| Vaadittava vastaanottoaika | `RequiredReceiptTime` | Vaadittava vastaanottoaika, jonka suunnittelun optimointi oikaisee. | **Tarvepäivä** (`ReqDate`) ja **Tarveaika** (`ReqTime`) |
| Suunniteltu tilausaika | `PlannedOrderingTime` | Suunnittelun optimoinnin laskema tilauspäivämäärä. | **Tilauspäivä** (`ReqDateOrder`) ja **Tilausaika** (`ReqTimeOrder`) |
| Suunniteltu tehtävän aloitusaika | `PlannedActivityStartTime` | Päivämäärä, jona tämän vastaanoton tehtävän pitäisi alkaa. | **Alkamispäivä** (`SchedFromDate`) |
| Vastaanoton aikaviive | `ReceiptTimeDelay` | Aikaero suunnitellun vastaanottoajan ja vaadittavan vastaanottoajan välillä. | **Viive (päivinä)** ( `FuturesDays`) ja **Lykätty aikaan** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Esimerkkejä suunnittelun optimoinnin päivämääräparametrin käytöstä

Seuraavien kuvien suunnitelmat ovat päivätasolla, mutta suunnittelun optimointi suoritetaan yksityiskohtaisemmalla tasolla. Koska marginaalit voivat olla esimerkiksi tuntien muodoissa, suunnittelun tilausaika voi olla 22. tammikuuta 2021 klo 11.35 jne.

### <a name="example-1-simple-scenario"></a>Esimerkki 1: Yksinkertainen skenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Seuraavia asetuksia käytetään:

- Ei läpimenoaikaa
- Ei kalentereita (Kaikki päivät ovat avoimena).
- Ei marginaaleja

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Yksinkertainen skenaario.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Esimerkki 2: Läpimenoaikaskenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Seuraavia asetuksia käytetään:

- Kolmen päivän läpimenoaika
- Ei kalentereita (Kaikki päivät ovat avoimena).
- Ei marginaaleja

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Läpimenoaikaskenaario.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Esimerkki 3: Marginaaliskenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Seuraavia asetuksia käytetään:

- Kolmen päivän läpimenoaika
- Neljän päivän tilausmarginaali
- Viiden päivän käytettävyysmarginaali
- Ei kalentereita (Kaikki päivät ovat avoimena).

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Marginaaliskenaario.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Esimerkki 4: Viiveskenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Tässä esimerkissä käytetään samoja asetuksia kuin esimerkissä 3, mutta suunnittelupäivämääränä on 15. tammikuuta. Takautuva ajastus (punaiset merkit) epäonnistuu, koska suunnitellun tilausajan on oltava ennen kuluvaa päivämäärää. Pääsuunnittelun on siksi ajoitettava eteenpäin, mistä aiheutuu viiveitä.

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Viiveskenaario](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Esimerkki 5: Siirtoskenaario

Suunniteltu ostotilaus kattaa yhden siirtotilauksen varastosta 1, joka vuorostaan kattaa yhden myyntitilauksen varastosta 2, jonka pyydetty varasto-ottoaika on 22. tammikuuta. Seuraavia asetuksia käytetään:

- Kolmen päivän siirron läpimenoaika (varasto 1)
- Kahden päivän oston läpimenoaika (varasto 2)
- Ei kalentereita (Kaikki päivät ovat avoimena).

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Siirtoskenaario.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Esimerkki 6: Läpimenoaika- ja kalenteriskenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Seuraavia asetuksia käytetään:

- Kolmen päivän läpimenoaika
- Varasto-ottokalenteri (suljettu perjantaina)
- Käytettävyyskalenteri (suljettu torstaina ja perjantaina)
- Vastaanottokalenteri (suljettu tiistaina, keskiviikkona ja sunnuntaina)
- Läpimenoaikakalenteri (suljettu torstaina ja perjantaina)
- Tilauskalenteri (avoimena maanantaina ja lauantaina)

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![Läpimenoaika- ja kalenteriskenaario.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Esimerkki 7: Viive- ja kalenteriskenaario

Yksi ostotilaus kattaa myyntitilauksen, jonka pyydetty varasto-ottoaika on 22.tammikuuta. Tässä esimerkissä käytetään samoja asetuksia kuin esimerkissä 6, mutta suunnittelupäivämääränä on 13. tammikuuta. Takautuva ajastus (punaiset merkit) epäonnistuu, koska suunnitellun tilausajan on oltava ennen kuluvaa päivämäärää. Pääsuunnittelun on siksi ajoitettava eteenpäin, mistä aiheutuu viiveitä.

Tämä skenaario näkyy seuraavassa kuvassa. (Voit avata suuremman version kuvasta valitsemalla sen.)

[![ Viive- ja kalenteriskenaario.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
