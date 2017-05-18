---
title: Dynamics 365 for Operations -asiakasohjelman UKK
description: "Tässä artikkelissa on vastauksia Microsoft Dynamics 365 for Operations -asiakasohjelmaa koskeviin usein kysyttyihin kysymyksiin."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 94f5874cb24b53476843f1a073dc9c4cfdb36ac9
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-client-faq"></a>Dynamics 365 for Operations -asiakasohjelman UKK

[!include[banner](../includes/banner.md)]


Tässä artikkelissa on vastauksia Microsoft Dynamics 365 for Operations -asiakasohjelmaa koskeviin usein kysyttyihin kysymyksiin.

<a name="why-arent-symbols-loaded-when-i-use-dynamics-365-for-operations"></a>Miksi symbolit eivät ole ladattu käyttäessäni Dynamics 365 for Operationsia?
-----------------------------------------------------------------

Selaimesi suojausasetukset voivat estää symbolien oikein lataamisen. Voit ratkaista tämän ongelman yrittämällä seuraavaa:

-   Jos ongelma ilmenee Internet Exploreria käytettäessä, klikkaa **Työkalut**, ja sitten **Internet-asetukset**.  Valitse Internet-asetukset-valintaikkunassa **Tietosuoja**-välilehdessä **Mukautettu taso**, ja varmista, että **Fonttien lataaminen** -vaihtoehto on valittuna.
-   Muussa tapauksessa, sinun on lisättävä Dynamics 365 for Operations -sivusto luotettujen sivustojen luetteloon.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Valintanauhaa ei ole Dynamics AX 2012:ssa. Voinko pitää toimintoruudun välilehdet aina auki?
Olemme aikeissa toteuttaa tämän ominaisuuden pian. Käyttäjät voivat sitten halutessaan pitää välilehtien toimintoruudut aina avattuina. Muussa tapauksessa välilehdet painuvat kokoon, kun niitä ei käytetä, jotta sivun näyttötilaa voidaan lisätä.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-rightclick"></a>Miksi näen joskus eri pikavalikon kun klikkaan hiiren kakkospainikkeella?
Jos napsautat hiiren kakkospainikkeella muokattavaa kenttää (tai jos teksti on valittu), selaimen pikavalikko ilmestyy näkyviin. Tämän valikon avulla voiy käyttää **leikkaa**, **kopioi** ja **liitä** komentoja. Microsoft ei voi upottaa komentoja Dynamics 365 for Operations -pikavalikkoihin, koska turvallisuussyistä selaimet eivät salli meille systemaattista pääsyä järjestelmän leikepöydälle.

Jos kaksoisnapsautat kenttäotsikkoa tai ohjausobjektin vain luku -arvoa, näkyviin tulee Dynamics 365 for Operations -pikavalikko.

Helpottaaksemme näppäimistöön pääsyä, suunnittelemme sellaisen pikanäppäimen käyttöönottoa tulevaisuudessa, joka avaa Dynamics 365 for Operations -pikanäppäimistön.

## <a name="where-is-the-view-details-functionality-in-dynamics-365-for-operations"></a>Missä on Dynamics 365 for Operationsin Näytä tiedot -toiminto?
**Näytä tiedot** -vaihtoehtoa voi käyttää useilla tavoilla:

-   Jos ohjausobjektissa on **Näytä tiedot**-valmius ja ohjausobjektilla on arvo, kyseinen arvo näytetään hyperlinkkinä. Napsauttamalla hyperlinkkiä voit avata sivun, jossa on lisätietoja.
-   **Näytä tiedot** on myös vaihtoehtona Dynamics 365 for Operationsin pikavalikoissa. Lisätietoja siitä, milloin Dynamics 365 for Operations -pikavalikko tulee näkyviin kun napsautat hiiren oikealla painikkeella, on edellisessä jaksossa.





