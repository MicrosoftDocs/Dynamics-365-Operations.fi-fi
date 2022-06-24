---
title: Helppokäyttöisyyden toiminnot ja ominaisuudet
description: Tässä artikkelissa tietoja helppokäyttöominaisuuksista ja -toiminnoista Microsoft Dynamics 365 Commercen eri versioissa.
author: BrianShook
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8f4e73ebaf6dc3fc6eb97f69df8545c9ab9fa9df
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853899"
---
# <a name="accessibility-features-and-capabilities"></a>Helppokäyttöisyyden toiminnot ja ominaisuudet

[!include [banner](includes/banner.md)]

Tässä artikkelissa tietoja helppokäyttöominaisuuksista ja -toiminnoista Microsoft Dynamics 365 Commercen eri versioissa.

Helppokäyttöominaisuudet ja -toiminnot mahdollistavat kaikkien käyttäjien toimintojen käytön ja suorittamisen, jotta he voivat saavuttaa tavoitteensa. Tämä laaja käyttäjäryhmä voi tarvita apuvälineitä kuulo-, näkö-, liikkuvuus- tai neurodiversiteetin vuoksi.

Voit rakentaa sivustosi Dynamics 365 Commercessa erilaisten ominaisuuksien avulla niin, että se sisältää aputoimintoja. Kun suunnittelet sivustoa, harkitse helppokäyttötoimintojen alueita, jotka mainitaan [Microsoft Accessibility Centerissä](https://www.microsoft.com/accessibility). 

Tässä artikkelissa käsitellään helppokäyttötoimintojen lisätoimintoja, jotka kannattaa ottaa huomioon, kun käytät Dynamics 365 Commercea.

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

Commerce-sivuston **Mediakirjasto**-osiossa voit ladata videoresursseja, joissa on erilliset tiedostot, kuten tekstitys, tavallinen ääni ja kuvaava ääni. Tekstitys voidaan luoda myös automaattisesti, kun videoresurssi ladataan.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Luo tai lataa suljettuja tekstitystiedostoja videoresurssien lataamisen aikana

Seuraa tätä vaihetta, jos haluat, että tekstitystiedosto luodaan automaattisesti, kun lataat videon.

- Valitse **Resurssien lataaminen** -valintaikkunassa **Luo automaattisesti suljetut tekstitykset**. Jos olet muodostamassa suljettua tekstitystiedostoa, suljettujen tekstitystiedostojen tiedostovalitsin ei ole käytettävissä valintaikkunassa.

Seuraa tätä vaihetta, jos haluat ladata tekstitystiedoston manuaalisesti, kun lataat videon.

- Tyhjennä **Resurssien lataaminen** -valintaikkunassa **Luo automaattisesti suljetut tekstitykset**.

Jos haluat ladata videolle tavallisia ääni- tai kuvaavia äänitiedostoja, käytä **Resurssien lataaminen** -valintaikkunassa olevaa tiedoston valitsinta.

> [!NOTE]
> Tekstitys, tavallinen ääni ja kuvaileva äänisisältö voidaan lisätä myös videoresurssin lataamisen jälkeen. Siirry **Mediakirjasto**-kohtaan, valitse **Muokkaa** tarkistaaksesi sen. Lataa sitten videoresurssin ominaisuudet -ruudussa lisäresurssit.

#### <a name="edit-cc-and-audio-transcript-files"></a>Muokkaa tekstitys- ja äänitallennetiedostoja

Tekstitys- ja äänitallennetiedostoja voi muokata suoraan sisällönluontityökalussa. Videon toisto on käytettävissä muokkauksen aikana.

Voit muokata tekstitys- ja äänitallennetiedostoja seuraavasti.

1. Siirry kohtaan **Mediakirjasto** ja valitse videoresurssin tiedostonimi. Näyttöön tulee tekstityksen ja tallenteen sisältöeditori.
1. Valitse **Muokkaa**.
1. Muokkaa tekstitystä tai tallennetekstiä.
1. Kun olet valmis, valitse **Tallenna** ja valitse sitten **Lopeta muokkaus**.
1. Kun olet valmis julkaisemaan, valitse **Julkaise**.

#### <a name="set-the-minimum-age-attribute"></a>Vähimmäisikämääritteen määrittäminen

**Vähimmäisiän** metatietoattribuutti voidaan liittää videoresursseihin.

Voit määrittää videoresurssin **Vähimmäisikä**-määritteen noudattamalla seuraavia ohjeita.

1. Siirry **Mediakirjasto**-kohtaan ja valitse videosisältö.
1. Valitse **Muokkaa**.
1. Määritä **Vähimmäisikämäärite** videoresurssin ominaisuudet-ruudussa.

> [!NOTE]
> Ominaisuudet-ruutua käytetään vain metatietomääritteen arvon asettamiseen ja tallentamiseen. Mukautetut moduulit on luotava, jotta tätä määritettä voidaan käyttää toisto-ominaisuutta varten.

## <a name="additional-resources"></a>Lisäresurssit

[Lomakkeiden, tuotteiden ja ohjausobjektien helppokäyttöomaisuudet](/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoftin helppokäyttökeskus](https://www.microsoft.com/accessibility)

[Dynamics 365:n helppokäyttökeskus](/dynamics365/get-started/accessibility/index)

[Yhteensopivuuden yleiskatsaus](compliance-overview.md)

[Evästeen yhteensopivuus](cookie-compliance.md)

[Lisää tietosuojakäytäntösivu](add-privacy-page.md)

[Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]