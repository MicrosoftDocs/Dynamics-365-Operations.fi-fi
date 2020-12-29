---
title: Vastuulliset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka vastuulliset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 113ee2b45c569c7dae3609f1027e31c4e5e5c54a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427183"
---
# <a name="responsible-maintenance-workers"></a>Vastuulliset ylläpitotyöntekijät

[!include [banner](../../includes/banner.md)]

 

Vastuulliset huoltotyöntekijät voivat liittyä resurssityyppeihin, resursseihin, toiminnallisiin sijainteihin, kunnossapitotöiden tyyppiluokkiin, kunnossapidon työtyyppeihin, kunnossapidon työn tyypin variantteihin ja toimialoihin. Niitä voidaan käyttää työtilauksiin ja ylläpitopyyntöihin, jotka ilmaisevat ensisijaisuuden työtilauksesta vastuussa oleville huoltotyöntekijöille. (Nämä kunnossapitotyöntekijät eivät kuitenkaan välttämättä ole samoja työntekijöitä, jotka on ajoitettu suorittamaan työtilauksen.) Tämän toiminnon käyttö on valinnaista. Sen avulla voidaan esimerkiksi valita vastuulliset työntekijät tai työntekijäryhmät tietyille työtyypeille tai työalueille.

Työtilauksen elinkaaren tai huoltopyynnön elinkaaren aikana vastuullisia kunnossapitotyöntekijöitä voidaan muuttaa tai päivittää. Tämä muutos tai päivitys voi liittyä esimerkiksi huoltopyynnön elinkaaren tilan muutokseen tai työtilauksen elinkaaren tilaan.

**Vastuulliset ylläpitotyöntekijät** -sivun asetuksia *ei* käytetä työtilauksen ajoituksen aikana.

> [!NOTE]
> Resurssien hallinnassa voit myös määrittää *ensisijaiset* kunnossapitotyöntekijät, jotka voidaan kohdistaa työtilauksiin työtilauksen ajoituksen aikana.

Ennen kuin voit määrittää vastuullisia kunnossapitotyöntekijöitä, sinun on määritettävä työntekijät ja kunnossapitotyöntekijäryhmät, joiden pitäisi olla valittavissa. Lisätietoja työntekijöiden ja kunnossapitotyöntekijäryhmien määrittämisestä on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-responsible-maintenance-workers"></a>Määritä vastuulliset ylläpitotyöntekijät

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työntekijät** \> **Vastuulliset ylläpitotyöntekijät**.
2. Luo tietue valitsemalla **Uusi**.
3. Luo ensin oletusarvoisen vastuullisen huoltotyöntekijän tai vastuullisen ylläpitotyöntekijäryhmän määritys, jossa määrität vain **Vastuullinen ylläpitotyöntekijäryhmä** -kentän ja/tai **Vastuullinen työntekijä** -kentän. Jätä muut kentät tyhjäksi. Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä.

    > [!NOTE]
    > Huoltopyynnön luomisen aikana, kun vastuullinen huoltotyöntekijä tai vastuullinen kunnossapitotyöntekijäryhmä on valittavissa **Kaikki ylläpitopyynnöt** -sivulla, resurssien hallinta käy läpi kaikki vastuulliset kunnossapitotyöntekijätietueet tarkistaen mahdollisen vastaavuuden. Se tarkistaa aina kaikkein erikoisimman yhdistelmän ensin. Toisin sanoen resurssien hallinta tarkistaa ensin **Kauppa**-kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Ylläpitotyön tyypin variantti** -kentän vastaavuuden. Jos vastaavuutta ei löydy, se tarkistaa **Ylläpitotyön tyyppi** -kentän vastaavuuden ja niin edelleen. Kuten näet sivun asettelussa, tämä tarkoittaa, että löytääksesi täsmällisimman yhdistelmän, resurssien hallinta tarkistaa kunkin tietueen oikealta vasemmalle, jotta osuvuus (ensin **Kauppa**, sitten **Ylläpitotyön tyypin variantti**, sitten **Ylläpitotyön tyyppi**, sitten **Ylläpitotyön tyypin luokka**, sitten **Toiminnallinen sijainti**, sitten **Resurssi** ja lopuksi **Resurssin tyyppi**). Jos vastaavuutta ei löydy, käytetään oletustietuetta, jolla ei ole valintoja kyseisissä seitsemässä kentässä.

Seuraavassa kuvassa on esimerkki **Vastuulliset ylläpitotyöntekijät** -sivusta.

![Vastaavien ylläpitotyöntekijöiden sivu](media/08-setup-for-requests.png)
