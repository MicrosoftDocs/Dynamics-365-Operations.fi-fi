---
title: Fyysiset ja kirjanpidolliset päivitykset
description: Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee65fa43b43bc8b6cbf9763ac4fa8774f30afb98
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263563"
---
# <a name="physical-and-financial-updates"></a>Fyysiset ja kirjanpidolliset päivitykset

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon. 

Varastotapahtumia voi päivittää sekä fyysisesti että kirjanpidollisesti Dynamics 365 Supply Chain Managementissa. Tietynlaisen fyysiset ja kirjanpidolliset tapahtumat lisäävät varastomääriä, ja toisenlaiset laskevat varastomääriä.

## <a name="physical-increases"></a>Fyysisiä lisäyksiä
Kun fyysinen tapahtuma kirjataan, tapahtumatietueen tila on **Vastaanotettu**. Seuraavat tapahtumat ovat fyysisiä lisäyksiä:

-   ostotilauksen vastaanotto
-   myyntitilauksen pakkausluettelon palautus
-   Tuotantotilauksen ilmoittaminen valmiiksi
-   tuotantotilauksen keräysluettelon sivutuote.

## <a name="financial-increases"></a>Taloudelliset lisäykset
Kun maksuvastaanottotapahtuma kirjataan, määrää lisäävän tapahtumatietueen tila on **Ostettu**. Seuraavat tapahtumat ovat kirjanpidollisia lisäyksiä:

-   Toimittajan lasku
-   palautuksen myyntitilauslasku
-   tuotantotilauksen kustannuslaskenta
-   Positiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto

## <a name="transactions-that-increase-quantity"></a>Tapahtumat, jotka lisäävät määrää.
Määrää lisäävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla. Laskettu juokseva keskimääräinen kustannushinta perustuu kirjanpidollisesti seurattavien varastodimensioiden tapahtumien kustannuksiin. Lisätietoja juoksevasta keskimääräisestä kustannushinnasta: [Juokseva keskimääräinen kustannushinta](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Tapahtumat, jotka vähentävät määrää.
Varastoon liittyvästä varastomallista riippumatta käytetään laskettua juoksevaa keskimääräistä kustannushintaa, kun määrää vähentävä tapahtuma kirjataan. Määrää vähentävää tapahtumaa ei saa olla merkitty aiemmin toiseen tapahtumaan ennen kirjaamista. Jos fyysinen käytettävissä oleva varasto muuttuu negatiiviseksi, käytetään varaston kustannusta, joka määritetään nimikkeelle **Nimike**-lomakkeessa. 

> [!NOTE]
> Jos multisite-toiminnot on otettu käyttöön, tätä kustannusta käytetään toimipaikan varastokustannuksena, joka on määritetty sivustolle **Tilauksen oletusasetukset** -lomakkeessa.

## <a name="physical-issues-vs-financial-issues"></a>Kirjanpidolliset varasto-otot verrattuina fyysiseen ottoon
Kun fyysinen varasto-ottotapahtuma kirjataan, tapahtumatietueentila on **Toimitettu**. Seuraavat tapahtumat ovat fyysisiä varasto-ottoja:

-   tuotantotilauksen keräysluettelon kirjauskansio
-   myyntitilauksen pakkausluettelo
-   ostotilauksen pakkausluettelon palautus.

Kun kirjanpitotapahtuma kirjataan, tapahtumatietueen tila on **Myyty**. Seuraavat tapahtumat ovat kirjanpidollisia varasto-ottoja:

-   Tuotantotilauksen lopetus
-   Myyntitilauslasku
-   Toimittajalaskun palautus
-   Negatiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto

Määrää vähentävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla. Tämän vuoksi varaston sulkemistoiminto vaaditaan varasto-ottotapahtumien täsmäyttämiseksi vastaanottotapahtumiksi jokaiseen nimikkeeseen määritetyn varastomallin perusteella.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]