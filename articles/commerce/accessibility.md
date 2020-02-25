---
title: Helppokäyttöisyyden toiminnot ja ominaisuudet
description: Tässä ohjeaiheessa tietoja helppokäyttöominaisuuksista ja -toiminnoista Microsoft Dynamics 365 Commercein eri versioissa.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3edc6250dd5438be31d80a9d6b0f3b730438ca53
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001757"
---
# <a name="accessibility-features-and-capabilities"></a>Helppokäyttöisyyden toiminnot ja ominaisuudet


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa tietoja helppokäyttöominaisuuksista ja -toiminnoista Microsoft Dynamics 365 Commercein eri versioissa.

## <a name="overview"></a>Yleiskatsaus

Helppokäyttöominaisuudet ja -toiminnot mahdollistavat kaikkien käyttäjien toimintojen käytön ja suorittamisen, jotta he voivat saavuttaa tavoitteensa. Tämä laaja käyttäjäryhmä voi tarvita apuvälineitä kuulo-, näkö-, liikkuvuus- tai neurodiversiteetin vuoksi.

Voit rakentaa sivustosi Dynamics 365 Commercessa erilaisten ominaisuuksien avulla niin, että se sisältää aputoimintoja. Kun suunnittelet sivustoa, harkitse helppokäyttötoimintojen alueita, jotka mainitaan [Microsoft Accessibility Centerissä](https://www.microsoft.com/accessibility). 

Tässä ohjeaiheessa käsitellään helppokäyttötoimintojen lisätoimintoja, jotka kannattaa ottaa huomioon, kun käytät Dynamics 365 Commercea.

## <a name="image-alt-text"></a>Kuvan vaihtoehtoinen teksti

Dynamics 365 Commercessa on sisäänrakennettu digitaalisten resurssien hallintajärjestelmä, jonka avulla voit seurata sivustollasi käytettäviä kuva- ja videoresursseja. Kuvatekstit, kuvaukset ja vaihtoehtoinen teksti voidaan lisätä kuvan ominaisuudet -ruutuun, kun kuva on valittu tai ladattu.

## <a name="video-accessibility"></a>Videon helppokäyttötoiminnot

Dynamics 365 Commercen digitaalisten resurssien hallintajärjestelmä tukee useita videosisällön helppokäyttötoimintoja. Seuraavassa taulukossa on kuvattu eräitä esimerkkejä.

| Video-ominaisuus               | Kuvaus |
|-----------------------------|-------------|
| Tekstitys (CC)      | Teksti, joka voidaan näyttää videon ääni- ja äänikuvaelementeille kuulovammaisten käyttäjien auttamiseksi |
| Tekstitys                   | Tekstitystiedostot, jotka näyttävät kontekstivihjeitä tai dialogin näytöllä |
| Äänitallenteet           | Puhuttujen sanojen tekstitiedote, joka luodaan videosisällön äänestä |
| Kuvaava ääni           | Muu kuin ensisijainen äänikanava, joka kuvaa näytöllä esiintyvää sisältöä tai kontekstia |
| Vähimmäisikä            | Määrite, joka voi säilyttää vähimmäisiän, jonka katselijan on oltava katsoakseen videon (vain metatiedot) |

### <a name="configure-video-accessibility-elements"></a>Videon helppokäyttötoimintojen määrittäminen

Dynamics 365 Commerce -sivuston **Resurssit**-osiossa voit ladata videoresursseja, joissa on erilliset tiedostot, kuten tekstitys, tavallinen ääni ja kuvaava ääni. Tekstitys voidaan luoda myös automaattisesti, kun videoresurssi ladataan.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Luo tai lataa suljettuja tekstitystiedostoja videoresurssien lataamisen aikana

Seuraa tätä vaihetta, jos haluat, että tekstitystiedosto luodaan automaattisesti, kun lataat videon.

- Valitse **Resurssien lataaminen** -valintaikkunassa **Luo automaattisesti suljetut tekstitykset**. Jos olet muodostamassa suljettua tekstitystiedostoa, suljettujen tekstitystiedostojen tiedostovalitsin ei ole käytettävissä valintaikkunassa.

Seuraa tätä vaihetta, jos haluat ladata tekstitystiedoston manuaalisesti, kun lataat videon.

- Tyhjennä **Resurssien lataaminen** -valintaikkunassa **Luo automaattisesti suljetut tekstitykset**.

Jos haluat ladata videolle tavallisia ääni- tai kuvaavia äänitiedostoja, käytä **Resurssien lataaminen** -valintaikkunassa olevaa tiedoston valitsinta.

> [!NOTE]
> Tekstitys, tavallinen ääni ja kuvaileva äänisisältö voidaan lisätä myös videoresurssin lataamisen jälkeen. Siirry **Resurssit**-kohtaan, valitse videosisältö ja tarkista se ja lataa sitten videoresurssin ominaisuudet -ruudussa lisäresurssit.

#### <a name="edit-cc-and-audio-transcript-files"></a>Muokkaa tekstitys- ja äänitallennetiedostoja

Tekstitys- ja äänitallennetiedostoja voi muokata suoraan sisällönluontityökalussa. Videon toisto on käytettävissä muokkauksen aikana.

Voit muokata tekstitys- ja äänitallennetiedostoja seuraavasti.

1. Siirry **Resurssit**-kohtaan, valitse videoresurssi ja valitse sitten **Muokkaa tekstitystä/tallennetta**. Näyttöön tulee tekstityksen ja tallenteen sisältöeditori.
1. Valitse **Kirjaa ulos**.
1. Muokkaa tekstitystä tai tallennetekstiä.
1. Kun olet valmis, valitse **Tallenna** ja valitse sitten **Kuittaa sisään**.
1. Kun olet valmis julkaisemaan, valitse **Julkaise**.

#### <a name="set-the-minimum-age-attribute"></a>Vähimmäisikämääritteen määrittäminen

**Vähimmäisiän** metatietoattribuutti voidaan liittää videoresursseihin.

Voit määrittää videoresurssin **Vähimmäisikä**-määritteen noudattamalla seuraavia ohjeita.

1. Siirry **Resurssit**-kohtaan ja valitse videosisältö.
1. Valitse **Kirjaa ulos**.
1. Määritä **Vähimmäisikämäärite** videoresurssin ominaisuudet-ruudussa.

> [!NOTE]
> Ominaisuudet-ruutua käytetään vain metatietomääritteen arvon asettamiseen ja tallentamiseen. Mukautetut moduulit on luotava, jotta tätä määritettä voidaan käyttää toisto-ominaisuutta varten.

## <a name="additional-resources"></a>Lisäresurssit

[Lomakkeiden, tuotteiden ja ohjausobjektien helppokäyttöomaisuudet](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoftin helppokäyttökeskus](https://www.microsoft.com/accessibility)

[Dynamics 365:n helppokäyttökeskus](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Yhteensopivuuden yleiskatsaus](compliance-overview.md)

[Evästeen yhteensopivuus](cookie-compliance.md)

[Lisää tietosuojakäytäntösivu](add-privacy-page.md)
