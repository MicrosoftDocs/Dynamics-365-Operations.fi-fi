---
title: Aiemmin luodun sivuston sivun muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803726"
---
# <a name="modify-an-existing-site-page"></a>Aiemmin luodun sivuston sivun muokkaaminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.

Sivun muokkauksen ensimmäinen vaihe on sivun avaaminen sivueditorissa. Siirry sivustoon, joka sisältää sivun. Etsi haluamasi sivu sivuluettelosta. Jos et löydä sivua, voit käyttää muokkaustyökalun monipuolisia hakutoimintoja. Kirjoita sivun tarkka nimi tai sen ensimmäiset kirjaimet ja sen jälkeen tähti (\*). Näkyviin tulee suodatettu luettelo sivuista. Tämän luettelon avulla voit etsiä haluamasi sivun. Kun olet löytänyt oikean sivun, avaa sivu sivueditorissa valitsemalla sivun nimi.

> [!TIP]
> Jos sivusi näkyy sivun tarkistusohjelmassa, voit valita **Muokkaa** ja tarkistaa sivun ennen kuin avaat sen sivueditorissa. Näin voit kuitata ulos useita sivuja samalla kertaa.

Kun sivu on avattu sivueditorissa, sinun on varmistettava, että se on kuitattu ulos sinulle. Muokkaustyökalun komentopalkki on dynaaminen sekä tilanne- ja tilakohtainen. Tämän vuoksi siinä näkyvät vain toiminnot, jotka voidaan määrittää sivulla tällä hetkellä. Jos sivua ei esimerkiksi ole kuitattu ulos sinulle, **Tallenna**- ja **Lopeta muokkaus** -painikkeet eivät näy komentopalkissa. Sivun tila näkyy myös ikkunan oikealla puolella.

Jos sivua ei ole vielä kuitattu ulos sinulle, valitse **Muokkaa** komentopalkissa. Komentopalkki muuttuu sivun uuden tilan mukaiseksi. Saat myös ilmoituksen, jossa kerrotaan, että sivu on kuitattu ulos sinulle.

Seuraava vaihe on todellisten muutosten tekeminen. Sivun vasemmalla puolella olevaa jäsennyspuuta käytetään usein muutettavan moduulin etsimisessä ja valitsemisessa. Tämän jälkeen muutokset tehdään oikealla olevassa ominaisuusruudussa. 

Muutos voi kuitenkin joskus vaatia mallien tai osien lisäämisen tai poistamisen. Voit lisätä osan tai moduulin sivun jäsennyspuun avulla. Etsi paikka, johon moduuli tai osa lisätään, ja valitse sitten kyseisen paikan kolmen pisteen painike (**...**). Näyttöön tulee valikko, joka sisältää moduulin tai osan lisäämisessä käytettävät komennot. Voit poistaa moduulin tai osan etsimällä sen sivun jäsennyspuusta ja valitsemalla sen. Valitse kolmen pisteen painike ja valitse sitten moduulin tai osan poistamisen komento.

> [!TIP]
> Voit myös tarkastella minkä tahansa sellaisen moduulin ominaisuuksia, joka näkyy visuaalisessa sivunmuodostimen esikatselussa, ja muokata niitä. Tällöin voit valita moduulin suoraan.

Kun muutokset on tehty ja niiden vaikutusta esikatseltu, kuittaa sivu sisään valitsemalla **Lopeta muokkaus** komentopalkissa. 

Voit julkaista tekemäsi muutokset heti valitsemalla **Julkaise** komentopalkissa. Sivun viimeisin sisäänkuitattu versio, jota muokkasit, on julkaistu. Se on sivustoa tarkastelevien ulkoisten käyttäjien käytettävissä. 

## <a name="example-change-the-video-on-the-home-page"></a>Esimerkki: Aloitussivun videon muuttaminen

Seuraavassa esimerkissä näytetään, miten aloitussivua muokataan muuttamalla videota, joka näkyy videotoistinmoduulissa.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.
1. Etsi ja valitse aloitussivu, joka avataan sivueditorissa.
1. Valitse komentopalkissa **Muokkaa**.
1. Valitse sivun jäsennyksessä **pääpaikka**.
1. Laajenna kaikki nestesäilömoduulit **pääpaikassa**.
1. Etsi ja valitse videotoistinmoduuli.
1. Valitse oikealla olevassa ominaisuusruudussa **Video**-ominaisuus. Resurssin valitsin tulee näkyviin.
1. Valitse resurssin valitsimessa käytettävissä oleva videoresurssi tai valitse **Lataa uusi resurssi**, jos haluat ladata uuden videoresurssin.
1. Valitse **OK**.
1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Syötä **Kommentit**-kenttään **Videota muutettiin** ja valitse **OK**.
1. Esikatsele päivitettyä sivua valitsemalla **Esikatsele**. Kun olet valmis, palaa muokkaustyökaluun sulkemalla Esikatselu-välilehti.
1. Valitse **Julkaise**.

## <a name="additional-resources"></a>Lisäresurssit

[Uuden sivuston sivun lisääminen](add-new-page.md)

[Sivun asettelujen valitseminen](select-page-layouts.md)

[SEO-metatietojen hallinta](manage-seo-metadata.md)

[Sivun tallentaminen, esikatseleminen ja julkaiseminen](save-preview-publish-page.md)

[Tuotesivun täydentäminen](enrich-product-page.md)

[Luokan saapumissivun täydentäminen](enrich-category-page.md)

[Sivun sisällön helppokäyttöisyyden tarkistaminen](verify-accessibility.md)

[Dynaamisten verkkokauppasivujen luominen URL-parametrien perusteella](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
