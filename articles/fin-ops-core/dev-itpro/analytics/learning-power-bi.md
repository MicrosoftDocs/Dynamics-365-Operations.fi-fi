---
title: Oppimisen Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään oppimisen Power BI -sisältöä.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 668308b0a5cfe2fe242a218250c4f714d6f2c279
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744260"
---
# <a name="learning-power-bi-content"></a>Oppimisen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **oppimisen** Microsoft Power BI -sisältöä.

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

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]