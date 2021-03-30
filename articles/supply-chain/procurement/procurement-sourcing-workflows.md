---
title: Hankinnan työnkulut
description: Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e591007a1330fe11b3f586185f9daca845798908
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218462"
---
# <a name="procurement-and-sourcing-workflows"></a>Hankinnan työnkulut

[!include [banner](../includes/banner.md)]

Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.

Työnkulku vastaa liiketoimintaprosessia. Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja. Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:

- **Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille. Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.
- **Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja. Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.
- **Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitetyssä työluettelossa olevia työnkulkutehtäviä ja niille annettuja hyväksyntöjä kaikissa työnkuluissa, joissa he ovat osallisina. Tämän voi tehdä Työnimikkeet-sivulla.

## <a name="the-types-of-workflows-that-you-can-create"></a> Luotavissa olevat työnkulkutyypit

Hankinnoissa voi käyttää seuraavia työnkulkutyyppejä.

| Laji | Käytä tätä tyyppiä |
|---|---|
| Ostoehdotuksen tarkastelu | Luo ostoehdotusten tarkistus- ja hyväksyntätyönkulkuja. |
| Ostoehdotusrivin tarkistus | Luo ostoehdotusrivien tarkistus- ja hyväksyntätyönkulkuja. |
| Ostotilaustyönkulku | Luo ostotilauksille tarkistus- ja hyväksymistyönkulkuja. |
| Ostotilausrivin työnkulku | Luo ostotilauksen riveille tarkistus- ja hyväksymistyönkulkuja. |
| Toimittajan sovelluksen lisäystyönkulku | Luo toimittajapyyntöjen kautta lisättävien uusien toimittajien tarkistus- ja hyväksyntätyönkulkuja. |

> [!IMPORTANT]
> Uutta työnkulkua lisättäessä näkyvissä saattaa olla seuraavat **Luo työnkulku** -valintaikkunassa mainitut vanhentuneet työnkulut. Ne liittyvät *vastaanoton vahvistuksen* toimintoon, joka oli käytössä [Dynamics AX 2012:ssa](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows) mutta joka on nyt vanhentunut. Näitä työnkulkuja ei tueta tällä hetkellä.
> 
> - Toimituksen eräpäiväilmoitustyönkulku
> - Laskun vastaanottoilmoitustyönkulku
> - Tuotteen vastaanoton epäonnistumisilmoituksen työnkulku
> - Vahvistamattoman tuotevastaanoton hylkäysilmoitustyönkulku

## <a name="creating-a-workflow"></a>Työnkulun luominen

Jos haluat luoda työnkulun, valitse Hankinta &gt; Asetukset &gt; Hankinnan työnkulut ja luo uusi työnkulku valitsemalla haluamasi työnkulkutyyppi. 

Voit vetää työnkulkualustassa työnkulun elementit suunnitteluun ja linkittää ne työnkulkuun. Työnkulun elementtien asetukset täytyy määrittää. Hyväksynnän ja tehtävän työnkulun elementeille voit määrittää, kenen osallistujan tulee tehdä niille toimia.

## <a name="types-of-participants"></a>Osallistujien tyypit

Voit määrittää hyväksyntävaiheen seuraaville osallistujaryhmille.

| Käyttäjäryhmä | Kuvaus |
|---|---|
| Osallistuja | Määritä hyväksyntävaihe ryhmän tai roolin jäsenille. |
| Hierarkia | Määritä hyväksyntävaihe tietyssä organisaatiohierarkiassa oleville käyttäjille. |
| Työnkulun käyttäjä | Määritä hyväksyntävaihe tämän työnkulun käyttäjille. |
| Jono | Määritä hyväksyntävaihe työnimikejonolle. |
| Käyttäjä | Määritä hyväksyntävaihe tietyille käyttäjille. |

## <a name="additional-resources"></a>Lisäresurssit

- [Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen (raportti)](https://www.microsoft.com/download/details.aspx?id=101821)
- [Ostoehdotuksen työnkulku](purchase-requisitions-workflow.md)
- [Toimittajien aktivointi](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]