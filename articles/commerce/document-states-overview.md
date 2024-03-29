---
title: Asiakirjan tilat ja elinkaari
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269913"
---
# <a name="document-states-and-lifecycle"></a>Asiakirjan tilat ja elinkaari

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.

## <a name="document-state-descriptions"></a>Asiakirjan tilan kuvaukset

[Sivuelementit](page-elements-overview.md)-artikkelissa on sisällönhallintajärjestelmän (CMS) eri asiakirjatyyppejä. Näillä asiakirjatyypeillä voi olla useita tiloja muokkaustyökalussa. Asiakirjan tilat auttavat estämään tietoristiriitoja ja ottavat käyttöön versionhallinnan. Ne määrittävät, ketkä voivat muuttaa asiakirjoja, milloin asiakirjoja voi muuttaa ja milloin muut voivat tarkastella muutoksia.

Seuraavassa taulukossa esitetään sivuelementtien mahdolliset asiakirjojen tilat Commercessa.

| Asiakirjan tila      | Sivustonmuodostimen toiminta        | kuvaus                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Kuitattu ulos         | Valitse **Muokkaa**.           | Asiakirja kuitataan ulos. Kun asiakirja on tässä tilassa, muut todennetut järjestelmän käyttäjät eivät voi muuttaa sitä, ja kaikki tiedostoon tekemäsi muutokset näkyvät vain sinulle. |
| Tallennettu               | Valitse **Tallenna**.           | Uloskuitattuun tiedostoon tehdyt muutokset tallennetaan tietokantaan, mutta asiakirjaa ei ole vielä kuitattu sisään tai julkaistu. Tallennetut muutokset eivät näy muille todennetuille järjestelmäkäyttäjille ennen kuin laatija valitsee **Lopeta muokkaaminen**. Ulkoiset käyttäjät eivät näe niitä, ennen kuin nimike on julkaistu. |
| Hylätty uloskuittaus | Valitse **Hylkää muokkaukset**.  | Kaikki uloskuitattuun tiedostoon tehdyt muutokset hylätään, ja nimike palautuu viimeksi kuitattuun versioon. |
| Kuitattu sisään          | Valitse **Viimeistele muokkaus**. | Muokattu asiakirja kuitataan sisään. Kaikki muutokset näkyvät muille todennetuille järjestelmän käyttäjille, ja käyttäjät voivat muokata tiedostoa. Jokainen sisäänkuittaus luo asiakirjaversiotietueen nimikkeen historiaan. |
| Julkaistu           | Valitse **Julkaise**.        | Tiedosto julkaistaan, ja muutokset siirretään Live-sivustoon ja ulkoiset käyttäjät voivat löytää ne. Nimikkeet voidaan julkaista vain, jos ne on ensin kuitattu sisään valitsemalla **Lopeta muokkaaminen**. |

## <a name="additional-resources"></a>Lisäresurssit

[Tapoja lisästä sisältöä](add-manage-content.md)

[Sivumallisanasto](page-elements-overview.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)

[Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen](cross-channel-sharing.md)

[Moduulien käyttäminen](work-with-modules.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Sivuston selauksen mukauttaminen](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
