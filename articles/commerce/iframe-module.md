---
title: iFrame-moduuli
description: Tässä ohjeaiheessa käsitellään iFrame-moduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
ms.date: 11/04/2021
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bce6a50e8c145f8961bd0c839fe16c1f4d69e811
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/05/2021
ms.locfileid: "7754011"
---
# <a name="iframe-module"></a>iFrame-moduuli

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään iFrame-moduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.

iFrame-moduuli sisältää iFrame-kehyksen (sisäinen kehys), joka isännöi sivuston ulkoista sisältöä. Sen avulla voidaan esimerkiksi isännöidä YouTube-videota tai PDF-tiedoston katseluohjelmaa millä tahansa sivuston sivulla. 

iFrame-moduuli edellyttää kohde-URL-osoitetta. Sen jälkeen se isännöi kohdesivun sisältöä HTML:n **iFrame**-elementin sisällä. Ulkoisten URL-osoitteiden on oltava sallittujen luettelossa sivuston sisällön suojauskäytännön direktiivien mukaan. iFrame-sisällössä URL-osoitteet tulisi sallia käyttämällä **frame-ancestor**-direktiiviä. Lisätietoja on kohdassa [Sisällön suojauskäytännön hallinta](manage-csp.md).

> [!NOTE]
> iframe-moduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.13.

Seuraavassa kuvassa näkyy esimerkkejä iFrame-moduuleista, jotka esittelevät sivuston sivujen ulkoisia videoita.

![Esimerkki iframe-moduuleista, jotka esittelevät ulkoisia videoita.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>iFrame-moduulin ominaisuudet

| Ominaisuuden nimi             | Arvo                 | kuvaus |
|---------------------------|-----------------------|-------------|
| Otsikko | Teksti | Moduulin otsikko. |
| Kohde-URL-osoite | URL-osoite | Moduulissa isännöity URL-osoite. |
| Korkeus | Numero tai prosenttiosuus | Moduulin korkeus kuvapisteinä tai prosentteina. Esimerkiksi arvoa **100** käsitellään kuvapisteinä ja arvoa **100 %** prosenttina. |
| Aria-otsikko | Teksti | ARIA-otsikko (Accessible Rich Internet Applications) voidaan määrittää helppokäyttöisyyttä varten. |

## <a name="add-an-iframe-module-to-a-page"></a>iFrame-moduulin lisääminen sivulle

Voit lisätä sivulle ulkoisen videon näyttävän iFrame-moduulin seuraavasti.

1. Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.
1. Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan **Markkinointimalli** ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.
1. Valitse **Valitse malli** -valintaikkunassa **Markkinointimalli**-malli. Kirjoita **Sivun nimi** -kohtaan **Markkinointisivu** ja valitse sitten **OK**.
1. Valitse uudella sivulla **Pää**-paikka. Valitse kolmen pisteen painike (**…**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **Kontti**-moduuli ja valitse sitten **OK**.
1. Määritä moduulin ominaisuusruudussa **Leveys**-kohdan arvoksi **Täytä kontti**.
1. Valitse kolme pistettä (**...**) **Kontti**-paikassa ja valitse sitten **Lisää moduuli**.
1. Valitse **Lisää moduuli** -valintaikkunassa **iFrame**-moduuli ja valitse sitten **OK**.
1. Määritä moduulin ominaisuuksien ruudussa **kohde-URL:n** arvo videon ulkoiselle URL-osoitteelle.
1. Määritä halutessasi muut ominaisuudet, kuten **otsikko** ja **korkeus**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.
1. Siirry sivuston markkinointisivulle. Videon tulisi olla hahmonnettu iFrame-moduuliin.

> [!NOTE]
> Koska iframe-moduuli isännöi ulkoista sisältöä, sivuston tekijöiden on varmistettava, että iframe-moduulissa isännöity sisältö ei riko sisällön rajoituskäytäntöjä kyseisellä markkina-alueella. Jos iframe-moduulia käyttävällä sivulla on sisältörikkomus, sivuston tekijä voi poistaa iframe-moduulin avaamalla sivun sivustonmuodostimessa, valitsemalla **Poista moduuli** iframe-moduulipaikassa sekä tallentamalla sivun ja julkaisemalla sivun sitten uudelleen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Sisällön suojauskäytännön (CSP) hallinta](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
