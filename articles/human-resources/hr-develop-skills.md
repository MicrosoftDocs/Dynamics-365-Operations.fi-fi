---
title: Osaamisalueiden määritykset
description: Voit seurata työntekijän osaamisalueita Dynamics 365 Human Resourcesissa. Voit myös määrittää tietyn työn edellyttämät osaamisalueet.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 13206bb3c961f001620e8b65a8b1bb39bf95ee49
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075068"
---
# <a name="configure-skills"></a>Osaamisalueiden määritykset

> [!IMPORTANT]
> Tässä ohjeaiheessa mainittu toiminto on tällä hetkellä Finance-infrastruktuurin Human Resources -asiakkaiden käytettävissä.  


Voit seurata työntekijän osaamisalueita Dynamics 365 Human Resourcesissa. Voit myös määrittää tietyn työn edellyttämät osaamisalueet.

Seurattavia osaamisalueita ovat esimerkiksi:

- Esimiestaito – kyky valvoa muiden työskentelyä.
- Johtajuus – kyky johtaa työntekijöitä ja liiketoimintayksiköitä.
- Suunnittelu – kaukonäköisyys - kyky nähdä eteenpäin, luoda visiolausekkeita ja saattaa ne loppuun.
- HTML-kyky kirjoittaa HTML-koodia.

Jos et ole vielä määrittänyt osaamisaluetyyppejä ja arviointimalleja, sinun on lisättävä joitakin tietoja ennen osaamisalueiden luomista.

Seuraavat henkilöt voivat määrittää työntekijälle osaamisalueita:

- Työntekijät voivat määrittää itseään varten osaamisalueita työntekijän itsepalvelussa. Nämä osaamisalueet edellyttävät esimiehen hyväksyntää.
- Esimiehet voivat määrittää työntekijöille osaamisalueita. Voit luoda työnkulun, joka hyväksyy nämä osaamisalueet automaattisesti.

## <a name="create-a-skill-type"></a>Luo osaamisaluetyyppi

Osaamisaluetyypit ovat luokkia, joihin yksittäiset osaamisalueet, kuten Hallinto tai Myynti, kuuluvat.

1. Valitse **Työntekijän kehitys** -työtilassa **Linkit**.

2. Valitse **Tasoasetukset**-kohdasta **Osaamisaluetyypit**.

3. Valitse **Uusi**.

4. Täytä seuraavat kentät:

   - **Osaamisaluetyyppi**: anna osaamisaluetyypin nimi.
   - **Kuvaus**: anna osaamisaluetyypin kuvaus.

5. Valitse **Tallenna**.

## <a name="create-a-rating-model"></a>Luo arvostelujärjestelmä

Arviointimallien avulla voit arvioida henkilön osaamisalueen todellisen tason, tason joka hänen tulee saavuttaa tai tason, joka tarvitaan työssä. Kullekin arviointimallin tasolle määritetään kerroin.

1. Valitse **Työntekijän kehitys** -työtilassa **Linkit**.

2. Valitse **Osaamisasetukset**-kohdasta **Arviointimallit**.

3. Valitse **Uusi**.

4. Täytä seuraavat kentät:

   - **Luokitus**: Kirjoita arviointimallille nimi, esimerkiksi **Osaamisalueet**.
   - **Kuvaus**: Kirjoita arviointimallille kuvaus, esimerkiksi **Osaamisalueluokitukset**.

5. Valitse **Tasot**-osassa **Uusi**. Täytä kunkin lisättävän tason kentät:

   - **Taso**: Kirjoita tason nimi.
   - **Kuvaus**: Kirjoita tason kuvaus.
   - **Kerroin**: Syötä kerroinarvo väliltä 0-9. Kertoimet auttavat normalisoimaan eri luokitusmalleja käyttäviä taitoja. Jokaisella tasolla on oltava yksilöivä kerroin. Tasoja, joilla on korkeammat kertoimen arvot, painotetaan enemmän arviointimallissa.

   Jatka tasojen lisäämistä tarvittaessa. Voit syöttää kullekin arviointimallille enintään 10 tasoa.

6. Valitse **Tallenna**.

## <a name="create-a-skill"></a>Luo osaamisalue

Ennen kuin voit määrittää osaamisalueen, luoda osaamisaluekartoitushaun tai osaamisprofiilin, osaamisalueiden tiedot on lisättävä **Osaamisalueet**-sivulle. Voit valita jokaiselle osaamisalueelle osaamisaluetyypin ja arviointimallin.

1. Valitse **Työntekijän kehitys** -työtilassa **Linkit**.

2. Valitse **Tasoasetukset**-kohdasta **Osaamisalueet**.

3. Valitse **Uusi**.

4. Täytä seuraavat kentät:

   - **Osaamisalue**: anna osaamisalueen nimi.
   - **Kuvaus**: anna osaamisalueen kuvaus.
   - **Arvostelu**: Valitse arvostelumalli, jota haluat käyttää tässä osaamisalueessa.
   - **Osaamisaluetyyppi**: Valitse osaamisaluetyyppien luettelosta.

5. Valitse **Tallenna**.

## <a name="see-also"></a>Lisätietoja

[Syötä osaamisalueet](hr-develop-enter-skills.md)<br>
[Osaamisalueiden kartoitus](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
