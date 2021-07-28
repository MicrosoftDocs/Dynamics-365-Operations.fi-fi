---
title: Interaktiivinen ominaisuusmoduuli
description: Tässä ohjeaiheessa on tietoja interaktiivista ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a01fb446a1b7dd07e0429b96ff949b88a591f800
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479451"
---
# <a name="interactive-feature-module"></a>Interaktiivinen ominaisuusmoduuli

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja interaktiivista ominaisuusmoduuleista ja niiden lisäämisestä Microsoft Microsoft Dynamics 365 Commercen sivuston sivuille.

Interaktiiviset ominaisuusmoduulit ovat mosaiikkimaisia moduuleja, joita voidaan käyttää useiden tuoteluokkien tai tuotemerkkien markkinoimiseen käyttämällä kuvien ja tekstien yhdistelmää. Esimerkiksi vähittäismyyjä voi lisätä interaktiivisen ominaisuusmoduulin sähköisen kaupankäynnin sivuston aloitussivulle mainostaakseen myydyimpiä tuoteluokkia. Interaktiivinen ominaisuusmoduuli muistuttaa ruutuluettelomoduulia, mutta sillä on erilainen asettelu ja erilaiset interaktiiviset toiminnot.

Jokainen interaktiivinen ominaisuusmoduuli on kokoelma interaktiivisia ominaisuusnimikemoduuleja. Jokaista ominaisuusnimikemoduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Se ei ole riippuvainen muista Commerce headquarters -sovelluksen muista moduuleista tai tiedoista. Interaktiivinen ominaisuusmoduuli voidaan lisätä mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, luokkia tai tuotemerkkejä).

> [!IMPORTANT]
> - Interaktiivinen ominaisuusmoduuli on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.
> - Interaktiivinen ominaisuusmoduuli on esillä Adventure Works -teemassa.

Seuraavassa kuvassa on esimerkki interaktiivisesta ominaisuusmoduulista Adventure Works -aloitussivulla.

![Esimerkki interaktiivisesta ominaisuusmoduulista Adventure Works -aloitussivulla](./media/Feature.PNG)

## <a name="interactive-feature-module-and-themes"></a>Interaktiivinen ominaisuusmoduuli ja teemat

Interaktiivinen ominaisuusmoduuli voi tukea erilaisia teemaan perustuvia asetteluja ja tyylejä. Esimerkiksi Adventure Works -teemassa interaktiivisella ominaisuusmoduulilla on kaksisarakkeinen asettelu, jossa näytetään animaatiotehosteita, kun käyttäjä siirtää osoittimensa nimikkeen ylle. Interaktiivinen ominaisuusmoduuli on optimoitu parilliselle määrälle kuvia, jotka on järjestetty kaksisarakkeiseen asetteluun.

## <a name="interactive-feature-module-properties"></a>Interaktiivisen ominaisuusmoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Interaktiivisen ominaisuusmoduulin tekstiotsikko. |

## <a name="interactive-feature-item-module-properties"></a>Interaktiivisen ominaisuusnimikemoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Kuva         | Kuvatiedosto | Tuotetta tai luokkaa edustava kuva. Kuva voidaan ladata Commerce-sivuston luontiohjelman mediakirjastoon. Myös olemassa olevaa kuvaa voi käyttää. |
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Otsikolle käytetään oletusarvoisesti **H2**-otsikkotunnistetta, mutta tunnistetta voi kuitenkin muuttaa tarvittaessa helppokäyttötoimintojen vaatimusten noudattamiseksi. |
| Kappale     | Kappaleen teksti | Moduuli tukee kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan, kuten hyperlinkit, lihavointi, alleviivaus ja kursiivi. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä          | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** -valitsin | Moduuli tukee yhtä tai useampaa toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |

## <a name="add-an-interactive-feature-module-to-a-new-page"></a>Interaktiivisen ominaisuusmoduulin lisääminen uudelle sivulle

Voit lisätä interaktiivisen ominaisuusmoduulin uudelle sivulle ja määrittää sen vaaditut ominaisuudet Commerce-sivuston luontiohjelmassa noudattamalla seuraavia ohjeita.

1. Valitse **Mallit** ja avaa sivustosi aloitussivun markkinointimalli (tai luo uusi markkinointimalli).
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunasta **Interaktiivinen ominaisuus** -moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Valitse **Sivut** ja avaa sivuston aloitussivu (tai luo uusi aloitussivu käyttämällä markkinointimallia).
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunan **Valitse moduulit** -osiosta **Interaktiivinen ominaisuus** -moduuli ja valitse sitten **OK**.
1. Lisää otsikko interaktiivisen ominaisuusmoduulin ominaisuusruudussa.
1. Valitse **Interaktiivinen ominaisuus** -paikasta kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunasta **Interaktiivinen ominaisuusnimike** -moduuli ja valitse sitten **OK**.
1. Lisää interaktiivisen ominaisuusnimikemoduulin ominaisuusruudusta kuva, otsikkoteksti, kappaleteksti ja URL-osoite.
1. Lisää ja määritä muita interaktiivisia ominaisuusnimikemoduuleita tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Adventure Works -teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
