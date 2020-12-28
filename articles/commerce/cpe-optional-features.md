---
title: Valinnaisten toimintojen määrittäminen Dynamics 365 Commerce -arviointiympäristöä varten
description: Tässä ohjeaiheessa kerrotaan, miten valinnaiset toiminnot määritetään Microsoft Dynamics 365 Commercen arviointiympäristössä.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f7ba7e6de3791720458b509059f008423c73a82
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411866"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>Valinnaisten toimintojen määrittäminen Dynamics 365 Commerce -arviointiympäristöä varten

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten valinnaiset toiminnot määritetään Microsoft Dynamics 365 Commercen arviointiympäristössä.

## <a name="prerequisites"></a>Edellytykset

Jos haluat arvioida tapahtuman sähköpostiominaisuuksia, seuraavat edellytykset on täytettävä:

- Käytettävissä on sähköpostipalvelin (Simple Mail Transfer Protocol \[SMTP\]-palvelin), jota voi käyttää sen Microsoft Azure -tilauksen kanssa, jossa arviointiympäristö valmisteltiin.
- Sinulla on käytettävissä palvelimen täydellinen nimi (FQDN)/IP-osoite, SMTP-portin numero ja todennustiedot.

## <a name="configure-the-image-back-end"></a>Kuvan taustan määrittäminen

### <a name="find-your-media-base-url"></a>Median URL-perusosoitteen löytäminen

> [!NOTE]
> Ennen kuin voit suorittaa nämä toimet, sinun on suoritettava [sivuston määrittäminen Commercessa](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Kirjaudu Commercen sivustonmuodostimeen käyttämällä URL-osoitetta, johon olet tehnyt huomautuksen verkkokaupan valmistelusta valmistelun aikana (katso [verkkokaupan alustaminen](provisioning-guide.md#initialize-e-commerce)).
1. Avaa **Fabrikam**-sivusto.
1. Valitse vasemmalla olevasta valikosta **Mediakirjasto**.
1. Valitse jokin yksittäinen kuvaresurssi.
1. Etsi oikealta puolelta ominaisuuksien tarkistamisen **Julkinen URL** -ominaisuus. Arvo on URL-osoite. Tässä on esimerkki:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Korvaa URL-osoitteen viimeinen tunniste (**MA1nQC** edellisessä esimerkissä) seuraavalla merkkijonolla **search?fileName=**. Tässä on esimerkki siitä, miltä URL-osoite näyttää tämän muutoksen jälkeen:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    Tämä URL-osoite on median perus-URL-osoite. Merkitse se muistiin.

### <a name="update-the-media-base-url"></a>Median URL-perusosoitteen päivittäminen

1. Kirjaudu sisään Commercen pääkonttoriversioon.
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Kanavan asetukset \> Kanavaprofiilit**.
1. Valitse **Muokkaa**.
1. Mene **Profiilin ominaisuudet** -kohdan alle, korvaa **Mediapalvelimen URL-perusosoite** -ominaisuus aiemmin luodulla Median URL-perusosoite -arvolla.
1. Valitse kanava, jonka nimi on **scXXXXXXXXX**.
1. Valitse **Profiilin ominaisuudet** -kohdassa **Lisää**.
1. Valitse lisättyjen ominaisuuksien kohdalla **Mediapalvelimen perus-URL-osoite** ominaisuusavaimeksi. Kirjoita ominaisuuden arvoksi aiemmin luomasi median perus-URL-osoitteen URL-osoite.
1. Valitse **Tallenna**.

## <a name="configure-and-test-the-email-server"></a>Sähköpostipalvelimen määrittäminen ja testaaminen

> [!NOTE]
> Tähän syötettävän SMTP-palvelimen tai sähköpostipalvelun on oltava käytettävissä ympäristössä käytettävän Azure-tilauksen avulla.

1. Kirjaudu sisään Commercen pääkonttoriversioon.
1. Valitse vasemman valikon avulla **Moduulit \> Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Sähköpostiparametrit**.
1. Kirjoita **SMTP-asetukset**-välilehden **Lähtevän postin palvelin** -kenttään SMTP-palvelimen tai sähköpostipalvelun FQDN-tai IP-osoite.
1. Kirjoita **SMTP-porttinumero**-kenttään porttinumero. (Jos et käytä Secure Sockets Layer \[SSL\]-suojausta, oletusportin numero on **25**.)
1. Jos todennus on pakollinen, kirjoita arvot **Käyttäjänimi**- ja **Salasana**-kenttiin.
1. Valitse **Tallenna**.
1. Valitse **Päivitä**.
1. Valitse **Testaa sähköposti** -välilehdellä **Sähköpostipalvelu**-kentässä **SMTP**.
1. Kirjoita **Lähetä**-kenttään sähköpostiosoite, johon testisähköpostiviesti tulee toimittaa.
1. Valitse **Lähetä testisähköpostiviesti**.

## <a name="configure-email-templates"></a>Sähköpostimallien määrittäminen

Jokaista tapahtumaa kohti, josta haluat lähettää sähköposteja, on päivitettävä sähköpostimalli, jossa on sallittu lähettäjän sähköpostiosoite.

1. Kirjaudu sisään Commercen pääkonttoriversioon.
1. Valitse vasemman valikon avulla **Moduulit \> Retail ja Commerce \> Pääkonttorin asetukset \> Parametrit \> Organisaation sähköpostimallit**.
1. Valitse **Näytä luettelo**.
1. Luo kukin luettelossa oleva malli seuraavasti:

    1. Kirjoita **Lähettäjän sähköpostiosoite** -kenttään lähettäjän sähköpostiosoite.
    1. Valinnainen: Kirjoita **Lähettäjän nimi** -kenttään nimi, jota käytetään lähettäjän nimenä.

1. Valitse **Tallenna**.

## <a name="customize-email-templates"></a>Mukauta sähköpostimalleja

Haluat ehkä mukauttaa sähköpostimalleja niin, että ne käyttävät eri kuvia. Tai haluat ehkä päivittää mallien linkit niin, että ne menevät arviointiympäristöön. Tässä menettelyssä kerrotaan, miten oletusmallit ladataan ja mukautetaan ja miten järjestelmän mallit päivitetään.

1. Lataa selaimessa [Microsoft Dynamics 365 Commerce -arviointisovelluksen oletussähköpostimallien zip-tiedosto](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) paikalliseen tietokoneeseen. Tämä tiedosto sisältää seuraavat HTML-asiakirjat:

    - Tilauksen vahvistuksen malli
    - Lahjakorttimallin lähettäminen
    - Uusi tilausmalli
    - Pakkaustilauksen malli
    - Keräystilauksen malli

1. Mukauta malleja teksti- tai HTML-editorin avulla. Katso [tuettujen tunnusten](#supported-tokens-in-the-email-template) luettelo myöhemmin tässä ohjeaiheessa.
1. Kirjaudu sisään Commerce-sovellukseen.
1. Siirry vasemmalla olevan valikon avulla kohtaan **Moduulit \> Organisaation hallinta \> Asetukset \> Organisaation sähköpostimallit**.
1. Laajenna vasemmanpuoleista luetteloa, niin näet kaikki mallit.
1. Noudata seuraavia vaiheita jokaiselle mukautettavan mallin kohdalle:

    1. Valitse luettelossa oleva malli.
    1. Valitse **Sähköpostiviestin sisältö** -kohdassa soveltuva kieliversio luettelosta. (Oletuskieli on **fi-fi**.)
    1. Valitse **Sähköpostiviestin sisältö** -kohdassa **Muokkaa**. **Lataa sähköpostimalli** -ruutu tulee näkyviin.
    1. Valitse **Selaa** ja Etsi HTML-tiedosto, jolla on mukautettu sisältö.
    1. Valitse **Lataa palvelimeen**. Malli ladataan järjestelmään ja näkyviin tulee esikatselu.
    1. Valitse **OK**.
    1. Valinnainen: Mukauta mallin **Aihe**-ominaisuutta.
    1. Valitse **Tallenna**.

### <a name="supported-tokens-in-the-email-template"></a>Sähköpostimallin tuetut tunnukset

Kun sähköposti lähetetään, nämä tunnukset korvataan todellisilla arvoilla, jotka koskevat asiakasta ja asiakkaan tilausta.

#### <a name="sales-order"></a>Myyntitilaus

Seuraavat tunnukset koskevat yleistä myyntitilausta.

| Tunnuksen nimi | Tunnus |
|-------------------|-------|
| Tilausnumero      | %salesid% |
| Asiakkaan nimi   | %customername% |
| Toimitusosoite  | %deliveryaddress% |
| Laskutusosoite   | %customeraddress% |
| Tilauspäivämäärä        | %shipdate% |
| Toimitustapa     | %modeofdelivery% |
| Alennus          | %discount% |
| Arvonlisävero         | %tax% |
| Tilauksen kokonaissumma       | %total% |

#### <a name="sales-line"></a>Myyntirivi

Seuraavat tunnukset korvataan arvoilla jokaisessa tuotteessa tilauksessa.

> [!NOTE]
> Sijoita **Tuoteluettelo - aloitus** -tunnus jokaiselle tuotteelle toistetun HTML-lohkon alkuun ja sijoita **Tuoteluettelo - lopetus** -tunnus lohkon loppuun.

| Tunnuksen nimi      | Tunnus |
|------------------------|-------|
| Tuoteluettelo - alku   | \<!--%tablebegin.salesline% --\> |
| Tuoteluettelo - loppu     | \<!--%tableend.salesline%--\> |
| Tuotteen nimi           | %lineproductname% |
| kuvaus            | %lineproductdescription% |
| Määrä               | %linequantity% |
| Rivin yksikköhinta        | %lineprice% (verify) |
| rivinimikkeen kokonaissumma        | %linenetamount% |
| rivin alennus          | %linediscount% |
| Lähetyspäivä              | %lineshipdate% |
| Hankintamenetelmä     | %linedeliverymode% |
| toimitusosoite       | %linedeliveryaddress% |
| Rivin myyntiyksikkö | %lineunit% |

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commerce -arviointiympäristön yleiskuvaus](cpe-overview.md)

[Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md)

[Dynamics 365 Commerce -arviointiympäristön määritykset](cpe-post-provisioning.md)

[BOPIS:n määritykset Dynamics 365 Commerce -arviointiympäristössä](cpe-bopis.md)

[Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure -portaali](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce -sivusto](https://aka.ms/Dynamics365CommerceWebsite)
