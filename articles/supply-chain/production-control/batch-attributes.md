---
title: Erämääritteet
description: Tässä ohjeaiheessa on tietoja erämääritteistä. Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia. Ohjeaiheessa selvitetään myös, kuinka erämääritteitä määritetään ja kuinka niitä voi hakea eriä varattaessa.
author: ShylaThompson
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 064b3dc7f0209b5c81580d4eb80384df74155aee
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811843"
---
# <a name="batch-attributes"></a>Erämääritteet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja erämääritteistä. Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia. Ohjeaiheessa selvitetään myös, kuinka erämääritteitä määritetään ja kuinka niitä voi hakea eriä varattaessa.

Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia. Erämääritteet voivat vaihdella monen tekijän, esimerkiksi ympäristöolosuhteiden, erän tuottamiseen käytettävien raaka-aineiden laadun tai tuloksena syntyvän lopputuotteen mukaan. Erämääritteiden määrä ja tyypit voivat vaihdella paljon eri toimialojen välillä. Seuraavassa on kaksi esimerkkiä erämääritteiden käyttämisestä:

-   Juustoteollisuudessa maito on yksi juuston raaka-aineista, jolla on eri määritteitä, kuten rasvapitoisuus ja prosenttipaino. Maidosta tuotetulla juustolla voi olla muita määritteitä, kuten kosteus ja ikä.
-   Terästeollisuudessa valmistetulla raudalla voi olla määritteitä, kuten magnesiumpitoisuus, hopeapitoisuus ja sinkkipitoisuus prosentteina.

Määritteiden määrää ja tyyppiä on helpompi hallita erämääriteryhmien avulla. Näin jokaista määritettä ei tarvitse lisätä erikseen.

## <a name="assign-batch-attributes"></a>Erämääritteiden liittäminen
Erämääritteet liitetään yksittäisiin tuotteisiin, joita pidetään varastoerissä, tai tuotteisiin, jotka liittyvät tiettyihin asiakkaisiin. Ennen kuin liität erämääritteen asiakastasolla, se täytyy liittää tuotetasolla. Tuotteen erädimensioksi on määritettävä **Aktiivinen** seurantadimensioryhmässä. Jos haluat määrittää erämääritteen yksittäiselle tuotteelle, käytä kyseisen tuotteen sivua. Jos määrite koskee tietyn asiakkaan tuotetta, käytä kyseisen asiakkaan sivua. Kun lisäät tuotteeseen määritettä, määritä myös muut parametrit. Seuraavassa on muutamia esimerkkejä:

-   Määritetyyppien **Kokonaisluku** ja **Nimellinen** minimi- ja maksimialueet.
-   Toleranssitoiminnot määritteelle, jonka tyyppi on **Kokonaisluku** tai **Nimellinen**. Jos määritteen arvo on minimi- ja maksimialueen ulkopuolella, toimenpide voi olla varoitus- tai virheilmoitus.
-   Määritteen kohdearvo. Arvo on määritteen optimaalinen arvo, joka koskee kaikkia määritetyyppejä.

Voit käyttää **Vapautetut tuotteet** -sivulla valittujen tuotteiden sivuja Tuotetietojen hallinnassa. Kun olet liittänyt erämääritteet tuotteeseen, voit lisätä määritteille arvoja **Varastoerämääritteet**-sivulla.

## <a name="reserve-batches"></a>Erien varaaminen
Voit hakea erämääritteitä tehdessäsi erävarauksia myyntitilaukselle asiakkaan tilauksen täyttämiseksi tai keräillessäsi ja varatessasi eriä tuotantotilaukselle. Haun avulla voit etsiä varastoerää, joka sisältää tuotteen, jolla on haluamasi erämäärite. Kun olet paikantanut erän tai erät, voit varata tuotteen lähdevaraston tapahtumariville.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]