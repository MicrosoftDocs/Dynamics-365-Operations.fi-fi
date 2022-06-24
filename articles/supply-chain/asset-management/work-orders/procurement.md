---
title: Hankinta
description: Tässä artikkelissa kerrotaan hankinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderPurchaseListPagePreviewPane, EntAssetWorkOrderPurchaseListPage, EntAssetWorkOrderPurchaseLineAmountInfoPart, EntAssetWorkOrderPurchReqListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 015499463f1eab4aaa3f3658b3204229382e73cb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893639"
---
# <a name="procurement"></a>Hankinta

[!include [banner](../../includes/banner.md)]

Resurssienhallinnassa voit saada yleiskatsauksen työtilauksiin liittyvistä ostoehdotuksista ja ostotilauksista. Voit myös luoda työtilauksesta ostotilauksen tai ostoehdotuksen.

**Työtilauksen ostoehdotus** -luettelosivulla (**Resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen ostoehdotus**), näkyy luettelo työtilauksiin liittyvistä ostoehdotuksista. Kun valitset työtilaustehtävän tällä sivulla, voit käyttää **Näytä**-ryhmän painikkeita toimintoruudun **Työtilauksen ostoehdotus** -välilehdessä suorittaaksesi erilaisia toimintoja:

- Avaa liittyvä ostoehdotus valitsemalla **Ostoehdotus**. 
- Avaa liittyvä työtilaus valitsemalla **Työtilaus**.
- Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**. Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).

Seuraavassa kuvassa on esimerkki **Työtilauksen ostoehdotus** -luettelosivusta.

![Kuva 1.](media/08-work-orders.png)


**Työtilauksen osto** -luettelosivulla (**Resurssien hallinta** > **Yhteiset** > **Hankinta** > **Työtilauksen osto**), näkyy luettelo työtilauksiin liittyvistä ostotilauksista. Kun valitset työtilaustehtävän tällä sivulla, voit käyttää **Näytä**-ryhmän painikkeita toimintoruudun **Työtilauksen osto** -välilehdessä suorittaaksesi erilaisia toimintoja:

- Avaa liittyvä ostotilaus valitsemalla **Ostotilaus**. 
- Avaa liittyvä työtilaus valitsemalla **Työtilaus**.
- Saat yleiskatsauksen siitä, miten valitulla rivillä olevaa nimikettä käytetään resurssienhallinnassa suhteessa resursseihin, ylläpitotyötyypin oletuksiin, varaosiin ja työtilauksiin, valitse **Nimike, missä käytetty**. Lisätietoja tästä yleiskatsauksesta esitetään kohdassa [Nimike, missä käytetty](../controlling-and-reporting/item-where-used.md).

Seuraavassa kuvassa on esimerkki **Työtilauksen osto** -luettelosivusta.

![Kuva 2.](media/09-work-orders.png)


Sekä luettelosivulla **Työtilauksen osto** että luettelosivulla **Työtilauksen ostoehdotus** kunkin rivin oikealla puolella näkyy symboli, joka liittyy toimituspäivämäärän seurantaan. Jos symboli on huutomerkki punaisessa ympyrässä, siihen liittyvän ostotilauksen tai ostoehdotuksen toimitus voi viivästyä.

Ostotilauksen osalta ostotilaukseen liittyvää päivämäärää käytetään mahdollisen viivästyksen laskemiseen. Voit tarkastella tätä päivämäärää valitsemalla ostotilausrivi **Ostotilaus**-sivulla. Päivämäärä näkyy **Rivitiedot**-pikavälilehden **Asetukset**-välilehden **Vahvistettu toimituspäivämäärä** -kentässä. Jos **Vahvistettu toimituspäivämäärä**-kenttää ei ole määritetty, laskemiseen käytetään **Ostotilauksen otsikko** -pikavälilehden **Toimituspäivämäärä**-kentän päivämäärää. Yhtä näistä päivistä verrataan työtilauksen tai työtilauksen työn käytettävissä olevaan päivään seuraavassa järjestyksessä:

1. Työtilauksen todellinen alkamispäivämäärä  

2. Liittyvän työtilauksen työn ajoitettu alkamispäivämäärä 

3. Työtilauksen ajoitettu alkamispäivämäärä 

4. Työtilauksen odotettu alkamispäivämäärä. 

Kaikissa ostoehdotuksessa mahdollisen viivästyksen laskemiseen käytetään **Ostoehdotukset**-sivun **Ostoehdotuksen otsikko** -pikavälilehden **Pyydetty päivämäärä** -kentän päivämäärää. Tätä päivää verrataan työtilauksen tai työtilaustehtävän käytettävissä olevaan päivään samassa järjestyksessä kuin ostotilauksen osalta.


## <a name="create-a-purchase-order-from-a-work-order"></a>Ostotilauksen luominen työtilauksesta

**Kaikki työtilaukset** -luettelosivulla voit valita työtilaustehtävän ja sitten luoda siihen liittyvän ostotilauksen tai ostoehdotuksen. Näin autat varmistamaan, että ostotilauksen tai ostoehdotuksen ja työtilauksen välillä on projektisuhteita.

1. Valitse **Resurssienhallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.

2. Valitse työtilaus, jolle tehdään ostotilaus, ja sitten **Muokkaa**.

3. Valitse **Työtilauksen ylläpitotyöt** -pikavälilehdessä työtilaustehtävä, jolle haluat luoda ostotilauksen.

4. Valitse **Nimiketehtävät** > **Ostotilaus työtilaustehtävästä**.

5. Valitse **Projektin ostotilaukset** -luettelosivulla **Uusi**.

6. Luo ostotilaus.

>[!NOTE]
>Samalla tavalla voit luoda myös liittyvän ostoehdotuksen. Valitse vaiheessa 4 kuitenkin **Nimiketehtävät** > **Ostoehdotus työtilaustehtävästä**.


## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Työtilauksen ja ostotilauksen tai ostoehdotuksen välinen projektisuhde

Ostotilausrivi tai ostoehdotusrivi liittyy työtilaustyöhön työtilausprojektin ja siihen liittyvän projektitehtävän numeron kautta. Kun luot työtilaustyöstä ostotilauksen tai ostoehdotuksen, siihen liittyvä projektitehtävän numero on pakollinen. Projektitehtävän numero lisätään automaattisesti ostotilaukseen tai ostoehdotukseen, jos siihen liittyvä työtilaus sisältää työtilaustehtäviä, jotka kaikki käyttävät samaa ylläpitotyön tyyppiä. Jos työtilaustehtävillä on erilaisia ylläpitotehtävien tyyppejä, projektitehtävän numero on lisättävä ostotilaukseen tai ostoehdotukseen manuaalisesti.

Voit tarkastella ostotilausriviin liittyvää tehtävänumeroa tai syöttää sen valitsemalla **Työtilauksen osto** -luettelosivulla ostotilauksen tietueen ja sitten **Ostotilaus**-sarakkeessa ostotilauksen linkin. **Tehtävänumero**-kenttä löytyy **Rivitiedot**-pikavälilehden **Projekti**-välilehdeltä.

Alla olevassa kuvassa näkyy esimerkki **Ostotilaus**-sivusta, jossa **Tehtävänumero** on korostettuna.

![Kuva 3.](media/10-work-orders.png)

Samoin voit tarkastella työtilauksen ostoehdotusriviin liittyvää tehtävänumeroa tai syöttää sen valitsemalla **Työtilauksen ostoehdotus** -luettelosivulla ostoehdotuksen tietueen ja sitten **Ostoehdotus**-sarakkeessa ostoehdotuksen linkin. **Tehtävänumero**-kenttä löytyy **Rivitiedot**-pikavälilehden **Projekti**-välilehdeltä.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]