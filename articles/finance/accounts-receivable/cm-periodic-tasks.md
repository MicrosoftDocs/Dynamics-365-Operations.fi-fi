---
title: Kausittaiset luotonhallinnan tehtävät
description: Tässä ohjeaiheessa käsitellään kausittaisia tehtäviä, jotka ovat välttämätön osa asiakkaiden luottorajojen hallintaprosessia.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f6b04c28c0f7b5e4d58d464ad45d42478cde4e0ffb584e5afa43c99ebaed7166
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724012"
---
# <a name="periodic-credit-management-tasks"></a>Säännölliset luotonhallintatehtävät

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään kausittaisia tehtäviä, jotka ovat välttämätön osa asiakkaiden luottorajojen hallintaprosessia.

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