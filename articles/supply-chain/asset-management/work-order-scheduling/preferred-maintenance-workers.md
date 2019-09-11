---
title: Määritä ensisijaiset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka ensisijaiset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887408"
---
# <a name="preferred-maintenance-workers"></a>Ensisijaiset ylläpitotyöntekijät

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Voit määrittää, mitkä kunnossapitotyöntekijät kohdistetaan ensisijaisesti työtilausten ajoituksessa. Tämän toiminnon käyttäminen on valinnaista, mutta sen avulla voit tehdä valinnan pätevimman kunnossapitotyöntekijän kanssa työn suorittamiseksi työntekijöiden taitojen ja osaamisen perusteella. Näin ollen **Ensisijaiset ylläpitotyöntekijät** -asetuksen avulla määritetään, onko työtilaukselle tarkoitus ajoittaa tietty kunnossapitotyöntekijä tai työntekijäryhmä työtilauksen ajoituksen aikana. Vain ajoitushetkellä käytettävissä olevat kunnossapitotyöntekijät ajoitetaan. Jos ensisijaisen kunnossapitotyöntekijän asetus vastaa työtilausta ajoituksen aikana, mutta kunnossapitotyöntekijä kohdistetaan muihin töihin, työtilaus ajoitetaan toiselle, käytettävissä olevalle huoltotyöntekijälle.

Ennen kuin voit määrittää ensisijaisia kunnossapitotyöntekijöitä, sinun on ensin määritettävä ylläpitotyöntekijät ja kunnossapitotyöntekijäryhmät, joiden pitäisi olla valittavissa. Lisätietoja työntekijöiden ja kunnossapitotyöntekijäryhmien määrittämisestä on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Ensisijaisten ylläpitotyöntekijöiden määrittäminen

Ensisijainen kunnossapitotyöntekijä tai työntekijäryhmä voi liittyä tiettyyn

- kauppa  
- ylläpitotyön tyypin muunnos  
- ylläpitotyön tyyppi  
- ylläpitotyön tyypin luokka  
- käyttöomaisuuserä  
- resurssin tyyppi  

tai näiden valintojen yhdistelmä. Mitä enemmän valintoja teet samalle tietueelle, sitä tarkempia ovat määritykset.

1. Valitse **Resurssien hallinta** > **Asetukset** > **työntekijät** > **Ensisijaiset ylläpitotyöntekijät**.

2. Luo uusi tietue valitsemalla **Uusi**.

3. Aloita luomalla "oletusarvoisen" ylläpitotyöntekijän tai työntekijäyhmän asetukset, jolla ei ole valintoja edellä olevan luettelon kentissä. Tämä tarkoittaa, että valitset vain haluamasi **Ensisijainen ylläpitotyöntekijäryhmä**- tai **Ensisijainen ylläpitotyöntekijä** -kentän. Alla olevassa kuvassa on esimerkki ensimmäisestä tietueesta, jossa "Pyynnöt" valitaan ensisijaiseksi kunnossapitotyöntekijäryhmäksi.

>[!NOTE]
>Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä työtilauksen ajoituksen aikana.

4. Luo uusi tietue toistamalla vaihe 2. Tee tarvittavat valinnat ensisijaisen työntekijän tai työntekijäryhmän tietojen yksityiskohtaisuuden tason mukaan. *Esimerkki:* Alla olevassa kuvassa kuudennen tietueen kunnossapitotyöntekijä Shawn Richardson valitaan ensisijaiseksi työntekijäksi. Hänet valitaan automaattisesti sellaisen työtilauksen ajoituksen yhteydessä, joka sisältää käyttöomaisuuden CH-BP1-03-02 ja ylläpitotyötyypin" Facility Assessment", jos hän on käytettävissä ajoitettuna ajankohtana.

>[!NOTE]
>Yleensä kun työtilauksen ajoituksessa valitaan ensisijainen kunnossapitotyöntekijä, käyttöomaisuuden hallinta käy läpi kaikki **Ensisijainen ylläpitotyöntekijä** -tietueet ja etsii mahdollisen vastaavuuden tarkistamalla aina tarkimman yhdistelmän ensin. Jos vastinetta ei löydy, käytetään oletustietuetta, jonka valinta on joko **Ensisijainen ylläpitotyöntekijäryhmä** -kentässä tai **Ensisijainen ylläpitotyöntekijä** -kentässä.


![Kuva 1](media/02-work-order-scheduling.png)

Voit myös määrittää vastuulliset huoltotyöntekijät, jotka voidaan valita, kun kunnossapitopyyntö tai työtilaus luodaan. Voit tarvittaessa muokata valintaa kohdassa **Kaikki työtilaukset** ja **Kaikki ylläpitopyynnöt**. Lisätietoja on kohdassa [Vastuulliset huoltotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).

Työtilausten ajoituksessa lasketaan eri pisteet, joiden perusteella määritetään, mitkä työn tekijät voivat suorittaa työtilaukseen liittyvät työt (nämä pisteet määritetään kohdassa **Resurssienhallinnan parametrit** > **Työtilausten ajoitus** -linkki). Jos vähintään kaksi ensisijaista huoltotyöntekijää tai vastaavaa huolto työntekijä saavat samat pisteet työtilauksen ajoituksessa, toinen työntekijä valitaan satunnaisesti. Muussa tapauksessa työtilauksen suorittaa aina työntekijä, jolla on korkein pistemäärä.

