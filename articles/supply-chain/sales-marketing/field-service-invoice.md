---
title: Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin
description: Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Field Servicen sopimuslaskut synkronoidaan Dynamics 365 Supply Chain Managementiin vapaatekstilaskuihin.
author: Henrikan
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c4ef70af71ae223baaa2abb2b64428beab946e3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900880"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Field Servicen sopimuslaskujen synkronointi Supply Chain Managementin vapaatekstilaskuihin

[!include[banner](../includes/banner.md)]



Tässä artikkelissa käsitellään malleja ja taustalla olevia tehtäviä, joilla Dynamics 365 Field Servicen sopimuslaskut synkronoidaan Dynamics 365 Supply Chain Managementiin vapaatekstilaskuihin.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Field Servicen sopimuslaskut synkronoidaan Supply Chain Managementin vapaatekstilaskuihin seuraavien mallien ja taustalla olevien tehtävien avulla.

**Mallin nimi Tietojen integroinnissa**

- Sopimuslaskut (Field Servicesta Supply Chain Managementiin)

**Tietojen integrointiprojektin tehtävien nimet**

- Laskun ylätunnisteet
- Laskurivit

Seuraavat synkronointi tarvitaan, ennen kuin sopimuslaskut voidaan synkronoida:

- Asiakkaat (Salesista Supply Chain Managementiin) - suora

## <a name="entity-set"></a>Yksikköjoukko

| Field Service  | Toimitusketjun hallinta                 |
|----------------|----------------------------------------|
| laskut       | Dataversen asiakkaan vapaatekstilaskujen otsikot |
| invoicedetails | Dataversen asiakkaan vapaatekstilaskujen rivit   |

## <a name="entity-flow"></a>Yksikön työnkulku

Field Servicen sopimukset luodut laskut voidaan synkronoida Supply Chain Managementiin Microsoft Dataverse -palvelun tietojen integrointiprojektina. Näiden laskujen päivitykset synkronoidaan Supply Chain Managementin vapaatekstilaskuihin, jos vapaatekstilaskun kirjanpidollinen tila on **Käsittelyssä**. Sen jälkeen kun vapaatekstilasku on kirjattu Supply Chain Managementissa ja kirjanpidolliseksi tilaksi on päivitetty **Valmis**, päivityksiä ei voi enää synkronoida Field Servicestä.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu

**Sisältää sopimuksesta peräisin olevia rivejä** -sarake on lisätty **Lasku**-taulukkoon. Tämän sarakkeen avulla voi varmistaa, että vain sopimuksesta luodut laskut synkronoidaan. Arvo on **tosi**, jos laskussa on vähintään yksi sopimuksesta peräisin oleva laskurivi.

**On peräisin sopimuksesta** -sarake on lisätty **Laskurivi**-taulukkoon. Tämän sarakkeen avulla voi varmistaa, että vain sopimuksesta luodut laskurivit synkronoidaan. Arvo on **tosi**, jos laskurivi on peräisin sopimuksesta.

**Laskun päivämäärä** on pakollinen kenttä Supply Chain Managementissa. Tämän vuoksi sarakkeessa on Field Service -arvo ennen synkronointia. Seuraava logiikka lisättiin, jotta tämä vaatimus toteutuisi:

- Jos **Laskun päivämäärä** -sarake on tyhjä **Lasku**-taulukossa (eli siinä ei ole arvoa), siksi määritetään se kuluva päivä, jolloin sopimuksesta peräisin oleva laskurivi lisätään.
- Käyttäjä voi muuttaa **Laskun päivämäärä** -saraketta. Kun käyttäjä kuitenkin yrittää tallentaa sopimuksesta peräisin olevan laskun, hänen vastaanottaa liiketoimintaprosessin virheen, jos laskun **Laskun päivämäärä** -sarake on tyhjä.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="in-supply-chain-management"></a>Supply Chain Managementiin

Laskun alkuperä on määritettävä integraatiota varten, jotta Supply Chain Managementiin Field Servicen sopimuslaskuista luodut vapaatekstilaskut voidaan erottaa. Kun laskun alkuperän tyyppi on **Sopimuksen laskun integrointi**, **Ulkoisen laskun numero** -kenttä näkyy **Myyntilasku**-ylätunnisteessa.

Sen lisäksi että **Ulkoisen laskun numero** näkyy ylätunnisteessa, sen tietojen avulla voidaan varmistaa, että Field Servicen sopimuslaskuista luodut laskut suodatetaan pois synkronoitaessa laskuja Supply Chain Managementista Field Serviceeen.

1. Valitse **Myyntireskontra** \> **Asetukset** \> **Laskun alkuperän koodit**.
2. Luo uusi laskun alkuperä valitsemalla **Uusi**.
3. Anna **Laskun alkuperä** -kentässä laskun alkuperän nimi, kuten **FS**.
4. Kirjoita **Kuvaus**-kenttään kuvaus, kuten **Field Servicen sopimuslasku**.
5. Valitse **Alkuperän tyypin määritys** -valintaruutu.
6. Valitse **Laskun alkuperän tyyppi** -kentässä **Sopimuksen laskun integrointi**.
7. Valitse **Tallenna**.

### <a name="in-the-data-integration-project"></a>Tietojen integrointiprojektissa

Tehtävä: **Laskurivit**  

Varmista, että Supply Chain Managementin kentän **Päätilin näyttöarvon** oletusarvo päivitetään vastaamaan haluttua arvoa.

Oletusmallin arvo on **401100**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Sopimuslaskut (Field Servicesta Supply Chain Managementiin): Laskujen otsikot

[![Laskun otsikoiden tietojen integroinnin mallimääritys.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Sopimuslaskut (Field Servicesta Supply Chain Managementiin): Laskurivit

[![Laskun rivien tietojen integroinnin mallimääritys.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]