---
title: Osittain varattujen siirtotilauserien vapautus
description: Tässä artikkelissa kerrotaan mobiililaitteen osittain varattujen siirtotilauksen vapautuksen erätoiminnon määrittämisestä ja käyttämisestä.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218679"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Osittain varattujen siirtotilauserien vapautus

[!include [banner](../includes/banner.md)]

Osittain varattujen siirtotilausten vapauttamisen erätoiminto mahdollistaa siirtotilausten osittaisen vapauttamisen varastoon erätyön avulla.
Koska voit vapauttaa osan määrästä, sinun ei tarvitse odottaa, että koko määrä on saatavilla varastossa ennen kuin vapautat tilauksen.

Tilausten vapauttaminen varastoon on varastonhallintaprosessi (WMS). Tämä prosessi käsittää tehtäviä, kuten keräily, pakkaus ja toimitus, jotka varastotyöntekijä voi tehdä mobiililaitteen avulla.

## <a name="where-it-applies"></a>Käyttö

Tässä toiminnossa siirtotilaukset vapautetaan varastoon erätyön avulla. Tämä toiminto on hyödyllinen, jos sinulla ei ole varastossa riittävästi varastoa, mutta haluat siirtää nimikkeitä varastosta toiseen.

## <a name="how-it-is-set-up"></a>Määritysohjeet

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Määritä myyntitilausten ja siirtotilausten täyttämisehdot

Täyttämisehtojen tulee täyttyä ennen kuin tilauksen voi vapauttaa osittain varastoon erässä. Täyttämisehdot määritetään täyttämiskäytännöissä.

Siirto- ja myyntitilausten täyttämiskäytännöt määritetään yrityksen tasolla. Täyttämiskäytännön määrityksistä riippuu, hyväksytäänkö vai hylätäänkö tilausten vapauttaminen eräajossa. Tilaukset käsitellään sitten tavalliseen tapaan.

- Siirto- ja myyntitilauksille luodaan täyttämiskäytäntöjä valitsemalla **Varastonhallinta \> Asetukset \> Varastoon vapauttaminen \> Täyttämiskäytäntö** ja kirjoittamalla sitten käytännölle nimi ja kuvaus.
- Voit määrittää täytäntöönpanoasteen, arvotyypin ja viestin, joka näytetään, jos käytäntöä rikotaan valitsemalla **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Täyttämiskäytäntö**, ja määritä sitten **Täytäntöönpanoaste**, **Arvotyyppi**, ja **Viesti täytäntöönpanon rikkomuksista** -kentät.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Määritä myyntitilausten ja siirtotilausten täyttämiskäytännöt

- Voit asettaa siirtotilausten täyttämiskäytännöt valitsemalla **Varastonhallinta \> Asetukset \> Varasto ja varastonhallinnan parametrit** ja sitten **Siirtotilaukset**-välilehdessä **Varastonhallinta**-osassa valitsemalla siirtotilauksen täyttämiskäytännön.
- Myyntitilausten täyttämiskäytännöt voit asettaa kohdassa **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit** ja sitten **Varastonhallinta**-välilehdessä valitsemalla myyntitilauksen täyttämiskäytännön.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Salli vapauttaminen eräajossa ja aseta erässä vapautettava määrä

Tilaukset vapautetaan varastoon erässä erätyön avulla. Erätyössä ajettavien tilausten tunnistamiseen käytettävät parametrit asetetaan erätyössä itsessään.

**Määrä**-parametri määrää, vapautetaanko erässä koko määrä vai fyysisesti varattu määrä. **Salli osittain vapautettujen tilausten vapautus** -parametri määrää, hyväksytäänkö vai hylätäänkö erässä olevat tilaukset, jos ne on vapautettu osittain aiemmin.

- Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit siirtotilauksille kohdassa **Varastonhallinta \> Vapauta varastoon \> Siirtotilauksien automaattinen vapauttaminen**.
- Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit myyntitilauksille kohdassa **Varastonhallinta \> Vapauta varastoon \> Myyntitilauksien automaattinen vapauttaminen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
