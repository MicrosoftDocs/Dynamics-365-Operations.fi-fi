---
title: "Fyysiset ja kirjanpidolliset päivitykset"
description: "Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1d20faab03a46e39077890a19ce16f6324982a29
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="physical-and-financial-updates"></a>Fyysiset ja kirjanpidolliset päivitykset

[!include[banner](../includes/banner.md)]


Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon. 

Varastotapahtumia voi päivittää sekä fyysisesti että kirjanpidollisesti Microsoft Dynamics 365 for Operationsissa. Tietynlaisen fyysiset ja kirjanpidolliset tapahtumat lisäävät varastomääriä, ja toisenlaiset laskevat varastomääriä.

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
Määrää lisäävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla. Dynamics 365 for Operations laskee juoksevan keskimääräisen kustannushinnan, joka perustuu kirjanpidollisesti seurattavien varastodimensioiden tapahtumien kustannuksiin. Lisätietoja juoksevasta keskimääräisestä kustannushinnasta: [Juokseva keskimääräinen kustannushinta](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Tapahtumat, jotka vähentävät määrää.
Dynamics 365 for Operations käyttää varastoon liittyvästä varastomallista riippumatta laskettua juoksevaa keskimääräistä kustannushintaa, kun määrää vähentävä tapahtuma kirjataan. Määrää vähentävää tapahtumaa ei saa olla merkitty aiemmin toiseen tapahtumaan ennen kirjaamista. Jos fyysinen käytettävissä oleva varasto muuttuu negatiiviseksi, Dynamics 365 for Operations käyttää varaston kustannusta, joka määritetään nimikkeelle **Nimike**-lomakkeessa. **Huomautus:**Jos multisite-toiminnot on otettu käyttöön, tätä kustannusta käytetään toimipaikan varastokustannuksena, joka on määritetty sivustolle **Tilauksen oletusasetukset** -lomakkeessa.

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




