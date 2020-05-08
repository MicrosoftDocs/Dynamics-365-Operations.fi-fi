---
title: Synkronointi Dynamics 365 Supply Chain Management -hinnoittelumoduulin kanssa tarvittaessa
description: Tässä ohjeaiheessa kuvataan, kuinka hinnoittelumoduulia käytetään Microsoft Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesista.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 5ffc0358ff58b2a05aa84b4467a27d88b5e1ec42
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270333"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Synkronointi Dynamics 365 Supply Chain Management -hinnoittelumoduulin kanssa tarvittaessa

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management sisältää hinnoittelumoduulin, joka käsittelee kauppasopimukset, hinnastot, kanta-asiakasohjelmat, kampanjat ja alennukset. Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä. Kun käytät kaksoiskirjoittamista, voit käyttää joko staattista hinnoittelua tai hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesin tarjous- ja tilaussivuilla.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Hinnoittelumoduulin käyttäminen Salesin Supply Chain Managementista

1. Siirry Salesissa kohtaan **Myynti \> Tilaukset**.
2. Valitse **Uusi** luodaksesi uuden tilauksen tai valitse olemassa oleva tilaus **Omat tilaukset** -luettelosta.
3. Uuden tilausrivin lisääminen.
4. Jos luot uuden tilauksen, valitse toimintoruudusta **Hintatilaus**. Jos päivität olemassa olevan tilauksen, valitse toimintoruudusta **Laske uudelleen**.

    Seuraavat kentät täytetään automaattisesti:

    + Tietojen määrä
    + Alennusprosentti
    + Alennus
    + Rahdin ennakkosumma
    + Rahdin summa
    + Vero yhteensä
    + Loppusumma
    
5. Sen varmistamiseksi, että järjestelmä ottaa huomioon kauppa- ja myyntisopimukset hinnan laskennassa:
    1. Siirry Supply Chain Management -ympäristöön.
    2. Siirry kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
    3. Valitse sivunavigointipalkista **Hinnat**-välilehti.
    4. Poista **kauppasopimuksen arviointi** -pikavälilehdestä **manuaalinen syöttö** -valinta.

## <a name="how-it-works"></a>Näin se toimii

Kun valitset **Hintatilauksen** Salesissa, **Yhteensä**-toiminto **Myyntitilaus \>Näkymä** -välilehden Supply Chain Managementissa on nimeltään liittyvä myyntitilaus. Myynnin tilauksen kokonaissumman arvoja käytetään toimitusketjun hallinnan vastaavien kenttien täyttämiseen.

Kun myyntitilauksen kokonaissumma lasketaan Supply Chain Managementissa, laskelma laskee asiakkaan ja myyntitilauksessa lueteltujen tuotteiden olemassa olevat kauppasopimukset ja myyntisopimukset. Näitä tietoja käytetään summien laskemiseen. Kun **Hintatilaus** valitaan, Sales vastaa automaattisesti kaikkia Supply Chain Managementin asetuksia.

## <a name="limitations"></a>Rajoitukset

Kun Salesin kentät on täytetty, seuraavat rajoitukset ovat voimassa:

+ Supply Chain Managementin kuluja ja kulujen kohdistuksia ei replikoida Salesiin.
+ Hinnoittelu ei ota huomioon erikoisvähittäismyyntihinnoittelua, joka on määritetty **Vähittäismyyntikanava**-kentässä myyntitilausrivisivulla Supply Chain Managementissa.
+ Supply Chain Managementin **Myynninedistämispalkkioiden hallinta** -osassa määritettyjä alennuksia ei oteta huomioon.
