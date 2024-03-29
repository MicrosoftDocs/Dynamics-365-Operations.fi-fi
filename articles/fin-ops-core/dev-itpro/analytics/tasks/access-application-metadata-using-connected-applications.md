---
title: Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla
description: Tämän artikkelin vaiheissa selitetään, miten Regulatory Configuration Servicen käyttäjä voi suunnitella uuden sähköisen raportoinnin mallin yhdistämisen käyttämällä metatietoja.
author: kfend
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 1a935b96e247978fc2b2f9449d403c92bff35f17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267869"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava Regulatory Configuration Service (RCS) -käyttäjä voi suunnitella uuden sähköisen raportoinnin ER-mallin yhdistämisen talous- ja toimintosovellusten metatietojen avulla. Sovelluksen metatietoja käytetään verkossa RCS:n yhdistetyllä sovelluksella. ER-näytemallin yhdistäminen määritetään käyttämään ulkomaankauppatapahtumia. Näitä vaiheita varten on ensin suoritettava RCS:ssä artikkelissa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet. Jos olet suorittanut artikkelin [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](access-application-metadata-er-configuration.md) vaiheet, lataa [Esimerkki sähköisestä raportoinnista](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) ja tallenna seuraavat ER-konfiguraatiot: Ulkomaankaupan metatiedot.xml, Ulkomaankauppamalli.xml ja Ulkomaankaupan yhdistäminen.xml. Suorita lopuksi toimenpiteen vaiheet.

## <a name="prerequisites"></a>Edellytykset
1. Valitse **Kaikki työtilat** > **Sähköinen raportointi**. 
2. Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet. 

## <a name="get-required-er-configurations"></a>Tarvittavien ER-konfiguraatioiden hankkiminen
1. Valitse **Raportointikonfiguraatiot**. 
2. Jos olet jo suorittanut toimenpiteen [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](access-application-metadata-er-configuration.md) vaiheet, sinulla on jo tarvittavat nykyisen RCS-esiintymän ER-määritykset (ulkomaankaupan metatietojen, mallin ja yhdistämisen määritykset). Voit ohittaa tämän alitehtävän kaikki jäljellä olevat vaiheet. 
3. Valitse **Vaihto**. 
4. Valitse **Lataa XML-tiedostosta**. 
5. Valitse ensin **Selaa** ja sitten **Ulkomaankaupan metatiedot.xml** -tiedosto. 
6. Valitse **OK**. 
7. Valitse **Vaihto**. 
8. Valitse **Lataa XML-tiedostosta**. 
9. Valitse ensin **Selaa** ja sitten **Ulkomaankauppamalli.xml**-tiedosto. 
10. Valitse **OK**. 
11. Valitse **Vaihto**. 
12. Valitse **Lataa XML-tiedostosta**. 
13. Valitse ensin **Selaa** ja sitten **Ulkomaankaupan yhdistäminen.xml** -tiedosto. 
14. Valitse **OK**. 

## <a name="register-a-connected-application"></a>Yhdistetyn sovelluksen rekisteröiminen
1. Sulje sivu. 
2. Sulje sivu. 
3. Valitse **Kaikki työtilat** > **Sähköinen raportointi**. 
4. Valitse **Yhdistetyt sovellukset**. 
5. Varmista, että määritetty sovellus on Azure-pohjainen ja että nykyinen RCS-käyttäjä voi käyttää sitä. Nykyisellä RCS-käyttäjällä on lisäksi oltava valitun sovelluksen käyttöoikeus ja hänen on oltava rekisteröitynyt sovelluksen käyttäjäksi roolilla, jolla voi käyttää sovelluksen metatietoja. 
6. Valitse **Uusi**. 
7. Kirjoita **Nimi**-kenttään MyConnectedApp. 
8. Kirjoita **Sovellus**-kenttään https:// mycompany.operations.dynamics.com. 
9. Kirjoita **Vuokraaja**-kenttään mycompany.onmicrosoft.com. 
10. Valitse **Tallenna**. 
11. Voit tarkistaa yhteyden määritettyyn sovellukseen valitsemalla **Yhdistä etäsovellukseen** -sivulla **Muodosta yhteys etäsovellukseen napsauttamalla tätä** -linkki. 
12. Valitse **Tarkista yhteys**. 
13. Valitse **Sulje**. 
14. Kun yhteyden tarkistus onnistuu, nykyisen ruudukon määritetyn sovelluksen version ja vuokraajan tiedot päivitetään. 

## <a name="review-existing-model-mapping-configuration"></a>Aiemmin määritetyn mallin yhdistämismäärityksen tarkasteleminen
1. Sulje sivu. 
2. Valitse **Raportointikonfiguraatiot**. 
3. Laajenna puussa **Ulkomaankauppamalli**. 
4. Valitse puussa **Ulkomaankauppamalli\Ulkomaankaupan yhdistäminen**. 
5. Laajenna **Edellytykset**-osa. 

    > [!NOTE]
    > Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan. 

6. Valitse **Suunnittelutoiminto**. 
7. Valitse **Suunnittelutoiminto**. 
8. Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**. 
9. Valitse **Lisää juuri**. 
10. Anna tai valitse **Taulu**-kentässä arvo. 

    > [!NOTE]
    > Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen. Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan. 

11. Valitse **Peruuta**. 
12. Sulje sivu. 
13. Sulje sivu. 

## <a name="assign-connected-application-to-model-mapping"></a>Yhdistetyn sovelluksen määrittäminen mallin yhdistämiseen 
1. Valitse **Muokkaa**. 
2. Valitse **MyConnectedApp**-sovellus. 

    > [!NOTE]
    > Tällä hetkellä yhdistämismääritys viittaa valitun yhdistetyn sovelluksen metatietoihin. Kun sama yhdistämismääritys viittaa samanaikaisesti metatietojen määritykseen ja yhdistettyyn sovellukseen, yhdistetyn sovelluksen metatietoja käytetään. 

3. Valitse **Suunnittelutoiminto**. 
4. Valitse **Suunnittelutoiminto**. 
5. Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**. 
6. Valitse **Lisää juuri**. 
7. Anna tai valitse **Taulu**-kentässä arvo. 

    > [!NOTE]
    > Valittavana on nyt enemmän kuin kaksi sovellustaulukkoa, sillä tämä yhdistämismääritys käyttää siihen määritetyn yhdistetyn sovelluksen kaikkia metatietoja. 

8. Valitse **Peruuta**. 
9. Valitse **Vahvista**. 

    > [!NOTE]
    > Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä tähän yhdistämismääritykseen määritetyn yhdistetyn sovelluksen metatietoja. 

10. Sulje sivu. 
11. Sulje sivu. 

Kun tämä malli on arvioitava käyttämällä toisen version sovelluksen metatietoja, rekisteröi toinen yhdistetty sovellus, määritä se tähän mallin yhdistämismääritykseen ja vahvista se käyttämällä uusia metatietoja.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

