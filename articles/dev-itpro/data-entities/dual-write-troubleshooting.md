---
title: Tietojen integroinnin vianmääritysopas
description: Tässä ohjeaiheessa on vianetsintätietoja tietojen integroinnista Microsoft Dynamics 365 for Finance and Operationsin ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797272"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Tietojen integroinnin vianmääritysopas

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Ota laajennusten seuranta käyttöön Common Data Servicessa ja tarkista kaksoiskirjoituksen laajennusvirheiden tiedot.

Jos kaksoiskirjoitussynkronoinnilla on ongelma tai virhe, voit tarkastaa jäljityslokin virheet:

1. Ennen kuin voit tarkastaa virheet, sinun on otettava laajennusten seuranta käyttöön [Laajennuksen rekisteröiminen](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) -ohjeiden avulla laajennuksen jäljityksen mahdollistamiseksi. Nyt voit tarkastaa virheet.
2. Kirjaudu Dynamics 365 for Salesiin.
3. Napsauta Asetukset-kuvaketta (ratas) ja valitse **Lisäasetukset**.
4. Valitse **Asetukset**-valikosta **Mukautus > Laajennuksen jäljitysloki**.
5. Näet virheen tiedot napsauttamalla tyypin nimeä **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Tarkista kaksoiskirjoituksen synkronointivirheet Finance and Operationsissa

Voit tarkistaa virheet testauksen aikana noudattamalla seuraavia vaiheita:

+ Kirjaudu Lifecycle Servicesiin (LCS).
+ Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.
+ Siirry pilvipalveluympäristöihin.
+ Etätyöpöytäyhteys Finance and Operationsin virtuaalikoneeseen käyttämällä paikallista tiliä, joka näkyy LCS:ssä.
+ Avaa tapahtumien katseluohjelma. 
+ Siirry kohtaan **Sovellusten ja palveluiden lokit > Microsoft > Dynamics > AX-DualWriteSync > Toiminnassa**. Virheet ja tiedot näytetään.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Toisen Common Data Service -ympäristön linkityksen poistaminen ja linkittäminen Finance and Operationsissa

Voit päivittää linkkejä noudattamalla seuraavia vaiheita:

+ Siirry Finance and Operations -ympäristöön.
+ Avaa Tietojen hallinta.
+ Valitse **Linkki CDS for Appsiin**.
+ Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse **Pysäytä**. 
+ Valitse kaikki yhdistämismääritykset ja valitse **Poista**.

    > [!NOTE]
    > **Poista**-vaihtoehto ei tule näkyviin, jos **CustomerV3-Account** -malli on valittuna. Poista sen valinta tarvittaessa. **CustomerV3-Account** on vanhempi valmisteltu malli, joka toimii Prospektista käteiseksi -ratkaisun kanssa. Koska se julkaistaan maailmanlaajuisesti, se näkyy kaikkien mallien näkymässä.

+ Valitse **Poista ympäristön linkitys**.
+ Valitse **Kyllä** vahvistusta varten.
+ Voit linkittää uuden ympäristön noudattamalla [asennusoppaan](https://aka.ms/dualwrite-docs) ohjeita.

