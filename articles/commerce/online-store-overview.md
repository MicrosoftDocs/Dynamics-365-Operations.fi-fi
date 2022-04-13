---
title: Sähköisen kaupankäynnin sivuston yleiskuvaus
description: Tässä aiheessa on yleiskatsaus verkkokauppasivustojen tuesta Microsoft Dynamics 365 Commercessa.
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 90f0f01115b00f231af8d4ae11be1d18d379399b
ms.sourcegitcommit: 6f6ec4f4ff595bf81f0b8b83f66442d5456efa87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/25/2022
ms.locfileid: "8487765"
---
# <a name="e-commerce-site-overview"></a>Sähköisen kaupankäynnin sivuston yleiskuvaus

[!include [banner](includes/banner.md)]

Tässä aiheessa on yleiskatsaus verkkokauppasivustojen tuesta Microsoft Dynamics 365 Commercessa. Se sisältää tietoja siitä, miten sähköisen kaupan verkkokaupat alustetaan ja hallitaan Dynamics 365 Commercessa. Se tarjoaa myös linkkejä lisätietoihin verkkokaupoista ja tietoja sähköisen kaupankäynnin sivuston asentamisesta määrittämisestä. Vaikka tämä ohje aihe kattaa monet perusasiat, se ei kata kaikkea, mikä on tarpeen sähköisen kaupankäynnin tuotantosivuston määrittämistä varten. Edistyneitä aiheita on Dynamics 365 Commercen dokumentaatiossa.

## <a name="online-store-channel"></a>Verkkokauppakanava

Ennen kuin voit rakentaa uuden sivuston Dynamics 365 Commerce -sovellukseen on perustettava vähintään yksi verkkokauppakanava. Lisätietoja on ohjeaiheessa [online-kanavan määrittäminen](channel-setup-online.md). 

Dynamics 365 Commercessa voit käyttää verkkokauppakanavaa tuotteiden, hinnoittelun, kielten, maksutapojen, toimitustapojen, toteutuspaikkojen ja muiden asiakkaiden käytettävissä olevien verkkokokemuksen osa-alueiden määrittämiseksi.

Vain yksi verkkokauppakanava on määritettävä, ennen kuin voit aloittaa Dynamics 365 Commercen käytön. Yksittäinen sähköisen kaupankäynnin sivusto voi kuitenkin tarjota verkkokokemusta useissa verkkokaupoissa. Jos esimerkiksi useita verkkokauppoja on määritetty tukemaan eri maantieteellisiä alueita, kunkin myymälän määrittämien yksilöllisten kokemusten tarjoamiseen voidaan käyttää yhtä sähköisen kaupankäynnin sivujoukkoa. Lisätietoja sivuston määrittämisestä tukemaan useita verkkokauppoja on kohdassa [Online-sivuston liittäminen kanavaan](associate-site-online-store.md).

Kun verkkokauppa on määritetty, se voidaan liittää Dynamics 365 Commerce -sivustoon, joka toimii verkkokaupalla. Lisätietoja verkkokaupoista ja niiden määrittämisestä on kohdassa [Verkkokauppojen määrittäminen](/dynamics365/unified-operations/retail/online-stores).

## <a name="deploy-a-new-e-commerce-tenant"></a>Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto

Sähköisen kaupankäynnin sivuston alustuksen aikana sinulta kysytään toimialueen nimeä. Lisätietoja Commerce-toimialueista on kohdassa [Toimialueen nimen määrittäminen](configure-your-domain-name.md) ja [Toimialueet Dynamics 365 Commercessa](domains-commerce.md). Jos haluat ottaa käyttöön uuden sähköisen kaupankäynnin vuokraajan käyttämällä [Microsoft Dynamics Lifecycle Servicesiä (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide), noudata kohdan [Uuden sähköisen kaupan vuokraajan käyttöönotto](deploy-ecommerce-site.md) ohjeita. Kun sähköisen kaupankäynnin vuokraaja on määritetty LCS:iin, se tarjoaa linkin Commercen sivuston muodostimeen. Tämän jälkeen voit käyttää Commercen sivuston muodostinta sähköisen kaupankäynnin sivustojen alustamiseen ja konfiguroimiseen.

## <a name="initialize-your-e-commerce-site"></a>Sähköisen kaupankäynnin sivuston alustaminen

Kun käynnistät Commerce sivuston muodostimen LCS:ista, **Sivustot**-sivu tulee näkyviin. Tämä sivu sisältää kaksi esimääritettyä sivustoja, **oletus** ja **fabrikam**, kuten seuraavassa kuvassa on esitetty.

![Sivustot-sivu Commercen-sivuston luontiohjelmassa.](media/e-commerce-site-01.png)

Kun valitset jommankumman näistä sivustoista, sinua kehotetaan valitsemaan toimialueen nimi, oletusverkkokauppakanava, tuettu kieli valitulle kanavalle ja polku. Jos käytössä on vain yksi kanava, voit jättää polun tyhjäksi. Lisää verkkokauppakanavia tai kieliä voi määrittää myöhemmin Commercen sivuston muodostimessa. Jokainen lisäkanava tai -kieli edellyttää yksilöllistä polkua. Sinulla on esimerkiksi kaksi verkkokanavaa, jotka liittyvät yhteen sivustoon, ja sivuston toimilueen nimi on `www.fabrikam.com`. Tässä tapauksessa yhden kanavan polku voi olla oletusarvo, jolla ei ole polkua ( `https://www.fabrikam.com`), ja toinen kanava voidaan määrittää uudelle polulle, kuten **site2**, jolla on URL-osoite `https://www.fabrikam.com/site2`. Seuraavassa kuvassa näkyy esimerkki sivuston alustuksen valintaikkunasta Commercen sivuston muodostimessa.

![Sivuston alustaminen -valintaikkuna Commerce-sivuston luontiohjelmassa.](media/e-commerce-site-02.png)

**Sivustot**-sivulla on myös **Uusi sivusto** -painike. Valintaikkuna, joka tulee näkyviin, kun valitset tämän painikkeen, muistuttaa sivuston alustaminen -valinta ikkunaa, mutta sen avulla luodaan uusi sivusto. Uudet sivustot ovat tyhjiä. Ne eivät sisällä samoja oletusmalleja, katkelmia, sivuja ja kuvia, jotka ovat **oletus**- ja **fabrikam**-sivustojen mukana. Voit kuitenkin halutessasi avata tukipyynnön ja pyytää, että oletussisällön kopio lisätään uuteen tyhjään sivustoon. Katso lisätietoja kohdasta [Luo sähköisen kaupankäynnin sivusto](create-ecommerce-site.md).

Kun uusi sivusto on alustettu, Commercen sivuston muodostimen **Aloitus**-sivu tulee näkyviin. Tämä sivu sisältää linkkejä yleisiin toimiin ja ohjesisältöön, kuten seuraavassa kuvassa on esitetty.

![Commerce-sivuston luontiohjelman Aloitus-sivun linkit.](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>Verkkokauppakanavien muokkaaminen tai verkkokauppakanavien lisääminen sähköisen kaupankäynnin sivustoon

Kun olet luonut sähköisen kaupankäynnin sivuston, voit vaihtaa kanavan, johon se liittyy, noudattamalla ohjeita kohdassa [Sähköisen kaupankäynnin sivuston liittäminen online-kanavaan](associate-site-online-store.md). Seuraavan kuvan esimerkissä näkyy, miten kanavan toimintayksikön numeroa (OUN) voidaan muuttaa **Kanavat**-sivulla (**Sivuston asetukset \> Kanavat**). Kun olet tehnyt muutoksen, muista valita **Tallenna ja julkaise**. Näin varmistat, että muutos julkaistaan.

![Kanavat-sivu Commerce-sivuston luontiohjelmassa.](media/e-commerce-site-04.png)

Voit lisätä uusia kanavia valitsemalla **Lisää kanava**. Jos haluat lisätä kanavalle uusia kieliä, valitse kanava ja valitse sitten **Lisää kielialue** näkyviin tulevassa Kanava-valintaikkunassa. Ennen kuin kielialaueita voi näkyä valintaikkunassa, ne pitää esimäärittää Internet-kauppakanavalle Commerce Headquarters -sovelluksessa.

![Kanava-valintaikkuna Commerce-sivuston luontiohjelmassa.](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Azure B2C -vuokraajan määrittäminen

Dynamics 365 Commerce käyttää Azure Active Directory (Azure AD) B2C -ratkaisua käyttäjän tunnistetietojen ja todennuksen työnkulkujen tukemisessa. Lisätietoja Azure B2C -vuokraajan määrittämisestä on ohjeaiheissa [B2C-vuokraajan määrittäminen Commercessa](set-up-b2c-tenant.md), [Mukautettujen sivujen määrittäminen käyttäjän kirjautumisille](custom-pages-user-logins.md) sekä [Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-b2c-tenants.md).

## <a name="overview-of-the-default-site-pages"></a>Oletussivuston sivujen yleiskatsaus

**Oletus**- ja **fabrikam**-sivustoissa on valmiiksi määritettyjä malleja, katkelmia ja sivuja, joiden avulla pääset alkuun. Lisätietoja on seuraavissa aiheissa:

- [Aloitussivun yleiskatsaus](quick-tour-home-page.md)
- [Tuotetietosivun yleiskatsaus](quick-tour-pdp.md)
- [Ostoskorin ja maksusivun yleiskatsaus](quick-tour-cart-checkout.md)
- [Tilinhallintasivujen yleiskatsaus](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>Sivuston asetusten hallinta

Lisätietoja asetusten hallinnasta on seuraavissa ohjeaiheissa:

- [Sähköisen kaupankäynnin käyttäjien ja roolien hallinta](manage-ecommerce-users-roles.md)
- [Sivuston hakukoneoptimointia (SEO) koskevia tietoja](search-engine-optimization-considerations.md)
- [Sisällön suojauskäytännön (CSP) hallinta](manage-csp.md)
- [Sivuston teeman valitseminen](select-site-theme.md)

## <a name="manage-site-content"></a>Sivuston sisällön hallinta

Lisätietoja sisällön hallinnasta on seuraavissa ohjeaiheissa:

- [Sivumallisanasto](page-elements-overview.md)
- [Asiakirjan tilat ja elinkaari](document-states-overview.md)
- [Mallit ja asettelu](templates-layouts-overview.md)
- [Katkelmien käyttäminen](work-with-fragments.md)
- [Moduulien käyttäminen](work-with-modules.md)
- [Digitaalisten resurssien hallinnan yleiskatsaus](dam-overview.md)
- [Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]