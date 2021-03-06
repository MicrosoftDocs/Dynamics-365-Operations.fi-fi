---
title: Sähköisen laskutuksen yleiskatsaus
description: Tässä aiheessa annetaan tietoja sähköisestä laskutuksesta Microsoft Dynamics 365 Financessa ja Dynamics 365 Supply Chain Managementissa.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: a6a8ea3fcad980dc02f489e07a7b21fe1c1b5a5a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839977"
---
# <a name="electronic-invoicing-overview"></a>Sähköisen laskutuksen yleiskatsaus

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin sähköinen laskutus on lisäosa on äärimmäisen skaalautuva usean vuokraajan palvelu, joka mahdollistaa sähköisten laskuasiakirjojen määritettävän prosessoinnin sekä määritettävän asiakirjanvaihdon. Käsittely- ja integrointisäännöt ovat täysin määritettävissä, ja logiikka suoritetaan Financen ja Supply Chain Managementin ulkopuolella. Palvelu on kohdistettu pääasiassa sähköisten laskujen käsittelyyn yritysten ja valtioiden välisissä skenaarioissa, mutta se voidaan mukauttaa myös muihin tarkoituksiin.

Sähköinen laskutus voi auttaa seuraavien tavoitteiden saavuttamisessa:

- Nopea ja helppo maa-/aluekohtaisten määritysten käyttöönotto
- Sähköisen laskutuksen ratkaisun vakioidut toimeenpanot
- Parannettu asiakirjahistorian jäljitettävyys
- Lyhyempi täytäntöönpanosykli
- Pienemmät kokonaiskustannukset (TCO)
- Helposti muokattavat määritykset, jotka eivät edellytä muutoksia koodiin
- Yksinkertaistettu määrityksen pakkaus
- Sisäänrakennettu vienti, tuonti ja integrointi sekä helppo laajennettavuus sähköisten laskuasiakirjojen käsittelyssä
- Samojen vienti-, tuonti-ja integrointimääritysten helppo uudelleenkäyttö eri yrityksissä

Jos haluat käyttää sähköistä laskutusta, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesin (LCS) projektistasi. Noudata seuraavaksi määritysmenettelyä, jolla integrointi Financeen tai Supply Chain Managementiin otetaan käyttöön. Lisätietoja: [Sähköisen laskutuksen käytön aloittaminen](e-invoicing-get-started.md).

## <a name="service-availability"></a><a name="availability"></a>Palvelun käytettävyys

Tällä hetkellä sähköinen laskutus on asiakkaiden käytettävissä esiversio-ohjelman kautta, ja seuraavassa vaiheessa palvelu tulee yleisesti saataville. Koska maa-/aluekohtaisia vaatimuksia koskevat toiminnot saattavat olla rajoitettuja julkaisun eri vaiheissa, kannattaa aina tarkistaa ajantasaisin dokumentaatio, joka käsittelee tuettujen maa-/aluekohtaisten ratkaisujen kattavuutta ja laajuutta.

Sähköinen laskutus otetaan käyttöön seuraavilla Azuren maantieteellisillä alueilla:

- Yhdysvallat
- Eurooppa

> [!NOTE]
> Sähköinen laskutus ei tue paikallisia käyttöönottoja.

## <a name="extended-configurability"></a>Laajennettu määritettävyys

Sähköistä laskutusta voidaan käyttää skenaarioissa, joissa on luotava ja lähetettävä sähköinen asiakirja tietyille osapuolille. Se on suunniteltu erityisesti määritettävän prosessointitehtävien kulun suorittamiseen vastaanotettujen tietojen perusteella. Financessa ja Supply Chain Managementissa käytettävissä olevat määritysvaihtoehdot rajoittuvat asiakirjan muuntamiseen. Palvelu laajentaa näitä asetuksia lisäämällä siinä käytettävissä olevat määritettävät integroinnit. Lisäksi kaikki aiemmin käytettävissä olleet sähköisen laskutuksen toiminnot, kuten Brasilian Nota fiscal eletrônica (NF-e), Meksikon Comprobante Fiscal Digital por Internet (CFDI) tai muu Western European Universal Business Language (UBL)- tai Pan-European Public Procurement OnLine (PEPPOL) -toiminto, alkavat käyttää määrityksiä viennille ja tuonnille sekä mahdollistamaan integrointeja ulkoisiin verkkopalveluihin.

## <a name="feature-highlights"></a>Toiminnon tärkeimmät ominaisuudet

- Käyttövalmis integrointi Financeen ja Supply Chain Managementiin
- Yhdenmukainen käyttökokemus kaikkien maiden tai alueiden sähköisen laskutusprosessin määrittämiseen ja seuraamiseen
- Nopeampi, helpompi ja edullisempi sähköisen laskutuksen ratkaisujen käyttöönotto uusissa maissa tai uusilla alueilla
- Palvelun määrittäminen Regulatory Configuration Servicen (RCS) ja globalisointitoiminnon määrityksen kautta
- Liiketoimintatietojen muuntaminen useisiin sähköisen laskutuksen muotoihin (XML, JavaScript Object Notation \[JSON\], TXT ja pilkuin erotetut arvot \[CSV\]) käyttämällä RCS:ssä määritettyjä määrityksiä:

    - Sähköisen raportoinnin muotoja, jotka ovat käytettävissä maille tai alueille, joissa sähköisen laskutuksen muuntamisen määritettävyys ei ole käytettävissä

- Sähköisten laskujen määritettävä lähettäminen ulkoisiin verkkopalveluihin, varmenteiden käsittely digitaalisten allekirjoitusten avulla mukaan luettuna:

    - Sisäänrakennettu, helposti laajennettava ja määritettävä integrointi lisäsisältöön useissa maissa

    > [!NOTE]
    > Tällä hetkellä tuetaan rajoitettua määrää suoria lähetyksiä. Lisätietoja on osassa [Palvelun käytettävyys](#availability) aiemmin tässä aiheessa. Tukea jatketaan tulevaisuudessa.

- Verkkopalveluiden vastausten käsittely, mukaan lukien määritettävä poikkeussanomien käsittely
- Sähköisten allekirjoitusten tuki (esimerkiksi XMLDSig-allekirjoitusalgoritmin avulla)
- Sähköisten laskujen sanomien eräkäsittely

## <a name="architecture-and-data-flow"></a>Arkkitehtuuri ja tiedonkulku

Kun sähköinen laskutus asennetaan LCS:stä ja vaaditut määritykset suoritetaan kaikissa tarvittavissa sovelluksissa, muodostetaan suojattu yhteys. Palvelu sijaitsee tällä hetkellä palvelinkeskuksissa Yhdysvalloissa ja Euroopassa. Tämän vuoksi palvelun sijainti voi poiketa liittyvän Financen tai Supply Chain Managementin esiintymän sijainnista. Kun olet suorittanut sähköisen laskutuksen määrittämisen ja otat integroinnin käyttöön, tiettyyn asiakirjaan liittyvät päätiedot ja siirtotiedot lähetetään sähköiseen laskutukseen aina, kun sähköinen lasku lähetetään.

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

Seuraavassa kuvassa näkyy, miten tieto kulkee sähköiseen laskutukseen ja sieltä pois.

![Sähköisen laskutuksen tietovuo](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Tietosuojatiedot
Sähköisen laskutuksen käyttöönotto ja käyttö saattaa edellyttää rajoitettujen tietojen, joihin kuuluu organisaation verorekisteritunnus, lähettämistä. Ne välitetään kolmannen osapuolen virastoille, jotka veroviranomaiset ovat hyväksyneet sähköisten laskujen kyseiselle veroviranomaiselle lähettämistä varten niissä esimääritetyssä muodoissa, jota integrointi valtion verkkopalveluihin edellyttää. Näistä ulkoisista järjestelmistä tähän Dynamics 365 -verkkopalveluun tuotuihin tietoihin sovelletaan [tietosuojalausuntoamme](https://go.microsoft.com/fwlink/?LinkId=512132). Katso lisätietoja maakohtaisten toimintodokumentaatioiden tietosuojaosista.

## <a name="additional-resources"></a>Lisäresurssit
- [Palvelun hallinta](e-invoicing-service-administration.md)
- [Konfiguroi sähköiset laskut RCS:ssä](e-invoicing-configuration-rcs.md)
- [Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
