---
title: Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille
description: Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0c4f028367c894c54392963ffc4f6a0f0c04c03a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795258"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.

Dynamics 365 Commerce -sovelluksen tehtävienhallinnan avulla voit määrittää tehtäväluettelon useille myymälöille tai työntekijöille tai myymälöiden ja työntekijöiden yhdistelmille. Esimerkiksi 20 myymälän aluepäällikkö voi haluta määrittää kaikille 20 myymälälle **Loma-ajan valmistelu** -tehtäväluettelon.

## <a name="start-the-task-list-assignment-process"></a>Tehtäväluettelon määritysprosessin käynnistäminen

Voit aloittaa tehtäväluettelon määrittämisen seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.
1. Valitse määritettävä tehtäväluettelo.
1. Valitse **Käynnistä prosessi**.
1. Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi (esimerkiksi **Itäisen alueen myymälät**).
1. Määritä **Tavoitepvm**-kentässä päivämäärä.
1. Jos haluat määrittää myymälöille tehtäväluettelot, etsi ja valitse myymälät **Myymälät**-välilehden **Organisaatiohierarkia**-suodattimen avulla.

    Voit määrittää tehtäväluettelon työntekijöille etsimällä ja valitsemalla työntekijät **Työntekijät**-välilehdessä.

1. Käynnistä prosessi valitsemalla **OK**. Tehtäväluettelo määritetään valituille myymälöille tai työntekijöille.

Seuraavassa kuvassa on esimerkki siitä, miten myymälät etsitään ja valitaan **Käynnistä prosessi** -valintaikkunassa.

![Myymälöiden etsiminen ja valitseminen Käynnistä prosessi -valintaikkunassa](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Tehtäväluetteloiden määrittäminen toistuviksi

Vähittäiskauppiailla on joskus toistuvia tehtäviä, kuten torstain sulkemisen tarkistuslista tai kuukauden ensimmäisen päivän tarkistuslista. Tämän vuoksi he saattavat haluta määrittää tehtäväluettelon toistuvaksi.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.
1. Valitse määritettävä tehtäväluettelo.
1. Valitse **Käynnistä prosessi**.
1. Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi.
1. Määritä **Toistuvuus**-asetukseksi **Kyllä**.
1. Anna **Toistuvuuden tavoitepvm:n vastakirjaus päivinä** -kenttään päivien määrä. Jos esimerkiksi annat arvoksi **4**, tavoitepäivämäärä on toistumispäivämäärä plus neljä päivää.
1. Valitse **Suorita taustalla** -välilehdessä **Toistuminen**.
1. Anna **Määritä toistuvuus** -valintaikkunaan taajuuden ehdot ja valitse sitten **OK**.

Seuraavassa kuvassa on esimerkki siitä, miten taajuuden ehdot annetaan **Määritä toistuminen** -valintaikkunassa.

![Taajuuden ehtojen antaminen Määritä toistuvuus -valintaikkunassa](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Tehtäväluettelon tilan seuraaminen

Jos olet alue- tai myymäläpäällikkö, haluat ehkä seurata useille myymälöille tai työntekijöille määritettyjen tehtäväluetteloiden tilaa. Tämän jälkeen voit seurata niitä myymälöitä tai työntekijöitä, jotka eivät ole suorittaneet heille määritettyjä tehtäviä ajoissa. Commercen taustatoiminnon avulla voit tarkastella tehtäväluetteloiden tilaa, määrittää tehtäviä uudelleen ja muuttaa tehtävän tilaa.

Voit seurata kaikkien tehtävien tehtäväluettelon tilaa seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.
1. Valitsemalla **Kaikki tehtäväluettelot** -välilehden voit tarkastella eri myymälöihin määritettyjen tehtäväluetteloiden tilaa.

Voit seurata kaikkien sinulle määritettyjen tehtävien tehtäväluettelon tilaa seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan prosessit**.
1. Valitse **Omat tehtävät**- tai **Kaikki tehtävät** -välilehti, jos haluat tarkastella tai päivittää sinulle määritettyjen tehtävien tilaa.

## <a name="additional-resources"></a>Lisäresurssit

[Tehtävien hallinnan yleiskatsaus](task-mgmt-overview.md)

[Tehtävien hallinnan määrittäminen](task-mgmt-configure.md)

[Tehtäväluetteloiden luominen ja tehtävien lisääminen](task-mgmt-create-lists.md)

[Tehtävien hallinta myyntipisteessä](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
