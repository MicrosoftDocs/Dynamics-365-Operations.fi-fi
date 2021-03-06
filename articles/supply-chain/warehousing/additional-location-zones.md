---
title: Sijainnin lisävyöhykkeet
description: Tässä aiheessa annetaan yleiskatsaus uusista sijainnin vyöhykkeistä, jotka on lisätty Microsoft Dynamics 365 Supply Chain Management -järjestelmään.
author: Mirzaab
ms.date: 07/01/2020
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
ms.openlocfilehash: ee6e0b824ff16bf757159da5198a4215f4f5d121
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808939"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]