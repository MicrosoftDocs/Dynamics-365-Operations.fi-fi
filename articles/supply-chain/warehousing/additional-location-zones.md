---
title: Sijainnin lisävyöhykkeet
description: Tässä aiheessa annetaan yleiskatsaus uusista sijainnin vyöhykkeistä, jotka on lisätty Microsoft Dynamics 365 Supply Chain Management -järjestelmään.
author: Mirzaab
manager: AnnBe
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9727187ad555f9e3d09beed3f3447a22c29ed22a
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530164"
---
# <a name="additional-location-zones"></a>Sijainnin lisävyöhykkeet

[!include [banner](../includes/banner.md)]

Kolme uutta vyöhykekenttää on saatavilla Microsoft Dynamics 365 Supply Chain Management -järjestelmässä. Varaston esimiehet voivat käyttää niitä apuna varaston uusien järjestelyjen ja asettelujen määrittämisessä. Uudet vyöhykekentät voidaan asettaa manuaalisesti tai ohjatun **Sijaintien asetus** -toiminnon avulla. Niitä voidaan hyödyntää missä tahansa kyselyssä tai suodatuksessa, joka käyttää Sijainnit-taulukkoa.

Vyöhykekenttien käyttö ei vaadi lisäasetuksia.

## <a name="turn-on-the-additional-location-zone-feature"></a>Lisävyöhyketoiminnon käyttöönotto

Ennen kuin voit käyttää *Sijainnin lisävyöhyke* -toimintoa, sen pitää olla otettu käyttöön järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä ottaa sen käyttöön, jos sitä vaaditaan. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Varastonhallinta*
- **Toiminnon nimi:** *Sijainnin lisävyöhyke*

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
