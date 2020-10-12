---
title: Sähköisen laskutuksen yleiskatsaus
description: Tässä aiheessa annetaan tietoja sähköisen laskutuksen lisäosasta Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b3445157efce6349b3febafb6c860260052f7d6c
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835944"
---
# <a name="electronic-invoicing-add-on-overview"></a>Sähköisen laskutuksen yleiskatsaus

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin sähköisen laskutuksen lisäosa on lisäosa on äärimmäisen skaalautuva usean vuokraajan palvelu, joka mahdollistaa sähköisten laskuasiakirjojen määritettävän prosessoinnin sekä määritettävän asiakirjanvaihdon. Käsittely- ja integrointisäännöt ovat täysin määritettävissä, ja logiikka suoritetaan Financen ja Supply Chain Managementin ulkopuolella. Palvelu on kohdistettu pääasiassa sähköisten laskujen käsittelyyn yritysten ja valtioiden välisissä skenaarioissa, mutta se voidaan mukauttaa myös muihin tarkoituksiin.

Sähköisen laskutuksen lisäosa voi auttaa seuraavien tavoitteiden saavuttamisessa:

- Nopea ja helppo maa-/aluekohtaisten määritysten käyttöönotto
- Sähköisen laskutuksen lisäosaratkaisun vakioidut toimeenpanot
- Parannettu asiakirjahistorian jäljitettävyys
- Lyhyempi täytäntöönpanosykli
- Pienemmät kokonaiskustannukset (TCO)
- Helposti muokattavat määritykset, jotka eivät edellytä muutoksia koodiin
- Yksinkertaistettu määrityksen pakkaus
- Sisäänrakennettu vienti, tuonti ja integrointi sekä helppo laajennettavuus sähköisten laskuasiakirjojen käsittelyssä
- Samojen vienti-, tuonti-ja integrointimääritysten helppo uudelleenkäyttö eri yrityksissä

Jos haluat käyttää sähköisen laskutuksen lisäosaa, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesin (LCS) projektistasi. Noudata seuraavaksi määritysmenettelyä, jolla integrointi Financeen tai Supply Chain Managementiin otetaan käyttöön. Lisätietoja: [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md).

## <a name="availability"></a>Käytettävyys

Aluksi sähköisen laskutuksen lisäosa on valittujen asiakkaiden käytettävissä esikatseluohjelman kautta. Myöhemmin esikatselu avataan laajemmalle asiakaskunnalle. Lopuksi palvelu tulee yleisesti saataville. Koska maa-/aluekohtaisia vaatimuksia koskevat toiminnot saattavat olla rajoitettuja julkaisun eri vaiheissa, kannattaa aina tarkistaa ajantasaisin dokumentaatio, joka käsittelee tuettujen maa-/aluekohtaisten ratkaisujen kattavuutta ja laajuutta.

Sähköisen laskutuksen lisäosa otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla:

- Yhdysvallat
- Eurooppa

> [!NOTE]
> Sähköisen laskutuksen lisäosa ei tue paikallisia käyttöönottoja.

## <a name="extended-configurability"></a>Laajennettu määritettävyys

Sähköisen laskutuksen lisäosaa voidaan käyttää skenaarioissa, joissa on luotava ja lähetettävä sähköinen asiakirja tietyille osapuolille. Se on suunniteltu erityisesti määritettävän prosessointitehtävien kulun suorittamiseen vastaanotettujen tietojen perusteella. Financessa ja Supply Chain Managementissa käytettävissä olevat määritysvaihtoehdot rajoittuvat asiakirjan muuntamiseen. Palvelu laajentaa näitä asetuksia lisäämällä siinä käytettävissä olevat määritettävät integroinnit. Lisäksi kaikki aiemmin käytettävissä olleet sähköisen laskutuksen toiminnot, kuten Brasilian Nota fiscal eletrônica (NF-e), Meksikon Comprobante Fiscal Digital por Internet (CFDI) tai muu Western European Universal Business Language (UBL)- tai Pan-European Public Procurement OnLine (PEPPOL) -toiminto, alkavat käyttää määrityksiä viennille ja tuonnille sekä mahdollistamaan integrointeja ulkoisiin verkkopalveluihin.

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

- Käyttövalmis integrointi Financeen ja Supply Chain Managementiin
- Yhdenmukainen käyttökokemus kaikkien maiden tai alueiden sähköisen laskutusprosessin määrittämiseen ja seuraamiseen
- Nopeampi, helpompi ja edullisempi sähköisen laskutuksen lisäosaratkaisujen käyttöönotto uusissa maissa tai uusilla alueilla
- Palvelun määrittäminen Regulatory Configuration Servicen (RCS) ja globalisointitoiminnon määrityksen kautta
- Liiketoimintatietojen muuntaminen useisiin sähköisen laskutuksen muotoihin (XML, JavaScript Object Notation \[JSON\], TXT ja pilkuin erotetut arvot \[CSV\]) käyttämällä RCS:ssä määritettyjä määrityksiä:

    - Sähköisen raportoinnin muotoja, jotka ovat käytettävissä maille tai alueille, joissa sähköisen laskutuksen muuntamisen määritettävyys ei ole käytettävissä

- Sähköisten laskujen määritettävä lähettäminen ulkoisiin verkkopalveluihin, varmenteiden käsittely digitaalisten allekirjoitusten avulla mukaan luettuna:

    - Sisäänrakennettu, helposti laajennettava ja määritettävä integrointi lisäsisältöön useissa maissa

    > [!NOTE]
    > Tällä hetkellä tuetaan rajoitettua määrää suoria lähetyksiä. Lisätietoja on osassa [Käytettävyys](#availability) aiemmin tässä aiheessa. Tukea jatketaan tulevaisuudessa.

- Verkkopalveluiden vastausten käsittely, mukaan lukien määritettävä poikkeussanomien käsittely
- Sähköisten allekirjoitusten tuki (esimerkiksi XMLDSig-allekirjoitusalgoritmin avulla)
- Sähköisten laskujen sanomien eräkäsittely

## <a name="architecture-and-data-flow"></a>Arkkitehtuuri ja tiedonkulku

Kun sähköisen laskutuksen lisäosa asennetaan LCS:stä ja vaaditut määritykset suoritetaan kaikissa tarvittavissa sovelluksissa, muodostetaan suojattu yhteys. Palvelu sijaitsee tällä hetkellä palvelinkeskuksissa Yhdysvalloissa ja Euroopassa. Tämän vuoksi palvelun sijainti voi poiketa liittyvän Financen tai Supply Chain Managementin esiintymän sijainnista. Kun olet suorittanut sähköisen laskutuksen lisäosan määrittämisen ja otat integroinnin käyttöön, tiettyyn asiakirjaan liittyvät päätiedot ja siirtotiedot lähetetään sähköisen laskutuksen lisäosaan aina, kun sähköinen lasku lähetetään.

> [!NOTE]
> Jos sähköinen laskusi tai jokin muu asiakirja sisältää henkilötietoja, varmista, että tämän toiminnon käyttö on yleisen tietosuoja-asetuksen (GDPR) ja muiden henkilötietojen siirtämiseen liittyvien asetusten mukaista.

### <a name="high-level-description-of-the-data-flow"></a>Tietovuon ylätason kuvaus

1. Asiakasohjelma lähettää kanonisen liiketoimintatiedoston palveluun.
2. Palvelu valitsee sovellettavan käsittelytyönkulun asiakkaalta saatujen kontekstitietojen perusteella.
3. Palvelu suorittaa käsittelytoimet. Näitä toimia voivat olla esimerkiksi liiketoiminta-asiakirjan muuntaminen sähköiseksi laskuksi, sähköisen allekirjoituksen käyttäminen ja asiakirjan lähettäminen ulkoiseen verkkopalveluun.
4. Kaikki vastaanotetut ja käsitellyt asiakirjat tallennetaan asiakkaan Azure Blob -tallennustilaan.
5. Kaikki käsittelyyn käytetyt vuokralaisen salasanat ja varmenteet tallennetaan asiakkaan Azure-avainsäilöön.
6. Palvelu toimittaa asiakkaalle tarvittaessa tietoja lähetetyn liiketoiminta-asiakirjan käsittelytilasta.
7. Asiakas saa tietoja valmiiksi saadusta käsittelyn suorituksesta ja asettaa kaikki lokitiedot saataville. Se asettaa saataville myös työnkulun käsittelyn aikana luodun tai vastaanotetun asiakirjan.

Seuraavassa kuvassa näkyy, miten tieto kulkee sähköisen laskutuksen lisäosaan ja sieltä pois.

![Sähköisen laskutuksen lisäosan tietovuo](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Tietosuojatiedot
Sähköisen laskutuksen käyttöönotto ja käyttö saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä. Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten niissä esimääritetyssä muodoissa, jota integrointi valtion verkkopalveluihin edellyttää. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-get-started.md)
- [Brasilian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-bra-get-started.md)
- [Meksikon sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-mex-get-started.md)
- [Italian sähköisen laskutuksen lisäosan käytön aloittaminen](e-invoicing-ita-get-started.md)
- [Sähköisen laskutuksen lisäosan määrittäminen](e-invoicing-setup.md)
