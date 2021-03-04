---
title: Eräseurannassa olevien nimikkeiden parannettu käsitteleminen
description: Tässä aiheessa kuvataan parannuksia, jotka on tehty eräseurannassa olevien nimikkeiden laskelman kirjausprosessin aikana tehtävää erien käsittelyä varten.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef946df30c68373b83660fce98b472dc94b42719
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989590"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Eräseurannassa olevien nimikkeiden parannettu käsitteleminen


[!include [banner](includes/banner.md)]


Myyntipisteen eränumeroita ei voi tallentaa eräseurannassa oleville nimikkeille myynnin aikana. Kun myynti kirjataan pääkonttorissa asiakastilausten tai laskelman kirjauksen avulla, Microsoft Dynamics -järjestelmä kuitenkin odottaa, että tietyissä määrityksissä on sallitut eränumerot eräseurannassa oleville nimikkeille ja että niitä käytetään laskutusprosessin aikana.

Jos tuotteilla on sallitut eränumerot, laskelman kirjauksen asiakastilauksen ja myyntitilauksen laskutusprosessi käyttää niitä. Muussa tapauksessa asiakastilauksen laskutusprosessi ei voi tehdä kirjausta, ja myyntipisteen käyttäjälle lähetetään virhesanoma. Tällöin laskelman kirjaus siirtyy virhetilaan. Tämä virhetila ilmenee, vaikka tuotteille olisi otettu käyttöön negatiivinen varasto.

Retail-sovelluksen versioon 10.0.4 ja uudempiin versioihin tehdyt parannukset varmistavat sen, että negatiivisen varaston ollessa käytössä eräseurannassa oleville nimikkeille, asiakastilausten ja myyntitilausten laskutusta laskelman kirjauksen kautta ei estetä nimikkeille, jos varasto on 0 (nolla) tai eränumeroa ei ole saatavilla. Uusi toiminto käyttää myyntiriveissä oletuserätunnusta, kun eränumerot eivät ole saatavilla.

Voit määrittää asiakastilauksissa käytettävän oletuserätunnuksen **Tilaus**-pikavälilehden **Asiakastilaukset**-välilehden **Kaupan parametrit** -sivun **Oletuserätunnus**-kenttään.

Voit määrittää laskelman kirjauksen myyntitilauksen laskutuksessa käytettävän oletuserätunnuksen **Varaston päivitys** -pikavälilehden **Kirjaus**-välilehden **Kaupan parametrit** -sivun **Oletuserätunnus**-kentässä.

> [!NOTE]
> Tämä toiminto on käytettävissä vain, kun edistyksellinen varastotoiminto on käytössä tietyn myymälän varastoa ja nimikkeitä varten. Myöhemmässä versiossa toimintoa tuetaan myös skenaarioissa, joissa edistyksellistä varastonhallintaa ei käytetä.

> [!NOTE]
> Parannetun eräseurannassa olevien nimikkeiden käsittelyn tuki laskelman kirjaamisen aikana muissa kuin edistyksellisen varastonhallinnan skenaarioissa sisältyi Retail-sovelluksen versioon 10.0.5.
