---
title: Suunniteltujen tilausten tarkasteleminen, hallinta ja hyväksyminen
description: Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tarkastelusta, hallinnasta ja hyväksymisestä.
author: ChristianRytt
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 71ec26bea2063bcf8b6d302a7ece804b3ac934b3
ms.sourcegitcommit: 3673eeca1ada0f3e4ec277176515a946706f8a41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304364"
---
# <a name="view-manage-and-approve-planned-orders"></a>Suunniteltujen tilausten tarkasteleminen, hallinta ja hyväksyminen

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa on tietoja suunnittelun optimoinnin suunniteltujen tilausten tarkastelusta, hallinnasta ja hyväksymisestä.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Suunniteltujen tilausten tarkasteleminen ja hallinta

Voit tarkastella ja hallita suunniteltuja tilauksia minkä tahansa suunnitellun tilauksen luettelosivulla. Siirry yhteen seuraavista paikoista sen mukaan, minkä tyyppisiä suunniteltuja tilauksia haluat käyttää:

- Pääsuunnittelu \> Työtila \> Pääsuunnittelu
- Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset
- Tuotannonhallinta \> Tuotantotilaukset \> Suunnitellut tuotantotilaukset
- Hankinta \> Ostotilaukset \> Suunnitellut ostotilaukset
- Varastonhallinta \> Saapuvat tilaukset \> Suunnitellut siirrot
- Varastonhallinta \> Lähtevät tilaukset \> Suunnitellut siirrot

## <a name="view-and-edit-the-status-of-planned-orders"></a>Tarkastele ja muokkaa suunniteltujen tilausten tilaa

Kunkin suunnitellun tilauksen **Tila**-kentän avulla voit seurata etenemistäsi tai muuttaa suunnitellun tilauksen käsittelyjärjestystä. Seuraavat **Tila**-arvot ovat käytettävissä:

- **Käsittelemätön** – Kun pääsuunnittelu luo suunniteltuja tilauksia, niille annetaan tämä tila. Tässä tilassa olevat suunnitellut tilaukset poistetaan seuraavan suunnittelun suorittamisen aikana.
- **Valmis** – Tämä tila ilmaisee, että suunniteltu tilaus on valmis. Jos et halua vahvistaa suunniteltua tilausta, voit muuttaa sen tilaksi manuaalisesti *Valmis*. Huomaa, että *Käsittelemätön*- ja *Valmis*-tiloja käsitellään järjestelmässä samalla tavalla.
- **Hyväksytty** – Tämä tila ilmaisee, että suunniteltu tilaus on hyväksytty vahvistettavaksi. Jos haluat vahvistaa suunnitellun tilauksen, voit muuttaa sen tilaksi *Hyväksytty*. Jos haluat säilyttää suunniteltuun tilaukseen tehdyt muutokset tai jos aiot vahvistaa suunnitellun tilauksen, muuta sen tilaksi *Hyväksytty*. Suunnitellut tilaukset, joiden tila on *Hyväksytty*, pidetään valmiina. Niiden toimitusta odotetaan pääsuunnittelussa. Siksi niitä ei muokata tai poisteta myöhemmin pääsuunnittelun suorituksissa. Tämän käytöksen saavuttamiseksi suunnittelulogiikka kopioi *Hyväksytty*-tilassa olevat suunnitellut tilaukset vanhasta suunnitelmaversiosta uuteen suunnitelmaversioon pääsuunnittelun aikana. Huomaa, että *Hyväksytty*-tilassa olevia suunniteltuja tilauksia pidetään tarjontana vain tietyssä pääsuunnitelmassa.

Jos haluat muuttaa yksittäisen suunnitellun tilauksen tilan, [avaa jokin suunniteltujen tilausten luettelosivu](#view-planned-orders), avaa tilaus ja noudata sitten toista seuraavista vaiheista:

- Muuta **Yleinen**-pikavälilehdellä **Tila**-kentän arvoa.
- Valitse toimintoruudun **Suunniteltu tilaus**-välilehden **Prosessi**-ryhmässä **Muuta tila**.
- Voit merkitä tilauksen hyväksytyksi valitsemalla toimintoruudussa **Hyväksy**.

Jos haluat muuttaa usean suunnitellun tilauksen tilaa samanaikaisesti, [avaa jokin suunniteltujen tilausten luettelosivu](#view-planned-orders), valitse kunkin muutettavan tilauksen valintaruutu ja tee jokin seuraavista vaiheista:

- Valitse toimintoruudun **Suunniteltu tilaus**-välilehden **Prosessi**-ryhmässä **Muuta tila**.
- Voit merkitä tilaukset hyväksytyksi valitsemalla toimintoruudussa **Hyväksy**.

## <a name="approve-planned-orders"></a>Suunniteltujen tilausten hyväksyminen

Suunniteltujen tilausten hyväksyminen on valinnainen vaihe. Se tehdään luotaessa vahvistettu tilaus suunnitellusta tilauksesta.

Seuraavassa kuvassa näytetään, kuinka voit käyttää kullekin suunnitellulle tilaukselle määritettyä **Tila**-arvoa hyväksyntätyönkulun käyttöönotossa. Voit ottaa hyväksyntäprosessin käyttöön säätämällä kunkin suunnitellun tilauksen **Tila**-arvon manuaalisesti edellisessä osassa kuvatulla tavalla.

![Suunniteltu tilausten työnkulku](media/approved-planned-orders-1.png)

> [!TIP]
> On suositeltavaa hyväksyä kaikki muokatut suunnitellut tilaukset. Muussa tapauksessa seuraava suunnitteluajo ohittaa ja korvaa muokkaukset.

## <a name="additional-resources"></a>Lisäresurssit

- [Vahvista suunnitellut tilaukset](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
