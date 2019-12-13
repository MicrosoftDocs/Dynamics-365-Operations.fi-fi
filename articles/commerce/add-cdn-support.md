---
title: Sisältöverkon (CDN) tuen lisääminen
description: Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb757672fffb56892837c066d552773908dd1ec1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696965"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Sisältöverkon (CDN) tuen lisääminen

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.

## <a name="overview"></a>Yleiskatsaus

Kun määrität Dynamics 365 Commerce -sovelluksessa sähköisen kaupankäynnin ympäristön, voit määrittää sen käyttämään CDN-palvelua. 

Mukautettu toimialue voi olla käytössä sähköisen kaupankäynnin ympäristön valmisteluprosessin aikana. Vaihtoehtoisesti voit käyttää palvelupyyntöä määrittämiseen valmisteluprosessin päätyttyä. Sähköisen kaupankäynnin ympäristön valmisteluprosessi luo isäntänimen, joka liittyy ympäristöön. Tällä isäntänimellä on seuraava muoto, jossa *e-commerce-tenant-name* on ympäristön nimi.

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Isäntänimi tai päätepiste, joka luodaan valmisteluprosessin aikana, tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com. Se ei tue SSL-varmennetta mukautetuissa toimialueissa. Tämän vuoksi SSL on päätettävä CDN:n mukautetuissa toimialueissa ja ohjattava liikenne CDN:stä isäntänimelle tai päätepisteelle, jonka Commerce on luonut. 

Lisäksi Commerce-sovelluksen *tilastot* (JavaScript- tai Cascading Style Sheets \[CSS\] -tiedostot) saadaan Commercen luomasta päätepisteestä (\*.commerce.dynamics.com). Tilastot voidaan tallentaa välimuistiin vain, jos Commercen luoma isäntänimi tai päätepiste sijoitetaan CDN:n jälkeen.

## <a name="set-up-ssl"></a>Määritä SSL

Jos haluat varmistaa, että SSL on määritetty ja että tilastot tallennetaan välimuistiin, määritä CDN niin, että se liittyy isäntänimeen, jonka Commerce on luonut ympäristöä varten. Myös seuraava muoto on tallennettava välimuistiin tilastoja varten: 

/\_msdyn365/\_scnr/\*

Kun Commerce-ympäristö on valmisteltu annetun mukautetun toimialueen avulla tai kun ympäristön mukautettu toimialue on annettu palvelupyynnön avulla, osoita mukautettu toimialue isäntänimelle tai päätepisteelle, jonka Commerce on luonut.

Kuten aiemmin mainittiin, luotu isäntänimi tai päätepiste tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com. Se ei tue SSL-varmennetta mukautetuissa toimialueissa.

## <a name="cdn-services"></a>CDN-palvelut

Commerce-ympäristössä voi käyttää mitä tahansa CDN-palvelua. Seuraavassa on kaksi esimerkkiä:

- **Microsoft Azure Front Door Service** – Azuren CDN-ratkaisu. Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Azure Front Door Service -dokumentaatio](https://docs.microsoft.com/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – Lisätietoja on kohdassa [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-asetukset

CDN-määritysprosessi koostuu seuraavista yleisistä vaiheista:

1. Lisää edustaisäntä.
1. Määritä taustapooli.
1. Määritä reitityksen ja välimuistiin tallennuksen säännöt.

### <a name="add-a-front-end-host"></a>Lisää edustaisäntä

Mitä tahansa CDN-palvelua voi käyttää. Tämän ohjeaiheen esimerkissä käytetään Azure Front Door Service -palvelua. 

Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Pika-aloitus: Luo Front Door erittäin käytettävissä olevalle yleiselle verkkosovellukselle](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a>Azure Front Door Service -palvelun taustapooli

Voit määrittää Azure Front Door Service -palvelun taustapoolin seuraavasti.

1. Lisää **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** taustapooliin mukautettuna isäntänä, jolla on tyhjä taustan isännän otsikko.
1. Syötä **Kuntotutkimukset**-kohdan **Polku**-kenttään **/keepalive**.
1. Kirjoita **Aikavälit (sekunteina)** -kenttään **255**.
1. Jätä **Kuormituksen tasaus** -kohtaan oletusarvot.

Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa.

![Taustapooli-valintaikkunan lisääminen](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Sääntöjen määrittäminen Azure Front Door Service -palvelussa

Määritä reitityssääntö Azure Front Door Service -palvelussa seuraavasti.

1. Lisää reitityssääntö.
1. Kirjoita **Nimi**-kenttään **oletus**.
1. Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.
1. Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.
1. Syötä ylempään **Kohdistettavat mallit** -kenttään **/\***.
1. Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.
1. Valitse **Taustapooli**-kentässä **ecom-backend**.
1. Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto. 
1. Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.
1. Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.

Määritä välimuistiin tallennuksen sääntö Azure Front Door Service -palvelussa seuraavasti.

1. Lisää välimuistiin tallennuksen sääntö.
1. Kirjoita **Nimi**-kenttään **tilastot**.
1. Valitse **Hyväksytty protokolla** -kentässä **HTTP ja HTTPS**.
1. Syötä **Edustaisännät**-kenttään **dynamics-ecom-tenant-name.azurefd.net**.
1. Syötä ylempään **Kohdistettavat mallit** -kenttään **/\_msdyn365/\_scnr/\***.
1. Määritä **Reitin tiedot** -kohdan **Reitin tyyppi** -vaihtoehdon arvoksi **Välitä edelleen**.
1. Valitse **Taustapooli**-kentässä **ecom-backend**.
1. Valitse **Välitysprotokolla**-kenttäryhmässä **Pyynnön vastaavuus** -vaihtoehto.
1. Määritä **URL-osoitteen uudelleenkirjoitus** -vaihtoehdon arvoksi **Poistettu käytöstä**.
1. Määritä **Välimuistiin tallennus** -vaihtoehdon arvoksi **Poistettu käytöstä**.
1. Valitse **Kyselymerkkijonon välimuistiin tallennuksen toiminta** -kentässä **Tallenna jokainen yksilöllinen URL-osoite välimuistiin**.
1. Valitse **Dynaaminen pakkaus** -kenttäryhmässä **Käytössä**-vaihtoehto.

Seuraavassa kuvassa näkyy **Lisää sääntö** -valintaikkuna Azure Front Door Service -palvelussa.

![Lisää sääntö -valintaikkuna](./media/CDN_CachingRule.png)

Kun tämä ensimmäinen määritys on otettu käyttöön, lisää mukautettu toimialue Azure Front Door Service -palvelun määritykseen. Jos haluat lisätä mukautetun toimialueen (esimerkiksi `www.fabrikam.com`), määritä toimialueelle kanoninen nimi (CNAME).

Seuraavassa kuvassa näkyy **CNAME-määritys**-valintaikkuna Azure Front Door Service -palvelussa.

![CNAME-määritys-valintaikkuna](./media/CNAME_Configuration.png)

> [!NOTE]
> Jos käyttämäsi toimialue on jo aktiivinen ja julkaistu, ota yhteyttä tukeen, jotta tämä toimialue otetaan käyttöön Azure Front Door Service -palvelun kanssa testin määrittämistä varten.

Voit käyttää Azure Front Door Service -palvelua varmenteen hallinnassa tai voit käyttää omaa varmennetta mukautetussa toimialueessa.

Seuraavassa kuvassa näkyy **Mukautetun toimialueen HTTPS**-valintaikkuna Azure Front Door Service -palvelussa.

![Mukautetun toimialueen HTTPS -valintaikkuna](./media/Custom_Domain_HTTPS.png)

CDN:n tulisi nyt olla määritetty niin, että sitä voi käyttää Commerce-sivuston kanssa.

## <a name="additional-resources"></a>Lisäresurssit

[Verkkokaupan yleiskatsaus](online-store-overview.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)
