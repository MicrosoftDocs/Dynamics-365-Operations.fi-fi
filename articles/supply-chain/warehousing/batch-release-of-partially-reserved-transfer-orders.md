---
title: Osittain varattujen siirtotilauserien vapautus
description: Tässä ohjeaiheessa kerrotaan mobiililaitteen osittain varattujen siirtotilauksen vapautuksen erätoiminnon määrittämisestä ja käyttämisestä.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13e3525049c893a7193b549f5b4ba63b8841b87
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233268"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Osittain varattujen siirtotilauserien vapautus

[!include [banner](../includes/banner.md)]

Osittain varattujen siirtotilausten vapauttamisen erätoiminto mahdollistaa siirtotilausten osittaisen vapauttamisen varastoon erätyön avulla.
Koska voit vapauttaa osan määrästä, sinun ei tarvitse odottaa, että koko määrä on saatavilla varastossa ennen kuin vapautat tilauksen.

Tilausten vapauttaminen varastoon on varastonhallinnan lisäprosessi. Tämä prosessi käsittää tehtäviä, kuten keräily, pakkaus ja toimitus, jotka varastotyöntekijä voi tehdä mobiililaitteen avulla.

## <a name="where-it-applies"></a>Käyttö

Tässä toiminnossa siirtotilaukset vapautetaan varastoon erätyön avulla. Tämä toiminto on hyödyllinen, jos sinulla ei ole varastossa riittävästi varastoa, mutta haluat siirtää nimikkeitä varastosta toiseen.

## <a name="how-it-is-set-up"></a>Määritysohjeet

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Määritä myyntitilausten ja siirtotilausten täyttämisehdot

Täyttämisehtojen tulee täyttyä ennen kuin tilauksen voi vapauttaa osittain varastoon erässä. Täyttämisehdot määritetään täyttämiskäytännöissä.

Siirto- ja myyntitilausten täyttämiskäytännöt määritetään yrityksen tasolla. Täyttämiskäytännön määrityksistä riippuu, hyväksytäänkö vai hylätäänkö tilausten vapauttaminen eräajossa. Tilaukset käsitellään sitten tavalliseen tapaan.

-   Siirto- ja myyntitilauksille luodaan täyttämiskäytäntöjä valitsemalla **Varastonhallinta** \> **Asetukset** \> **Varastoon vapauttaminen** \> **Täyttämiskäytäntö** ja kirjoittamalla sitten käytännölle nimi ja kuvaus.

-   Voit määrittää täytäntöönpanoasteen, arvotyypin ja viestin, joka näytetään, jos käytäntöä rikotaan valitsemalla **Varastonhallinta** \> **Asetukset** \> **Vapauta varastoon** \> **Täyttämiskäytäntö**, ja määritä sitten **Täytäntöönpanoaste**, **Arvotyyppi**, ja **Viesti täytäntöönpanon rikkomuksista** -kentät.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Määritä myyntitilausten ja siirtotilausten täyttämiskäytännöt

-   Voit asettaa siirtotilausten täyttämiskäytännöt valitsemalla **Varastonhallinta** \> **Asetukset** \> **Varasto ja varastonhallinnan parametrit** \> **Siirtotilaukset** \> **Varastonhallinta** ja valitsemalla sitten siirtotilauksen täyttämiskäytännön.

-   Myyntitilausten täyttämiskäytännöt voit asettaa kohdassa **Myyntireskontra** \> **Asetukset** \> **Myyntireskontran parametrit** \> **Varastonhallinta** ja valitsemalla myyntitilauksen täyttämiskäytännön.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a>Salli vapauttaminen eräajossa ja aseta erässä vapautettava määrä

Tilaukset vapautetaan varastoon erässä erätyön avulla. Erätyössä ajettavien tilausten tunnistamiseen käytettävät parametrit asetetaan erätyössä itsessään.

**Määrä**-parametri määrää, vapautetaanko erässä koko määrä vai fyysisesti varattu määrä. **Salli osittain vapautettujen tilausten vapautus** -parametri määrää, hyväksytäänkö vai hylätäänkö erässä olevat tilaukset, jos ne on vapautettu osittain aiemmin.

-   Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit siirtotilauksille kohdassa **Varastonhallinta** \> **Vapauta varastoon** \> **Siirtotilauksien automaattinen vapauttaminen**.

-   Voit määrittää **Määrä**- ja **Salli osittain vapautettujen tilausten vapautus** -parametrit myyntitilauksille kohdassa **Varastonhallinta** \> **Vapauta varastoon** \> **Myyntitilauksien automaattinen vapauttaminen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]