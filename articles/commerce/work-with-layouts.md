---
title: Esimääritettyjen asettelujen käyttö
description: Tässä artikkelissa käsitellään esimääritettyjen asettelujen käsittelemistä Microsoft Dynamics 365 Commercessa.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: b588df5702657f07e1e790ffba39d2e459901557
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286273"
---
# <a name="work-with-preset-layouts"></a>Esimääritettyjen asettelujen käyttö

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään esimääritettyjen asettelujen käsittelemistä Microsoft Dynamics 365 Commercessa.

Ennen kuin suoritat tämän artikkelin toiminnot, muista tutustua kohtaan [Esimääritetyt ja mukautetut asettelut](templates-layouts-overview.md#preset-and-custom-layouts). Yleinen yleiskuvaus on kohdassa [Mallien ja asettelujen yleiskatsaus](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Uuden esimääritetyn asettelun luominen

Esimääritetty asettelu voidaan luoda kahdella eri tavalla. Voit tallentaa aiemmin luodun mukautetun asettelun uudeksi esimääritetyksi asetteluksi tai luoda esimääritetyn asettelun alusta alkaen.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Esimääritetyn asettelun luominen aiemmin luodusta mukautetusta asettelusta

Voit luoda esimääritetyn asettelun aiemmin luodusta mukautetusta asettelusta seuraavasti.

1. Avaa aiemmin luotu sivu, joka ei tällä hetkellä käytä esimääritettyä asettelua ja jonka moduulirakennetta haluat käyttää muilla sivuston sivuilla.
1. Valitse **Muokkaa** tarkistaaksesi sivun.
1. Valitse **Tallenna uutena asetteluna**. **Tallenna uutena asetteluna** -valintaikkuna tulee näkyviin.
1. Kirjoita esimääritetyn asettelun nimi ja kuvaus. Syöttämäsi arvot näkyvät muille tekijöille, kun ne luovat uusia sivuja asettelusta tai siirtyvät siihen. Anna sen vuoksi arvoja, joista on hyötyä sivujen tekijöille.
1. Valitse **OK**.

Esimääritetty asettelu on nyt käytettävissä, kun luotu uusia sivuja tai valitset toisen asettelun saman mallihierarkian sivulle.

> [!TIP]
> Voit tarkistaa nopeasti, onko tietty sivu sidottu esimääritettyyn asetteluun, valitsemalla sivuluettelonäkymän sivun ja tarkastamalla asettelun metatiedot oikeanpuoleisessa ominaisuusruudussa.

### <a name="create-a-new-preset-layout"></a>Uuden esimääritetyn asettelun luominen

Voit luoda esimääritetyn asettelun alusta alkaen seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Asettelut**.
1. Valitse **Uusi asettelu**. **Uusi asettelu** -valintaikkuna tulee näkyviin.
1. Valitse esimääritetyssä asettelussa käytettävä malli.
1. Kirjoita esimääritetyn asettelun nimi ja kuvaus. Syöttämäsi arvot näkyvät muille tekijöille, kun ne luovat uusia sivuja asettelusta tai siirtyvät siihen. Anna sen vuoksi arvoja, joista on hyötyä sivujen tekijöille.
1. Luo uusi esimääritetty asettelu ja avaa asettelueditori valitsemalla **OK**.
1. Lisää moduulit asettelueditoriin ja määritä ne siellä käyttämällä jäsennyspuuta vasemmalla ja ominaisuusruutua oikealla. (Prosessi muistuttaa moduulien lisäämistä ja määrittämistä mallieditorin mallissa.) Moduulien järjestys ja mahdolliset lukitut oletusasetukset ovat keskitetyn moduulin määrityksessä kaikissa tätä esimääritettyä asettelua käyttävillä sivuilla.

## <a name="modify-a-preset-layout"></a>Esimääritetyn asettelun muokkaaminen

Voit muokata esimääritettyä asettelua seuraavasti.

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Asettelut**.
1. Valitse muokattava moduuli asettelueditorissa jäsennyspuussa vasemmalla. Tee sitten jokin seuraavista toiminnoista:

    - Jos haluat siirtää moduulia ylös- tai alaspäin päätasolla, valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Siirrä ylös** tai **Siirrä alas**.
    - Jos haluat muuttaa moduulin oletusasetuksia, määritä oletusarvot ominaisuusruudun avulla. Halutessasi voit lukita ne verkosta tietoa lataavia sivuja varten.
    - Jos haluat lisätä uusia moduuleja tai osia säilömoduuleihin, valitse kolmen pisteen painike ja valitse sitten **Lisää moduuli**- tai **Lisää osa**.
    - Jos haluat poistaa moduulin asettelusta, valitse kolmen pisteen painike ja valitse sitten **Poista**.

## <a name="change-a-preset-layout-theme"></a>Esimääritetyn asettelun teeman muuttaminen

Normaali käytäntö on määrittää oletusteema kaikille sivuille, jotka käyttävät esimääritettyä asettelua.

Seuraavalla tavalla voit määrittää kaikkien niiden alisivujen teeman, jotka käyttävät valmista asettelua, tai muuttaa sitä.

1. Valitse sivun säilömoduuli asettelueditorissa jäsennyspuussa vasemmalla. (Yleensä tämä moduuli on toinen solmu, ja sen nimi on **Oletussivu**.)
1. Valitse oikealla olevan ominaisuusruudun **Teema**-kentässä teema.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Esimääritetyn asettelun tallentaminen kirjaaminen sisään, esikatseleminen ja julkaiseminen

Voit tallentaa esimääritetyn asettelun ja kirjata sen sisään seuraavasti.

1. Valitse **Tallenna** asettelueditorin yläosassa. Tallennetut muutokset eivät vaikuta verkosta tietoja lataaviin sivuihin, ennen kuin ne on kuitattu sisään.
1. Valitse **Viimeistele muokkaus**. Tekemäsi muutokset ovat nyt verkosta tietoja lataavien työnkulkujen löydettävissä.

Voit esikatsella muutoksia avaamalla olemassa olevan esimääritettyä asettelua käyttävän sivun tai luomalla uuden sivun asettelusta.

Kun olet esikatsellut esimääritettyyn asetteluun tehdyt muutokset, julkaise asettelu live-sivustossa jonkin seuraavan vaiheen avulla.

1. Siirry **Asettelut**-kohtaan, valitse asettelu ja valitse sitten **Julkaise**.
1. Valitse asettelun nimi avataksesi asettelueditorin ja valitse sitten **Julkaise**.
1. Julkaise sivu, joka viittaa julkaisemattomaan asetteluun. Asettelu julkaistaan automaattisesti.

> [!WARNING]
> Useat sivut voivat viitata esimääritettyihin asetteluihin. Kun julkaiset esimääritetyn asettelun, ota huomioon, että saatat vaikuttaa useiden sivujen asetteluun.

## <a name="rename-a-preset-layout"></a>Esimääritetyn asettelun uudelleennimeäminen

Voit nimetä esimääritetyn asettelun uudelleen sivuston muodostimessa seuraavasti.

1. Valitse vasemmassa siirtymisruudussa **Asettelut**.
1. Valitse sen asettelun asettelun nimi, jonka haluat nimetä uudelleen.
1. Aloita asettelun muokkaaminen valitsemalla **Muokkaa**.
1. Valitse asettelun nimen vieressä oleva kynäsymboli asettelun ominaisuusruudusta.
1. Muokkaa asettelun nimeä tarpeen mukaan.
1. Vahvista nimenmuutos valitsemalla valintamerkki.
1. Valitse **Viimeistele muokkaus**.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Mallien käyttö](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
