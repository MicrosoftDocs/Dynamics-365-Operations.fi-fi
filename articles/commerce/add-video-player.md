---
title: Videotoistinmoduuli
description: Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b7ec2ea0f8360bbf1dffa023e4546e4deadb5ff9
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780761"
---
# <a name="video-player-module"></a>Videotoistinmoduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa on tietoja videotoistinmoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Videotoistinmoduulia käytetään tukemaan videotoistoa. Se voidaan lisätä mille tahansa sivulle, kunhan videosisältö on ladattu ja käytettävissä sisällönhallintajärjestelmässä (CMS). Videotoistinmoduuli tukee .mp4-mediatyypin.

## <a name="video-player-module"></a>Videotoistinmoduuli

Videotoistinmoduulin avulla voit esitellä videoita sähköisen kaupankäynnin sivustossa. Se tukee kaikkia toisto-ominaisuuksia, kuten toistoa, pysäytystä, koko näytön tilaa, äänikuvauksia ja tekstityksiä. Videotoistinmoduuli tukee myös tekstitysten mukauttamista Microsoftin helppokäyttötoimintojen standardien mukaisesti. Voit esimerkiksi mukauttaa fontin kokoa ja taustaväriä.

Videosoitinmoduuli tukee myös toissijaisia ääniraitoja. Kun video ladataan CMS-järjestelmään, myös toissijainen ääniraita voidaan ladata. Videosoitinmoduuli voi sitten toistaa toissijaisen ääniraidan, jos käyttäjä valitsee sen.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Esimerkkejä videotoistinmoduuleista sähköisessä kaupankäynnissä

- Tuotetietosivujen tai markkinointisivujen ohjevideot
- Markkinointisivuilla olevat käytäntöjä koskevat kampanjavideot tai videot
- Markkinointivideot, joissa kerrotaan tuotteen ominaisuuksista tuotetietosivuilla tai markkinointisivuilla

Seuraavassa kuvassa on esimerkki videotoistinmoduulista kotisivulla.

![Esimerkki videotoistinmoduulista.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Videotoistinmoduulin ominaisuudet

| Ominaisuuden nimi         | Arvo                               | kuvaus |
|-----------------------|-------------------------------------|-------------|
| Otsikko               | Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**) | Otsikolle käytetään oletusarvoisesti **H2**-otsikkotunnistetta, mutta tunnistetta voi kuitenkin muuttaa tarvittaessa helppokäyttötoimintojen vaatimusten noudattamiseksi. |
| Muotoiltu teksti             | Kappaleen teksti | Moduuli tukee kappaleen tekstiä RTF-muodossa. Joitakin RTF-ominaisuuksia tuetaan, kuten hyperlinkit, lihavointi, alleviivaus ja kursiivi. Moduulissa käytössä oleva sivun teema voi ohittaa jotkin näistä ominaisuuksista. |
| Linkitä                  | Linkin teksti, URL-osoite, ARIA (Accessible Rich Internet Applications) -otsikko ja **Avaa linkki uudessa välilehdessä** -valitsin | Moduuli tukee yhtä tai useampaa toimintokutsulinkkiä. Jos linkki on lisätty, linkin teksti, URL-osoite ja ARIA-otsikko ovat pakollisia. ARIA-otsikkojen on oltava kuvailevia, jotta ne vastaavat helppokäyttötoimintojen vaatimuksia. Linkit voidaan määrittää niin, että ne avautuvat uuteen välilehteen. |
| Alateksti              | Otsikko, teksti tai linkit | Videotoistinmoduulille voidaan lisätä lisätietoja, kuten kirjoittajan tai suunnittelijan nimi, tai linkkejä henkilökohtaisiin blogeihin. |
| Automaattinen toisto             | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, videota toistetaan automaattisesti. |
| Vaimenna                  | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, ääni on vaimennettu. Tämän toistimen oletusarvo on **Epätosi**. Chrome-selaimessa automaattisen toiston videot vaimennetaan oletusarvoisesti. Ääni toistetaan vain, jos käyttäjä toistaa videon manuaalisesti. |
| Silmukka                  | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, video toistetaan silmukassa. |
| Mediat                 | Videotiedostopolku ja -nimi | Videotiedosto, jota videotoistin toistaa. |
| Toista koko näyttössä       | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, videota toistetaan koko näytön tilassa. |
| Toiston/keskeytyksen valitsin    | **Tosi** vai **Epätosi**               | Kun arvoksi on asetettu **Tosi**, videossa näkyy toisto/pysäytys-painike. |
| Videosoittimen säätimet | **Tosi** vai **Epätosi**               | Kun arvoksi on määritetty **Tosi**, kaikki videotoistimen ohjausobjektit näkyvät. Näitä ohjausobjekteja ovat toisto- ja pysäytyspainikkeet, tilanneilmaisin ja tekstitysvaihtoehdot. |
| Piilota julistekuva     | **Tosi** vai **Epätosi**               | Videossa voi olla julistekehys. Kun tämän ominaisuuden arvoksi määritetään **Tosi**, julistekehys piilotetaan. |
| Peitteen taso            | Numero väliltä **0**–**100** | Muoto, jota käytetään videon muotoiluun. |

> [!IMPORTANT]
> **Otsikko**-, **Muotoiltu teksti**-, **Linkki**- ja **Alateksti**-ominaisuudet ovat käytettävissä Dynamics 365 Commerce -version 10.0.20 julkaisusta eteenpäin.

## <a name="add-a-video-player-module-to-a-page"></a>Videotoistinmoduulin lisääminen sivulle

> [!NOTE] 
> Video on ennen videotoistinmoduulin luontia ladattava mediakirjastoon.

Voit lisätä videotoistinmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Videotoistimen malli** ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.
1. Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**. 
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Syötä **Luo uusi sivu** -dialogiruudussa, kohdan **Sivun nimi** alla, **Videosoitinsivu** ja valitse sitten **Seuraava**.
1. Valitse **Valitse malli** -kohdassa luomasi **Videosoitinmalli** ja valitse sitten **Seuraava**.
1. Valitse **Valitse asettelu** -kohdassa sivun asettelu (esimerkiksi **Joustava asettelu**) ja valitse sitten **Seuraava**.
1. Tarkista sivun konfigurointi kohdassa **Tarkista ja viimeistele**. Jos haluat muokata sivun tietoja, valitse **Takaisin**. Jos sivun tiedot ovat oikein, valitse **Luo sivu**.
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Videotoistin**-moduuli ja valitse sitten **OK**.
1. Valitse videotoistinmoduulin ominaisuusruudussa **Lisää video**.
1. Valitse **Mediavalitsin**-valintaikkunassa video ja valitse sitten **Lataa uusi medianimike**.
1. Valitse Resurssienhallinnassa videotiedosto ja valitse sitten **Avaa**.
1. Kirjoita **Lataa mediakohde** -valintaikkunaan otsikko ja muut tarvittavat tiedot ja valitse sitten **OK**.
1. Valitse **Mediavalitsin**-valintaikkunassa **Sulje**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**. Videomoduulin pitäisi näkyä sivulla. Voit muokata moduulin toimintaa muuttamalla lisäasetuksia.
1. Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen. 

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Promopalkkimoduuli](add-alert.md)

[Karusellimoduuli](add-carousel.md)

[Tekstilohkomoduuli](add-content-rich-block.md)

[Sisältölohkomoduuli](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
