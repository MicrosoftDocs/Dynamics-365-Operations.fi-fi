---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen
description: Tässä aiheessa on tietoja Microsoft Dynamics Lifecycle Services (LCS) -tallennusvaraston poistosta, joka suunnitellaan osana Regulatory Configuration Service (RCS) -yleistietovaraston käyttöönottoa.
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 8862f42f3ceaed7e1413c49cf9b91f0449fab67b
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547979"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) -tallennustilan vanhentuminen

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) -palveluiden käyttö sähköisen raportoinnin (ER) konfiguraatioiden tallennusvarastona on vanhentunut. Tämä poisto käsittää seuraavat muutokset:

- Microsoftin tuottamia Microsoft Dynamics 365 -sovellusten käyttämiä konfiguraatioita ei enää julkaista jaetussa käyttöomaisuuskirjastossa LCS:ssä. Sen sijaan ne julkaistaan vain RCS Global -tietovaraston kautta. Dynamics AX 2012:n konfiguraatiot julkaistaan kuitenkin edelleen jaetussa käyttöomaisuuskirjastossa LCS:ssä, kunnes AX:n vuoden 2012 elinkaaren tuki päättyy.
- Toiminnot, jonka avulla voit ladata konfiguraatioita LCS:n projektin käyttöomaisuuskirjastoon talous- ja toimintosovelluksista ja RCS:stä, poistetaan käytöstä. Voit kuitenkin ladata konfiguraatiot projektin käyttöomaisuuskirjastoon LCS-järjestelmän selaimen avulla. Näin ollen voit edelleen lisätä konfiguraatioita LCS:han, jotta ne voidaan sisällyttää ratkaisupaketteihin.
- Konfiguraatioiden tuonti LCS:stä on edelleen käytettävissä ja tuettu talous- ja toimintosovelluksissa ja RCS:ssä jonkin aikaa. Toiminto kuitenkin vanhentuu pian. (Täsmällinen poistopäivämäärä ilmoitetaan myöhemmin.)

## <a name="deprecation-notice"></a>Poistoilmoitus

LCS:n käyttö varastona -toiminnon poisto ilmoitettiin seuraavassa: [Poistetut tai vanhentuneet ominaisuudet Dynamics 365 Finance -sovelluksissa – Vanhentumisilmoitus LCS:lle](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Suunniteltu poistopäivä on 1.4.2022.

## <a name="key-features"></a>Tärkeimmät ominaisuudet

- Käytä RCS:ää ER-määritysten ja globalisointiominaisuuksien luomiseen.
- Vie määrityksiä suoraan RCS-suunnitteluohjelmasta liitettyyn sovellukseen, kuten Dynamics 365 Finance -ympäristöön, jotta voit tehdä määrityksiin muutoksia ja testata ne nopeasti.
- Tallenna, jaa ja hallitse sekä ER-määritysten että globalisointiominaisuuksien elinkaaria keskitetysti yleisen tietovaraston keskitetyn tallennustilan avulla.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Ohje kertaluotoisille ja jatkuville toimenpiteille

Tässä osassa kuvataan joukko vaiheita, jotka on suoritettava kerran. Siinä kuvataan myös vaiheet, jotka on suoritettava säännöllisesti jälkeenpäin.

### <a name="one-time-action"></a>Kertatoimi

Tuo kaikki pakolliset konfiguraatiot LCS:stä RCS:iin ja julkaise ne RCS:stä yleistietovarastoon. Jos käytät projektikohtaisia käyttöomaisuuskirjastoja johdettujen konfiguraatioiden tallentamista varten LCS:ssä, seuraavat vaiheet on suoritettava, kun LCS on yhä käytettävissä.

1. Jos RCS-esiintymä ei ole vielä käytettävissä, valmistele esiintymä. Lisätietoja on kohdassa [RCS:n yleiskatsaus](rcs-overview.md).
2. Rekisteröi varatussa RCS-instanssissa soveltuva LCS-säilö kullekin käyttöomaisuuskirjaston LCS-projektille, joka sisältää johdetut ER-konfiguraatiot.
3. Tuo ER-konfiguraatiot LCS-tietovarastosta RCS:ään. Lisätietoja on kohdassa [Konfiguraatioiden tuonti LCS:stä](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Jos yleistietovarastoa ei valmistella automaattisesti, rekisteröi se RCS:ssä.
5. Lataa kaikki johdetut konfiguraatiot nykyisestä RCS-instanssista yleistietovarastoon. Käytä **Määrityspaketit**-ominaisuutta apuna latauksessa. Lisätietoja on kohdassa [Lataus yleiseen RCS-tietovarastoon](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Siirtyminen eteenpäin

Käytä RCS:n visuaalisia suunnittelutoimintoja seuraaviin tarkoituksiin:

- Laajenna Microsoftin tarjoamia malleja.
- Luo uusia määrityksiä, joita organisaatio tarvitsee.
- Mukauta sähköisen laskutuksen ja veronlaskentapalvelun globalisointiominaisuuksia.

Käytä Globalisointisäilöä seuraaviin tarkoituksiin:

- Käytä Microsoftin tuottamia määrityksiä ja globalisointiominaisuuksia.
- Lataa luomasi tai laajentamasi määritykset yleiseen säilöön säilyttämistä varten ja jaa ne organisaation Dynamics 365 -sovellusympäristöihin tai ulkoisille organisaatioille. Lisätietoja: [ER-konfiguraation luominen RCS:ssä ja lataaminen yleiseen tietovarastoon](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Tarkoittaako tämä muutos, että LCS:ää ei voi käyttää konfiguraatioiden keskitettynä tallennuspaikkana?

Kyllä. Toiminnot, jonka avulla voit ladata konfiguraatioita LCS:n projektin käyttöomaisuuskirjastoon talous- ja toimintosovelluksista, poistetaan käytöstä. Voit kuitenkin edelleen ladata konfiguraatiot projektin käyttöomaisuuskirjastoon LCS-järjestelmän selaimen avulla tarpeen mukaan.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Luulin, että RCS on korvaava tietovarasto yleismallitiedostojen tuomista varten. En ajatellut, että sitä käytetään konfiguraatioiden tallentamiseen. Mikä pitää paikkansa?

RCS on suunnittelupalvelu, jossa voi luoda ja muokata ER-konfiguraatioita. RCS:llä on oma tietovarasto, jota kutsutaan yleistietovarastoksi. Tätä tietovarastoa käytetään RCS:ssä luotujen konfiguraatioiden tallentamiseen. Kun LCS-järjestelmän käyttö tallennukseen on vanhentunut, yleinen tietovarasto on ainoa Microsoft-konfiguraatioiden lähde. Sinun on suoritettava kertatoiminto, jotta voit tuoda kaikki tarvittavat konfiguraatiot LCS:stä RCS:ään ja julkaista ne sitten RCS:stä yleistietovarastoon.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Ilman LCS:ää, mikä on ehdotettu tapa tallentaa konfiguraatiot niin, että "testi" ja "tuotanto" -konfiguraatioita voi helposti hallita ja siirtää?

RCS käyttää *liitetyn sovelluksen* käsitettä. Liitetty sovellus muodostaa yhteyden RCS:n ja kaikkien talous- ja toimintosovellusten esiintymien välille. Koska RCS:n avulla voidaan muokata konfiguraatioita, liitettyä sovellusta voidaan käyttää viemällä konfiguraatiot suoraan suunnitteluohjelmasta talous- ja toimintosovellusympäristöihin. Näin ollen voit nopeasti muuttaa ja testata konfiguraatioita sen sijaan, että käyt läpi LCS:n projektitason varastoa.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Onko joitakin esimerkkejä, jotka näyttävät määritykset ja hallinnan?

Esimerkkejä ei ole, mutta voit edellä tämän ohjeaiheen vaiheiden mukaisesti siirtääksesi konfiguraatiosi RCS:n yleistietovarastoon.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Onko RCS edellytys sähköisen raportoinnin määritykselle?

Kyllä. RCS sisältää ominaisuuksia, jotka tukevat globalisointiominaisuuksia, joita globalisointipalvelut, kuten sähköinen laskutus ja veronlaskentapalvelu, käyttävät. Palvelulla on kuitenkin sama visuaalinen suunnittelutoiminto, jonka avulla voit laajentaa tai luoda uusia ER-määrityksiä. RCS tarjoaa myös elinkaarihallintaa sekä ER-määrityksille että globalisointiominaisuuksille.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Millä alueilla RCS voidaan ottaa käyttöön?

RCS on käytettävissä seuraavilla Azure-alueilla:

- Yhdysvallat
- Intia
- Ranska
- Eurooppa

Lisätietoja tuotetuesta: [Dynamicsin globalisointipalvelujen yleiskatsaus](globalization-services-overview.md). Lisätietoja maantieteellisestä tuesta: [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja localization](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Mitä RCS:n käyttö maksaa?

RCS ja globalisointisäilö tarjotaan maksutta osana olemassa olevia talous- ja toimintosovellusten käyttöoikeuksia. RCS:n suunnittelutoiminnon käytöstä tai määritysten tallennuksesta yleiseen säilöön ei aiheudu erillisiä kustannuksia. Määritysten tai yhdistettyjen sovellusten määrää ei tällä hetkellä ole rajoitettu.