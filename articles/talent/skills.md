---
title: "Työvoiman osaamisalueiden kohdistaminen liiketoimintatarpeisiin"
description: "Voit seurata työntekijöillä, hakijoilla tai yhteyshenkilöillä olevia osaamisalueita tai mitä osaamisalueita heillä pitäisi olla voidakseen suoriutua rooleistaan tehokkaasti. Voit myös määrittää tietyn työn edellyttämät osaamisalueet."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9e66d3c6309c195e076fd86c31aa0adade97394
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="align-workforce-skills-with-business-needs"></a>Työvoiman osaamisalueiden kohdistaminen liiketoimintatarpeisiin

[!INCLUDE [banner](includes/banner.md)]

Voit seurata työntekijöillä, hakijoilla tai yhteyshenkilöillä olevia osaamisalueita tai mitä osaamisalueita heillä pitäisi olla voidakseen suoriutua rooleistaan tehokkaasti. Voit myös määrittää tietyn työn edellyttämät osaamisalueet.

Seurattavia osaamisalueita ovat esimerkiksi seuraavat:
-   Esimiestaito – kyky valvoa muiden työskentelyä.
-   Johtajuus – kyky johtaa työntekijöitä ja liiketoimintayksiköitä.
-   Suunnittelu – kaukonäköisyys - kyky nähdä eteenpäin, luoda visioita ja saattaa ne loppuun.
-   HTML-kyky kirjoittaa HTML-koodia.

Ennen kuin voit määrittää osaamisalueen henkilölle tai työlle, luoda osaamisaluekartoitushaun tai luoda osaamisprofiilin, osaamisalueiden tiedot on lisättävä **Osaamisalueet**-sivulle. Voit valita jokaiselle osaamisalueelle osaamisaluetyypin ja arviointimallin.

## <a name="rating-models"></a>Arviointimallit
Arviointimallien avulla voit arvioida henkilön osaamisalueen todellisen tason, tason joka hänen tulee saavuttaa tai tason, joka tarvitaan työssä. Voit kirjoittaa arviointimallille enintään 10 tasoa.  Kullekin arviointimallin tasolle määritetään kerroin.  Kertoimen arvoa käytetään eri luokitusmalleja käyttävien osaamisalueiden normalisointiin.  Kertoimen on oltava numero väliltä 0-9, ja kullakin tasolla on oltava yksilöllinen kerroin.  Tasoja, joilla on korkeammat kertoimen arvot, painotetaan enemmän arviointimallissa.

## <a name="specify-job-skills"></a>Määritä työn osaamisalueet
Kun syötät tietoja työstä, voit määrittää osaamisalueita joita henkilöllä tulisi olla, ennen kuin hän voi toimia kyseisessä työssä.  Voi lisäksi määrittää kullekin osaamisalueelle toivotun tason sekä osaamisalueen tärkeystason. Eri töissä voidaan edellyttää saman osaamisalueen eri tärkeystasoja.

## <a name="enter-skills-for-workers-applicants-or-contacts"></a>Kirjoita työntekijöiden, hakijoiden tai yhteyshenkilöiden osaamisalueet.
Määritä tavoite- tai todelliset osaamisalueet työntekijöille, hakijoille tai yhteyshenkilöille. Tavoitetaito on taito, jonka henkilö aikoo saavuttavansa. Todellisella osaamisalueella tarkoitetaan osaamista, jonka henkilöllä tällä hetkellä on.

## <a name="skill-mapping-and-skill-mapping-profiles"></a> Osaamisaluekartoitukset ja kartoitusprofiilit
Voit luoda osaamisaluekartoitushaun ja etsiä työntekijän, hakijan tai yhteyshenkilön, jolla on tietyntyyppiseen tehtävään tarvittava pätevyys. Osaamisaluekartoitushaku etsii osaamisalueita, koulutusta, todistuksia, luottamustehtäviä ja projektikokemusta ja palauttaa annettuja ehtoja vastaavat tulokset.  Voi esimerkiksi olla hyödyllistä tietää organisaation työntekijöiden koulutustaso.

Osaamisaluekartoitusprofiilien avulla voit etsiä nykyisiä työntekijöitä tai hakijoita, joiden pätevyys vastaa suoraan liiketoiminnan tarpeita.  Voit esimerkiksi luoda osaamisaluekartoitusprofiileja organisaatiossa avoimena olevia toimia varten. Luomalla profiilin tietylle työlle ja kopioimalla työn osaamisalueet, koulutuksen ja todistukset profiiliin voit nopeasti hakea työntekijöitä, hakijoita ja yhteyshenkilöitä, jotka vastaavat yhtä tai useampaa profiilissa määritettyä ehtoa, ja tarkastella sellaisten hakijoiden luetteloa, joiden osaamisalueet lähimmin vastaavat työn vaatimuksia.

> **Huomautus** Vain osaamisaluekartoitushakuihin valitut työntekijät, hakijat ja yhteyshenkilöt voidaan näyttää osaamisaluekartoituksen tulosluettelossa tai sisällyttää osaamisalueprofiilin. Jos haluat sisällyttää työntekijän, hakijan tai yhteyshenkilön osaamisaluekartoitushakuihin, määritä **Sisällytä osaamisaluekartoitukseen** -asetukseksi Kyllä seuraavilla sivuilla:
> 
> + Työntekijä
> + Työntekijä
> + Hakija
> + Yhteyshenkilöt

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a>Osaamiseroanalyysi ja osaamisprofiilianalyysi
Luomalla osaamisprofiilianalyysin voit tarkastella luetteloa työntekijän, hakijan tai yhteyshenkilön osaamisalueista tiettynä päivänä. Voit luoda osaamisalueaukkoanalyysi, jotta voit verrata henkilön taitoja työhön vaadittaviin taitoihin  



<a name="see-also"></a>Lisätietoja
--------

[Henkilöstöhallinto](index.md)




