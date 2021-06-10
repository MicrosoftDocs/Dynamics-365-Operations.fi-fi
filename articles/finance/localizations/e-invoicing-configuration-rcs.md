---
title: Sähköisen laskutuksen määrittäminen Regulatory Configuration Services (RCS) -palvelussa
description: Tässä ohjeaiheessa on tietoja Dynamics 365 Regulatory Configuration Servicesin (RCS) sähköisen laskutuksen määrittämisestä.
author: gionoder
ms.date: 05/19/2021
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
ms.openlocfilehash: 6c1d309744c4c8dd0d17f5259551d31c257ede61
ms.sourcegitcommit: 633d51834d7d29b745824924315a3898dc471f1a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2021
ms.locfileid: "6075140"
---
# <a name="configure-electronic-invoicing-in-regulatory-configuration-services-rcs"></a>Sähköisen laskutuksen määrittäminen Regulatory Configuration Services (RCS) -palvelussa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja Dynamics 365 Regulatory Configuration Servicesin (RCS) sähköisen laskutuksen konfigurointiominaisuuksista.

Sähköinen laskutus auttaa sähköisten laskujen liiketoiminta- ja sääntelyvaatimusten saavuttamisessa tarvitsematta tehdä koodausta. Skenaarioissa, joissa verkkopalveluiden on hyväksyttävä sähköiset laskut sähköisesti, konfigurointiominaisuudet auttavat myös viestinvaihdossa verkkopalvelujen kanssa ilman koodia.

## <a name="electronic-reporting"></a>Sähköinen raportointi

Sähköinen raportointi (ER) tukee sähköistä laskutusta.

Tietomallien määritys ja muodot ovat konfiguroitavissa olevia komponentteja, jotka luodaan ja ylläpidetään ER:n kautta ja joita käytetään sähköisessä laskutuksessa. ER-muotosuunnittelu on työkalu, jolla luodaan ja ylläpidetaan tiedostomuotoja. Sitä käytetään sähköisen laskutuksen ominaisuuksien konfiguroinnissa.

Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) yleiskuvaus](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

## <a name="electronic-invoicing-features"></a>Sähköisen laskutuksen ominaisuudet

Sähköisen laskutuksen ominaisuudet vastaavat sähköisten laskujen luomisesta sähköisen laskutuksen kautta. Ne keräävät konfiguraatiosäännöt ja käyttävät niitä niiden tietojen käsittelemiseen, joita Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management lähettävät sähköiseen laskutukseen ja sähköisiin laskuihin.

Toiminnot tukevat myös skenaarioita, joissa tiedostomuotomääritysten säännöstenmukaisuus on pakollista ja tulostus on erillinen sähköinen tiedosto. Useimmissa tapauksissa veroviranomainen julkaisee tiedostomuotomääritykset.

Toiminnot tukevat sanomien vaihtoa ulkoisten Internet-palvelujen kanssa, joita joko veroviranomainen tai jokin valtuutettu osapuoli isännöi, jotta voidaan pyytää valtuutusta tai hyväksyntäleimaa tai sähköiseen laskuun.

### <a name="availability-of-electronic-invoicing-features"></a>Sähköisten laskutusominaisuuksien käytettävyys

Sähköisten laskutusominaisuuksien käytettävyys määräytyy maan tai alueen mukaan. Vaikka jotkin toiminnot ovat yleisesti saatavilla, jotkin ovat esiversio-ominaisuuksia.

#### <a name="generally-available-features"></a>Yleisesti käytettävissä olevat toiminnot

Seuraavassa taulukossa näkyvät sähköiset laskutusominaisuudet, jotka ovat yleisesti saatavilla.

| Maa tai alue | Toiminnon nimi                         | Yritysasiakirja |
|----------------|--------------------------------------|-------------------|
| Egypti          | Egyptin sähköinen lasku (EG) | Myyntilaskut ja projektilaskut |

#### <a name="preview-features"></a>Esiversio-ominaisuudet

Seuraavassa taulukossa näkyvät sähköiset laskutusominaisuudet, jotka ovat esiversiona.

| Maa tai alue | Toiminnon nimi                         | Yritysasiakirja |
|----------------|--------------------------------------|-------------------|
| Itävalta        | Itävallan sähköiset laskut (AT)    | Myyntilaskut ja projektilaskut |
| Belgia        | Belgian sähköinen lasku (BE)      | Myyntilaskut ja projektilaskut |
| Brasilia         | Brasilian NF-e (BR)                  | Veroasiakirjamalli 55, oikaisukirjeet, peruutukset ja hylkäämiset |
| Brasilia         | Brasilian NFS-e ABRASF Curitiba (BR) | Palvelun veroasiakirjat |
| Tanska        | Tanskan sähköinen lasku (DK)       | Myyntilaskut ja projektilaskut |
| Viro        | Viron sähköinen lasku (EE)     | Myyntilaskut ja projektilaskut |
| Suomi        | Suomen sähköinen lasku (FI)      | Myyntilaskut ja projektilaskut |
| Ranska         | Ranskan sähköinen lasku (FR)       | Myyntilaskut ja projektilaskut |
| Saksa        | Saksan sähköinen lasku (DE)       | Myyntilaskut ja projektilaskut |
| Italia          | FatturaPA (IT)                       | Myyntilaskut ja projektilaskut |
| Meksiko         | Meksikon CFDI (MX)                    | Myyntilaskut, pakkausluettelot, varastosiirrot, maksutäydennykset ja peruutukset |
| Alankomaat    | Alankomaiden sähköinen lasku (NL)        | Myyntilaskut ja projektilaskut |
| Norja         | Norjan sähköinen lasku (NO)    | Myyntilaskut ja projektilaskut |
| Espanja          | Espanjan sähköinen lasku (ES)      | Myyntilaskut ja projektilaskut |
| Eurooppa         | Sähköinen PEPPOL-lasku            | PEPPOL-myyntilaskut ja -projektilaskut |

### <a name="configurable-components-of-electronic-invoicing-features"></a>Sähköisen laskutuksen ominaisuuksien konfiguroitavissa olevat komponentit

Sähköisen laskutuksen ominaisuudet koostuvat seuraavista konfiguroitavissa olevien komponenttien ryhmistä:

- **Muodot** – Muotojen avulla voit määrittää, mitä sähköisen laskutuksen on luotava, kun sähköisestä asiakirjasta tulee sähköinen lasku. Muotoja ovat sähköisen laskun muotomääritys sekä tiedostojen ja sanomien muoto, joita käytetään pyyntöjen lähettämiseen ja vastausten vastaanottamiseen, kun ulkoisen Internet-palvelun kanssa tarvitaan viestintää.
- **Toiminnot** – Toimintojen avulla voit määrittää, miten sähköinen laskutus luo sähköisen tiedoston muuntamisen, jonka Finance ja Supply Chain Management ovat lähettäneet sähköiseksi laskuksi.
- **Käytettävyyssäännöt** – Käytettävyyssääntöjen avulla voit konfiguroida kontekstin, jonka sähköisen laskutuksen on otettava huomioon käsiteltäessä sähköisen laskutuksen ominaisuutta.
- **Muuttujat** – Muuttujien avulla voit määrittää konfiguraatiologiikan rakenteen tuen. Muuttujia voidaan käyttää arvojen syötteenä tietyn toiminnon suorittamiseen. Vaihtoehtoisesti ne voivat toimia arvojen vaihdossa Financen ja Supply Chain Managementin sekä sähköisen laskutuksen välillä.
- **Sähköisen tiedostomallin määritys** – Sähköisen asiakirjamallin määrityksen avulla voit konfiguroida ER-mallimäärityksen. Mallimääritys määrittää abstraktin laskun tietomäärityksen, joka integroidaan sähköiseen laskutukseen sähköisiä tiedostoja lähetettäessä.
- **Laskun kontekstimalli** – Laskun kontekstimallin avulla voit konfiguroida ER-laskun kontekstimallin ja määrittää sähköisen laskutusominaisuuden kontekstin.
- **Vastaustyypit** – Vastaustyyppien avulla voit konfiguroida, mitä sähköisen laskutuksen on päivitettävä Financessa ja Supply Chain Managementissa sähköisen laskun käsittelyn tuloksena.

### <a name="formats"></a>Muodot

Seuraavissa luetteloissa näkyvät sähköisen laskutuksen ominaisuuksissa käytettävissä olevat ER-muotokonfiguraatiot.

#### <a name="austrian-at-electronic-invoices-sales-and-project-invoices-for-austria"></a>Itävaltalaiset (AT) sähköiset laskut: Itävallan myynti- ja projektilaskut

- OIOUBL-myyntilasku
- OIOUBL-projektilasku
- OIOUBL-myyntihyvityslasku
- OIOUBL, projektin hyvityslasku

#### <a name="belgian-be-electronic-invoice-sales-and-project-invoices-for-belgium"></a>Belgian (AT) sähköinen lasku: Belgian myynti- ja projektilaskut

- UBL-myyntilasku BE
- UBL-projektilasku BE
- UBL, projektin hyvityslasku, BE
- UBL, myynnin hyvityslasku, BE

#### <a name="brazilian-br-nf-e-nf-e-federal-brazil"></a>Brasilian (BR) NF-e: NF-e Federal (Brasilia)

- NF-e-lähetyksen vientimuoto(BR)
- NF-e-oikaisukirjeen vientimuoto (BR)
- NF-e-peruutuksen vientimuoto (BR)
- NF-e-hylkäyksen vientimuoto (BR)

#### <a name="brazilian-nfs-e-br-nfs-e-abrasf-curitiba-city"></a>Brasilian NFS-e (BR): NFS-e ABRASF Curitiba city

- NFS-e ABRASF Curitiba (BR)
- NFS-e ABRASF Inquire Curitiba (BR)

#### <a name="danish-dk-electronic-invoice-sales-and-project-invoices-for-denmark"></a>Tanskan (DK) sähköinen lasku: Tanskan myynti- ja projektilaskut

- OIOUBL-myyntilasku
- OIOUBL-projektilasku
- OIOUBL-myyntihyvityslasku
- OIOUBL, projektin hyvityslasku

#### <a name="dutch-nl-electronic-invoice-sales-and-project-invoices-for-netherlands"></a>Alankomaiden (AT) sähköinen lasku: Alankomaiden myynti- ja projektilaskut

- UBL-myyntilasku NL
- UBL-projektilasku NL
- UBL, projektin hyvityslasku, NL
- UBL, myynnin hyvityslasku, NL

#### <a name="egyptian-eg-electronic-invoice-sales-and-project-invoices-for-egypt"></a>Egyptin (EG) sähköinen lasku: Egyptin myynti- ja projektilaskut

- Myyntilasku (EG)(Laskutus)
- Projektilasku (EG)(Laskutus)

#### <a name="estonian-ee-electronic-invoice-sales-and-project-invoices-for-estonia"></a>Viron (EG) sähköinen lasku: Viron myynti- ja projektilaskut

- Myyntilasku (EE)
- Projektilasku (EE)

#### <a name="finnish-fi-electronic-invoice-sales-and-project-invoices-for-finland"></a>Suomen (FI) sähköinen lasku: Suomen myynti- ja projektilaskut

- Myyntilasku (FI)
- Projektilasku (FI)

#### <a name="french-fr-electronic-invoice-sales-and-project-invoices-for-france"></a>Ranskan (EG) sähköinen lasku: Ranskan myynti- ja projektilaskut

- UBL-myyntilasku (FR)
- UBL-projektilasku FR
- UBL, projektin hyvityslasku, FR
- UBL, myynnin hyvityslasku, FR

#### <a name="german-de-electronic-invoice-sales-and-project-invoices-for-germany"></a>Saksan (DE) sähköinen lasku: Saksan myynti- ja projektilaskut

- Myyntilasku (DE)
- Projektilasku (DE)

#### <a name="italian-it-electronic-invoice-sales-and-project-invoices-for-italy"></a>Italian (IT) sähköinen lasku: Italian myynti- ja projektilaskut

- Myyntilasku (IT)
- Projektilasku (IT)

#### <a name="mexican-mx-cfdi-cfdi-for-mexico"></a>Meksikon (MX) CFDI: CFDI – Mexico

- CFDI-laskumuoto (MX)
- CFDI-pakkausluettelo (MX)
- CFDI-varastosiirto (MX)
- CFDI-maksumuoto (MX)
- CFDI-laskuperuutusmuoto (MX)

#### <a name="norwegian-no-electronic-invoice-sales-and-project-invoices-for-norway"></a>Norjan (NO) sähköinen lasku: Norjan myynti- ja projektilaskut

- OIOUBL-myyntilasku
- OIOUBL-projektilasku
- OIOUBL-myyntihyvityslasku
- OIOUBL, projektin hyvityslasku

#### <a name="peppol-electronic-invoice-peppol-sales-and-project-invoices"></a>PEPPOL – sähköinen lasku: PEPPOL-myynti- ja projektilaskut

- PEPPOL-myyntilasku
- PEPPOL-projektilasku
- PEPPOL, myynnin hyvityslasku
- PEPPOL, projektin hyvityslasku

#### <a name="spanish-es-electronic-invoice-sales-and-project-invoices-for-spain"></a>Espanjan (ES) sähköinen lasku: Espanjan myynti- ja projektilaskut

- Myyntilasku (ES)
- Projektilasku (ES)

Sähköisen laskutuspalvelun kanssa käytettävissä olevista ER-muotokonfiguraatioista voit luoda myös omia ER-muotokonfiguraatioita. Sähköisen laskutuksen ominaisuuksissa käytettävät muotokonfiguraatiot eivät kuitenkaan tue suoraa viittausta Financen tai Supply Chain Managementin tauluihin tai vastaaviin metatietoihin. Vain viitteitä ER-mallin määritykseen tuetaan.

### <a name="actions"></a>Toimenpiteet

Seuraavassa taulukossa on lueteltu käytettävissä olevat toiminnnot sekä tiedot siitä, ovatko ne tällä hetkellä yleisesti käytettävissä vai vielä esiversiona.

| Toimenpide                                        | kuvaus                                                                  | Käytettävyys         |
|-----------------------------------------------|------------------------------------------------------------------------------|----------------------|
| Muunna asiakirja                            | Muunna tiedosto suorittamalla sähköinen raportointimuoto.                   | Yleisesti saatavilla  |
| Allekirjoita XML-tiedosto                             | Allekirjoita XML-tiedostoja digitaalisella allekirjoituksella.                                   | Esiversiossa           |
| Allekirjoita JSON-asiakirja Egyptin veroviranomaiselle | Allekirjoita JSON-asiakirjoja Egyptin veroviranomaiselle digitaalisella allekirjoituksella.       | Yleisesti saatavilla  |
| Integroi Egyptin ETA-palvelun kanssa           | Viestintä Egyptin veroviranomaisen kanssa.                                     | Yleisesti saatavilla  |
| Brasilian SEFAZ-palvelun kutsuminen                  | Integroi Brasilian SEFAZ-palvelun kanssa veroasiakirjojen lähetystä varten.       | Esiversiossa           |
| Kutsu Meksikon PAC-palvelua                      | Integroi Meksikon PAC-palvelun kanssa CFDI-lähetystä varten.                      | Esiversiossa           |
| Käsittele vastaus                              | Analysoi verkkopalvelukutsusta saatu vastaus.                     | Yleisesti saatavilla  |
| Käytä MS Power Automatea                         | Integroi Microsoft Power Automatella luodun työnkulun kanssa.                       | Esiversiossa           |

### <a name="applicability-rules"></a>Soveltuvuussäännöt

Sovellettavuussäännöt ovat konfiguroitavissa olevia lauseita, jotka on määritetty sähköisen laskutuksen ominaisuustasolla. Säännöt on määritetty antamaan konteksti sähköisen laskutuksen ominaisuuksien suoritukselle sähköisen laskutuksen ominaisuusjoukon avulla.

Kun Financen tai Supply Chain Managementin liiketoiminta-asiakirja lähetetään sähköiseen laskutukseen, liiketoiminta-asiakirjassa ei ole täsmällistä viitettä, jonka avulla sähköinen laskutustoiminto voi kutsua tiettyä sähköistä laskutustoimintoa lähetyksen käsittelemiseksi.

Kun liiketoiminta-asiakirja on konfiguroitu oikein, se sisältää tarvittavat elementit, joiden avulla sähköinen laskutus voi ratkaista sähköisen laskutuksen, minkä ominaisuuden on oltava valittuna, ja muodostaa sitten sähköisen laskun.

Sovellettavuussääntöjen avulla sähköinen laskutustoiminto voi etsiä lähetyksen suorittamisessa käytettävät tarkat sähköiset laskutusominaisuudet. Tämä tapahtuu täsmäyttämällä lähetetyn liiketoiminta-asiakirjan sisältö ja sovellettavuussääntöjen lausekkeet.

Esimerkiksi kaksi sähköistä laskutustoimintoa, joissa on liittyvät käytettävyyssäännöt, otetaan käyttöön sähköisen laskutuksen ominaisuussarjassa.

| Sähköisen laskutuksen ominaisuus | Soveltuvuussäännöt        |
|------------------------------|--------------------------- |
| A                            | <p>Maa = BR</p><p>ja</p><p>Yritys = BRMF</p>  |
| D                            | <p>Maa = MX</p><p>ja</p><p>Yritys = MXMF</p>  |

Jos Financen tai Supply Chain Managementin liiketoiminta-asiakirja lähetetään sähköisen laskutuksen toimintosarjaan, liiketoiminta-asiakirja sisältää seuraavat määritteet:

- Maa = BR
- Yritys = BRMF

Sähköisen laskutuksen toimintosarja valitsee sähköisen laskutusominaisuuden **A**, joka käsittelee lähetyksen ja luo sähköisen laskun.

Jos yritysasiakirja sisältää samalla tavalla seuraavat tiedot:

- Maa = MX
- Yritys = MXMF

Sähköisen laskutuksen toiminto **B** on valittuna, kun haluat luoda sähköisen laskun.

Käytettävyyssääntöjen konfigurointi ei voi olla tulkinnanvarainen. Tämä tarkoittaa, että vähintään kahdella sähköisellä laskutusominaisuudella ei voi olla samoja lauseita, muussa tapauksessa se ei tuota valintaa. Jos sähköisen laskutusominaisuuden kaksoiskappaleet ovat olemassa, voit välttää tulkinnanvaraisuuden käyttämällä lisälausekkeita, joiden avulla sähköinen laskutustoiminto erottuu toisistaan kahden sähköisen laskutusominaisuuden välillä.

Harkitse esimerkiksi sähköistä laskutustoimintoa **C**. Tämä ominaisuus on kopio sähköisestä laskutuksesta **A**.

| Sähköisen laskutuksen ominaisuus | Soveltuvuussäännöt        |
|------------------------------|--------------------------- |
| A                            | <p>Maa = BR</p><p>ja</p><p>Yritys = BRMF</p>  |
| K                            | <p>Maa = BR</p><p>ja</p><p>Yritys = BRMF</p>  |

Tässä esimerkissä toiminto **C** on yritysasiakirjan lähetyksen edessä, ja se sisältää seuraavat tiedot:

- Maa = BR
- Yritys = BRMF

Sähköisen laskutuksen avulla ei voi erottaa toisistaan sähköistä laskutustoimintoa, jota lähetyksen käsittelemiseen käytetään, koska lähetykset sisältävät samat lausekkeet.

Jotta näiden kahden ominaisuuden välille voidaan luoda käytettävyyssäännön avulla uusi lauseke, on lisättävä uusi lauseke, jotta sähköisen laskutuksen ominaisuus voi valita oikean sähköisen laskutuksen.

| Sähköisen laskutuksen ominaisuus | Soveltuvuussäännöt        |
|------------------------------|--------------------------- |
| A                            | <p>Maa = BR</p><p>ja</p><p>Yritys = BRMF</p>  |
| K                            | <p>Maa = BR</p><p>ja</p><p>Yritys = BRMF</p><p>ja</p><p>Malli=55</p>  |

Jotta voit luoda monimutkaisempia lauseita, käytettävissä ovat seuraavat resurssit:

Logiikan operaattorit:
- Ja
- Tai

Operaattorityypit:
- Equal
- Not equal
- Greater than
- Less than
- Suurempi tai yhtä suuri
- Pienempi tai yhtä suuri
- Contains
- Alkaa

Tietotyypit:
- Merkkijono
- Numero
- Boolen arvo
- Päivämäärä
- UUID

Kyky ryhmitellä ja poistaa lausekkeiden ryhmityksiä.
Esimerkki näyttää tältä.

| Sähköisen laskutuksen ominaisuus | Soveltuvuussäännöt        |
|------------------------------|--------------------------- |
| K                            | <p>Maa = BR</p><p>ja</p><p>(Yritys = BRMF</p><p>tai</p><p>Malli=55)</p>  |


## <a name="configuration-providers"></a>Konfiguraation tarjoajat

Konfigurointitoimittajat tarjoavat sähköisen laskutuksen ominaisuudet ja niiden ER-komponentit, kuten mallin määrityksen, muodon konfiguraation ja kontekstimallin. Ne julkaisevat sähköisen laskutuksen ominaisuudet ja ER-komponentit liittyvässä yleisessä tietovarastossa. Muut organisaatiot voivat ladata ne sieltä.

Ennen kuin konfiguroit sähköisen laskutuksen toiminnot RCS:n kautta, sinun on määritettävä oma organisaatiosi **Sähköinen raportointi** -moduulissa konfiguraatiopalveluksi. Tietoja konfiguraatiopalvelun arvon **Aktiivinen**-muotoon määrittämisestä: [Luo määrityspalveluja ja merkitse ne aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="viewing-electronic-invoicing-features-in-the-global-repository"></a>Sähköisten laskutusominaisuuksien tarkasteleminen yleisessä tietovarastossa

Synkronoi organisaation RCS-esiintymä, kun haluat selata tietyn konfiguraation tarjoajan yleisessä tietovarastossa käytettävissä olevia sähköisiä laskutustoimintoja. Kun synkronointi on valmis, käytettävissä olevien sähköisten laskutusominaisuuksien luettelo päivitetään.

## <a name="importing-electronic-invoicing-features"></a>Sähköisten laskutuksenominaisuuksien tuominen

Ennen sähköisten laskutusominaisuuksien käyttöä tai konfiguroimista ne on tuotava organisaation RCS-esiintymään. Tuontitoiminto luo ominaisuukisen paikallisen kopion ja kopioi kaikki ER-artefaktit, joita toiminnot käyttävät (esimerkiksi muotokonfiguraatiot ja mallikonfiguraatiot) organisaation RCS-esiintymään.

Voit tuoda sähköisen laskutuksen ominaisuudet mistä tahansa konfiguraatiopalvelusta.

## <a name="creating-electronic-invoicing-features"></a>Sähköisten laskutuksenominaisuuksien luominen

Voit joko luoda sähköisen laskutuksen toiminnon tyhjästä tai johtaa sen aiemmin luodusta sähköisen laskutuksen toiminnosta.

Kun luot sähköisen laskutusominaisuuden tyhjästä, sinun on lisättävä ER-komponentit (kuten toimintoversion konfiguraatiot ja muut konfiguraatiot, kuten toimintoversion asetukset ja sovelluksen asetukset) manuaalisesti. Kun luot ominaisuuden johtamalla sen toisesta ominaisuudesta, uusi ominaisuus perii kaikki konfiguraatiot alkuperäisestä ominaisuudesta. 

## <a name="electronic-invoicing-feature-version"></a>Sähköisen laskutuksen ominaisuuden versio

Sähköisen laskutuksen ominaisuuksilla on versiot. Kun uusi versio luodaan, versionumero kasvaa automaattisesti. Uudelle versiolle voidaan määrittää voimaantulopäivämäärä.

Sähköiset laskutusominaisuusversiot seuraavat elinkaarta, jossa voi olla kolme tilaa:

- **Luonnos** – Jos toimintoversio on tässä tilassa, voit muokata sen konfigurointimääritteitä ja sen artefakteja (esimerkiksi tiedostomuodon konfiguraatioita).
- **Valmis** – Jos toimintoversio on tässä tilassa, se on julkaistu organisaatioosi liittyvässä yleisessä tietovarastossa. Et voi enää muokata toimintoversiota tai ER-komponentteja.
- **Julkaistu** – Jos toimintoversio on tässä tilassa, se on julkaistu sähköisessä laskutuksessa. Et voi enää muokata toimintoversiota tai ER-komponentteja.

### <a name="feature-configurations"></a>Ominaisuuden konfiguraatiot

Toimintokonfiguraatiot sisältävät kaikki sähköisen laskutuksen ominaisuuksien käyttämät ER-muotokonfiguraatiot. Kaikki sähköiset tiedostot, joita sähköinen laskutusominaisuus käyttää käsittelyn aikana, tulevat kyseisen ominaisuuden toimintokonfiguraatioihin lisätyistä muotokonfiguraatioista.

Ominaisuuskonfiguraatioiden avulla voit käyttää ER-muodon suunnittelutoimintoa, joka on muotokonfiguraatioiden luomiseen käytettävä ER-työkalu.

### <a name="feature-setup"></a>Ominaisuuden asetus

Ominaisuuksien asetuksia käytetään yhdessä ominaisuuskonfiguraatioiden kanssa. Kunkin toiminnon asetukset sisältävät joukon toimintoja, käytettävyyssääntöjä ja muuttujia, joiden avulla sähköinen laskutusominaisuus voi täyttää sähköisen laskun erityisvaatimukset.

### <a name="application-setup"></a>Sovelluksen asetukset

Sovelluksen asetukset täytyy liittää aiemmin luotuun liitettyyn sovellukseen.

Sovelluksen asetusten avulla voit konfiguroida sähköisen laskutusominaisuuden osan, joka on tehtävä Financessa ja Supply Chain Managementissa. Sähköisen laskutuksen ominaisuudesta riippumatta vähintään kolme konfiguroitavaa komponenttia ovat pakollisia:

- **Taulun nimi** – Financen ja Supply Chain Managementin yksikkö, joka sisältää kirjatut laskut ja johon sähköinen laskutustoiminto perustuu.
- **Konteksti** – ER:n avulla konfiguroidun laskun kontekstimallin nimi.
- **Liiketoiminta-asiakirjan yhdistämismääritys** – ER:n avulla konfiguroidun laskun yhdistämismallin nimi.

> [!IMPORTANT]
> Sovelluksen asetuksiin määritettyä konfiguraatiota voi tarkastella Financessa ja Supply Chain Managementissa. Siirry kohtaan **Organisaation hallinta \> Määritys \> Sähköisen asiakirjan parametri**. Valitse **Sähköinen asiakirja** -välilehdessä **Ota käyttöön** ja valitse sitten **Yhdistetty sovellus** -vaihtoehto.

### <a name="deploying-feature-versions"></a>Toimintoversioiden käyttöönotto

RCS:ssä käytetään **Ota käyttöön** -komentoa sähköisen laskutusominaisuusversion julkaisemiseen. Valitse **Ota käyttöön** ja määritä käyttöönoton kohde valitsemalla jokin seuraavista vaihtoehdoista: 

- **Palveluympäristö** – Kun käyttöönoton kohde on palveluympäristö, sähköisen laskutuksen ominaisuusversio julkaistaan palveluympäristössä. Sähköinen laskutus on tämän jälkeen valmis vastaanottamaan ja käsittelemään sähköisiä asiakirjoja, jotka Finance ja Supply Chain Management lähettävät.
- **Yhdistetty sovellus** – Kun kohde on liitetty sovellus, sovelluksen asetusten konfiguraatio on kirjoitettu aiemmin siihen liittyvässä Financen ja Supply Chain Managementin esiintymässä.

Vain sähköisiä laskutustoiminnon versioita, joiden tila on **Valmis**, voidaan ottaa käyttöön joko palveluympäristössä tai liitetyssä sovelluksessa.

### <a name="removing-feature-versions"></a>Toimintoversioiden poistaminen

RCS:ssä käytetään **Poista käytöstä** -komentoa tietyn sähköisen laskutusominaisuuden version poistamiseen palveluympäristöstä sähköisessä laskutuksessa.

> [!IMPORTANT]
> **Poista käytöstä** -komento toimii vain palveluympäristöissä. Se ei poista sähköisiä laskutusominaisuusversioita yhdistetyistä sovelluksista.

### <a name="rebasing-electronic-invoicing-features"></a>Sähköisten laskutuksenominaisuuksien pohjustaminen

Kun sähköinen laskutusominaisuus johdetaan toisesta ominaisuudesta, **Pohjusta**-komento päivittää johdettuun toimintoon muutokset, jotka on otettu käyttöön alkuperäisessä ominaisuudessa.

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisten laskujen lähettäminen Financessa ja Supply Chain Managementissa](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
