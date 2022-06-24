---
title: Oppimisen Power BI -sisältö
description: Tässä artikkelissa käsitellään oppimisen Power BI -sisältöä.
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
ms.openlocfilehash: 05146eef92fa0ef973df832aa3431ec32ea0c297
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847308"
---
# <a name="learning-power-bi-content"></a>Oppimisen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **oppimisen** Microsoft Power BI -sisältöä.

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