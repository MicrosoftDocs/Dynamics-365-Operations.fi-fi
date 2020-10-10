---
title: Ylläpidon tila
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpidon tila lasketaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889574"
---
# <a name="maintenance-status"></a>Ylläpitotila

[!include [banner](../../includes/banner.md)]

 

Resurssienhallinnassa voit laskea yhteenvedon, jossa on tietoja uusista, aktiivisista ja valmiista ylläpitopyynnöistä, työtilauksista ja ylläpidon käyttökatkoista tietyltä kaudelta. Voit tarkastella myös saman kauden suoritettujen kuntoarviointien määrää. Tämän laskennan avulla saat yleiskuvan saapuvien ja suoritettujen kunnossapitopyyntöjen ja työtilausten kuormituksesta.

## <a name="make-a-maintenance-status-calculation"></a>Ylläpidon tilan laskennan suorittaminen

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Ylläpidon tila**.

2. Valitse **Laske tila** -valintaikkunassa aikaväli, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät).

3. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoriveistä haluat liittyen toiminnallisiin sijainteihin. 

  Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitorivit näkyvät ylimmällä tasolla, joten rivin tila voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
  
  Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitorivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

4. Aloita laskenta valitsemalla **OK**.

5. Valitse **Ryhmittely...**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

6. Muista napsauttaa **Päivitä**-painiketta, jos haluat päivittää laskemisen aina, kun teet muutoksia aktivoimalla tai poistamalla käytöstä **Ryhmittely...**-painikkeita tai tekemällä laskelmia uudelle kaudelle.

7. Valitse **Tila**, jos haluat luoda uuden ylläpitotilan laskemisen.

>[!NOTE]
>**Ylläpitotila**-kohdassa näkyvät tulokset koskevat vain huoltopyyntöjä ja työtilauksia, joilla on todellinen alkamispäivämäärä ja -aika. Päättymispäivämäärä ja -aika voivat olla tyhjiä.

## <a name="example-1"></a>Esimerkki 1

Alla olevassa näyttökuvassa **Vuosi**- ja **Kuukausi**-painikkeet on aktivoitu. Kun nämä **Ryhmittely...**-asetukset on valittu, saat yleiskuvan ylläpitopyyntöihin ja työtilauksiin liittyvästä kuormituksesta ja suoritusnopeudesta kuukausittain. 

![Esimerkki kuukausittaisesta kuormituksesta](media/13-controlling-and-reporting.png)

## <a name="example-2"></a>Esimerkki 2

Alla olevassa näyttökuvassa on lisätty tietoja toiminnallisista sijainneista. Nyt on mahdollista vertailla työmäärää ja suorituskykyä eri toiminnallisissa sijainneissa, jotka voivat edustaa maantieteellisiä sijainteja, tehtaita tai työalueita. 

![Esimerkki kuukausittaisesta kuormituksesta ja toiminnallisista sijainneista](media/14-controlling-and-reporting.png)

