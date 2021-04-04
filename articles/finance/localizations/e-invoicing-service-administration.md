---
title: Sähköisen laskutuksen lisäosien hallintakomponentit
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592571"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Sähköisen laskutuksen lisäosien hallintakomponentit

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja sähköisen laskutuksen lisäosan hallintaan liittyvistä komponenteista. Se sisältää myös tietoja sähköisen laskutuksen lisäpalvelun konfiguroinnista.

## <a name="azure"></a>Azure

Microsoft Azuren avulla voit luoda avainsäilön ja tallennustilin salaisia koodeja. Käytä sen jälkeen sen salaisia koodeja sähköisen laskutuksen lisäosan konfiguroinnissa.

## <a name="lifecycle-services"></a>Lifecycle Services

Ota Microsoft DynamicsLifecycle Servicesin (LCS) avulla käyttöön lisäosa LCS-käyttöönottoprojektin mikropalveluille.

> [!NOTE]
> Mikropalveluiden lisäosan asennus LCS:ssä edellyttää vähintään Tier 2 -virtuaalikoneen asentamista. Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) on liittymä, jota käytetään sähköisen laskutuksen lisäosan määrittämisessä. Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja ylläpidetään RCS:ssä. Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen lisäpalvelussa.

Lisätietoja RCS-rekisteröitymisistä on kohdassa [Regulatory services](https://marketing.configure.global.dynamics.com/).

Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Sähköisen laskutuksen lisäosan integrointi

Ennen kuin sähköisten laskujen konfiguroinnissa voi käyttää RCS:ää, RCS on määritettävä sallimaan tietoliikenne sähköisen laskutuksen lisäosan kanssa. Tämä konfigurointi tehdään **Sähköisen raportoinnin parametrit** -sivun **Sähköisen laskutuksen lisäosa** -välilehdessä.

#### <a name="service-endpoint"></a>Palvelun päätepiste

Sähköisen laskutuksen lisäosa on käytössä useilla Azure-palvelinkeskusten maantieteellisillä alueilla. Seuraavassa taulukossa luetellaan käytettävyys alueittain.

| Azure-konesalin alue |
|----------------------------|
| Itä-Yhdysvallat                    |
| Länsi-Yhdysvallat                    |
| Pohjois-EU                   |
| Länsi-EU                    |

### <a name="service-environments"></a>Palveluympäristöt

Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen lisäosan sähköisten laskutusominaisuuksien suorittamista varten. Suojauksen salasanat ja digitaaliset varmenteet sekä hallinto (eli käyttöoikeudet) on määritettävä palveluympäristön tasolla.

Asiakkaat voivat luoda niin monta palveluympäristöä kuin haluavat. Kaikki asiakkaan luomat palveluympäristöt ovat toisistaan riippumattomia.

Palveluympäristöt on luotava ja ylläpidettävä RCS:ssä. Kun palveluympäristöt ovat valmiita, ne pitää julkaista sähköisen laskutuksen lisäosassa.

#### <a name="service-environment-status"></a>Palveluympäristön tila

Palveluympäristöjä voidaan hallita tilan kautta. Mahdolliset vaihtoehdot ovat:

- **Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.
- **Julkaistu** – Ympäristö on julkaistu sähköisen laskutuksen lisäosassa.
- **Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.

#### <a name="customer-secrets"></a>Asiakkaan salaiset koodit

Sähköisen laskutuksen lisäosapalvelu vastaa kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Azure-resursseihin. Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköisen laskutuksen lisäosaa varten tarvittavat ja sen luomat liiketoimintatiedot ovat vain lisäosan käytettävissä, on luotava kaksi keskeistä Azure-resurssia:

- Azure-tallennustili (Blob-tallennus) sähköisten laskujen tallentamista varten
- Azure-avainsäilö, johon tallennetaan tallennustilin tallennusvarmenteet ja Uniform Resource Identifier (URI)

> [!NOTE]
> Erillinen avainsäilö ja asiakkaan tallennustili on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen lisäosan kanssa.

Lisätietoja: [Azure-tallennustilin ja -avainsäilön luominen](e-invoicing-create-azure-storage-account-key-vault.md).

#### <a name="users"></a>Käyttäjät

Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista sähköisen laskutuksen lisäosaan.

#### <a name="publication"></a>Julkaisu

Palveluympäristöt pitää julkaista sähköisen laskutuksen lisäosassa, enne kuin niitä voi käyttää. Finance ja Supply Chain Management voivat käyttää vain julkaisuja ympäristöjä. Lisäksi palveluympäristö on julkaistava, ennen kuin sen määritteiden päivitykset tulevat voimaan sähköisessä laskutuspalvelussa.

### <a name="connected-applications"></a>Sovellukset, joista on muodostettu yhteys

Liitetyt sovellukset ovat ne Finance- ja Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä RCS:n kautta. Sovelluksen URL-osoitteen ja vuokraajan lisäksi liitetty sovellus sisältää tunnistetiedot, joiden avulla RCS voi muodostaa yhteyden ympäristöön.

Toisiinsa liitettyjen sovellusten avulla voit konfiguroida osan sähköistä laskutustoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköinen laskutustoiminto toimisi.

## <a name="finance-and-supply-chain-management"></a>Finance ja Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Sähköisen laskutuksen lisäosan integrointi

Ennen kuin Financea ja Supply Chain Managementia voidaan käyttää sähköisten laskujen lähettämiseen sähköisen laskutuksen lisäosan kautta, lisäosa on määritettävä niin, että se sallii viestinnän palvelun kanssa.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Sähköisen laskutuksen lisäosan integrointiominaisuus

Financen ja Supply Chain Managementin ja sähköisen laskutuksen lisäosan välisen viestinnän mahdollistamiseksi **Sähköisen laskutuksen lisäosan integrointi** -ominaisuus on otettava käyttöön **Ominaisuuden hallinta** -työtilassa.

#### <a name="service-endpoint"></a>Palvelun päätepiste

Palvelun päätepiste on URL-osoite, jossa sähköisen laskutuksen lisäosa sijaitsee. Ennen kuin sähköisiä laskuja voidaan lähettää palvelun päätepiste pitää määrittää Financessa ja Supply Chain Managementissa niin, että se sallii viestinnän palvelun kanssa.

Voit määrittää palvelun päätepisteen siirtymällä kohtaan **Organisaation hallinto \> Määritys \> Sähköisen asiakirjan parametri** ja kirjoita **Lähetyspalvelut**-välilehden **Sähköisen laskutuksen lisäosan URL-osoite** -kenttään URL-osoite, kuten on kuvattu osan **Palvelun päätepiste** -osan taulukossa.

#### <a name="environments"></a>Ympäristöt

Financeen ja Supply Chain Managementiin syötetty ympäristönimi viittaa RCS:ssä luotavaan ja sähköiseen laskutukseen lisäosaan julkaistavaan ympäristön nimeen.

Ympäristö on konfiguroitava **Sähköisen tiedoston parametri** -sivun **Lähetyspalvelut**-välilehdessä, jotta kaikki sähköisten laskujen lähetyspyynnöt sisältävät ympäristön, jossa sähköisen laskutuksen lisäosa voi määrittää, mikä sähköisen laskutuksen toiminto käsittelee pyynnön.

## <a name="additional-resources"></a>Lisäresurssit

- [Konfiguroi sähköiset laskut RCS:ssä](e-invoicing-configuration-rcs.md)
- [Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
