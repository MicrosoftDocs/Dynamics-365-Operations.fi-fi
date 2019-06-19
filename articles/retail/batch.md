---
title: Eräseurannassa olevien nimikkeiden parannettu käsitteleminen
description: Tässä aiheessa kuvataan parannuksia, jotka on tehty eräseurannassa olevien nimikkeiden vähittäismyynnin laskelman kirjausprosessin aikana tehtävää erien käsittelyä varten.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617386"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Eräseurannassa olevien nimikkeiden parannettu käsitteleminen

Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteen eränumeroita ei voi tallentaa eräseurannassa oleville nimikkeille myynnin aikana. Kun myynti kirjataan pääkonttorissa asiakastilausten tai laskelman kirjauksen avulla, Microsoft Dynamics -järjestelmä kuitenkin odottaa, että tietyissä määrityksissä on sallitut eränumerot eräseurannassa oleville nimikkeille ja että niitä käytetään laskutusprosessin aikana.

Jos tuotteilla on sallitut eränumerot, laskelman kirjauksen asiakastilauksen ja myyntitilauksen laskutusprosessi käyttää niitä. Muussa tapauksessa asiakastilauksen laskutusprosessi ei voi tehdä kirjausta, ja myyntipisteen käyttäjälle lähetetään virhesanoma. Tällöin laskelman kirjaus siirtyy virhetilaan. Tämä virhetila ilmenee, vaikka tuotteille olisi otettu käyttöön negatiivinen varasto.

Microsoft Dynamics for Retail -sovelluksen versioon 10.0.4 ja uudempiin versioihin tehdyt parannukset varmistavat sen, että negatiivisen varaston ollessa käytössä eräseurannassa oleville nimikkeille, asiakastilausten ja myyntitilausten laskutusta laskelman kirjauksen kautta ei estetä nimikkeille, jos varasto on 0 (nolla) tai eränumeroa ei ole saatavilla. Uusi toiminto käyttää myyntiriveissä oletuserätunnusta, kun eränumerot eivät ole saatavilla.

Voit määrittää asiakastilauksissa käytettävän oletuserätunnuksen **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kenttään.

Voit määrittää laskelman kirjauksen myyntitilauksen laskutuksessa käytettävän oletuserätunnuksen **Varaston päivitys** -pikavälilehden **Kirjaus**-välilehden **Vähittäismyynnin parametrit** -sivun **Oletuserätunnus**-kentässä.

> [!NOTE]
> Tämä toiminto on käytettävissä vain, kun edistyksellinen varastotoiminto on käytössä tietyn myymälän varastoa ja nimikkeitä varten. Myöhemmässä versiossa toimintoa tuetaan myös skenaarioissa, joissa edistyksellistä varastonhallintaa ei käytetä.