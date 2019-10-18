---
title: Tietojen integroinnin vianmääritysopas
description: Tässä ohjeaiheessa on vianetsintätietoja tietojen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.
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
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249106"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Tietojen integroinnin vianmääritysopas

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Ota laajennusten seurantalokit käyttöön Common Data Servicessa ja tarkista kaksoiskirjoituksen laajennusvirheiden tiedot.

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Jos kaksoiskirjoituksen synkronoinnin aikana ilmenee ongelma tai virhe, tarkista jäljityslokin virheet noudattamalla näitä ohjeita.

1. Ennen kuin voit tarkastaa virheet, sinun on otettava käyttöön laajennuksen jäljityslokit. Lisätietoja on seuravan oppaan Näytä seurantaloki -osassa: [Laajennuksen kirjoittaminen ja rekisteröinti](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Nyt voit tarkastaa virheet.

2. Kirjaudu Microsoft Dynamics 365 Salesiin.
3. Valitse ensin **Asetukset**-painike (rataskuvake) ja sitten **Lisäasetukset**.
4. Valitse **Asetukset**-valikosta **Mukautus \> Laajennuksen jäljitysloki**.
5. Näet virheen tiedot napsauttamalla tyypin nimeä **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.

## <a name="inspect-dual-write-synchronization-errors"></a>Kaksoiskirjoituksen synkronointivirheiden tarkastaminen

Tarkista testauksen aikana tapahtuvat virheet noudattamalla näitä ohjeita.

1. Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).
2. Avaa LCS-projekti, jotta voit tehdä kaksoiskirjoitustestauksen.
3. Valitse **Pilvipalveluympäristöt**.
4. Luo etätyöpöytäyhteys sovelluksen virtuaalikoneeseen (VM) käyttämällä LCS:ssä näkyvää paikallista tiliä.
5. Avaa tapahtumien katseluohjelma. 
6. Siirry kohtaan **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**. Virheet ja tiedot näytetään.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Common Data Service -ympäristön linkityksen poistaminen sovelluksesta ja toisen ympäristön linkittäminen

Voit päivittää linkit seuraavien ohjeiden avulla:

1. Siirry sovellusympäristöön.
2. Avaa Tietojen hallinta.
3. Valitse **Linkki CDS for Appsiin**.
4. Valitse kaikki suoritettavat yhdistämismääritykset ja valitse sitten **Pysäytä**.
5. Valitse kaikki yhdistämismääritykset ja valitse sitten **Poista**.

    > [!NOTE]
    > **Poista**-vaihtoehto ei tule näkyviin, jos **CustomerV3-Account** -malli on valittuna. Tyhjennä tämän mallin valinta tarpeen mukaan. **CustomerV3-Account** on vanhempi valmisteltu malli, joka toimii Prospektista käteiseksi -ratkaisun kanssa. Koska se julkaistaan maailmanlaajuisesti, se näkyy kaikkien mallien näkymässä.

6. Valitse **Poista ympäristön linkitys**.
7. Vahvista toiminto valitsemalla **Kyllä**.
8. Voit linkittää uuden ympäristön noudattamalla [asennusoppaan](https://aka.ms/dualwrite-docs) ohjeita.
