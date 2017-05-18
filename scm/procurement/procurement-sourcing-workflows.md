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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 17573977224045f4afe1124a29ea8f07b3333b3e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Hankinnan työnkulut

[!include[banner](../includes/banner.md)]


Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.

Työnkulku vastaa liiketoimintaprosessia. Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja. Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:
-   **Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille. Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.
-   **Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja. Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.
-   **Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitetyssä työluettelossa olevia työnkulkutehtäviä ja niille annettuja hyväksyntöjä kaikissa työnkuluissa, joissa he ovat osallisina. Tämän voi tehdä Työnimikkeet-sivulla.

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
Jos haluat luoda työnkulun, valitse Hankinta &gt; Asetukset &gt; Hankinnan työnkulut ja luo uusi työnkulku valitsemalla haluamasi työnkulkutyyppi.  

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

[Ostoehdotuksen työnkulku](purchase-requisitions-workflow.md)




