---
title: Sivumallisanasto
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commerce -sivuston sivuilla käytettävistä useista elementeistä.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
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
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5c772a19958ebf0687d09af4c3055c733d99d750
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412066"
---
# <a name="page-model-glossary"></a>Sivumallisanasto


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commerce -sivuston sivuilla käytettävistä useista elementeistä.

## <a name="page-element-definitions"></a>Sivuelementin määritykset

Seuraavassa taulukossa on yhteenveto termeistä, jotka sinun tulisi tuntea, kun muutat sivuston ulkoasua, ulkoasua ja sisältöä. Tarkempia selityksiä ja ohjeita saat seuraamalla linkkejä.

| Kausi | Kuvaus ja muistiinpanot |
|------|-----------------------|
| [Moduuli](work-with-modules.md) | <p>**Määritelmä:** Moduulit ovat rakenneosa, jota voi muokata ja jonka avulla voidaan muodostaa verkkosivun rakenne. Esimerkkejä ovat ylätunniste-, hero- ja karusellimoduulit.</p><p>**Valittu:** Käytössä olevat moduulit voi valita ja niitä voi määrittää useissa sivuston muokkaustyönkulun vaiheissa. Näitä ovat esimerkiksi mallin, asettelun, sivun ja osan muokkauksen vaiheet.</p><p>**Muokattu:** Mukautetut moduulit luodaan koodissa SDK:n avulla Tämän jälkeen ne ladataan sivustoon, jossa ne ovat valittavana.</p> |
| Moduulin ominaisuus | <p>**Määritys:** Moduulin ominaisuudet ovat erityisiä moduulia varten määritettyjä asetuksia. Niitä voi muokata sähköisen kaupankäynnin muokkaustyökaluissa. Moduulin ominaisuuksia käytetään esimerkiksi ilmoituspalkkimoduulin ylätunnisteen ja taustaukuvan määrityksessä.</p><p>**Määritetty** : Moduulin ominaisuudet valitaan ja määritetään ominaisuusruudussa, joka näkyy mallien, asettelujen, sivujen, osien ja sovelluksen asetusten muokkausympäristöissä (editoreissa).</p> |
| [Sapluuna](templates-layouts-overview.md) | <p>**Määritys:** Mallit määrittävät moduuliyhdistelmät ja -asetukset, joita käytetään sivujen luokassa (esimerkiksi markkinointi-, luokka- ja tuotesivut).</p><p>**Valittu:** Malleja voi valita sivun tai asettelun luomistyönkulkujen aikana.</p><p>**Muokattu:** Malleja muokataan mallieditorissa. Niiden luominen ja muokkaaminen ei vaadi koodin muokkaamista.</p> |
| [Asettelu](templates-layouts-overview.md) | <p>**Määritys:** Asettelut määrittävät moduulien lopullisen valinnan ja järjestyksen päämallin asetusjoukosta. Asettelu voidaan määrittää yhdelle sivulle (*mukautettu asettelu)* tai se voidaan jakaa useilla sivuilla (*esimääritetty asettelu*).</p><p>**Valittuna:** Asettelut voidaan valita uuden sivun luomisen yhteydessä tai kun eri asettelu on pakollinen olemassa olevassa sivussa.</p><p>**Muokattu:** Asetteluja muokataan asettelueditorissa. Niiden luominen ja muokkaaminen ei vaadi koodin muokkaamista.</p> |
| [Sivuesiintymä](modify-existing-page.md) | <p>**Määritelmä:** Sivuesiintymät määrittävät yhdelle sivulle lopullisen, sivukohtaisen lokalisoidun sisällön. Tämä sisältö johdetaan moduulin ominaisuuksien arvoista.</p><p>**Valittuna:** Sivut valitaan, kun URL-osoitteet on määritetty.</p><p>**Muokattu:** Sivuja muokataan sivueditorissa. Niiden luominen ja muokkaaminen ei vaadi koodin muokkaamista.</p> |
| [Teema](select-site-theme.md) | <p>**Määritelmä:** Teemat määrittävät CSS-tyylisivun (CSS). Ne määrittävät sivulla hahmonnettavien moduulien ulkoasun.</p><p>**Valittuna:** Kun teema on ladattu sivustoon Microsoft Dynamics Lifecycle Services (LCS) -palvelun avulla, se voidaan valita sivun säilömoduulin ominaisuudeksi.</p><p>**Muokattu:** Teemoja luodaan ja muokataan SDK:n avulla. Ne ladataan sivustoon LCS:n avulla.</p> |
| [Osa](work-with-fragments.md) | <p>**Määritelmä:** Osat ovat täysin määritettyjä moduuleja, joissa on lokalisoitu sisältö. Sitä voidaan käyttää uudelleen ja päivittää keskitetysti useilla sivuilla. Esimerkiksi osaa, joka on luotu ylätunnistemoduulista, voidaan käyttää kaikissa malleissa ja kaikilla sivuilla sivustossa. Se voidaan päivittää keskitetysti yhdessä paikassa.</p><p>**Valittuna:** Osat voidaan valita aina, kun moduulit valitaan. Moduuli voi korvata ne. Näin voidaan tehostaa uudelleenkäytettävyyttä ja keskittämistä muokkauksessa.</p><p>**Muokattu:** Osia muokataan osaeditorissa. Niiden luominen ja muokkaaminen ei vaadi koodin muokkaamista.</p> |
| [URL-osoite](create-page-URL.md) | <p>**Määritelmä:** URL-osoitteet (Uniform resource locator) ovat osoitteita, jotka viittaavat verkkosivuihin tai muihin URL-osoitteisiin.</p><p>**Valittuna:** URL-osoitteet valitaan, jos sivujen väliset linkit ovat pakollisia.</p><p>**Muokattu:** URL-sivuja muokataan URL-osoite-editorissa. Niiden luominen ja muokkaaminen ei vaadi koodin muokkaamista.</p> |
| Resurssi | <p>**Määritelmä:** Resurssit ovat tiedostojen binaaritietoja, joilla on esimerkiksi seuraava pääte: .jpg, .docx, .pdf tai .mpg.</p><p>**Valittuna:** Resurssit valitaan moduulin ominaisuuksina niitä vaativille moduuleille.</p><p>**Muokattu:** Resurssit ladataan ja liittyviä metatietoja muokataan resurssien hallintaohjelmassa.</p> |

## <a name="additional-resources"></a>Lisäresurssit

[Tapoja lisästä sisältöä](add-manage-content.md)

[Asiakirjan tilat ja elinkaari](document-states-overview.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)

[Kanavienvälisen jakamisen käyttöönottaminen ja käyttäminen](cross-channel-sharing.md)

[Moduulien käyttäminen](work-with-modules.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Sivuston selauksen mukauttaminen](customize-site-navigation.md)
