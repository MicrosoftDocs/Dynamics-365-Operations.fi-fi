---
title: Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä
description: Tässä ohjeaiheessa kerrotaan, milloin ja miten usean kanavan Microsoft Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään käyttäjän todennusta varten määritetyssä Dynamics 365 Commerce -ympäristössä.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BriShoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6ca48badbe15b7e1bf543716a9b0e3da31477a20
ms.sourcegitcommit: 236672932ffd0a758012ebb7b2df9bc51249c126
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096502"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, milloin ja miten usean Microsoft Azure Active Directoryn (Azure AD) kuluttajakaupan (B2C) vuokraajat määritetään kanavaa kohti käyttäjän todennusta varten määritetyssä Dynamics 365 Commerce -ympäristössä.

## <a name="overview"></a>Yleiskuvaus

Dynamics 365 Commerce käyttää Azure AD B2C:n pilven tunnistetietopalvelua käyttäjän todennustietojen tukemisessa ja todennuksen työnkuluissa. Käyttäjät voivat rekisteröityä, kirjautua sisään ja palauttaa salasanan todennuksen työnkulkujen avulla. Azure AD B2C tallentaa käyttäjän luottamukselliset todennustiedot, kuten käyttäjätunnuksen ja salasanan. Käyttäjätietue on yksilöllinen jokaiselle B2C-vuokraajalle. Se käyttää joko käyttäjänimeä (sähköpostiosoitetta) tai yhteisöpalvelujen tunnistetietoja.

Useimmissa tapauksissa yksittäistä Azure AD B2C -vuokraajaa käytetään Commerce-ympäristössä. Tämän jälkeen Commerce-asiakkaat voivat luoda ja julkaista useita sivustoja samassa Commerce-ympäristössä. Samoja asiakastietoja käytetään kaikissa sivustoissa. Jos ympäristön sivustoja on kuitenkin käsiteltävä erillisinä brändeinä ja ne näkyvät käyttäjille erillisinä yrityksinä, B2C-vuokraaja voidaan määrittää kanavalle, jota käytetään sivuston/brändin erittelyssä.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Huomioitavaa, kun kanavaa kohden on määritetty useita B2C-vuokraajia

Usein, kun kanavaa tai sivustoa käsitellään erillisenä yrityksenä, paras vaihtoehto käyttäjän tunnistamisen työnkulkujen kannalta on käyttää erillisiä yrityksiä Commercessa. Jos kuitenkin haluat pitää kunkin kanavan/sivuston samassa ympäristössä ja yrityksessä, mutta haluat jokaiselle sivustolle erillisen käyttäjän todennuksen, on tärkeää ottaa huomioon seuraavat seikat ennen jatkamista:

- Käyttäjillä on omat erilliset tunnistetiedot kullekin kanavalle/sivustolle.

    Samalla henkilöllä voi olla kaksi erillistä tiliä kanavaa/sivustoa kohti, koska jokainen tili on yksilöivä merkintä eriliseen B2C-vuokraajaan.

- Microsoft Dynamics -ympäristössä erilliset asiakastietueet palautetaan yleisiin tietuehakuihin.

    Jos käyttäjä käyttää samaa sähköpostiosoitetta eri kanavissa/sivustoissa, yleiset asiakashaut palauttavat tulokset jokaiselle kanavalle/sivustolle. (Näkyviin tulee kanavan ilmaisin.)

- Osoitekirjaa voidaan käyttää käyttäjien ryhmittelyssä. Näin heitä voidaan seurata kanavakohtaisesti.
- Asiakastietueiden määrä kanavaa kohti voi nousta. Tämä nousu voi vaikuttaa yleisten asiakashakujen suorituskykyyn.
- B2C-vuokraajat on yhdistettävä huolellisesti kanavaan. Näin vältetään tilanteet, joissa asiakkaat rekisteröityvät väärään vuokraajaan. Muussa tapauksessa saattaa ilmetä sekaannuksia tai ongelmia seuraamisessa.

Seuraavassa kuvassa näkyy useita B2C-vuokraajia Commerce-ympäristössä.

![Useita B2C-vuokraajia Commerce-ympäristössä](media/MultiB2C_In_Environment.png)

Jos päätät, että yrityksesi edellyttää erillisiä B2C-vuokraajia kanavaa kohden samassa Commerce-ympäristössä, voit pyytää tätä toimintoa suorittamalla seuraavissa osissa olevat toimenpiteet.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Pyydä, että ympäristössä otetaan käyttöön B2C kanavaa kohti

Jos tällä hetkellä haluat, että samassa Commerce-ympäristössä on käytettävissä erilliset B2C-vuokraajat kanavaa kohti, lähetä pyyntö Dynamics 365 Commerce -sovellukseen. Lisätietoja on kohdassa [Lifecycle Services (LCS) -tuen hankkiminen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md). Voit myös pyytää lisätietoja Commerce-ratkaisujen yhteyshenkilöltä.

## <a name="configure-b2c-tenants-in-your-environment"></a>B2C-vuokraajan määrittäminen ympäristössä

Jos haluat määrittää B2C-vuokraajat ympäristössä, tee tässä osassa mainitut tarvittavat toimenpiteet.

### <a name="add-an-azure-ad-b2c-tenant"></a>Azure AD B2C -vuokraajan lisääminen

Voit lisätä Azure AD B2C -vuokraajan ympäristöön seuraavasti.

1. Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.
1. Valitse ensin **B2C-asetukset** ja sitten **Hallitse**.
1. Valitse **Lisää B2C-sovellus** ja syötä sitten seuraavat tiedot:

    - **Sovelluksen nimi**: Syötä nimi, jota sovelluksessa käytetään Commercessa. On suositeltavaa käyttää valittua sovelluksen nimeä, kun määrität Azure AD B2C -sovelluksen määrittämisajankohdan Azure-portaalissa. Näin voit auttaa vähentämään sekaannuksia, kun hallitset B2C-vuokraajaa Commercessa.
    - **Vuokraajan nimi**: Anna B2C-vuokraajan nimi samalla tavalla kuin se näkyy Azure-portaalissa.
    - **Unohdetun salasanan käytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).
    - **SignUp SignIn -käytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).
    - **Asiakasohjelman GUID**: Syötä Azure AD B2C -vuokraajan tunnus niin kuin se näkyy Azure-portaalissa (ei sovelluksen tunnus B2C-vuokraajalle).
    - **Profiilin muokkauskäytännön tunnus**: Anna käytännön tunnus (käytännön nimi Azure-portaalissa).

1. Kun olet syöttänyt nämä tiedot, tallenna muutokset valitsemalla **OK**.

> [!NOTE]
> Jätä kentät, kuten **Laajuus**, **Ei-interaktiivisen käytännön tunnus**, **Ei-interaktiivisen asiakasohjelman tunnus**, **Sisäänkirjauksen mukautettu toimialue** ja **Rekisteröitymisen käytännön tunnus** tyhjiksi, jos Dynamics 365 Commerce -ryhmä ei ohjeista määrittämään niitä.
Uusi Azure AD B2C -vuokraaja näkyy nyt luettelossa **Hallitse B2C-sovelluksia** -kohdassa.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Azure AD B2C -vuokraajan hallinta tai poistaminen

1. Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Vuokraajan asetukset**.
1. Valitse ensin **B2C-asetukset** ja sitten **Hallitse**.
1. Jos haluat muokata B2C-vuokraajaa, valitse sen vieressä oleva kynäsymboli. Jos haluat poistaa B2C-vuokraajan, valitse sen vieressä oleva roskakorisymboli.
1. Valitse **Tallenna** ja aktivoi muutoksesi valitsemalla **Julkaise**.

> [!WARNING]
> Kun B2C-vuokraaja määritetään reaaliaikaista/julkaistua sivustoa varten, käyttäjien on ehkä rekisteröidyttävä vuokraajan tilien avulla. Jos poistat määritetyn vuokraajan **Vuokraajan asetukset \> B2C-vuokraaja** -valikosta, poistat kyseisen B2C-vuokraajan liitoksen sivustoista, jotka on liitetty vuokraajan kanaviin. Tässä tapauksessa käyttäjät eivät ehkä enää voi kirjautua tileille. Ole sen vuoksi hyvin varovainen, kun poistat määritetyn vuokraajan.
>
> Kun määritetty vuokralainen poistetaan, B2C-vuokraajaa ja tietueita ylläpidetään yhä, mutta kyseisen vuokraajan Commerce-järjestelmämääritystä muutetaan tai se poistetaan. Käyttäjät, jotka yrittävät rekisteröityä tai kirjautua sivustoon, luovat uuden asiakastietueen oletusarvoisessa tai juuri liitetyssä B2C-vuokraajassa, joka on määritetty sivuston kanavalle.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Kanavan määrittäminen B2C-vuokraajan avulla

1. Kirjaudu sisään Commerce-sivuston luontiohjelmaan ympäristössä järjestelmänvalvojana. Voit määrittää Azure AD B2C -vuokraajat, jos olet Commerce-ympäristön järjestelmänvalvoja.
1. Laajenna se valitsemalla vasemmasta siirtymisruudusta **Sivuston asetukset**.
1. Valitse **Kanavat** ja valitse sitten kanava, jonka haluat määrittää.
1. Valitse oikeanpuoleisessa ominaisuusruudun **Valitse B2C-sovellus** -kentässä määritetty Azure AD B2C -vuokraaja, jos haluat käyttää tätä kanavaa.
1. Vahvista uusi tai päivitetty konfigurointi valitsemalla komentopalkissa **Tallenna ja julkaise**.

> [!WARNING]
> Jos muutat B2C-sovellusta, joka on liitetty kanavaan, poistat nykyiset ympäristöön jo rekisteröityneiden käyttäjien viitteet. Tässä tapauksessa mitkään tällä hetkellä B2C-sovellukseen liitetyt tunnistetiedot eivät ole käyttäjien käytettävissä. Tämän vuoksi kanavan Azure AD B2C -määritystä kannattaa muuttaa vain, jos olet määrittämässä kanavaa ensimmäistä kertaa, eikä käyttäjiä ole vielä rekisteröitynyt sen käyttäjiksi. Muussa tapauksessa käyttäjien on ehkä rekisteröidyttävä uudelleen ja luotava tietue uuteen Azure AD B2C -vuokralaiseen.
## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-osoitteen uudelleenohjausten lataaminen joukkona](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
