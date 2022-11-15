---
title: Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille
description: Tässä artikkelissa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: faff772051738f624b86fd23fb6bf29173e909ea
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746191"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Tehtäväluetteloiden määrittäminen myymälöille tai työntekijöille

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten tehtäväluettelot määritetään myymälöille tai työntekijöille Microsoft Dynamics 365 Commerce -sovelluksessa.

Dynamics 365 Commerce -sovelluksen tehtävienhallinnan avulla voit määrittää tehtäväluettelon useille myymälöille tai työntekijöille tai myymälöiden ja työntekijöiden yhdistelmille. Esimerkiksi 20 myymälän aluepäällikkö voi haluta määrittää kaikille 20 myymälälle **Loma-ajan valmistelu** -tehtäväluettelon.

## <a name="start-the-task-list-assignment-process"></a>Tehtäväluettelon määritysprosessin käynnistäminen

Ennen kuin aloitat tehtävien delegointiprosessin, varmista, että olet luonut tehtäväluettelon noudattamalla [Tehtäväluetteloiden luominen ja tehtävien lisääminen](task-mgmt-create-lists.md) -artikkelissa kuvattuja ohjeita. Voit aloittaa tehtäväluettelon määrittämisen seuraavasti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Tehtävienhallinta \> Tehtävienhallinnan hallinta**.
1. Valitse määritettävä tehtäväluettelo.
1. Valitse **Käynnistä prosessi**.
1. Anna **Käynnistä prosessi** -valintaikkunan **Yleistä**-välilehden **Prosessin nimi** -kenttään nimi (esimerkiksi **Itäisen alueen myymälät**).
1. Määritä **Tavoitepvm**-kentässä päivämäärä.
1. Jos haluat määrittää myymälöille tehtäväluettelot, etsi ja valitse myymälät **Myymälät**-välilehden **Organisaatiohierarkia**-suodattimen avulla.

    Voit määrittää tehtäväluettelon työntekijöille etsimällä ja valitsemalla työntekijät **Työntekijät**-välilehdessä.

1. Käynnistä prosessi valitsemalla **OK**. Tehtäväluettelo määritetään valituille myymälöille tai työntekijöille.

Seuraavassa kuvassa on esimerkki siitä, miten myymälät etsitään ja valitaan **Käynnistä prosessi** -valintaikkunassa.

![Myymälöiden etsiminen ja valitseminen Käynnistä prosessi -valintaikkunassa.](media/HQ-Assign-Tasks-Lists.png)

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

![Taajuuden ehtojen antaminen Määritä toistuvuus -valintaikkunassa.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

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
