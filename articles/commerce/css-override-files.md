---
title: Työskentely CSS-korvaustiedostojen kanssa
description: Tässä ohjeaiheessa kerrotaan, miksi, milloin ja miten CSS-tyylisivuja (CSS) käytetään ohittamaan tiedostot Microsoft Dynamics 365 Commercessa.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: f4a64735a1259f05de95aa6e129e4b12cbf5f197
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972954"
---
# <a name="work-with-css-override-files"></a>Työskentely CSS-korvaustiedostojen kanssa


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miksi, milloin ja miten CSS-tyylisivuja (CSS) käytetään ohittamaan tiedostot Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskatsaus

Pysyviä sivustotyylejä tulisi yleensä käsitellä sivuston teemalla. Teemat sisältävät perus-CSS- ja tyyliasetuksia mille tahansa sivustosi sivulla oleville moduuleille. Teemat luodaan käyttämällä Dynamics 365 Commerce online Software Development Kit (SDK) -pakettia, ja ne otetaan käyttöön sivustoillesi Microsoft Dynamics Lifecycle Servicesin (LCS) kautta. SDK-ohjesivuston kehittäjien teeman virheenkorjausominaisuudet ja moduuliliittymän määritykset luovat mukautettavia ja yhtenäisiä sivustonsuunnittelupaketteja. Kun nämä suunnittelupaketit otetaan käyttöön sivustossa, sivuston tekijät voivat keskittyä sisällön luomiseen, muokkaamiseen ja julkaisemiseen sivuston kehittämisen sijasta.

Teeman tavanomaisen elinkaaren vuoksi riippuvuus kehittäjistä tekee tyylimuutoksia SDK:n ja LCS-käyttöönottoputken kautta voi joissakin tilanteissa olla esteenä. Sivuston prototyypit tai hotfix-korjaukset voivat tuntua hankalilta, jos SDK:ta ei ole määritetty tai jos sinulla ei ole aikaa odottaa LCS-käyttöönottoa.

Näissä tilanteissa tiedostojen CSS-korvaaminen voi auttaa. Todennetut käyttäjät voivat ladata CSS-tiedoston Commercen julkaisutyökalujen avulla, esikatsella sitä ja aktivoida sen ja ohittaa sivuston teeman. SDK- tai LCS-käyttöönoton yleiskustannuksia ei tarvita. CSS-ohitustiedostossa määritetyt ohitukset voivat olla yhtä pieniä kuin yksittäisen tekstityylin muutos tai laaja-alainen koko tuotemerkin tarkistaminen.

Ennen kuin käytät CSS:n ohitustiedostoja, huomaa seuraavat rajoitukset:

- Vain yksi CSS-ohitustiedosto voi olla aktiivisena sivustossa kerrallaan. Siksi kaikkien aktiivisten ohitusten on oltava yhdessä ohitustiedostossa.
- Vaikka voit esikatsella ohituksia Commerce julkaisutyökaluissa, siinä ei ole erityisiä virheenkorjausominaisuuksia, jotka auttavat tunnistamaan mahdolliset virheet, joita ohittaa. Toisin sanoen, kun käytät CSS:n ohitustiedostoja, sinulla ei ole samaa työkalujoukkoa, jonka SDK tarjoaa moduulin ja sisällönluonnin validointiin.

CSS-ohitustiedostot ovat kuitenkin nopea tapa suunnitella mallin prototyyppi tai toteuttaa hotfix-korjaus, ennen kuin täydellinen teemapäivitys on kehitetty ja otettu käyttöön.

## <a name="create-a-css-override-file"></a>Luo CSS-ohitustiedosto

Voit luoda CSS-ohitustiedoston käyttämällä mitä tahansa integroitua kehitysympäristöä (IDE), tekstieditoria tai lähdekoodieditoria. Tyypillinen lähestymistapa on käyttää tavallisia verkkovirheenkorjaajia selaimessasi tunnistamaan tyylin valitsimet, ominaisuudet ja arvot nykyisessä sivustossa. Useimpien selainten avulla voit muuttaa arvoja ja esikatsella niitä virheenkorjaajassa. Kun olet määrittänyt muutokset, jotka haluat tehdä, voit tallentaa ne omaan CSS-tiedostoosi.

## <a name="upload-a-css-override-file"></a>Lataa CSS-ohitustiedosto

Jos haluat ladata CSS-tiedoston sivustoon Commerce-sivustossa, toimi seuraavasti.

1. Siirry muokkaustyökaluissa sivustoon.
1. Valitse vasemmanpuoleisessa siirtymisruudussa **Rakenne**.

    > [!NOTE]
    > Voit joutua laajentamaan siirtymisruudun **asetukset**, ennen kuin voit valita **Rakenne** käyttämäsi Commercen julkaisutyökalujen mukaan.

1. Valitse päärakenneruudun yläosassa **CSS-ohitus**-välilehti, jos se ei ole jo valittuna.
1. Valitse **Käytettävissä olevat CSS-ohitukset** -kohdasta **Lataa CSS-tiedosto**. Näyttöön tulee Resurssienhallinta-ikkuna.
1. Selaa Resurssienhallintaa ja valitse CSS-tiedosto ja valitse sitten **Avaa**. Ladattu CSS-tiedosto näkyy nyt **Käytettävissä olevat CSS-ohitukset** -kohdassa.

## <a name="preview-a-css-override-file"></a>CSS-ohitustiedoston esikatseleminen

Voit esikatsella CSS-ohitustiedostoa, ennen kuin teet sen aktiiviseksi sivustoosi, toimimalla seuraavasti.

1. Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jota haluat esikatsella.
1. Valitse CSS-tiedoston nimen vierestä **Esikatsele sivusto**.
1. Valitse **Valitse URL-osoite** -valintaikkunasta sen sivuston URL-osoite, jonka ohituksen haluat nähdä, ja valitse sitten **OK**.
1. Jos valitulle URL-osoitteella on useita variantteja, valitse haluamasi variantti näkyviin tulevasta **Esikatseluvariaatiot**-valintaikkunasta.

Uusi selainvälilehti tai -ikkuna avautuu, jossa voit tarkistaa tyyliisi ohitukset sivustoosi nähden. Voit sitten jakaa URL-osoitteen muiden todennettujen Commerce-käyttäjien kanssa tarkistusta ja palautetta varten.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Aktivoi CSS-ohitustiedosto live-sivustossasi

Kun olet esikatselut ja hyväksynyt CSS-ohitustiedoston, voit aktivoida sen live-sivustossa.

> [!NOTE]
> Vain yksi CSS-ohitustiedosto voi olla aktiivisena kerrallaan sivustossasi. Jos aktivoit uuden ohitustiedoston, aiempi ohitustiedosto poistetaan käytöstä. Varmista siksi, että kaikki pakolliset ohitukset ovat yksittäisessä CSS-ohitustiedostossa.

Voit aktivoida CSS-ohitusasiakirjan seuraavien vaiheiden avulla.

1. Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jonka haluat aktivoida.
1. Valitse CSS-tiedoston nimi -kohdasta **Aktivoi**. Ohitustiedosto aktivoituu välittömästi live-sivustossa.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Poista CSS-ohitustiedosto käytöstä live-sivustossasi

Voit poistaa CSS-ohitustiedoston käytöstä sivustossa seuraavasti.

1. Valitse vasemmalla olevasta siirtymisruudusta **Rakenne** ja etsi sitten **CSS-ohitus**-välilehdellä **Käytettävissä olevat CSS-ohitukset** -kohdasta CSS-tiedosto, jonka haluat poistaa käytöstä.
1. Valitse CSS-tiedoston nimi -kohdasta **Poista aktivointi**. Ohitustiedosto muuttuu passiiviseksi välittömästi live-sivustossa.

> [!TIP]
> Jos haluat käyttää lisäasetuksia CSS-ohitustiedostot-vaihtoehdolle, valitse kolme pistettä (**...**) CSS-tiedostonimen vieressä. **Lataa**-, **Nimeä uudelleen**, ja **Korvaa**-vaihtoehdoista on hyötyä aiemmin luodun CSS-ohitustiedoston nopeille muutoksille.

## <a name="additional-resources"></a>Lisäresurssit

[Logon lisääminen](add-logo.md)

[Sivuston teeman valitseminen](select-site-theme.md)

[Tyylien esimääritysten käyttäminen](style-presets.md)

[Favicon-kuvakkeen lisääminen](add-favicon.md)

[Tervetuloviestin lisääminen](add-welcome-message.md)

[Copyright-ilmoituksen lisääminen](add-copyright-notice.md)

[Kielten lisääminen sivustoon](add-languages-to-site.md)

[Komentosarjakoodin lisääminen sivuston sivuihin telemetrian tukemiseksi](add-telemetry.md)
