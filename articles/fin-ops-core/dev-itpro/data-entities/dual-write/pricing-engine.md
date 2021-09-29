---
title: Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa
description: Tässä ohjeaiheessa kuvataan, kuinka hinnoittelumoduulia käytetään Microsoft Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesista.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4467d313aa2518b23434ec05989eb3e87cd35dfa
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485731"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synkronointi tarvittaessa Supply Chain Managementin hinnoittelumoduulin kanssa

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management sisältää hinnoittelumoduulin, joka käsittelee kauppasopimukset, hinnastot, kanta-asiakasohjelmat, kampanjat ja alennukset. Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä. Kun käytät kaksoiskirjoittamista, voit käyttää joko staattista hinnoittelua tai hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa Dynamics 365 Salesin tarjous- ja tilaussivuilla.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Hinnoittelumoduulin käyttäminen Salesin Supply Chain Managementista

1. Siirry Salesissa kohtaan **Myynti \> Tilaukset**.
2. Valitse **Uusi** luodaksesi uuden tilauksen tai valitse olemassa oleva tilaus **Omat tilaukset** -luettelosta.
3. Uuden tilausrivin lisääminen.
4. Jos luot uuden tilauksen, valitse toimintoruudusta **Hintatilaus**. Jos päivität olemassa olevan tilauksen, valitse toimintoruudusta **Laske uudelleen**.

    Seuraavat sarakkeet täytetään automaattisesti:

    + Tietojen määrä
    + Alennusprosentti
    + Alennus
    + Rahdin ennakkosumma
    + Rahdin summa
    + Vero yhteensä
    + Loppusumma
    
5. Sen varmistamiseksi, että järjestelmä ottaa huomioon kauppasopimukset hinnan laskennassa:
    1. Siirry Supply Chain Management -ympäristöön.
    2. Siirry kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
    3. Valitse sivunavigointipalkista **Hinnat**-välilehti.
    4. Poista **kauppasopimuksen arviointi** -pikavälilehdestä **manuaalinen syöttö** -valinta.

## <a name="how-it-works"></a>Näin se toimii

Kun valitset **Hintatilauksen** Salesissa, **Yhteensä**-toiminto **Myyntitilaus \>Näkymä** -välilehden Supply Chain Managementissa on nimeltään liittyvä myyntitilaus. Myynnin tilauksen kokonaissumman arvoja käytetään Supply Chain Managementin vastaavien sarakkeiden täyttämiseen.

Kun myyntitilauksen kokonaissumma lasketaan Supply Chain Managementissa, laskelma laskee asiakkaan ja myyntitilauksessa lueteltujen tuotteiden olemassa olevat kauppasopimukset. Näitä tietoja käytetään summien laskemiseen. Kun **Hintatilaus** valitaan, Sales vastaa automaattisesti kaikkia Supply Chain Managementin asetuksia.

## <a name="limitations"></a>Rajoitukset

Kun Salesin sarakkeet on täytetty, seuraavat rajoitukset ovat voimassa:

+ Supply Chain Managementin kuluja ja kulujen kohdistuksia ei replikoida Salesiin.
+ Hinnoittelu ei ota huomioon erikoisvähittäismyyntihinnoittelua, joka on määritetty **Vähittäismyyntikanava**-sarakkeessa myyntitilausrivisivulla Supply Chain Managementissa.
+ Supply Chain Managementin **Myynninedistämispalkkioiden hallinta** -osassa määritettyjä alennuksia ei oteta huomioon.
+ Hinnoittelu ei ota huomioon myyntisopimuksia.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
