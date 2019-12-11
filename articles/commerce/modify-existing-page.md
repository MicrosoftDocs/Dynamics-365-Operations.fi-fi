---
title: Aiemmin luodun sivuston sivun muokkaaminen
description: Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ddbef381e9ded18ed1c9226057cac482d4c6e24d
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698369"
---
# <a name="modify-an-existing-site-page"></a>Aiemmin luodun sivuston sivun muokkaaminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten olemassa olevaa sivua muokataan Microsoft Dynamics 365 Commerce -sovelluksessa.

## <a name="overview"></a>Yleiskatsaus

Sivun muokkauksen ensimmäinen vaihe on sivun avaaminen sivueditorissa. Siirry sivustoon, joka sisältää sivun. Etsi haluamasi sivu sivuluettelosta. Jos et löydä sivua, voit käyttää muokkaustyökalun monipuolisia hakutoimintoja. Kirjoita sivun tarkka nimi tai sen ensimmäiset kirjaimet ja sen jälkeen tähti (\*). Näkyviin tulee suodatettu luettelo sivuista. Tämän luettelon avulla voit etsiä haluamasi sivun. Kun olet löytänyt oikean sivun, avaa sivu sivueditorissa valitsemalla sivun nimi.

> [!TIP]
> Jos sivusi näkyy sivun tarkistusohjelmassa, voit valita sen ja kuitata sen ulos, ennen kuin avaat sen sivueditorissa. Näin voit kuitata ulos useita sivuja samalla kertaa.

Kun sivu on avattu sivueditorissa, sinun on varmistettava, että se on kuitattu ulos sinulle. Muokkaustyökalun komentopalkki on dynaaminen sekä tilanne- ja tilakohtainen. Tämän vuoksi siinä näkyvät vain toiminnot, jotka voidaan määrittää sivulla tällä hetkellä. Jos sivua ei esimerkiksi ole kuitattu ulos sinulle, **Tallenna**- ja **Kuittaa sisään** -painikkeet eivät näy komentopalkissa. Sivun tila näkyy myös ikkunan oikealla puolella.

Jos sivua ei ole vielä kuitattu ulos sinulle, valitse **Kuittaa ulos** komentopalkissa. Komentopalkki muuttuu sivun uuden tilan mukaiseksi. Saat myös ilmoituksen, jossa kerrotaan, että sivu on kuitattu ulos sinulle.

Seuraava vaihe on todellisten muutosten tekeminen. Sivun vasemmalla puolella olevaa jäsennyspuuta käytetään usein muutettavan moduulin etsimisessä ja valitsemisessa. Tämän jälkeen muutokset tehdään oikealla olevassa ominaisuusruudussa. 

Muutos voi kuitenkin joskus vaatia mallien tai osien lisäämisen tai poistamisen. Voit lisätä osan tai moduulin sivun jäsennyspuun avulla. Etsi paikka, johon moduuli tai osa lisätään, ja valitse sitten kyseisen paikan kolmen pisteen painike (**...**). Näyttöön tulee valikko, joka sisältää moduulin tai osan lisäämisessä käytettävät komennot. Voit poistaa moduulin tai osan etsimällä sen sivun jäsennyspuusta ja valitsemalla sen. Valitse kolmen pisteen painike ja valitse sitten moduulin tai osan poistamisen komento.

> [!TIP]
> Voit myös tarkastella minkä tahansa sellaisen moduulin ominaisuuksia ja muokata niitä, joka näkyy WYSIWYG-esikatselussa. Tällöin voit valita moduulin suoraan.

Kun muutokset on tehty ja niiden vaikutusta esikatseltu, kuittaa sivu sisään valitsemalla **Kuittaa sisään** komentopalkissa. 

Voit julkaista tekemäsi muutokset heti valitsemalla **Julkaise** komentopalkissa. Sivun viimeisin sisäänkuitattu versio, jota muokkasit, on julkaistu. Se on sivustoa tarkastelevien ulkoisten käyttäjien käytettävissä. 

## <a name="example-change-the-video-on-the-home-page"></a>Esimerkki: Aloitussivun videon muuttaminen

Seuraavassa esimerkissä näytetään, miten aloitussivua muokataan muuttamalla videota, joka näkyy videotoistinmoduulissa.

1. Valitse **Sivustot**-kohdassa **Fabrikam** (tai sivuston nimi).
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Sivut**.
1. Etsi ja valitse aloitussivu, joka avataan sivueditorissa.
1. Valitse komentopalkissa **Kuittaa ulos**.
1. Valitse sivun jäsennyksessä **pääpaikka**.
1. Laajenna kaikki nestesäilömoduulit **pääpaikassa**.
1. Etsi ja valitse videotoistinmoduuli.
1. Valitse oikealla olevassa ominaisuusruudussa **Video**-ominaisuus. Resurssin valitsin tulee näkyviin.
1. Valitse resurssin valitsimessa käytettävissä oleva videoresurssi tai valitse **Lataa uusi resurssi**, jos haluat ladata uuden videoresurssin.
1. Valitse **OK**.
1. Valitse ensin **Tallenna** ja sitten **Kirjaa sisään**.
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
