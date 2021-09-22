---
title: Sähköisen laskutuksen hallintakomponentit
description: Tässä ohjeaiheessa on tietoja sähköisen laskutuksen hallintaan liittyvistä komponenteista.
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463878"
---
# <a name="electronic-invoicing-administration-components"></a>Sähköisen laskutuksen hallintakomponentit

[!include [banner](../includes/banner.md)]


Tässä ohjeaiheessa on tietoja sähköisen laskutuksen hallintaan liittyvistä komponenteista. Se sisältää myös tietoja sähköisen laskutuksen palvelun konfiguroinnista.

## <a name="azure"></a>Azure

Microsoft Azuren avulla voit luoda avainsäilön salaisia koodeja ja määrittää tallennustilin. Sitten voit käyttää avainsäilön salaisia koodeja ja tallennustilin SAS-tunnusta sähköisen laskutuksen määrityksessä.

## <a name="lifecycle-services"></a>Lifecycle Services

Ota Microsoft Dynamics Lifecycle Servicesin (LCS) avulla käyttöön LCS-käyttöönottoprojektin sähköisen laskutuksen apuohjelma.

> [!NOTE]
> Apuohjelmien asennus LCS:ssä edellyttää vähintään **Tier 2 -ympäristöä**. Lisätietoja ympäristöjen suunnittelusta on kohdassa [Ympäristön suunnittelu](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) on liittymä, jota käytetään sähköisen laskutuksen määrittämisessä. Resursseja, kuten ympäristöjä ja sähköistä laskutusta, luodaan, ylläpidetään ja ylläpidetään RCS:ssä. Kun resurssit ovat valmiita, ne julkaistaan sähköisen laskutuksen palvelussa.

Lisätietoja RCS-rekisteröitymisistä on kohdassa [Regulatory services](https://marketing.configure.global.dynamics.com/).

Lisätietoja RCS:stä: [Regulatory Configuration Services (RCS) – globalisointitoiminnot](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Sähköisen laskutuksen integrointi 

Ennen kuin sähköisten laskujen konfiguroinnissa voi käyttää RCS:ää, RCS on määritettävä sallimaan tietoliikenne sähköisen laskutuksen kanssa. Tämä konfigurointi tehdään **Sähköisen raportoinnin parametrit** -sivun **Sähköinen laskutus** -välilehdessä.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Palvelun päätepiste

Sähköinen laskutus on käytössä useilla Azure-palvelinkeskusten maantieteellisillä alueilla. Seuraavassa taulukossa luetellaan käytettävyys alueittain.


| Konesalin Azure-alue | Palvelun päätepisteen URI-osoite                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Yhdysvallat              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Eurooppa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Iso-Britannia             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Aasia                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Palveluympäristöt

Palveluympäristöt ovat loogisia osioita, jotka luodaan sähköisen laskutuksen globalisaatio-ominaisuuksien suorittamista varten. Suojauksen salasanat ja digitaaliset varmenteet sekä hallinto (eli käyttöoikeudet) on määritettävä palveluympäristön tasolla.

Asiakkaat voivat luoda niin monta palveluympäristöä kuin haluavat. Kaikki asiakkaan luomat palveluympäristöt ovat toisistaan riippumattomia.

Palveluympäristöt on luotava ja ylläpidettävä RCS:ssä. Kun palveluympäristöt ovat valmiita, ne pitää julkaista sähköisessä laskutuksessa.

#### <a name="service-environment-status"></a>Palveluympäristön tila

Palveluympäristöjä voidaan hallita tilan kautta. Mahdolliset vaihtoehdot ovat:

- **Ei julkaistu** – Ympäristö on luotu, mutta sitä ei ole vielä julkaistu.
- **Julkaistu** – Ympäristö on julkaistu sähköisessä laskutuksessa.
- **Muutettu** – Julkaistun ympäristön määritteitä on muutettu, mutta muutoksia ei ole vielä julkaistu.

#### <a name="customer-secrets"></a>Asiakkaan salaiset koodit

Sähköinen laskutus vastaa kaikkien liiketoimintatietojen tallentamisesta yrityksen omistamiin Azure-resursseihin. Sen varmistamiseksi, että palvelu toimii oikein ja että kaikki sähköistä laskutusta varten tarvittavat ja sen luomat liiketoimintatiedot ovat asianmukaisesti käytettävissä, on luotava kaksi keskeistä Azure-resurssia:

- Azure-tallennustili (blob-tallennustila), johon tallennetaan sähköisiä asiakirjoja, kuten sähköisiä laskuja, asiakirjamuuntojen tuloksia ja vastuksia ulkopuolisilta verkkopalveluilta.
- Azuren avainsäilö, johon tallennetaan tallennustilin (SAS-tunnus) tallennusvarmenteet ja Uniform Resource Identifier (URI)


Erillinen Key Vault ja asiakkaan tallennustili on määritettävä nimenomaisesti käytettäväksi sähköisen laskutuksen kanssa. Lisätietoja: [Azure-tallennustilin ja Key Vaultin luominen](e-invoicing-create-azure-storage-account-key-vault.md).

Jos haluat seurata Key Vaultin kuntoa ja vastaanottaa hälytyksiä, voit määrittää Azure Monitorin Key Vaultille. Ottamalla Key Vault -lokikirjauksen käyttöön voit valvoa, miten, koska ja kuka käyttää Key Vaulteja. Lisätietoja on kohdassa [Azure Key Vaultin seuranta ja hälytykset](/azure/key-vault/general/alert) ja [Key Vault -lokikirjauksen käyttöönotto](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Parhaana käytäntönä salaisia koodeja kannattaa vaihtaa säännöllisesti. Lisätietoja on kohdassa [Salaisten koodien dokumentaatio](/azure/key-vault/secrets/).

#### <a name="users"></a>Käyttäjät

Jokaisessa palveluympäristössä on oltava luettelo käyttäjistä, jotka voivat muodostaa yhteyden Dynamics 365 Financesta tai Dynamics 365 Supply Chain Managementista sähköiseen laskutukseen.

#### <a name="publication"></a>Julkaisu

Palveluympäristöt pitää julkaista sähköisessä laskutuksessa, ennen kuin niitä voi käyttää. Finance ja Supply Chain Management voivat käyttää vain julkaisuja ympäristöjä. Lisäksi palveluympäristö on julkaistava, ennen kuin sen määritteiden päivitykset tulevat voimaan sähköisessä laskutuspalvelussa.

### <a name="connected-applications"></a>Sovellukset, joista on muodostettu yhteys

Liitetyt sovellukset ovat ne Finance- ja Supply Chain Management -esiintymät, joihin haluat ehkä ottaa yhteyttä RCS:n kautta. Sovelluksen URL-osoitteen ja vuokraajan lisäksi liitetty sovellus sisältää tunnistetiedot, joiden avulla RCS voi muodostaa yhteyden ympäristöön.

Toisiinsa liitettyjen sovellusten avulla voit konfiguroida osan sähköistä laskutustoimintoa Financessa ja Supply Chain Managementissa, jotta koko sähköinen laskutustoiminto toimisi.

## <a name="finance-and-supply-chain-management"></a>Finance ja Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Sähköisen laskutuksen integrointi

Ennen kuin Financea ja Supply Chain Managementia voidaan käyttää sähköisten laskujen lähettämiseen sähköisen laskutuksen kautta, laskutus on määritettävä niin, että se sallii viestinnän palvelun kanssa.

#### <a name="electronic-invoicing-integration-feature"></a>Sähköisen laskutuksen integrointiominaisuus

Financen ja Supply Chain Managementin ja sähköisen laskutuksen välisen viestinnän mahdollistamiseksi **Sähköisen laskutuksen integrointi** -ominaisuus on otettava käyttöön **Ominaisuuden hallinta** -työtilassa.

#### <a name="service-endpoint"></a>Palvelun päätepiste

Palvelun päätepiste on URL-osoite, jossa sähköinen laskutus sijaitsee. Ennen kuin sähköisiä laskuja voidaan lähettää palvelun päätepiste pitää määrittää Financessa ja Supply Chain Managementissa niin, että se sallii viestinnän palvelun kanssa.

Voit määrittää palvelun päätepisteen siirtymällä kohtaan **Organisaation hallinto \> Määritys \> Sähköisen asiakirjan parametrit** ja kirjoita **Sähköinen laskutus**-välilehden **Päätepisteen URL-osoite** -kenttään asianmukainen URL-osoite [Palvelun päätepiste](#svc-endpoint-uris) -osan taulukosta aiemmin tässä aiheessa.

#### <a name="environments"></a>Ympäristöt

Financeen ja Supply Chain Managementiin syötetty ympäristönimi viittaa RCS:ssä luotavaan ja sähköiseen laskutukseen julkaistavaan ympäristön nimeen.

Ympäristö on määritettävä **Sähköisen asiakirjan parametrit** -sivun **Sähköinen laskutus** -välilehdessä. Tällöin kaikki pyynnöt sähköisen laskun tekemiseksi sisältävät ympäristön, jossa sähköinen laskutus voi määrittää, mitä sähköisen laskutuksen ominaisuutta on käytettävä pyynnön käsittelyssä.

## <a name="additional-resources"></a>Lisäresurssit

- [Konfiguroi sähköiset laskut RCS:ssä](e-invoicing-configuration-rcs.md)
- [Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
