---
title: Favicon-kuvakkeen lisääminen
description: Tässä artikkelissa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 41d6d8f823c7364f9206fd0f7588e35b6f0a018a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270434"
---
# <a name="add-a-favicon"></a>Favicon-kuvakkeen lisääminen

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, kuinka favicon-kuvake lisätään sivustoon.

Favicon on pieni grafiikkatiedosto, joka näkyy selaimen välilehdessä, osoitepalkissa, selaushistoriassa sekä muissa paikoissa, kuten kirjanmerkeissä tai suosikeissa. Suosittelemme, että lisäät favicon-kuvakkeen sivustoon, koska se edustaa ja vahvistaa omaa tuotemerkkiä ja auttaa sivuston erottumisessa muista sivustoista, joilla asiakkaat käyvät.

Voit lisätä useita eri kokoisia favicon-kuvakkeita ja erilaisia favicon-tiedostoja sivustoon. Tässä artikkelissa kerrotaan, miten voit lisätä yhden favicon-kohteen. Samaa prosessia ja sijaintia käytetään useiden favicon-kohteiden lisäämisessä.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Lataa favicon sivuston resurssikokoelmaan

Lataa favicon sivuston resurssikokoelmaan seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Mediakirjasto**.
1. Valitse komentopalkissa **Lataa \> Lataa medianimikkeet**.
1. Siirry Resurssienhallinnan ikkunassa ladattavan favicon-kuvaketiedoston kohdalle, valitse se ja valitse sitten **Avaa**.
1. Syötä **Lataa medianimike** -valintaikkunaan pakollinen otsikko ja vaihtoehtoinen teksti.
1. Jos haluat julkaista kuvan heti latauksen jälkeen, valitse **Julkaise medianimikkeet latauksen jälkeen** -valintaruutu.

    > [!NOTE]
    > Jos et valitse **Julkaise mediakohteet lataamisen jälkeen** -valintaruutua, palaa **Mediakohteet**-sivulle ja julkaise favicon myöhemmin manuaalisesti.

1. Valitse **OK**.
1. Kopioi oikealla olevaan ominaisuusruutuun favicon-tiedoston julkinen URL-osoite. Tätä URL-osoitetta käytetään myöhemmin.

## <a name="create-the-html-for-your-favicon"></a>Luo favicon-tiedostollesi HTML-koodia

Jos haluat luoda favicon-tiedostolle HTML-koodia, käytä seuraavaa HTML-merkkijonoa. Korvaa **href**-määritteessä **Public\_URL\_for\_your\_favicon** aiemmin kopioimallasi julkisella URL-osoitteella.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Luo osa, joka sisältää metatunnisteen omalle faviconillesi

Seuraa näitä ohjeita luodaksesi osan, joka sisältää metatunnisteen omalle faviconillesi.

1. Siirry kohtaan **Osat** ja valitse **Uusi**.
1. Valitse **Uusi osa** -valintaikkunan **Metatunnisteet** moduulina, johon osa perustuu.
1. Kirjoita osan nimi ja valitse **OK**.
1. Valitse fragmentti hierarkiapuussa **Oletusmetatunnisteet**-alikohde.
1. Valitse oikeanpuoleisessa ruudussa **Metatunnisteet**-kohdasta **Lisää** ja kirjoita sitten aiemmin luomasi favicon-HTML-merkkijono. 
1. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi osan.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Lisää metatunnisteen osa sivujesi HTML-pääosaan

Seuraa näitä ohjeita lisätäksesi metatunnisteen osa sivujesi HTML-**pää**-osaan.

1. Siirry **Mallit**-kohtaan ja avaa niiden sivujen malli, joihin haluat lisätä faviconisi ja valitse sitten **Muokkaa**.
1. Valitse mallihierarkiapuussa **HTML-pääsäilön** oikealla puolella oleva ellipsi- ( **...**)-painike ja valitse sitten **Lisää osa**.
1. Valitse **Uusi osa** -valintaikkunassa metatunnistesivukatkelma, jonka loit aiemmin ja valitse sitten **OK**.
1. Valitse **Lopeta muokkaus** ja valitse sitten **Julkaise** julkaistaksesi mallin.

> [!NOTE]
> Jos sivustossa käytetään useampaa kuin yhtä mallia, sinun on lisättävä metatunnisteen osa kaikkiin.

Kun esikatselet sivuja, jotka perustuvat malliin, johon lisäsit metatunnisteen osan, sinun pitäisi nyt nähdä favicon selaimen välilehdessä.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[CSS-ohitustiedostojen parissa työskentely](css-override-files.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
