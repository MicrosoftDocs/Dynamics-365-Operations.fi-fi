---
title: Hankinta
description: Tässä ohjeaiheessa kerrotaan hankinnasta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875628"
---
# <a name="procurement"></a>Hankinta


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Käyttöomaisuuden hallinnassa voit saada yleiskatsauksen työtilauksiin liittyvistä ostoehdotuksista ja ostotilauksista. On myös mahdollista luoda työtilauksesta ostotilaus tai ostoehdotus.

**Työtilauksen ostoehdotus** -luettelossa (**Resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen ostoehdotus**), saat näkyviin luettelon työtilauksiin liittyvistä ostoehdotuksista.

- Valitse työtilaustyö **Työtilauksen ostoehdotus** -luettelossa ja napsauta **Ostoehdotus** -painiketta, niin saat näkyviin liittyvän ostoehdotuksen.  
- Valitse työtilaustyö **Työtilauksen ostoehdotus** -luettelossa ja napsauta **Työtilaus** -painiketta, niin saat näkyviin liittyvän työtilauksen.  
- Valitse työtilaustyö **Työtilauksen ostoehdotus** -luettelosta ja valitse **Nimike, missä käytetään** -painike, jos haluat saada yleiskuvan siitä, missä valitulla rivillä olevaa nimikettä käytetään käyttöomaisuuden hallinnassa suhteessa resursseihin, kunnossapitotöiden tyypin oletusarvoihin, varaosiin ja työtilauksiin. 

![Kuva 1](media/08-work-orders.png)


**Työtilauksen osto** -luettelossa (**Yrityksen resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen osto**), saat näkyviin luettelon työtilauksiin liittyvistä ostotilauksista.

- Valitse työtilaustyö **Työtilauksen osto** -luettelossa ja napsauta **Ostotilaus** -painiketta, niin saat näkyviin liittyvän ostotilauksen.  
- Valitse työtilaustyö **Työtilauksen osto** -luettelossa ja napsauta **Työtilaus** -painiketta, niin saat näkyviin liittyvän työtilauksen.  
- Valitse työtilaustyö **Työtilauksen osto** -luettelosta ja valitse **Nimike, missä käytetään** -painike, jos haluat saada yleiskuvan siitä, missä valitulla rivillä olevaa nimikettä käytetään käyttöomaisuuden hallinnassa suhteessa resursseihin, kunnossapitotöiden tyypin oletusarvoihin, varaosiin ja työtilauksiin. 

![Kuva 2](media/09-work-orders.png)


Yllä olevissa luetteloissa toimituspäivämäärän valvontaa koskeva kuvake sijoitetaan kunkin rivin oikealle puolelle. Jos kuvakkeessa näkyy huutomerkki punaisessa ympyrässä, siihen liittyvän ostoehdotuksen tai ostotilauksen toimitus voi viivästyä.

Ostoehdotuksessa mahdollisen viiveen laskemisessa käytettävä päivämäärä löytyy **Ostoehdotukset** -lomakkeen **Ostoehdotuksen otsikko** -pikavälilehden **Pyydetty päivämäärä** -kentässä. Tätä päivää verrataan työtilauksen tai työtilauksen työn käytettävissä olevaan päivään samalla tavalla kuin ostotilauksen päivämäärää.

Ostotilauksessa mahdollisen viiveen laskennassa käytetty päivämäärä on ostotilaus riviin liittyvä päiväys , joka näkyy **Ostotilaus**-lomakkeessa > valitse ostotilaus rivi > **Rivin tiedot** -pikavälilehti > **Asetukset**-välilehti > **Vahvistettu toimituspäivämäärä** -kenttä. Jos tätä kenttää ei täytetä, käytetään **Ostotilauksen otsikko** -pikavälilehden **Toimituspäivämäärä**-kentän päivää. Yhtä näistä päivistä verrataan työtilauksen tai työtilauksen työn käytettävissä olevaan päivään seuraavassa järjestyksessä:

- Työtilauksen todellinen alkamispäivämäärä tai  

- Liittyvän työtilauksen työn ajoitettu alkamispäivämäärä tai  

- Työtilauksen ajoitettu alkamispäivämäärä tai  

- Työtilauksen odotettu alkamispäivämäärä.  


## <a name="create-purchase-order-from-a-work-order"></a>Ostotilauksen luominen työtilauksesta

**Kaikki työtilaukset** -kohdassa valitaan työtilauksen työ ja luodaan siihen liittyvä ostotilaus tai ostoehdotus. Näin varmistetaan ostotilauksen tai ostoehdotuksen ja työtilauksen väliset projektisuhteet.

1. Valitse **Resurssien hallinta** >  **yhteiset** >  **työtilaukset** >  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse **kaikki työtilaukset**- tai **Aktiiviset työtilaukset** -luettelosta työtilaus, jolle haluat luoda ostotilauksen, ja valitse sitten **Muokkaa.**

3. Valitse **Työtilaus**-lomakkeen **Työtilauksen ylläpitotyöt** -pikavälilehdessä työtilaus työ, jolle haluat luoda ostotilauksen.

4. Valitse **Nimiketehtävät** > **Ostotilaus työtilauksen työstä**.

5. Valitse **Projektin ostotilaukset** -luettelosivulla **Uusi**.

6. Luo ostotilaus.

>[!NOTE]
>Ostoehdotuksen luominen on lähes identtinen ostotilauksen luonnin kanssa. Ainoa ero on siinä, että napsautat edellä kuvatussa menetelmässä **Nimiketehtävät** > **Ostoehdotus työtilauksen työstä** vaiheessa 2.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Työtilauksen ja ostotilauksen tai ostoehdotuksen välinen projektisuhde

Ostotilausrivi tai ostoehdotusrivi liittyy työtilaustyöhön työtilausprojektin ja siihen liittyvän projektitehtävän numeron kautta. Kun luot työtilaustyöstä ostotilauksen tai ostoehdotuksen, siihen liittyvä projektitehtävän numero on pakollinen. Projektitehtävän numero lisätään automaattisesti ostotilaukseen tai ostoehdotukseen, jos siihen liittyvä työtilaus sisältää työtilaustöitä, jotka kaikki käyttävät samaa kunnossapitotyötyyppiä. Jos työtilaustyöt sisältävät eri kunnossapitotöiden tyyppejä, projektitehtävän numero on lisättävä manuaalisesti.

Jos haluat nähdä tai lisätä ostotilausriviin liittyvän tehtävänumeron, avaa **Työtilauksen osto** > valitse ostotilaustietue > napsauta ostotilausta **Ostotilaus**-sarakkeessa > **Rivin tiedot** -pikavälilehti > **Projekti**-välilehti > **Tehtävän numero** -kenttä.


![Kuva 3](media/10-work-orders.png)


Samoin jos haluat nähdä tai lisätä työtilauksen ostoehdotusriviin liittyvän tehtävänumeron, avaa **Työtilauksen ostoehdostus** > valitse ostoehdotustietue > napsauta ostoehdotusta **Ostoehdotus**-sarakkeessa > **Rivin tiedot** -pikavälilehti > **Projekti**-välilehti > **Tehtävän numero** -kenttä.

