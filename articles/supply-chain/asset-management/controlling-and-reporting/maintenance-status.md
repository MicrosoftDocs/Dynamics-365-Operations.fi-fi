---
title: Ylläpidon tila
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpidon tila lasketaan resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918346"
---
# <a name="maintenance-status"></a>Ylläpidon tila

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Käyttöomaisuuden hallinnassa voit laskea yhteenvedon, jossa on tietoja uusista, aktiivisista ja valmiista huoltopyynnöistä, työtilauksista ja ylläpitoseisokeista tietyltä kaudelta. Voit tarkastella myös saman kauden suoritettujen kuntoarviointien määrää. Tämän laskennan avulla saat yleiskuvan saapuvien ja suoritettujen kunnossapitopyyntöjen ja työtilausten kuormituksesta.

## <a name="make-a-maintenance-status-calculation"></a>Ylläpidon tilan laskennan suorittaminen

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Ylläpidon tila**.

2. Valitse **Laske tila** -valintaikkunassa kausi, jonka ajalta haluat tehdä laskennan (**Alkamispäivämäärä**- ja **Päättymispäivämäärä** -kentät).

3. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia ylläpitoriveistä haluat liittyen toiminnallisiin sijainteihin. Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin ylläpitorivit näkyvät ylimmällä tasolla, joten rivin tila voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki ylläpitorivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

4. Aloita laskenta valitsemalla **OK**.

5. Valitse toimintoruudun **Ryhmittely...** -ryhmissä asiaankuuluvia painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut toimintoruudun painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

6. Muista napsauttaa **Päivitä**-painiketta, jos haluat päivittää laskemisen aina, kun teet muutoksia aktivoimalla tai poistamalla käytöstä **Ryhmittely...**  -painikkeita tai tekemällä laskelmia uudelle kaudelle.

7. Valitse **Tila**, jos haluat luoda uuden ylläpitotilan laskemisen.

>[!NOTE]
>**Ylläpitotila**-kohdassa näkyvät tulokset koskevat vain huoltopyyntöjä ja työtilauksia, joilla on todellinen alkamispäivämäärä ja -aika. Päättymispäivämäärä ja -aika voivat olla tyhjiä.

*Esimerkki 1:*

Alla olevassa kuvassa **Vuosi**- ja **Kuukausi**-painikkeet on aktivoitu. Tässä saat yleiskuvan ylläpitopyyntöihin ja työtilauksiin liittyvästä kuormituksesta ja suoritusnopeudesta kuukausittain. 

![Kuva 1](media/13-controlling-and-reporting.png)

*Esimerkki 2:*

Alla olevassa kuvassa on lisätty tietoja toiminnallisista sijainneista. Nyt on mahdollista vertailla työmäärää ja suorituskykyä eri toiminnallisissa sijainneissa, jotka voivat edustaa maantieteellisiä sijainteja, tehtaita tai työalueita. 

![Kuva 2](media/14-controlling-and-reporting.png)

