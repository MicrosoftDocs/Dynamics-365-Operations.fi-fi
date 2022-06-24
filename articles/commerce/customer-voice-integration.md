---
title: Customer Voicen integroiminen sähköisen kaupankäynnin sivustoihin
description: Tässä artikkelissa kuvataan, kuinka integroidaan Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce -verkkokauppasivuston sivuihin..
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850327"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voicen integroiminen sähköisen kaupankäynnin sivustoihin

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka integroidaan Microsoft Dynamics 365 Customer Voice Dynamics 365 Commerce -verkkokauppasivuston sivuihin..

Voit integroida [Customer Voicen](https://dynamics.microsoft.com/customer-voice/overview/) osaksi sähköistä sivustoa kerätäksesi, analysoidaksesi ja seurataksesi reaaliaikaista asiakaspalautetta. Integroinnin aloittaminen edellyttää, että luot tilin ja valitset Customer Voice -projektimallin kerättävälle palautetyypille.

## <a name="integrate-the-customer-voice-service"></a>Customer Voice -palvelun integroiminen

Jos haluat luoda Customer Voice -tilin, siirry [Customer Voiceen](https://dynamics.microsoft.com/customer-voice/overview/) ja noudata kehotteita.

Kun olet luonut tilin ja kirjaudut sisään, seuraava vaihe on valita Customer Voice -projektimalli kerättävälle palautetyypille.

Voit valita Customer Voice -projektimallin noudattamalla seuraavia vaiheita.

1. Siirry [Customer Voice -projektimallisivulle](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Valitse **Aloitus**.
1. Valitse kerättävälle palautetyypille projektimalli ja valitse sitten **Seuraava**.
1. Valitse upotettu muoto **Lähetä**-välilehden **Valitse upotusmuoto** -kohdasta. **Upotettu koodi** -kentässä näkyy koodi, joka on upotettava Commerce-sivustonmuodostimeen.

Tämän artikkelin esimerkeissä käytetään **Kausittainen asiakaskysely** - projektimallia ja **Painike**-upotusmuotoa.

Seuraavassa esimerkissä havainnollistetaan **Kausittainen asiakaskysely** -projektimallin sivu,jossa **Painike**-upotusmuodon asetus on valittuna ja asetuksen upotuskoodi näkyy **Upotettu koodi** -kentässä. Sivuston sivuihin koodin upottaminen edellyttää kolme erillistä tehtävää seuraavien osien mukaisesti.

![Customer Voicen Kausittainen asiakaskysely -sivu, jossa Painike-vaihtoehto on valittuna.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Sisällytä ulkoisen komentosarjan URL-osoite

Kaikilla sivuston sivuilla, joilla on oltava Customer Voice -kysely, sinun on upotettava Customer Voicen toimittama ulkoisen komentosarjan URL-osoite koodiin. Paras tapa upottaa komentosarja useaan sivuston sivuun on luoda katkelma sivustonmuodostajassa, joka sisältää ulkoisen komentosarjan URL-osoitteen, ja lisätä katkelma sitten asianmukaisiin sivumalleihin. Kun olet julkaissut päivitetyn mallin, upotettu ulkoinen komentosarjakoodi muistuttaa seuraavaa esimerkkiä muuttuneilla sivuston sivuilla.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Lisätietoja katkelmista on osiossa [Katkelmien avulla työskentely](work-with-fragments.md).

> [!NOTE]
> Vain URL-osoite on lisättävä katkelmaan. Ulkoinen komentosarjamoduuli lisää muun komentosarjakoodin.

Voit upottaa ulkoisen komentosarjan URL-osoitteen katkelmaan noudattamalla seuraavia ohjeita.

1. Luo sivustonmuodostimessa katkelma, joka perustuu [Ulkoiset komentosarjat -moduuliin](script-module.md).
1. Valitse uudessa katkelmassa **Ulkoinen oletuskomentosarja** -kohta.
1. Kirjoita **ulkoisen oletuskomentosarjan** ominaisuuksien ruudun **Komentosarjan lähde** -kenttään ulkoisen komentosarjan URL-osoite seuraavan esimerkin mukaisesti.

    ![Ulkoisen komentosarjan URL-osoite uuden katkelman komentosarjan lähdekentässä.](media/customer-voice-integration-2.png)

1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Julkaise katkelma valitsemalla **Julkaise**.

Uusi katkelma, joka sisältää upotetun ulkoisen komentosarjalohkon, on nyt valmis lisättäväksi oikeaan sivumalliin.

### <a name="embed-the-external-style-sheet-code"></a>Upota ulkoisen tyylitiedoston koodi

Seuraavaksi kaikilla sivuston sivuilla, joilla on oltava Customer Voice -kysely, sinun on upotettava Customer Voicen toimittama ulkoisen tyylitiedoston koodi. Kuten edellisessä osassa, paras tapa upottaa ulkoisen tyylitiedoston koodi useaan sivuston sivuun on luoda katkelma sivustonmuodostajassa, joka sisältää ulkoisen tyylitiedoston koodin, ja lisätä katkelma sitten asianmukaisiin sivumalleihin. Upotettu ulkoisen tyylitiedoston koodi muistuttaa seuraavaa esimerkkikoodia.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Voit upottaa ulkoisen tyylitiedoston koodin katkelmaan noudattamalla seuraavia ohjeita.

1. Luo sivustonmuodostimessa katkelma, joka perustuu [Metatunnisteet-moduuliin](metatags-module.md).
1. Valitse fragmentissa **Oletusmetatunnisteet**-kohta.
1. Kirjoita **oletusmetatunnisteiden** ominaisuuksien ruudun **Metatunnisteet** -kenttään ulkoisen tyylitiedoston koodi seuraavan esimerkin mukaisesti.

    ![Ulkoisen tyylitiedoston koodi uuden katkelman metatunnisteiden kentässä.](media/customer-voice-integration-3.png)

1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Julkaise katkelma valitsemalla **Julkaise**.

Uusi katkelma, joka sisältää upotetun ulkoisen tyylitiedoston koodin, on nyt valmis lisättäväksi oikeaan sivumalliin.

### <a name="embed-the-inline-script-code"></a>Upota sisäisen komentosarjan koodi 

Seuraavaksi kaikilla sivuston sivuilla, joilla on oltava Customer Voice -kysely, sinun on upotettava sisäisen komentosarjan koodi Customer Voicen toimittama ulkoisen tyylitiedoston koodi. Kuten edellisissä osissa, paras tapa upottaa sisäisen komentosarjan koodi useaan sivuston sivuun on luoda katkelma sivustonmuodostajassa, joka sisältää sisäisen komentosarjan koodin, ja lisätä katkelma sitten asianmukaisiin sivumalleihin.

Seuraavassa sisäisen komentosarjan koodiesimerkissä **SURVEY\_KEY** on paikkamerkki. **SURVEY\_KEY** -arvon on oltava sama kuin varsinainen kyselyavain, jonka Customer Voice toimitti upotuskoodissa. Viimeinen rivi kutsuu koodia hahmontamaan kyselypainikkeen yhden sekunnin kuluttua, jotta voidaan varmistaa, että komentosarjoilla on tarpeeksi aikaa latautua. Valitsemasi kyselyn mukaan sinun on ehkä lisättävä tai päivitettävä myös muita metatietoja, kuten yrityksen nimi.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Voit upottaa sisäisen komentosarjan koodin katkelmaan noudattamalla seuraavia ohjeita.

1. Luo sivustonmuodostimessa katkelma, joka perustuu [Sisäiset komentosarjat -moduuliin](script-module.md).
1. Valitse katkelmassa **Sisäinen oletuskomentosarja** -kohta.
1. Kirjoita **sisäisen oletuskomentosarjan** ominaisuuksien ruudun **Sisäinen komentosarja** -kenttään sisäisen komentosarjan koodi seuraavan esimerkin mukaisesti.

    ![Sisäisen komentosarjan koodi uuden katkelman sisäisen komentosarjan kentässä.](media/customer-voice-integration-4.png)

1. Valitse ensin **Tallenna** ja sitten **Lopeta muokkaus**.
1. Julkaise katkelma valitsemalla **Julkaise**.

Uusi katkelma, joka sisältää upotetun sisäisen komentosarjan koodin, on nyt valmis lisättäväksi oikeaan sivumalliin.

## <a name="add-fragments-to-a-template"></a>Katkelmien lisääminen malliin

Kun olet saanut valmiiksi katkelmat, jotka sisältävät Customer Voicen upotetun koodin, sinun on lisättävä ne sivumalleihin, jotka liittyvät sivuston sivuihin, joita haluat käyttää. Seuraavassa esimerkissä on lisätty kolme esimerkkikatkelma tuotetietosivun (PDP) -malliin.

![PDP-malliin lisätyt esimerkkikatkelmat.](media/customer-voice-integration-5.png)

Kun päivitetty malli on julkaistu, Customer Voice -kysely tulee näkyviin kaikilla sivuilla, joita malli hallitsee.

Tietoja malleista on osiossa [Mallien avulla työskentely](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Sisällön suojauskäytännön (CSP) määritys

Oletusarvon mukaan sisällön suojauskäytäntö (CSP) ei salli kutsuja muihin palveluihin, ellei lisäkonfiguraatiota tehdä. Siksi päivitettyjen mallien julkaisemisen jälkeen on todennäköistä, että kyselyä ei ladata asianmukaisella sivuston sivuilla. Jos haluat tarkastella CSP:hen liittyviä virheitä, avaa selaimesi kehittäjätyökalut (F12) ja siirry sivulle, jolla on kysely. CSP:hen liittyvät virheet näkyvät konsolin tulostuksessa.

Määritä CSP sivustonmuodostimessa korjataksesi virheet noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset**.
1. Lisää **Sisällön suojauskäytäntö** -välilehdessä `https://customervoice.microsoft.com/` kohtaan **child-src**.
1. Lisää `https://customervoice.microsoft.com/` kohtaan **frame-src**.
1. Lisää `https://mfpembedcdnmsit.azureedge.net` ja **.azureedge.net** kohtaan **img-src**.

Lisätietoja on kohdassa [Sisällön suojauskäytäntö](manage-csp.md).

## <a name="additional-resources"></a>Lisäresurssit

[Ulkoinen komentosarja -moduuli](script-module.md)

[Metatunnistemoduuli](metatags-module.md)

[Sisäinen komentosarja -moduuli](script-module.md)

[Sisällön suojauskäytäntö](manage-csp.md)

[Katkelmien käyttäminen](work-with-fragments.md)

[Mallien käyttö](work-with-templates.md)
