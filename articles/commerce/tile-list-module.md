---
title: Ruutuluettelomoduuli
description: Tässä ohjeaiheessa kerrotaan ruutuluettelomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: dd714f29fe2f9acd459be7bda1c0bfac65b72cb0
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780790"
---
# <a name="tile-list-module"></a>Ruutuluettelomoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan ruutuluettelomoduuleista ja niiden lisäämisestä sivuston sivuille Microsoft Dynamics 365 Commercessa.

Ruutuluettelomoduuli on kokoelma ruutuja karusellissa. Sitä käytetään tuoteluokkien tai tuotemerkkien markkinointiin kuvien ja tekstin avulla. Esimerkiksi vähittäismyyjä voi lisätä ruutuluettelomoduulin sähköisen kaupankäynnin sivuston aloitussivulle mainostaakseen kaikkia myydyimpiä tuoteluokkia.

Ruutuluettelomoduulia ohjaavat sisällönhallintajärjestelmän (CMS) tiedot. Se ei ole riippuvainen muista Commerce headquarters -sovelluksen muista moduuleista tai tiedoista. Ruutuluettelomoduuli voidaan lisätä mille tahansa sivuston sivulle, jossa jälleenmyyjä haluaa markkinoida tai mainostaa jotakin (esimerkiksi tuotteita, luokkia tai tuotemerkkejä).

Seuraavassa kuvassa on esimerkki ruutuluettelomoduulista ja ruutumoduuleista Adventure Works -aloitussivulla.

![Esimerkki ruutuluettelomoduulista ja ruutumoduuleista Adventure Works -aloitussivulla](./media/Tile_list.PNG)

> [!IMPORTANT]
> Ruutuluettelomoduuli on käytettävissä Dynamics 365 Commerce -versiosta 10.0.20 eteenpäin.
> Ruutuluettelomoduuli on esillä Adventure Works -teemassa.

## <a name="tile-list-modules-and-themes"></a>Ruutuluettelomoduulit ja teemat

Ruutuluettelomoduuli voi tukea erilaisia teemaan perustuvia asetteluja ja tyylejä. Esimerkiksi Adventure Works -teemassa ruudut näyttävät animaatiotehosteen, kun käyttäjä siirtää osoittimensa niiden ylle. Jokainen teema voi sisältää lisäominaisuuksia ruutuluettelo- ja ruutumoduuleille. Lisäksi teemat kehittäjät voivat luoda lisää asetteluita ruutuluettelo- ja ruutumoduuleille.

## <a name="tile-list-module-properties"></a>Ruutuluettelomoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Otsikko       | Otsikkoteksti ja -tunnus | Ruutuluettelomoduulin tekstiotsikko. |

## <a name="tile-module-properties"></a>Ruutumoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Kuva         | Kuvatiedosto | Kuvan avulla voidaan esitellä tuotetta tai luokkaa. Kuva voidaan ladata Commerce-sivuston luontiohjelman mediakirjastoon. Myös olemassa olevaa kuvaa voi käyttää. |
| Otsikko       | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Otsikolle käytetään oletusarvoisesti **H2**-otsikkotunnistetta, mutta tunnistetta voi kuitenkin muuttaa tarvittaessa helppokäyttötoimintojen vaatimusten noudattamiseksi. |
| Kappale     | Kappaleen teksti | Moduuli tukee kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan, kuten hyperlinkit, lihavointi, alleviivaus ja kursiivi. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä          | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** | Moduulit tukevat vähintään yhtä toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |
| Ruudun linkki     | Linkin teksti, URL-osoite, ARIA-otsikko ja **Avaa linkki uudessa välilehdessä** -valitsin | Tätä ominaisuutta käytetään toimintokutsun linkin määrittämiseen. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen.|
| Kuvake          | Kuva | Voit lisätä tuotteen tai luokan kuvan lisäksi kuvakesymbolin. Kuvakesymbolin kuva näytetään tuotteen tai luokan kuvan yläpuolella. |

## <a name="add-a-tile-list-module-to-a-new-page"></a>Ruutuluettelomoduulin lisääminen uudelle sivulle

Voit lisätä ruutuluettelomoduulin uudelle sivulle ja määrittää sen pakolliset ominaisuudet seuraavalla tavalla.

1. Valitse **Mallit** ja avaa sivustosi aloitussivun markkinointimalli (tai luo uusi markkinointimalli).
1. Valitse oletussivun **pääpaikassa** kolme pistettä (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Ruutuluettelo**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Valitse **Sivut** ja avaa sivuston aloitussivu (tai luo uusi aloitussivu käyttämällä markkinointimallia).
1. Valitse oletussivulla **pääpaikka**. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Ruutuluettelo**-moduuli ja valitse sitten **OK**.
1. Lisää otsikko ruutuluettelomoduulin ominaisuusruudussa.
1. Valitse **Ruutuluettelo**-paikasta kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Ruutumoduuli**-moduuli ja valitse sitten **OK**.
1. Lisää kuva, otsikko ja kuvakesymbolin kuva ruutumoduulin ominaisuusruudusta.
1. Lisää ja määritä lisää ruutuluettelomoduuleita tarpeen mukaan.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Adventure Works -teema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
