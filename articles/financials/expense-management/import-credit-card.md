---
title: "Luottokorttitapahtumien tuonti ja ylläpito"
description: "Tässä ohjeaiheessa kerrotaan, miten kuluihin liittyviä luottokorttitapahtumia tuodaan ja ylläpidetään. Nämä tapahtumat voidaan määrittää niin, että ne tuodaan automaattisesti aikataulun mukaan, tai ne voidaan tuoda manuaalisesti tarvittaessa."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 3379e2f850653cb99231d4ab030b64beb72b626a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Luottokorttitapahtumien tuonti ja ylläpito

[!include[banner](../includes/banner.md)]

Kuluihin liittyvät luottokorttitapahtumat voidaan määrittää niin, että ne tuodaan automaattisesti aikataulun mukaan. Tapahtumat voidaan myös tuoda manuaalisesti tarvittaessa. Luottokorttitapahtumat tuodaan Luottokorttitapahtumat-tietoyksikön välityksellä.

Lisätietoja tietoyksiköistä on kohdassa [Tietoyksiköt](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Tuo luottokorttitapahtumat

1. Valitse **Luottokorttitapahtumat**-sivulla **Tuo tapahtumat**. Jos avaat tietojenhallinnan ensimmäisen kerran, järjestelmän on päivitettävä tietoyksiköiden luettelo ennen jatkamista.
2. Kirjoita tuontityölle yksilöivä nimi **Nimi** -kenttään.
3. Valitse **Lähdetietojen muoto** -kenttään sen tiedoston muoto, josta luottokorttitapahtumat tuodaan.
4. Valitse **Lataa** ja etsi tuotava tiedosto.
5. Kun tiedosto on ladattu, vahvista luottokorttitapahtumien tiedoston ja Luottokorttitapahtumat-tietoyksikön sarakkeiden yhdistämismääritys valitsemalla ruudun **Näytä määritys** -linkki. Jos tuonnissa on määritysvirheitä tai määritystä on muutettava, voit tehdä yhdistämismuutokset joko **Yhdistämismääritysten visualisointi** tai **Yhdistämistiedot** -välilehdellä.
6. Luottokorttitapahtumien automatisointi tehdään valitsemalla **Luo toistuva tietotyö**. Voit sitten määrittää toistovälin, jolla määritetään kuinka usein luottokorttitapahtumat tuodaan. Kun olet valmis, valitse **OK**.
7. Voit tuoda valitun tiedoston valitsemalla **Tuo**.
8. Jos tuonnin aikana tapahtuu virheitä, voit tarkastaa suorituslokista tai väliaikaisista tiedoista virheet, jotka on korjattava, jotta tuonti onnistuu.

> [!NOTE]
> Jos tuot useampaa tiedostomuotoa, luo kullekin tiedostomuodolle erilliset tuontityöt.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Poistettujen työntekijöiden luottokorttitapahtumien määrittäminen uudelleen

Kun työntekijän tietue poistetaan, kyseisen työntekijän Active Directory -hakemistopalvelun (AD DS) tilin käyttö estetään. Työntekijällä voi kuitenkin olla aktiivisia luottokorttitapahtumia, joiden kulut on kirjattava ja korvattava. Voit käyttää **Luottokorttitapahtumat**-sivua ja määrittää työntekijälle minkä tahansa luottokorttitapahtuman, vaikka työntekijä on poistettu.

Valitse vähintään yksi luottokorttitapahtuma ja valitse sitten **Määritä tapahtumat uudelleen**. Valitse sitten toinen työntekijä, jolle luottokorttitapahtuma määritetään. Kun olet siirtänyt luottokorttitapahtuman, ne voidaan valita kuluraporttiin ja maksaa kuluraportin hyväksynnän normaalimenettelyn kautta.
