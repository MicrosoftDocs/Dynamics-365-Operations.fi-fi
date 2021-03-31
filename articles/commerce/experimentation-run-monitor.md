---
title: Kokeen suorittaminen ja seuranta
description: Tässä ohjeaiheessa käsitellään kokeen suorittamista ja seurantaa kolmannen osapuolen palvelussa. Siinä käsitellään muutosten tekemistä variaatioihin kokeen aloittamisen jälkeen.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 956a9168ed7bf9282d9eeec39587d8e1f2d1856c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224879"
---
# <a name="run-and-monitor-an-experiment"></a>Kokeen suorittaminen ja seuranta

Tässä ohjeaiheessa käsitellään kokeen suorittamista ja seuraamista kolmannen osapuolen sovelluksessa sekä mahdollisia variaatioiden muutoksia. Koe on ensin [julkaistava](experimentation-preview-publish.md) Commercessa, ennen kuin tässä ohjeaiheessa olevat vaiheet voidaan suorittaa. 

Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä ohjeaiheissa.

[ ![Kokeilun käyttäjän siirtymä – suorittaminen ja seuranta](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)

Kun variaatiot on julkaistu, kaikki Commercessa tehtävät kokeen suorittamiseen tarvittavat vaiheet on tehty. Seuraavassa vaiheessa määritetään, mikä variaatio näytetään kullekin käyttäjälle, kun he pyytävät sivua. Kolmannen osapuolen palvelu tekee tämän päätöksen, mutta ennen sitä koe on aktivoitava kyseisessä palvelussa. Koska kokeen aktivointivaiheet ovat palvelukohtaisia, palvelun antamien ohjeiden noudattaminen on välttämätöntä. Jos koetta ei aktivoida, käyttäjät näkevät vain sivun oletusversion (yksikään variaatio ei ole näkyvissä).

Koetta on jatkettava niin kauan, että kerätyistä tiedoista voidaan muodostaa tilastollisesti kelvolliset tulokset. Kokeeseen liittyviä tietoja voi seurata ja analysoida kokeen aikana kolmannen osapuolen palvelussa.

## <a name="adjust-your-variations"></a>Variaatioiden säätäminen
Jos variaatioita on jostain syystä muokattava, voit tehdä sen seuraavien ohjeiden avulla.

> [!IMPORTANT]
> Jos live-kokeiluun tehdään muutoksia Commercessa tai kolmannen osapuolen palvelussa, niillä voi olla merkittäviä vaikutuksia tuloksiin. Jos muutokset ovat merkittäviä, kannattaakin harkita kokeen jatkamista loppuun saakka ja uuden kokeen luomista.

1. Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe. 
1. Valitse päivitettävä variaatio avattavassa valikossa.
1. Tee tarvittavat muutokset ja esikatsele ja julkaise variaatiot sen jälkeen. Lisätietoja on kohdassa [Kokeen esikatseleminen ja julkaiseminen](experimentation-preview-publish.md).
1. Jos muutokset liittyvät kokeen asetuksiin, siirry kolmannen osapuolen palveluun.
    
## <a name="previous-step"></a>Edellinen vaihe
[Kokeen esikatseleminen ja julkaiseminen](experimentation-preview-publish.md)

## <a name="next-step"></a>Seuraava vaihe
[Variaation korottaminen ja kokeen päättäminen](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]