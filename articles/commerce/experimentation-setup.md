---
title: Kokeen määrittäminen
description: Tässä artikkelissa käsitellään kokeen määrittämistä kolmannen osapuolen palvelussa.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946163"
---
# <a name="set-up-an-experiment"></a>Kokeen määrittäminen

Sen jälkeen kun olet [määrittänyt hypoteesin ja käytettävät onnistumismittarit](experimentation-identify.md), koe on määritettävä kolmannen osapuolen palvelussa. Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa. Muut vaiheet käsitellään erillisissä artikkeleissa.

[ ![Kokeilun käyttäjän siirtymä – määrittäminen.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Kokeen määrittäminen kolmannen osapuolen palvelussa
Tässä vaiheessa kolmannen osapuolen palvelun pitäisi olla valittuna kokeen suorittamista ja seurantaa varten sekä kokeen yhdistämisen määrittämistä varten. Nämä edellytykset on mainittu [Kokeilut Dynamics 365 Commercessa](experimentation-overview.md).

Luo koe kolmannen osapuolen palvelussa noudattamalla annettuja ohjeita. Jos yhdistin on määritetty oikein, täydellinen kolmannen osapuolen palvelussa määritettyjen kokeiden luettelo tulee näkyviin Commercen sivustonmuodostimeen noin 5 minuutin kuluessa.

## <a name="set-up-your-success-metrics"></a>Onnistumismittareiden määrittäminen
Kaikki kokeet tarvitsevat mittarin, jolla mitataan variaatioiden vaikutusta ja vahvistaa hypoteesi. Noudata seuraavia ohjeita ja ota mittareiden laskenta käyttöön kolmannen osapuolen palvelussa käyttämällä Dynamics 365 Commercen live-telemetriatapahtumia.

Onnistumismittarit määritetään heti käyttövalmiille moduuleille seuraavasti:

1. Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa **Sivut**-välilehti ja valitse sitten sivu, josta haluat kerätä mittaustietoja. 
1. Siirry **Seurattava tapahtumatunnukset** -osaan seurattavan sivun tai moduulin oikeassa ominaisuusruudussa.
1. Valitse **Näytä**. Näkyvissä on kaikki napsautustapahtumatunnukset sisältävä luettelo. Kopioi seurattava tapahtuma ja liitä tapahtuma-avain sille varattuun sijaintiin kolmannen osapuolen palvelussa. Jos tarvitset useita tapahtumia, kopioi avaimet yksi kerrallaan. 
1. Käytä sivunäkymissä sivun nimen SHA-256-hajautusarvoa sivustonmuodostimessa lisättynä arvolla `.PageView`. Esimerkiksi tapahtuman tunnus kohteelle `Homepage.PageView` olisi `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Suorita muut kolmannen osapuolen palvelun edellyttämät mittareiden seurantaan tarvittavat vaiheet.

Jos haluat mittailla napsautustapahtumia, noudata seuraavia ohjeita mukautetun moduulin napsautusten saamiseksi:

1. Valmistele **TelemetryContent**-objekti moduulia varten alla olevaa toimintoa käyttäen. Tämä toiminto määrittää syötteiksi sivun nimen, moduulin nimen ja SDK:n tarjoaman oletustelemetriikka-objektin.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Seuraavassa on esimerkki: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Luo kuormitustiedot, jotka sisältävät tietoa siepattavista kohteista. Voit lisätä painikkeisiin ja muihin staattisiin ohjausobjekteihin **etextin**, kuten "Osta nyt" tai "Etsi". Napsautuksia sisältävissä komponenteissa, esimerkiksi tuotekorttien napsautuksissa, voit lähettää **recidin**, joka on tuotteen tai tuotetunnuksen tietuetunnus.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Esimerkkinä staattisissa ohjausobjekteissa voit siirtää painikkeen tekstin merkkijonon alla olevan mukaisesti:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Esimerkkinä tuotteen napsautuksista siirrä tuotteen recordId, kuten alla on esitetty:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Voit rekisteröidä tapahtuman kutsumalla **OnClick**-toimintoa .

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Seuraavassa on esimerkki:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Edellinen vaihe
[Kokeilun hypoteesin ja mittarien määrittäminen](experimentation-identify.md) 


## <a name="next-step"></a>Seuraava vaihe
[Kokeilun yhdistäminen ja muokkaaminen](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
