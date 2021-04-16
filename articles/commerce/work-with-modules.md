---
title: Moduulien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6d872719d3b1aa27ccfdcf36d7739c883e7b4996
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801358"
---
# <a name="work-with-modules"></a>Moduulien käyttäminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.

Moduulit ovat loogisia rakenneosia, jotka muodostavat sivurakenteen. Niillä on eri tarkoitukset ja käyttöalueet. Jotkin moduulit ovat korkean tason säilöjä, joiden ainoa tarkoitus on säilyttää ja järjestää muita moduuleja (alimoduuleja). Muilla moduuleilla, kuten yksinkertaisella kuvansijoittelumoduulilla, on tarkkaan määritetty tarkoitus. Muut moduulit, kuten karusellimoduuli, ovat näiden kahden luokan välissä.

Dynamics 365 Commerce -sivusto sisältää oletusarvoisesti moduulikirjaston. Sen avulla voit arkistoida useimmat sähköisen kaupankäynnin perusskenaariot. Voit muodostaa kattavan sähköisen kaupankäynnin sivuston pelkästään näiden moduulien avulla. Saatat kuitenkin haluta mukauttaa näitä moduuleja tai luoda uusia mukautettuja moduuleja erityistarpeita varten. Voit käyttää mukautettujen moduulien luomisessa moduulin suunnittelun SDK:ta. Sen avulla voit luoda mukautetun moduulikirjaston.

## <a name="container-modules-and-slots"></a>Konttimoduulit ja -paikat

Kuten aiemmin mainittiin, jotkin moduulit on suunniteltu alimoduulien säilytystä varten. Näitä moduuleja kutsutaan *säilöiksi*. Ne mahdollistavat sisäkkäisten moduulien hierarkian muodostamisen. Konttimoduuleissa on *paikkoja*. Paikkojen avulla käsitellään säilön alimoduulien asettelua ja tarkoitusta. Seuraavassa on esimerkki perussivun säilömoduulista (ylimmän tason moduulista millä tahansa sivulla), joka määrittää useita tärkeitä paikkoja:

- Ylätunnistepaikka
- Aliylätunnistepaikka
- Pääpaikka
- Alatunnistepaikka
- Alialatunnistepaikka

Moduulin kehittäjä määrittää nämä paikat. Hän määrittää myös, mitkä alimoduulit ja miten monta alimoduulia voidaan laittaa suoraan paikan sisään. Esimerkiksi ylätunnistepaikka voi tukea vain yhtä **ylätunnistemoduuli**-tyyppiä, kun taas tekstiosapaikka voi tukea rajoittamatonta määrää moduulityyppejä (ei kutienkaan muita sivun säilömoduuleja).

Sivun tekijöiden ei tarvitse tietää etukäteen muokkaustyökaluissa, mitkä moduulit voi asettaa kuhunkin paikkaan. Kun sivun tekijät valitsevat paikan ja yrittävät sitten valita siihen lisättävän moduulin, he näkevät suodatetun näkymän moduulityypeistä, joita kyseinen paikka tukee.

## <a name="content-modules"></a>Sisältömoduulit

Sisältömoduulit sisältävät sisältö- ja mediaelementtejä, kuten tekstiä (esimerkiksi otsikoita, kappaleita ja linkkejä) tai resurssiviitteitä (esimerkiksi kuvia, videota ja PDF-tiedostoja). Tyypillisiä sisältömoduulin tyyppejä ovat sisältölohko-, tekstilohko- ja kampanjabannerimoduulit. Nämä kolme moduulityyppiä voivat sisältää tekstiä tai mediaa. Ne eivät tarvitse alimoduuleja voidakseen näyttää sivulla asioita.

Suurin osa yleisistä päivittäisistä sivun- ja sisällöntuottamisaktiviteeteista liittyy sisältömoduuleihin. Tämä pääasiassa sen vuoksi, että nämä moduulit määrittävät pääsäilömoduuleissa hahmonnetun todellisen sisällön. Käytettävissä on useita sisältömoduuleja. Nämä moduulit ovat yleensä viimeisiä sisäkkäisten moduulien sivuhierarkiaan lisättäviä osia.

Seuraavassa kuvassa näkyy, kuinka moduulit ovat sisäkkäin pääsäilömoduulin paikoissa.

![Sisäkkäiset moduulit](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moduulien lisääminen tai poistaminen

Seuraavissa ohjeissa kuvataan, miten moduuleja lisätään ja poistetaan.

### <a name="add-a-module"></a>Moduulin lisääminen

Voit lisätä sivun moduulin paikkaan tai säilöön seuraavasti.

1. Valitse vasemmalla olevasta jäsennysruudusta tai suoraan pääalustalla säilö tai paikka, johon alimoduuli voidaan lisätä.

    > [!NOTE]
    > Moduulin suunnittelija määrittää moduulityyppien luettelon, joka voidaan lisätä tiettyyn moduulipaikkaan. Mallien tekijät voivat tämän jälkeen tarkentaa sallittuja moduulivaihtoehtoja. Tämän avulla varmistetaan yhdenmukainen hakukoneoptimointi ja luotitehokkuus kaikilla sivuilla, jotka on luotu tietyn mallin avulla. Kun moduulia lisätään paikkaan, **Lisää moduuli** -valintaikkuna suodatetaan automaattisesti siten, että siinä näkyvät vain ne moduulit, joita valittu säilö tai paikka tukee. Tämä sallittujen moduulien luettelo määräytyy sivun mallin tai säilömoduulin määrityksen mukaan.

1. Jos käytössä on jäsennysruutu, valitse kolme pistettä (**...**) moduulin nimen vierestä ja valitse sitten **Lisää moduuli**. Jos käytät ohjausobjekteja suoraan alustassa, valitse plusmerkki (**+**) tyhjässä paikassa tai parhaillaan valittuna olevan moduulin vieressä. Valitse sitten **Lisää moduuli**.

    > [!NOTE]
    > Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää moduuli** -vaihtoehto ei ole käytettävissä.

1. Valitse **Lisää moduuli** -valintaikkunassa sivulle lisättävä moduuli.

    > [!TIP]
    > Aloittelijan kannattaa käyttää **Sisältölohko**-moduulityyppiä.

1. Valitse **OK**, jos haluat lisätä valitun moduulin sivun valittuun säilöön tai paikkaan.

### <a name="remove-a-module"></a>Moduulin poistaminen

Voit poistaa sivun moduulin paikasta tai säilöstä seuraavasti.

1. Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan moduulin nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten roskakorisymboli. Vaihtoehtoisesti voit valita pääalustalle valitun moduulin työkalurivin roskakorisymbolin.
1. Kun sinua pyydetään vahvistamaan moduulin poistaminen, valitse **OK**.

## <a name="move-a-module-to-a-new-position"></a>Moduulin siirtäminen uuteen kohtaan

Voit siirtää moduulin uuteen kohtaan sivulla jollakin seuraavista tavoista.

### <a name="move-a-module-using-the-outline-pane"></a>Moduulin siirtäminen jäsennysruudun avulla

Voit siirtää moduulin jäsennysruudun avulla noudattamalla seuraavia ohjeita.

1. Valitse ja pidä painettuna siirrettävää moduulia jäsennysruudussa. Vedä sitten moduuli uuteen kohtaan jäsennyksessä. Jäsennyksen ja alustan sininen viiva ilmaisee, mihin moduuli voidaan sijoittaa.
1. Vapauta moduuli ja pudota se uuteen kohtaan.

### <a name="move-a-module-directly-within-the-canvas"></a>Moduulin siirtäminen suoraan alustaan

Voit siirtää moduulin suoraan alustassa noudattamalla seuraavia ohjeita.

1. Valitse alustassa siirrettävä moduuli. 
1. Valitse joko ylös- tai alaspäin osoittava nuolisymboli moduulin työkalurivillä. Vedä nuolta uuteen kohtaan sivulla. Jäsennyksen ja kaavan sininen viiva ilmaisee, mihin moduuli voidaan sijoittaa. Jos moduulia ei voi siirtää ylös tai alas, nuolisymboli näkyy harmaana. 
1. Vapauta moduuli ja pudota se uuteen kohtaan.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Moduulin siirtäminen kolmen pisteen valikon avulla

Voit siirtää moduulin kolmen pisteen valikon avulla noudattamalla seuraavia ohjeita.

1. Valitse moduuli jäsennyksestä tai alustasta.
1. Valitse kolme pistettä (**...**) moduulin nimen vierestä jäsennysruudusta tai moduulin työkaluriviltä.
1. Jos moduulia voi siirtää ylös ja alas säilössä tai paikassa, näkyvissä ovat **Siirrä ylös**- tai **Siirrä alas** -vaihtoehdot. Valitse haluttu siirtovaihtoehto, kun haluat siirtää moduulia ylös tai alas suhteessa sen sisaruksiin.

## <a name="configure-modules"></a>Moduulien määrittäminen

Seuraavissa ohjeissa kuvataan, miten sisältö ja säilömoduulit määritetään.

### <a name="configure-a-content-module"></a>Sisältömoduulin määrittäminen

Voit määrittää sivun sisältömoduulin seuraavasti.

1. Laajenna puuta vasemmalla olevassa jäsennysruudussa ja valitse mikä tahansa sisältömoduuli (esimerkiksi **Sisältölohko**). Vaihtoehtoisesti voit valita moduulin pääalustassa.
1. Anna haluttujen moduulin ohjausobjektien ominaisuudet oikealla olevaan moduulin ominaisuuksien ruutuun.
1. Valitse **Tallenna** komentopalkissa. Tämä päivittää myös esikatselualustan.

### <a name="edit-module-text-properties"></a>Moduulin tekstiominaisuuksien muokkaaminen

Moduulin tekstiominaisuuksia, jotka eivät ole vain luku -tilassa, voi muokata suoraan alustassa.

Voit muokata moduulin tekstiominaisuuksia noudattamalla seuraavia ohjeita.

1. Valitse alustan tekstin ohjausobjekti ja sijoita kohdistin kohtaan, jossa haluat muokata tekstiä.
1. Anna tekstisisältö.
1. Jatka muiden sisältöjen muokkaamista valitsemalla kohta tekstisisällön ulkopuolelta.

### <a name="inline-image-selection"></a>Sisäisen kuvan valitseminen

Moduulin kuvia, jotka eivät ole vain luku -tilassa, voi muuttaa suoraan alustassa.

Voit valita sisältömoduulin uuden kuvan seuraavasti.

1. Kaksoisnapsauta kuvaa alustassa. Näkyviin tulee mediavalitsimen ikkuna.
1. Etsi ja valitse uusi kuva, jota haluat käyttää, ja valitse sitten **OK**. Uusi kuva hahmonnetaan nyt alustassa.

### <a name="configure-a-container-module"></a>Konttimoduulin määrittäminen

Voit määrittää sivun säilömoduulin seuraavasti.

1. Valitse sivulla oleva säilömoduuli (esimerkiksi karuselli- tai nestesäilömoduuli).
1. Laajenna oikeanpuoleisessa ominaisuusruudussa sisäkkäiset ohjausobjektit valitsemalla ylätunnisteet ja määrittämällä vaaditut ohjausobjektin arvot.
1. Valitse vasemmanpuoleisessa jäsennysruudussa säilön tai jonkin sen sisällä olevan paikan nimen vieressä oleva kolmen pisteen painike ja valitse sitten **Lisää moduuliin**. Lisää sitten alimoduulit valittuun säilöön. Lisätietoja on tämän ohjeaiheen edellä olevassa osassa [Moduulin kanssa työskenteleminen](#add-a-module).
1. Jos pääsäilössä on useita alimoduuleja sisaruksina, voit muuttaa niiden näyttöjärjestystä pääsäilössä. Valitse moduulin kolmen pisteen painike ja käytä sitten ylä- ja alanuolipainikkeita.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Mallien käyttö](work-with-templates.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Konttimoduulin lisääminen sivulle](add-container-module.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
