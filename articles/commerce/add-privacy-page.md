---
title: Lisää tietosuojakäytäntösivu
description: Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a9e09a1d0dbd6c0dc94b5668bb29de6605e2ca9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980204"
---
# <a name="add-a-privacy-policy-page"></a>Lisää tietosuojakäytäntösivu


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten tietosuojakäytäntösivu lisätään sivustollesi Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Tietosuojan noudattaminen sisältää organisatorisia toimenpiteitä, jotka ilmoittavat sivuston käyttäjille, miten heidän tietojaan kerätään ja käsitellään. Käyttäjät voivat sitten päättää, miten he haluavat henkilötietojaan käsiteltävän, ja ryhtyä asianmukaisiin toimiin.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Tarkastele Microsoftin tietosuojatietoja Dynamics 365 Commercessa

Jos haluat tarkastella Microsoftin tietosuojalausuntoa, kun olet kirjautuneena Dynamics 365 Commercen sisällönluontityökaluihin, valitse oikeasta yläkulmasta **Ohje**-painike (**?**) ja valitse sitten **Tietosuoja ja evästeet**. Avataan uusi välilehti, jolla on linkki [Microsoftin tietosuojalausuntoon](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Luo sivustoosi tietosuojakäytäntösivu

Dynamics 365 Commercesta löydät useita tapoja antaa sivustosi käyttäjille pääsy tietosuojakäytäntöihin. Tässä osassa kerrotaan, miten voit luoda tietosuojakäytäntösivun ja viitata sitten sivuun alatunnisteosan avulla.

Seuraavassa on esimerkki siitä, miten voit luoda yleisen tietosuojakäytäntösivun Commerce-sivustolle. Olet vastuussa siitä, että suunnittelet ja toteutat tietosuojakäytäntösivuratkaisun, joka vastaa parhaiten yrityksesi lakisääteisiä vaatimuksia.

Kun haluat aloittaa, siirry sisällönluontityökaluihin sivustossa, johon haluat luoda tietosuojakäytäntösivun.

### <a name="create-a-template"></a>Luo malli

> [!NOTE]
> Jos tietosuojakäytäntösivulla käytettävä malli on jo luotu, siirry eteenpäin [Muodosta tietosuojakäytäntösivu](#build-a-privacy-policy-page) -osioon.

Voit luoda mallin seuraavien vaiheiden avulla.

1. Siirry kohtaan **Mallit** ja luo sivumalli valitsemalla **Uusi**.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Mainosnauhan malli** ja valitse sitten **OK**.
1. Lisää tarvittavat moduulit malliin vaadittavien sivupaikkojen kohdalle. Jos haluat ohjeita, vie hiiri punaisen huutomerkin päälle. (Esimerkiksi **HTML-head-paikka** saattaa vaatia **ulkoisen oletuskomentosarjamoduulin**.)
1. Lisää **Tekstipaikkaan** **Oletussivumoduuli**.
1. Lisää **Sisällöntäyteinen lohkomoduuli** **Oletussivun** **Pääpaikkaan**.
1. Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.

### <a name="build-a-privacy-policy-page"></a>Luo tietosuojakäytäntösivu

Voit luoda tietosuojakäytäntösivun noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Sivut** ja sitten **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunan tietosuojakäytäntösivun malli.
1. Kirjoita sivun nimi ja URL-osoite ja valitse **OK**. 
1. Lisää **Sisällöntäyteinen lohkomoduuli** sivun **Pääpaikkaan**.
1. Lisää **Sisällöntäyteiseen lohkomoduuliin** **Sisällöntäyteinen lohkonimikemoduuli**.
1. Valitse **Sisällön Rich Block** -moduulin Ominaisuudet-ruudusta **Lisää tietolähde** ja valitse sitten **Rich Text -sisältö**.
1. Kirjoita RTF-editorissa tietosuojakäytäntösivun sisältö. Laajenna Rich Text -editori tarvittaessa koko näytön tilaan.
1. Kun olet lopettanut sisällön kirjoittamisen, esikatsele sivua verkkoselaimessa valitsemalla **Esikatselu**.
1. Täydennä kaikki sivun ja moduulin ominaisuuksien jäljellä olevat lisäykset.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.

Voit julkaista tietosuojakäytäntösivun URL-osoitteen seuraavasti.

1. Siirry **URL-osoitteisiin** ja valitse tietosuojakäytäntösivun URL-osoite.
1. Julkaise valittu URL-osoite valitsemalla **Julkaise**.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Luo linkki tietosuojakäytäntösivun alatunnisteeseen

Voit lisätä linkin tietosuojakäytäntösivun osaan. Tällä tavoin voit jakaa linkin ja päivittää sen useille sivustosivuille viittaamalla osaan. Tässä esimerkissä kerrotaan, kuinka voit lisätä linkin tietosuojakäytäntösivulle alatunnisteen osaan.

Voit lisätä linkin alatunnisteosaan seuraavasti.

1. Siirry kohtaan **Osat** ja **Uusi** luodaksesi sivun osan.
1. Valitse **Uusi osa** -valintaikkunassa **Alatunniste**-moduuli.
1. Kirjoita **Osan nimi** -kohtaan osan nimi ja valitse sitten **OK**.
1. Lisää **Alatunnisteluokka**-paikkaan **Alatunnisteen nimike** -moduuli.
1. Valitse oikeanpuoleisessa ominaisuusruudussa **Linkitä teksti**.
1. Kirjoita **Linkitä teksti** -valintaikkunassa tietosuojakäytäntösivun linkkiteksti ja linkkikohde ja valitse sitten **OK**.
1. Jos haluat saada tietosuojakäytäntösivun URL-osoitteen, siirry kohtaan **Sivut**, siirry tietosuojakäytäntösivulle ja kopioi URL-osoite Ominaisuudet-ruudusta.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi osan, ja julkaise se valitsemalla **Julkaise**.
1. Esikatsele osa ja testaa linkki tietosuojakäytäntösivulle.

Osaan voidaan nyt viitata muiden sivuston sivujen mallissa. Kun tähän osaan viitataan mallin **Alatunniste**-moduulissa, linkkiviittaus näkyy kaikilla sivuilla, jotka on rakennettu kyseisen mallin avulla.

## <a name="additional-resources"></a>Lisäresurssit

[Yhteensopivuuden yleiskatsaus](compliance-overview.md)

[Helppokäyttöisyyden toiminnot ja ominaisuudet](accessibility.md)

[Evästeen yhteensopivuus](cookie-compliance.md)

[Seurattuihin sisällönmuutoksiin liittyvien käyttäjätunnusten korvaaminen](replace-IDs-tracked-changes.md)
