---
title: Navigointipolkumoduuli
description: Tässä artikkelissa on tietoja navigointipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fe5dfea7e579d54d11be35eb657a1c1f617a5724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277082"
---
# <a name="breadcrumb-module"></a>Navigointipolkumoduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja navigointipolkumoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.

Linkkipolkua käytetään sivuston sivujen toissijaiseen navigointiin. Ne näkyvät yleensä sivun yläosassa otsikon alapuolella. Vaikka linkkipolkumoduulit voidaan lisätä mille tahansa sivulle, niitä käytetään useimmiten tuotetietosivuilla (PDP:t), jotka näyttävät tuoteluokkahierarkian ja tarjoavat nopean tavan liikkua sivustossa. Linkkipolkua käyttämällä voidaan myös näyttää takaisin tuloksiin -linkki, kun käyttäjät avaavat PDP:n haku- tai luettelosivulta. Tällä tavoin käyttäjät voivat palata nopeasti suodatettuun luettelosivuun ja jatkaa ostosten tekemistä.

Sivuilla, joilla on tuoteluokkakonteksti, kuten PDP:t ja luokkasivut, linkkipolkumoduulit näyttävät luokkahierarkian. Sivuilla, joilla ei ole luokkakontekstia, linkkipolkumoduulit näyttävät **&lt;sivuston juuri&gt; / &lt;nykyinen sivu&gt;** oletusarvon mukaan. Linkkipolkumoduulit voidaan määrittää myös manuaalisesti muun tyyppisillä sivuston sivuilla, jotka näyttävät linkit sivuston tietyille sivuille.

> [!NOTE]
> Linkkipolkumoduuli on käytettävissä Dynamics 365 Commercen versiossa 10.0.12.

Seuraavassa kuvassa on esimerkki linkkipolkumoduulista, jossa näkyy PDP:n luokkahierarkia.

![Esimerkki linkkipolkumoduulista.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Linkkipolkumoduulin asetukset

Linkkipolkumoduuli käyttää **linkkipolun näyttötyyppiä PDP**-asetuksessa, joka määritetään kohdassa **Sivuston asetukset \> Laajennukset** sivustomuodostustyökalussa. Tällä asetuksella on kolme mahdollista arvoa:

- **Näytä luokkahierarkia** – Kun tämä arvo on valittuna, linkkipolkumoduulissa näkyy PDP:n tarkasteltavissa olevan tuotteen koko luokkahierarkia.
- **Näytä takaisin tuloksiin** – Kun tämä arvo on valittu, linkkipolkumoduulissa näkyy PDP:n takaisin tuloksiin -linkki, jos käyttäjä avaa PDP:n moduulista, joka sallii takaisin tuloksiin -linkin. Tämä toiminto on käytettävissä, kun käyttäjät siirtyvät luokka-, haku-, luettelo- ja suositusluettelot -sivuista. Tämän toiminnon tukemiseksi tuotekokoelma- ja hakutulosmoduuleissa on ominaisuus, jonka nimi on **Salli takaisin PDP:n tuloksiin**. Tämän ominaisuuden avulla voit joustavasti määrittää, mitkä moduulit tukevat takaisin tuloksiin -linkkitoimintoa PDP:n yhteydessä. Jos esimerkiksi **Näytä takaisin tuloksiin** -asetus on valittuna **linkkipolkunäyttötyyppi PDP:ssä** -linkkipolkumoduulille, ja **Salli takaisin tulokset PDP:ssä** valitaan hakusivun hakutulokset-moduulille, näkyviin tulee takaisin tuloksiin -linkki, kun käyttäjät siirtyvät hakusivulta PDP:n kautta.
- **Näytä luokkahierarkia ja takaisin tuloksiin** – Tämä arvo on kahden edellisen yhdistelmä. Kun tämä arvo on valittu, linkkipolkumoduuli näyttää sekä koko luokkahierarkian että Takaisin tuloksiin -linkin (jos se on määritetty) PDP:n yhteydessä.

> [!IMPORTANT]
> Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.12. Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti. Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Navigointipolkumoduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Juuri | Teksti tai linkki| Tämä valinnainen ominaisuus määrittää linkkitekstin ja linkin kohteen polkua varten. Jos tätä ominaisuutta ei ole määritetty, pääkansiota ei määritetä. |
| Linkkipolkulinkki | Linkitä | Tämä valinnainen ominaisuus määrittää manuaalisesti määritetyn polun linkit, jos linkit ovat pakollisia. Linkit näkyvät siinä järjestyksessä, jossa ne ovat luettelossa. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Linkkipolkumoduulin lisääminen uudelle sivulle

Voit lisätä linkkipolkumoduulin PDP:hen ja määrittää pakolliset ominaisuudet seuraavasti.

1. Siirry kohtaan **Sivuston asetukset \> Laajennukset** ja valitse sitten **Linkkipolun näyttötyyppi PDP** -asetuksessa **Näytä luokkahierarkia**.
1. Siirry kohtaan **Mallit** ja valitse PDP-malli.
1. Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Navigointipolku**-moduuli ja valitse sitten **OK**.
1. Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.
1. Siirry kohtaan **Sivut** ja avaa PDP, joka käyttää PDP-mallia. Jos PDP:tä ei vielä ole olemassa, luo sellainen.
1. Valitse **Kontti**-paikka, joka sisältää ostoruutumoduulin. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.
1. Valitse **Valitse moduulit** -valintaikkunassa **Navigointipolku**-moduuli ja valitse sitten **OK**.
1. Valitse **Linkkipolku**-paikan ominaisuudet-ruudun **Pääkansio**-kohdasta **Linkitä teksti**.
1. Kirjoita **Linkin teksti** -valintaikkunaan **Koti** ja valitse sitten **Linkin kohde** -kohdasta **Lisää linkki**.
1. Valitse **Lisää linkki** -valintaikkunassa linkkipolkupääkansion linkki ja valitse sitten **OK**.
1. Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.
1. Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.

## <a name="additional-resources"></a>Lisäresurssit

[Moduulikirjaston yleiskatsaus](starter-kit-overview.md)

[Siirtymisvalikkomoduulit](nav-menu-module.md)

[Sivuston valitsinmoduuli](site-selector.md)

[Luokan oletussaapumis- ja oletushakutulossivun yleiskatsaus](category-search-page-overview.md)

[Tuotekokoelmamoduulit](product-collection-module-overview.md)

[Ostoruutumoduuli](add-buy-box.md)

[SDK:n ja moduulikirjaston päivitykset](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
