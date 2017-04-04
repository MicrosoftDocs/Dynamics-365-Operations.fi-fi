---
title: "Hankinnan työnkulut"
description: "Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Hankinnan työnkulut

Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.

Työnkulku vastaa liiketoimintaprosessia. Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja. Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:
-   **Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille. Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.
-   **Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja. Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.
-   **Keskitetty työluettelo**– käyttäjät voivat tarkastella työnkulkutehtäviä ja määrittää ne kaikki työnkulut, kun he osallistuvat hyväksynnät keskitetty työluettelo. Tämä on työtä nimikkeet-sivu.

## <a name="the-types-of-workflows-that-you-can-create"></a> Luotavissa olevat työnkulkutyypit
Hankinnoissa voi käyttää seuraavia työnkulkutyyppejä.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tyyppi**                         | **Käytä tätä tyyppiä**                                          |
| Ostoehdotuksen tarkastelu      | Luo ostoehdotuksille tarkistustyönkulkuja.            |
| Ostoehdotusrivin tarkistus | Luo ostoehdotuksen riveille tarkistustyönkulkuja.       |
| Ostotilaustyönkulku          | Luo ostotilauksille tarkistus- ja hyväksymistyönkulkuja.     |
| Ostotilausrivin työnkulku     | Luo ostotilauksen riveille tarkistus- ja hyväksymistyönkulkuja. |

## <a name="creating-a-workflow"></a>Työnkulun luominen
Jos haluat luoda työnkulun, siirry hankinta &gt;asennus &gt;ja työnkulut hankinta ja luo uusi työnkulku valitsemalla luotavan työnkulun tyyppi.  

Voit vetää työnkulkualustassa työnkulun elementit suunnitteluun ja linkittää ne työnkulkuun. Työnkulun elementtien asetukset täytyy määrittää. Hyväksynnän ja tehtävän työnkulun elementeille voit määrittää, kenen osallistujan tulee tehdä niille toimia.
Osallistujien tyypit
----------------------

Voit määrittää hyväksyntävaiheen seuraaville osallistujaryhmille.

| Käyttäjäryhmä    | Kuvaus                                                               |
|---------------|---------------------------------------------------------------------------|
| Osallistuja   | Määritä hyväksyntävaihe ryhmän tai roolin jäsenille.                   |
| Hierarkia     | Määritä hyväksyntävaihe tietyssä organisaatiohierarkiassa oleville käyttäjille. |
| Työnkulun käyttäjä | Määritä hyväksyntävaihe tämän työnkulun käyttäjille.                       |
| Jono         | Määritä hyväksyntävaihe työnimikejonolle.                            |
| Käyttäjä          | Määritä hyväksyntävaihe tietyille käyttäjille.                               |



<a name="see-also"></a>Lisätietoja
--------

[Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions) (raportti)

[Purchase requisition workflow](purchase-requisitions-workflow.md)


