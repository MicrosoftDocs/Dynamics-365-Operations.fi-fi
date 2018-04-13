---
title: "Fyysiset ja kirjanpidolliset päivitykset"
description: "Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e62bdbfb7b88f66ea1f6e4d57b6150c8b0bffb04
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="physical-and-financial-updates"></a>Fyysiset ja kirjanpidolliset päivitykset

[!INCLUDE [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon. 

Varastotapahtumia voi päivittää sekä fyysisesti että kirjanpidollisesti Microsoft Dynamics 365 for Finance and Operationsissa. Tietynlaisen fyysiset ja kirjanpidolliset tapahtumat lisäävät varastomääriä, ja toisenlaiset laskevat varastomääriä.

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
Määrää lisäävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla. Finance and Operations laskee juoksevan keskimääräisen kustannushinnan, joka perustuu kirjanpidollisesti seurattavien varastodimensioiden tapahtumien kustannuksiin. Lisätietoja juoksevasta keskimääräisestä kustannushinnasta: [Juokseva keskimääräinen kustannushinta](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Tapahtumat, jotka vähentävät määrää.
Finance and Operations käyttää laskettua juoksevaa kustannushintaa, kun määrää vähentävä tapahtuma kirjataan, riippumatta siitä mikä varastomalli on liitetty kyseiseen varastoon. Määrää vähentävää tapahtumaa ei saa olla merkitty aiemmin toiseen tapahtumaan ennen kirjaamista. Jos fyysinen käytettävissä oleva varasto muuttuu negatiiviseksi, Dynamics 365 for Finance and Operations käyttää nimikkeelle **Nimike**-lomakkeessa määritettyä varastokustannusta. **Huomautus:** Jos multisite-toiminnot on otettu käyttöön, tätä kustannusta käytetään toimipaikan varastokustannuksena, joka on määritetty sivustolle **Tilauksen oletusasetukset** -lomakkeessa.

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




