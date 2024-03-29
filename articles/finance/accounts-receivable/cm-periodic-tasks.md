---
title: Säännölliset luotonhallintatehtävät
description: Tässä artikkelissa käsitellään kausittaisia tehtäviä, jotka ovat osa asiakkaiden luottorajojen hallintaprosessia.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9ad72463acba301f7fc931f9fe316a9a9758922e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888003"
---
# <a name="periodic-credit-management-tasks"></a>Säännölliset luotonhallintatehtävät

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään kausittaisia tehtäviä, jotka ovat osa asiakkaiden luottorajojen hallintaprosessia.

## <a name="update-risk-scores"></a>Päivitä riskipisteet

Kun yritykset kehittyvät ja olosuhteet muuttuvat, myös tietyn asiakkaan luottoriskit voivat muuttua. Asiakkaiden asianmukaisten luottorajojen ylläpitäminen edellyttää, että kunkin riskipisteytyksen kriteerit tarkistetaan kausittain ja että kunkin asiakkaan pistemäärät päivitetään. Voit päivittää seuraavat pistemäärät **Päivitä riskipisteet** -sivulla (**Luotonvalvonta \> Kausittaiset tehtävät \> Luotonhallinta \> Päivitä riskipisteet**). Myös kaikki käyttäjän määrittämät laskelmat käsitellään.

- **Maksupäiviä keskimäärin** – tämä pistemäärä on se päivien määrä keskimäärin, joka asiakkaalta menee laskujen maksamiseen.
- **Asiakas lähtien** – tämä pistemäärä on aika vuosina, jonka asiakas on ollut organisaation asiakkaana.
- **Toiminut vuodesta** – Tämä pistemäärä ilmaisee vuosina, kuinka kauan asiakkaan yritystoiminta on kestänyt. Se käyttää **Asiakkaat**-sivun **Yritystoiminta alkoi** -kentän arvoa.
- **Selvittämätön päivämyynti** – tämä pistemäärä perustuu myyntireskontran saldoon, myyntituottoon ja päivien määrää kuluneen 12 kuukauden kaudelta.
- **Keskimääräinen saldo** – tämä pistemäärä perustuu kuluneen 12 kuukauden kauden myyntireskontran saldoon.
- **Luotonhallintaryhmä**, **Tilin tila** ja **Maa** – nämä pistemäärät käyttävät asiakkaalta saatuja tietoja.

## <a name="update-customer-balance-statistics"></a>Asiakkaan saldotilastojen päivittäminen

Voit suorittaa **Päivitä asiakkaan saldotilastot** -prosessin, joka päivittää **Saldotilastokysely**-sivulla näkyvän saldotilastolaskelman. Näitä tietoja käytetään riskipisteiden laskemiseen, ja nämä arvot näkyvät **Asiakas**-sivun luottotilastojen tietoruuduissa.

Kun prosessi suoritetaan, se päivittää yhden asiakkaan saldotilaston. Jos haluat määrittää erätyön suorittamaan prosessin useiden asiakkaiden osalta, voit käyttää **Laske saldotilastot** -sivua (**Luotonhallinta \> Kausittaiset tehtävät \> Laske saldotilastot**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
