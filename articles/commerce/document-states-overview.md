---
title: Asiakirjan tilat ja elinkaari
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen sivuelementtien eri asiakirjatiloista.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 04836ecf80fc86ab6abb96e4255779c8c03988d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909455"
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