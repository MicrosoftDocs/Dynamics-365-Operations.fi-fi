---
title: Moduulien käyttäminen
description: Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025876"
---
# <a name="work-with-modules"></a>Moduulien käyttäminen

Tässä ohjeaiheessa kuvataan, miten ja milloin moduuleja käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.


[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yleiskatsaus

Moduulit ovat loogisia rakenneosia, jotka muodostavat sivurakenteen. Niillä on eri tarkoitukset ja käyttöalueet. Jotkin moduulit ovat korkean tason säilöjä, joiden ainoa tarkoitus on säilyttää ja järjestää muita moduuleja (alimoduuleja). Muilla moduuleilla, kuten yksinkertaisella kuvansijoittelumoduulilla, on tarkkaan määritetty tarkoitus. Muut moduulit, kuten karusellimoduuli, ovat näiden kahden luokan välissä.

Dynamics 365 Commerce -sivusto sisältää oletusarvoisesti aloituspakkausmoduulikirjaston. Sen avulla voit arkistoida useimmat sähköisen kaupankäynnin perusskenaariot. Voit muodostaa kattavan sähköisen kaupankäynnin sivuston pelkästään näiden moduulien avulla. Saatat kuitenkin haluta mukauttaa näitä moduuleja tai luoda uusia mukautettuja moduuleja erityistarpeita varten. Voit käyttää mukautettujen moduulien luomisessa moduulin suunnittelun SDK:ta. Sen avulla voit luoda mukautetun moduulikirjaston.

## <a name="container-modules-and-slots"></a>Konttimoduulit ja -paikat

Kuten aiemmin mainittiin, jotkin moduulit on suunniteltu alimoduulien säilytystä varten. Näitä moduuleja kutsutaan *säilöiksi*. Ne mahdollistavat sisäkkäisten moduulien hierarkian muodostamisen. Konttimoduuleissa on *paikkoja*. Paikkojen avulla käsitellään säilön alimoduulien asettelua ja tarkoitusta. Seuraavassa on esimerkki perussivun säilömoduulista (ylimmän tason moduulista millä tahansa sivulla), joka määrittää useita tärkeitä paikkoja:

- Ylätunnistepaikka
- Tekstiosapaikka
- Alatunnistepaikka

Moduulin kehittäjä määrittää nämä paikat. Hän määrittää myös, mitkä alimoduulit ja miten monta alimoduulia voidaan laittaa suoraan paikan sisään. Esimerkiksi ylätunnistepaikka voi tukea vain yhtä **ylätunnistemoduuli**-tyyppiä, kun taas tekstiosapaikka voi tukea rajoittamatonta määrää moduulityyppejä (ei kutienkaan muita sivun säilömoduuleja).

Sivun tekijöiden ei tarvitse tietää etukäteen muokkaustyökaluissa, mitkä moduulit voi asettaa kuhunkin paikkaan. Kun sivun tekijät valitsevat paikan ja yrittävät sitten valita siihen lisättävän moduulin, he näkevät suodatetun näkymän moduulityypeistä, joita kyseinen paikka tukee.

## <a name="content-modules"></a>Sisältömoduulit

Sisältömoduulit sisältävät sisältö- ja mediaelementtejä, kuten tekstiä (esimerkiksi otsikoita, kappaleita ja linkkejä) tai resurssiviitteitä (esimerkiksi kuvia, videota ja PDF-tiedostoja). Esimerkkejä yleisistä sisältömoduulityypeistä ovat **Hero**, **Ominaisuus** ja **Ilmoituspalkki**. Nämä kolme moduulityyppiä voivat sisältää tekstiä tai mediaa. Ne eivät tarvitse alimoduuleja voidakseen näyttää sivulla asioita.

Suurin osa yleisistä päivittäisistä sivun- ja sisällöntuottamisaktiviteeteista liittyy sisältömoduuleihin. Tämä pääasiassa sen vuoksi, että nämä moduulit määrittävät pääsäilömoduuleissa hahmonnetun todellisen sisällön. Käytettävissä on useita sisältömoduuleja. Nämä moduulit ovat yleensä viimeisiä sisäkkäisten moduulien sivuhierarkiaan lisättäviä osia.

Seuraavassa kuvassa näkyy, kuinka moduulit ovat sisäkkäin pääsäilömoduulin paikoissa.

![Sisäkkäiset moduulit](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Moduulien lisääminen tai poistaminen

Seuraavissa ohjeissa kuvataan, miten moduuleja lisätään ja poistetaan.

### <a name="add-a-module"></a>Moduulin lisääminen

Voit lisätä sivun moduulin paikkaan tai säilöön seuraavasti.

1. Valitse vasemmalla olevasta jäsennysruudusta säilö tai paikka, johon alimoduuli voidaan lisätä.

    > [!NOTE]
    > Moduulin suunnittelija määrittää moduulityyppien luettelon, joka voidaan lisätä tiettyyn moduulipaikkaan. Mallien tekijät voivat tämän jälkeen tarkentaa sallittuja moduulivaihtoehtoja. Tämän avulla varmistetaan yhdenmukainen hakukoneoptimointi ja luotitehokkuus kaikilla sivuilla, jotka on luotu tietyn mallin avulla.

1. Valitse moduulin kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**. **Lisää moduuli** -valintaikkuna tulee näkyviin. Tämä valintaikkuna suodatetaan automaattisesti siten, että siinä näkyvät vain ne moduulit, joita valittu säilö tai paikka tukee. Moduuliluettelo määräytyy sivun mallin tai säilömoduulin määrityksen mukaan.

    > [!NOTE]
    > Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää moduuli** -vaihtoehto ei ole käytettävissä.

1. Hae valintaikkunassa sivulle lisättävä moduuli ja valitse se.

    > [!TIP]
    > Aloittelijan kannattaa käsitellä ensin **Ominaisuus**- ja **Hero**-moduulityyppejä.

1. Valitse **OK**, jos haluat lisätä valitun moduulin sivun valittuun säilöön tai paikkaan.

### <a name="remove-a-module"></a>Moduulin poistaminen

Voit poistaa sivun moduulin paikasta tai säilöstä seuraavasti.

1. Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan moduulin nimen vieressä oleva kolmen pisteen painike ja valitse sitten roskakoripainike.
1. Kun sinua pyydetään vahvistamaan moduulin poistaminen, valitse **OK**.

## <a name="configure-modules"></a>Moduulien määrittäminen

Seuraavissa ohjeissa kuvataan, miten sisältö ja säilömoduulit määritetään.

### <a name="configure-a-content-module"></a>Sisältömoduulin määrittäminen

Voit määrittää sivun sisältömoduulin seuraavasti.

1. Laajenna puuta vasemmalla olevassa kehysikkunassa ja valitse mikä tahansa sisältömoduuli (esimerkiksi **Ominaisuus**, **Hero** tai **Ilmoituspalkki**).
1. Etsi oikealla olevasta ominaisuudet-ruudusta moduulin sisältö- ja asetukset-ohjausobjektit.
1. Määritä haluamasi moduuliohjausobjektien ominaisuudet.
1. Valitse **Tallenna** komentopalkin yläosassa. Tämä päivittää myös esikatselualustan.

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

