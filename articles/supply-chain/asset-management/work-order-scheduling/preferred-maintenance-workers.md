---
title: Määritä ensisijaiset ylläpitotyöntekijät
description: Tässä ohjeaiheessa kerrotaan, kuinka ensisijaiset ylläpitopitotyöntekijät määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 327cda12a05ad54b310e472a652f1c822ad97142
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215329"
---
# <a name="set-up-preferred-maintenance-workers"></a>Määritä ensisijaiset ylläpitotyöntekijät

[!include [banner](../../includes/banner.md)]

 

Työtilausten ajoittamisen yhteydessä voit määrittää, mikä ylläpitotyöntekijä tai työntekijäryhmä kohdennetaan ensisijaisesti työtilauksen suorittamiselle. Tämän toiminnon käyttäminen on valinnaista, mutta sen avulla voit tehdä valinnan pätevimman kunnossapitotyöntekijän kanssa työn suorittamiseksi työntekijöiden taitojen ja osaamisen perusteella. Vain ajoitushetkellä käytettävissä olevat kunnossapitotyöntekijät ajoitetaan. Jos ensisijaisen ylläpitotyöntekijän asetus vastaa työtilausta ajoituksen aikana, mutta ylläpitotyöntekijä kohdistetaan muihin töihin, työtilaus ajoitetaan toiselle, käytettävissä olevalle ylläpitotyöntekijälle.

Ennen kuin voit määrittää ensisijaisia ylläpitotyöntekijöitä, sinun on ensin määritettävä ylläpitotyöntekijöitä ja työntekijäryhmiä. Kuvaus ylläpitotyöntekijöiden ja työntekijäryhmien määrityksestä esitetään kohdassa [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).

## <a name="set-up-preferred-workers"></a>Ensisijaisten ylläpitotyöntekijöiden määrittäminen

Ensisijainen ylläpitotyöntekijä tai työntekijäryhmä voi liittyä yhteen tai useampaan seuraavista:

- kauppa  
- ylläpitotyön tyypin muunnos  
- ylläpitotyön tyyppi  
- ylläpitotyön tyypin luokka  
- käyttöomaisuuserä  
- resurssin tyyppi  

Mitä enemmän valintoja teet samalle tietueelle, sitä tarkempia ovat määritykset.

1. Valitse **Resurssien hallinta** > **Asetukset** > **työntekijät** > **Ensisijaiset ylläpitotyöntekijät**.

2. Luo uusi tietue valitsemalla **Uusi**.

3. Aloita luomalla "oletusarvoinen" ylläpitotyöntekijä tai työntekijäryhmä. Tämä tarkoittaa, että valitset vain haluamasi **Ensisijainen ylläpitotyöntekijäryhmä**- tai **Ensisijainen ylläpitotyöntekijä** -kentän. Alla olevassa näyttökuvassa on esimerkki ensimmäisestä tietueesta, jossa kentän **Ensisijainen ylläpitotyöntekijäryhmä** -kentän arvoksi valitaan "Pyynnöt".

    [!NOTE] Tätä oletusasetusta käytetään työtilauksen ajoituksen aikana, jos mikään muu, tarkemmin määritettävä yhdistelmä ei vastaa työtilauksen sisältöä.

4. Luo uusi tietue toistamalla vaihe 2. Tee tarvittavat valinnat ensisijaisen työntekijän tai työntekijäryhmän tietojen yksityiskohtaisuuden tason mukaan. 

    *Esimerkki:* Alla olevassa näyttökuvassa kuudennen tietueen ylläpitotyöntekijä Shawn Richardson valitaan ensisijaiseksi työntekijäksi. Hänet valitaan automaattisesti sellaisen työtilauksen ajoituksen yhteydessä, joka sisältää resurssin CH-BP1-03-02 ja ylläpitotyötyypin "Facility Assessment", jos hän on käytettävissä ajoitettuna ajankohtana.

    [!NOTE] Yleensä kun työtilauksen ajoituksessa valitaan ensisijainen kunnossapitotyöntekijä, käyttöomaisuuden hallinta käy läpi kaikki **Ensisijainen ylläpitotyöntekijä** -tietueet ja etsii mahdollisen vastaavuuden tarkistamalla aina tarkimman yhdistelmän ensin. Jos vastinetta ei löydy, käytetään oletustietuetta, jonka valinta on joko **Ensisijainen ylläpitotyöntekijäryhmä** -kentässä tai **Ensisijainen ylläpitotyöntekijä** -kentässä.

![Kuva 1](media/02-work-order-scheduling.png)

Voit myös määrittää *Vastaavat ylläpitotyöntekijät*, jotka voidaan valita, kun ylläpitopyyntö tai työtilaus luodaan. Voit tarvittaessa muokata valintaa kohdassa **Kaikki työtilaukset** ja **Kaikki ylläpitopyynnöt**. Lisätietoja on kohdassa [Vastaavat ylläpitotyöntekijät](../setup-for-maintenance-requests/responsible-workers.md).

Työtilausten ajoituksessa lasketaan eri pisteet, joiden perusteella määritetään, mitkä työn tekijät voivat suorittaa työtilaukseen liittyvät työt (nämä pisteet määritetään kohdassa **Resurssienhallinnan parametrit** > **Työtilausten ajoitus** -linkki). Jos vähintään kaksi ensisijaista huoltotyöntekijää tai vastaavaa huolto työntekijä saavat samat pisteet työtilauksen ajoituksessa, toinen työntekijä valitaan satunnaisesti. Muussa tapauksessa työtilauksen suorittaa aina työntekijä, jolla on korkein pistemäärä.

