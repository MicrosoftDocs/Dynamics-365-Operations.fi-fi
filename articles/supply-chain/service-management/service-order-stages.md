---
title: Huoltotilauksen vaiheet
description: Huoltotilauksen vaiheet määrittämällä ja liittämällä ne työntekijöihin voit ohjata huoltotilauksen kulkua tehtävissä, joita eri henkilöt suorittavat huolto-organisaatiossa.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e748afbd159d7a8fca1372676872cc02dd7ea57
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671727"
---
# <a name="service-order-stages"></a>Huoltotilauksen vaiheet   

[!include [banner](../includes/banner.md)]


Voit määrittää huoltotilauksen tehtävät, jotka on suoritettava, niiden suoritusjärjestyksen ja työntekijät, jotka vastaavat niiden suorittamisesta. Huoltotilauksen vaiheet määrittämällä ja liittämällä ne työntekijöihin voit ohjata huoltotilauksen kulkua tehtävissä, joita eri henkilöt suorittavat huolto-organisaatiossa. Vaiheiden järjestyksen tulee sisältää alkuperäinen vaihe.

Voit myös määrittää toimenpiteet, jotka ovat sallittuja kussakin vaiheessa. Jos esimerkiksi poistat **Kirjaa**-valintaruudun valinnan muissa paitsi viimeisessä vaiheessa, huoltotilauksia ei voi kirjata, ennen kuin huoltotilaukset on käsitelty kaikkien vaiheiden läpi.

## <a name="branching-in-service-order-stages"></a>Haaroitus palvelutilauksen vaiheissa

Huollon vaiheen määrittäessäsi voit luoda useita vaihtoehtoja tai haaroja, joilla valitaan huoltotilauksen seuraava vaihe. Kaikki luomasi sivuliikkeet ovat valittavissa, kun ensimmäinen vaihe on suoritettu. Voit esimerkiksi asettaa **Suunnittelun** aloitusvaiheeksi. Luot kaksi vaihetta nimeltä **Käsittelyssä** ja **Peruuta** ja valitset sitten niiden ylätasoksi **Suunnittelu**. Voit määrittää **suunnittelu**-vaiheen myyntitilaukseen. Kun myyntitilauksen suunnitteluvaihe on valmis, voit valita **prosessivaiheessa**, onko myyntitilaus valmis käsiteltäväksi, tai voit valita **peruuta** vaihe, jos myyntitilaus peruutetaan.

## <a name="see-also"></a>Lisätietoja

[Määritä huoltotilausvaiheet](set-up-service-order-stages.md)

[Huoltotilauksen vaiheen muuttaminen](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]