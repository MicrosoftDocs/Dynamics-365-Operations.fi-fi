---
title: Työtuntien hallinta
description: Tässä artikkelissa kerrotaan työtuntien hallinnasta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f5f5dbb23c4d6c86bee7612c4ade65ef4b1cee8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869746"
---
# <a name="work-hour-control"></a>Työtuntien hallinta

[!include [banner](../../includes/banner.md)]

 

Käyttöomaisuuden hallinnassa voit laskea tunteja, jolloin saat yleiskuvan todellisista tunneista resurssien, toiminnallisten sijaintien tai työtilausten budjettitunteihin verrattuna. Todelliset tunnit perustuvat kirjattuihin tapahtumiin.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Käyttöomaisuuksien, toiminnallisten sijaintien ja työtilausten työtuntien hallinta

Käyttöomaisuudelle, toiminnallisille sijainneille ja työtilauksille tehdyt laskelmat ovat lähes identtiset. Ainoa ero on se, että käyttöomaisuudelle ja toimipaikoille voidaan sisällyttää myös aliresursseja ja alisijainteja laskennassa. Päivämäärä on tapahtumapäivämäärä, jolloin rekisteröinti tallennettiin.

1. Valitse **Resurssien hallinta** > **Kyselyt** > **Resurssit** > **Resurssituntien hallinta** tai **Toiminnallisen sijainnin tuntien hallinta** tai **Resurssien hallinta** > **Kyselyt** > **Työtilaukset** > **Työtilauksen tuntien hallinta**.

2. **Resurssituntien hallinta** -valintaikkunassa:

3. Valitse **Resurssituntien hallinta** / **Toiminnallisen sijainnin tuntien hallinta** / **Työtilauksen tuntien hallinta** -valintaikkunassa kausi, joka lasketaan **Päivämäärästä**- ja **Päivämäärään** -kenttien avulla.

4. Valitse tarvittaessa **Taloushallinnon dimensioyhdistelmä**, joka sisällytetään laskelmiin.

5. Valitse "kyllä" **Ohita nolla** -vaihtopainikkeessa, jos et halua näyttää tuloksia, joissa on nolla tuntia.

6. **Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia tuntien hallinnan riveistä haluat liittyen toiminnallisiin sijainteihin. 

    Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoineen toiminnallinen sijaintihierarkia, kaikki toimintosijainnin tuntien hallinnan rivit näkyvät ylimmällä tasolla, joten rivin tunnit voidaan lisätä hierarkiassa alemmista toiminnallisista sijainneista. 
    
    Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki tunetien hallinnan rivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.

7. Valitse "kyllä" **Sisällytä aliresurssit** -vaihtopainikkeessa, jos haluat näyttää aliresursseihin liittyvät kustannukset erillisinä riveinä.

8. Jos haluat rajata haun, voit valita tietyt käyttöomaisuudet / toiminnalliset siajinnit/ työtilaukset **Sisällytettävät tietueet** -pikavälilehdessä.

9. Aloita laskenta valitsemalla **OK**.

10. Napsauta **Resurssituntien hallinta** -sivulla **Ryhmittele**-painikkeita tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason. Valitut **Ryhmittely...**-painikkeet on korostettu. Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.

## <a name="example"></a>Esimerkki

Alla olevassa näyttökuvassa on esimerkki **Resurssituntien hallinta** -laskennasta.

- **Alkuperäinen budjetti** -kenttä sisältää työtilausennusteen budjetoidut tunnit. 
- **Todelliset tunnit** -kentässä näkyvät työtilausten kirjatut tunnit. 
- **Varatut tunnit** -kentässä näkyvät kokonaistunnit, joihin yritys on sitoutunut suhteessa työtilauksiin.

![Esimerkki resurssituntien hallinnan laskennasta.](media/04-controlling-and-reporting.png)

Toinen tapa määrittää tuntilaskennat on valita valita monta resurssia **Kaikki resurssit**- tai **Aktiiviset resurssit** -kohdassa. Napsauta sitten **Yleiset**-pikavälilehden **Tuntien hallinta** -painiketta. Valitut resurssit lisätään automaattisesti **Sisällytettävät tietueet** -pikavälilehden **Resurssi**-kenttään. Valitse **Resurssituntien hallinta** -valintaikkunassa **OK** ja näkyviin tulee valittujen käyttöomaisuuserien laskelma. Sama menettely voidaan tehdä toiminnallisille sijainneille kohdassa **Kaikki toiminnalliset sijainnit** tai **Aktiiviset toiminnalliset sijainnit** sekä kohdassa  **Kaikki työtilaukset** tai **Aktiiviset työtilaukset**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]