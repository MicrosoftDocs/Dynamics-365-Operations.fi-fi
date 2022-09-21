---
title: Varaston huomioon ottava tuoteluettelo
description: Tässä artikkelissa kuvataan, miten organisaatiot voivat määrittää tuoteluettelosivut Microsoft Dynamics 365 Commercen sähköisen kaupankäynnin sivustossa niin, että ne ottavat varaston huomioon.
author: boycez
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2022-08-23
ms.openlocfilehash: 2a65dedf2da62fcd92169077d75a0f3b7832a86d
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473730"
---
# <a name="inventory-aware-product-listing"></a>Varaston huomioon ottava tuoteluettelo

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, miten organisaatiot voivat määrittää tuoteluettelosivut Microsoft Dynamics 365 Commercen sähköisen kaupankäynnin sivustossa niin, että ne ottavat varaston huomioon. Tuoteluettelosivuilla ovat luokkien saapumissivut ja hakutulossivut.

Ostajat yleensä odottavat tuotteen sähköisen kaupankäynnin sivuston ottavan varaston huomioon. Tämä auttaa ostajia päättämään, mitä tehdä tuotteen ollessa loppu varastosta. [Commercen moduulikirjaston](starter-kit-overview.md) luokan ja hakutulosten moduulit voidaan määrittää sisältämään varastotiedot. Näin voidaan saavuttaa seuraavat käyttökokemukset:

- Näytä varastotason etiketit yhdessä tuotteiden kanssa.
- Piilota varastosta loppuneet tuotteet tuoteluettelosta.
- Siirrä varastosta loppuneet tuotteet tuoteluettelosivujen loppuun.
- Tukee varastoon perustuvaa tuotesuodatusta.

Ennen kuin voit ottaa nämä kokemukset käyttöön, on otettava käyttöön **Parannettu sähköisen kaupankäynnin tuotteiden etsintä, joka ottaa varaston huomioon** -ominaisuus Commerce headquartersissa.

> [!NOTE]
> Commercen versiossa 10.0.29 ja uudemmissa versioissa **Parannettu sähköisen kaupankäynnin tuotteiden etsintä, joka ottaa varaston huomioon** -ominaisuus on käytössä oletusarvoisesti.

## <a name="set-up-product-attribute-for-inventory-availability"></a>Tuotemääritteen määrittäminen varaston saatavuutta varten

Varaston huomioon ottava tuoteluettelo käyttää tuotemääritteiden kehystä. Edellytyksenä on luotava määritetty tuotemäärite, jonka avulla varaston saatavuustiedot siepataan.

Varaston saatavuuden uusi tuotemäärite määritetään Commerce headquartersissa alla olevien vaiheiden mukaisesti.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Tuotteet ja varasto \> Täytä tuotemääritteet varastotason avulla**.
1. Syötä **Täytä tuotemääritteisiin varastotaso** -valintaruudun **Tuotteen määrite ja tyypin nimi** -kenttään varastotietojen sieppaamista varten luotavan määritetyn tuotemääritteen mukautettu nimi.
1. Valitse **Varaston käytettävyyden peruste** -kentässä määrätyyppi, johon varastotason laskennan tulee perustua. Se voi olla **Saatavissa oleva fyysinen** tai **Yhteensä käytettävissä**.
1. Määritä **Eräkäsittely**-asetuksen arvoksi **Kyllä**.
1. Valitse **OK**.

> [!NOTE]
> Jotta varastotaso laskettaisiin yhdenmukaisesti sähköisen kaupankäynnin sivuston sivuilla, varmista, että valittuna on sama määrätyyppi **Varastosaatavuuden peruste** -kentässä **Täytä tuotemääritteisiin varastotaso** -työlle ja **Varastotaso perustuu** -asetus Commercen sivustomuodostimessa.

Kun määritetty tuotemäärite on luotu, määritetään verkkokanavan määrite.

Verkkokanavan määrite määritetään Commerce headquartersissa alla olevien vaiheiden mukaisesti.

1. Valitse **Retail ja Commerce \> Kanavan asetukset \> Kanavaluokat ja tuotemääritteet**.
1. Valitse verkkokanava, jossa varaston huomioon ottava tuoteluettelokokemus otetaan käyttöön.
1. Valitse ja avaa liittyvä määriteryhmä, ja lisää sitten uusi tuotemäärite siihen.
1. Siirry kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu** ja suorita työ **1150** (**Luettelo**). Tämä työ kannattaa ajoittaa eräkäsittelyksi, joka suoritetaan yhtä usein kuin **Täytä tuotemääritteisiin varastotaso** -työ.

> [!NOTE]
> Commercen versiossa 10.0.26 ja aiemmissa versioissa varastosaatavuuden tuotemääritteen määriteryhmään lisäämisen jälkeen on valittava myös **Määritä määritteen metatiedot** -kohta ja otettava uuden tuotemääritteen **Näytä määrite kanavassa**-, **Noudettavissa**-, **Voidaan tarkentaa**- ja **Voidaan kysellä** -vaihtoehdot käyttöön.

## <a name="configure-the-display-behavior-for-out-of-stock-products-on-product-listing-pages"></a>Näyttötoiminnon määrittäminen varastosta loppuneille tuotteille tuoteluettelosivuilla

Kun edellä mainitut määritysvaiheet on tehty loppuun, luokka- ja hakutulossivujen tarkenteilla on varastoon perustuva suodatusvalinta. Kaikille sivulla näkyville tuoteruuduille näytetään varastotason tunniste.

Luokka- ja hakutulossivulla näkyvät päätasolla olevat tuotteet. Tuotevarianttitasolla olevia tuotteita ei näytetä. Kunkin tuotteen yhteydessä näytettävä varastotaso on yhdistetty varastotaso, joka määräytyy kaikkien tuotevarianttien varastotason mukaan. Variantin varastotaso lasketaan Commerce headquartersin verkkokanavan oletusvaraston variantin varastosaldon perusteella. Päätuotteen varastotasolla on kaksi mahdollista arvoa, jotka esittävät varastossa olevien ja varastosta loppuneiden tilaa. Päätuotteen katsotaan loppuneen varastosta, kun kaikki sen variantit ovat loppuneet varastosta. Muussa tapauksessa tuotetta ajatellaan olevan varastossa. Arvon selite haetaan [varastotason](inventory-buffers-levels.md) määritelmästä. Jos varastotasoa ei ole määritetty, oletusselitteet ovat **Käytettävissä** ja **Loppuneet varastosta**.

Tämän jälkeen voit määrittää Commercen sivustonmuodostimen **Tuoteluettelosivujen varastoasetukset** -asetuksen, jolla hallitaan sitä, miten luokka- ja hakutulossivu näyttää varastosta loppuneet tuotteet. Lisätietoa kohdassa [Varastoasetusten käyttöönotto](inventory-settings.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
