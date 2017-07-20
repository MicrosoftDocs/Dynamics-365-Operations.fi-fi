---
title: "Oppimisen Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään oppimisen Power BI -sisältöä. Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: JCart
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a3f28d21a7e73d3ad462c5cc37198dd2b6f5f8af
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="learning-power-bi-content"></a>Oppimisen Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Power BI -sisällön **oppimista**. Siinä käsitellään sisällön käyttöä ja kerrotaan sisällön rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö

Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **oppimisen** Power BI -sisältö sijaitsee Microsoft Dynamics Lifecycle Servicesin (LCS) Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön

**Oppimisen** Power BI -sisältöön sisältyvissä raporteissa on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                | Sisältö |
|-----------------------|----------|
| Oppimisen yleiskuvaus     | Muiden raporttien yhteenveto |
| Kurssien analysointi       | Rekisteröinti sijainnin mukaan, osallistuja tilan mukaan, kurssit yrityksittäin tyypin mukaan ja kurssin osallistuminen työn mukaan |
| Rekisteröinnin analyysi | Rekisteröintiluettelo |
| Kurssityypit          | Kurssityypit osaamisalueittain |
| Opettaja-analyysi   | Kurssien ja ohjaajien suhde, opettajien määrä, kurssit opettajan mukaan, opettajakohtaiset kurssit ja kurssin työjärjestys opettajan mukaan |
| Tarjotut kurssit       | Kurssiluettelo |
| Kurssien rakenne        | Kurssin työjärjestys |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

**Oppimisen** Power BI -sisällön raporteissa käytetään seuraavia tietoja. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältö perustuu.

| Kokonaisuus           | Sisältö                                                         | Suhteet muihin yksiköihin |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalenterin vastakirjaus  | Kalenterin siirtymät raporttien osittamiseen                                | Kurssin työjärjestys, kurssin osallistujat |
| Yritys           | Yritykset, joiden mukaan raportit suodatetaan                                   | Kurssin työjärjestys, kurssin osallistujat |
| Kurssi           | Kurssi, kuvaus, opettajan nimi, sijainti, huone ja tila | Kurssin työjärjestys, kurssin osallistujat, kurssin osaamisalue |
| Kurssin työjärjestys    | Esityslista, kurssi sekä aloitus- ja lopetusajat                          | Yritys, kalenterin vastakirjaus, päivämäärä, kurssi |
| Kurssin osallistujat | Nimi, tila, työ ja rekisteröinnin päivämäärä                         | Yritys, kalenterin vastakirjaus, päivämäärä, kurssi, demografia, työsuhde, kurssi, työntekijän nimi, työntekijän nimike, työ, toimi |
| Kurssin osaamisalue     | Taito, osaamisalueen tyyppi ja taso                                     | Kurssi |
| Päivämäärä             | Päiviä, viikkoja, kuukausia ja vuosia                                   | Kurssin työjärjestys, kurssin osallistujat |
| Demografia     | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty         | Kurssin työjärjestys, kurssin osallistujat |
| Työsuhde       | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                        | Kurssin työjärjestys, kurssin osallistujat |
| Työ              | Tehtävä, tyyppi ja nimike                                        | Kurssin työjärjestys, kurssin osallistujat |
| Sijainti         | Toimi, nimike ja kokopäiväistä vastaavat (FTE)                  | Kurssin työjärjestys, kurssin osallistujat |
| Työntekijän nimi    | Etunimi , sukunimi ja koko nimi                             | Kurssin osallistujat |
| Työntekijän nimike   | Nimike ja virkaikä                                         | Kurssin osallistujat |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisällössä käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata .pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisällön luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.
