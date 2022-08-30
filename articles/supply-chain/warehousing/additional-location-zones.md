---
title: Sijainnin lisävyöhykkeet
description: Tässä artikkelissa annetaan yleiskatsaus uusista sijainnin vyöhykkeistä, jotka on lisätty Microsoft Dynamics 365 Supply Chain Management -järjestelmään.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 819330e0f6e6cd419da441f919d68ff996b6475c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336512"
---
# <a name="additional-location-zones"></a>Sijainnin lisävyöhykkeet

[!include [banner](../includes/banner.md)]

Kolme uutta vyöhykekenttää on saatavilla Microsoft Dynamics 365 Supply Chain Management -järjestelmässä. Varaston esimiehet voivat käyttää niitä apuna varaston uusien järjestelyjen ja asettelujen määrittämisessä. Uudet vyöhykekentät voidaan asettaa manuaalisesti tai ohjatun **Sijaintien asetus** -toiminnon avulla. Niitä voidaan hyödyntää missä tahansa kyselyssä tai suodatuksessa, joka käyttää Sijainnit-taulukkoa.

Vyöhykekenttien käyttö ei vaadi lisäasetuksia.

## <a name="turn-the-additional-location-zone-feature-on-or-off"></a>Lisävyöhyketoiminnon käyttöönotto tai käytöstä poisto

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.29, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Sijainnin lisävyöhyke* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="use-location-zones"></a>Sijainnin vyöhykkeiden käyttäminen

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varasto \> Ohjattu sijaintien asetustoiminto**.
2. Määritä seuraavat arvot:

    - Valitse **Varasto**-kentässä _62_.
    - Valitse **Vyöhyketunnus**-kentässä _KERROS_.
    - Valitse **Lisävyöhyke 1** -kentässä _VALITSEVYÖHYKE1_.
    - Valitse **Lisävyöhyke 2** -kentässä _VERKKOKAUPPA1_.
    - Valitse **Sijainnin profiilitunnus** -kentässä _KERROS_.

3. Valitse **Kerros**-niminen rivi.
4. Syötä **Ensimmäinen numero** -kenttään arvo _1_. Syötä **Viimeinen numero** -kenttään arvo _3_.
5. Valitse **Käytävä**-niminen rivi.
6. Syötä **Ensimmäinen numero** -kenttään arvo _1_. Syötä **Viimeinen numero** -kenttään arvo _5_.
7. Valitse **Luo**.
8. Näyttöön tulee sanomia, joissa todetaan, että uusia sijainteja on lisätty. Valitse **Näytä sanomat** -painike, jos haluat nähdä sanomat.
9. Valitse **Varastonhallinta \> Asetukset \> Varasto \> Sijainnit**. Uudet sijainnit näkyvät luettelossa, ja kaikki vyöhykekentät (aiemmin luotu vyöhykekenttä ja uudet lisävyöhykekentät) ovat käytettävissä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]