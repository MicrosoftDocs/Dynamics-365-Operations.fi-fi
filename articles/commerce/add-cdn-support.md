---
title: Sisältöverkon (CDN) tuen lisääminen
description: Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 59277323e0995f59d3a451395a038fa3708274eb
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936827"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>Sisällön toimitusverkoston (CDN) tuen lisääminen

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten sisältöverkko (CDN) lisätään Microsoft Dynamics 365 Commerce -ympäristöön.

Kun määrität Dynamics 365 Commerce -sovelluksessa sähköisen kaupankäynnin ympäristöä, voit määrittää sen käyttämään CDN-palvelua. 

Mukautettu toimialue voi olla käytössä sähköisen kaupankäynnin ympäristön valmisteluprosessin aikana. Vaihtoehtoisesti voit käyttää palvelupyyntöä määrittämiseen valmisteluprosessin päätyttyä. Sähköisen kaupankäynnin ympäristön valmisteluprosessi luo isäntänimen, joka liittyy ympäristöön. Tällä isäntänimellä on seuraava muoto, jossa \<*e-commerce-tenant-name*\> on ympäristön nimi.

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

Isäntänimi tai päätepiste, joka luodaan valmisteluprosessin aikana, tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com. Se ei tue SSL-varmennetta mukautetuissa toimialueissa. Tämän vuoksi SSL on päätettävä CDN:n mukautetuissa toimialueissa ja ohjattava liikenne CDN:stä isäntänimelle tai päätepisteelle, jonka Commerce on luonut. 

Lisäksi Commerce-sovelluksen *tilastot* (JavaScript- tai Cascading Style Sheets \[CSS\] -tiedostot) saadaan Commercen luomasta päätepisteestä (\*.commerce.dynamics.com). Tilastot voidaan tallentaa välimuistiin vain, jos Commercen luoma isäntänimi tai päätepiste sijoitetaan CDN:n jälkeen.

## <a name="set-up-ssl"></a>Määritä SSL

Kun Commerce-ympäristö on valmisteltu annetun mukautetun toimialueen avulla tai kun ympäristön mukautettu toimialue on annettu palvelupyynnön avulla, DNS-muutokset pitää suunnitella Commerce-perehdytystiimin kanssa.

Kuten aiemmin mainittiin, luotu isäntänimi tai päätepiste tukee SSL-varmennetta vain osoitteessa \*.commerce.dynamics.com. Se ei tue SSL-varmennetta mukautetuissa toimialueissa.

## <a name="cdn-services"></a>CDN-palvelut

Commerce-ympäristössä voi käyttää mitä tahansa CDN-palvelua. Seuraavassa on kaksi esimerkkiä:

- **Microsoft Azure Front Door Service** – Azuren CDN-ratkaisu. Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Azure Front Door Service -dokumentaatio](/azure/frontdoor/).
- **Akamai Dynamic Site Accelerator** – Lisätietoja on kohdassa [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).

## <a name="cdn-setup"></a>CDN-asetukset

CDN-määritysprosessi koostuu seuraavista yleisistä vaiheista:

1. Lisää edustaisäntä.
1. Määritä taustapooli.
1. Määritä reitityssäännöt.

### <a name="add-a-front-end-host"></a>Lisää edustaisäntä

Mitä tahansa CDN-palvelua voi käyttää. Tämän ohjeaiheen esimerkissä käytetään Azure Front Door Service -palvelua. 

Lisätietoja Azure Front Door Service -palvelusta on kohdassa [Pika-aloitus: Luo Front Door erittäin käytettävissä olevalle yleiselle verkkosovellukselle](/azure/frontdoor/quickstart-create-front-door).

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Azure Front Door Service -palvelun taustapooli

Voit määrittää Azure Front Door Service -palvelun taustapoolin seuraavasti.

1. Lisää **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** taustapooliin mukautettuna isäntäkoneena, jolla on taustakoneen otsikko, joka on sama kuin **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**.
1. Jätä **Kuormituksen tasaus** -kohtaan oletusarvot.
1. Poista taustapoolin kunnon tarkistukset käytöstä.

Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä annettu taustan isäntänimi.

![Taustapooli-valintaikkunan lisääminen](./media/CDN_BackendPool.png)

Seuraavassa kuvassa näkyy **Lisää taustapooli** -valintaikkuna Azure Front Door Service -palvelussa sekä kuormituksen tasauksen oletusarvot.

![Taustapooli-valintaikkunan lisääminen, jatkuu](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Varmista, että poistat **Kuntotutukimukset**, kun määrität omaa Azure Front Door -palvelua Commercelle.


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


> [!WARNING]
> Jos käytettävä toimialue on jo aktiivinen ja julkaistu, luo tukipalvelupyyntö **Tuki**-ruudussa [Microsoft Dynamics Lifecycle Services -sovelluksessa](https://lcs.dynamics.com/). Näin saat apua seuraavissa vaiheissa. Lisätietoja on kohdassa [Tuen pyytäminen Finance and Operations -sovelluksia tai Lifecycle Services (LCS) -sovellusta varten](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

Jos toimialueesi on uusi, eikä se ole aiemmin määritetty julkaistu toimialue, voit lisätä mukautetun toimialueen määritykseen Azure Front Door Service -palvelussa. Tämän jälkeen verkkoliikenne voi ohjata sivuston Azure Front Door -ilmentymän kautta. Jos haluat lisätä mukautetun toimialueen (esimerkiksi `www.fabrikam.com`), määritä toimialueelle kanoninen nimi (CNAME).

Seuraavassa kuvassa näkyy **CNAME-määritys**-valintaikkuna Azure Front Door Service -palvelussa.

![CNAME-määritys-valintaikkuna](./media/CNAME_Configuration.png)

Voit käyttää Azure Front Door Service -palvelua varmenteen hallinnassa tai voit käyttää omaa varmennetta mukautetussa toimialueessa.

Seuraavassa kuvassa näkyy **Mukautetun toimialueen HTTPS**-valintaikkuna Azure Front Door Service -palvelussa.

![Mukautetun toimialueen HTTPS -valintaikkuna](./media/Custom_Domain_HTTPS.png)

Lisätietoja mukautetun toimialueen lisäämisestä Azure Front Door -palveluun on kohdassa [Mukautetun toimialueen lisääminen Front Door -palveluun](/azure/frontdoor/front-door-custom-domain).

CDN:n tulisi nyt olla määritetty niin, että sitä voi käyttää Commerce-sivuston kanssa.

## <a name="additional-resources"></a>Lisäresurssit

[Sisällön toimitusverkoston käyttöönottoasetukset](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]