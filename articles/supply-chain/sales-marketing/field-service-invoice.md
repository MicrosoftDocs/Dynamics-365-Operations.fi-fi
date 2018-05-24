---
title: Field Servicen sopimuslaskujen synkronointi Finance and Operationsin vapaatekstilaskuihin
description: "Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Field Servicen sopimuslaskut synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin vapaatekstilaskuihin."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: 6672e283a5e56b068e3494d53a0fd6dd08253ba9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Field Servicen sopimuslaskujen synkronointi Finance and Operationsin vapaatekstilaskuihin

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja taustalla olevia tehtäviä, joilla Microsoft Dynamics 365 for Field Servicen sopimuslaskut synkronoidaan Microsoft Dynamics 365 for Finance and Operationsiin vapaatekstilaskuihin.

## <a name="templates-and-tasks"></a>Mallit ja tehtävät

Field Servicen sopimuslaskut synkronoidaan Finance and Operationsin vapaatekstilaskuihin seuraavien mallien ja taustalla olevien tehtävien avulla.

**Mallin nimi Tietojen integroinnissa:**

- Sopimuslaskut (Field Servicestä Fin and Opsiin)

**Tehtävien nimet tietojen integrointiprojektissa:**

- Laskun ylätunnisteet
- Laskurivit

Seuraavat synkronointi tarvitaan, ennen kuin sopimuslaskut voidaan synkronoida:

- Tilit (Salesista Fin and Opsiin) – suora

## <a name="entity-set"></a>Yksikköjoukko

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| laskut       | CDS-asiakkaan vapaatekstilaskujen otsikot |
| invoicedetails | CDS-asiakkaan vapaatekstilaskujen rivit   |

## <a name="entity-flow"></a>Yksikön työnkulku

Field Servicen sopimukset luodut laskut voidaan synkronoida Finance and Operationsiin Common Data Service (CDS) -palvelun tietojen integrointiprojektina. Näiden laskujen päivitykset synkronoidaan Finance and Operationsin vapaatekstilaskuihin, jos vapaatekstilaskun kirjanpidollinen tila on **Käsittelyssä**. Sen jälkeen kun vapaatekstilasku on kirjattu Finance and Operationsissa ja kirjanpidolliseksi tilaksi on päivitetty **Valmis**, päivityksiä ei voi enää synkronoida Field Servicestä.

## <a name="field-service-crm-solution"></a>Field Service CRM -ratkaisu

**Sisältää sopimuksesta peräisin olevia rivejä** -kenttä on lisätty **Lasku**-yksikköön. Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskut synkronoidaan. Arvo on **tosi**, jos laskussa on vähintään yksi sopimuksesta peräisin oleva laskurivi.

**On peräisin sopimuksesta** -kenttä on lisätty **Laskurivi**-yksikköön. Tämän kentän avulla voi varmistaa, että vain sopimuksesta luodut laskurivit synkronoidaan. Arvo on **tosi**, jos laskurivi on peräisin sopimuksesta.

**Laskun päivämäärä** on pakollinen kenttä Finance and Operationsissa. Tämän vuoksi kentässä on Field Service -arvo ennen synkronointia. Seuraava logiikka lisättiin, jotta tämä vaatimus toteutuisi:

- Jos **Laskun päivämäärä** -kenttä on tyhjä **Lasku**-yksikössä (eli siinä ei ole arvoa), siksi määritetään se kuluva päivä, jolloin sopimuksesta peräisin oleva laskurivi lisätään.
- Käyttäjä voi muuttaa **Laskun päivämäärä** -kenttää. Kun käyttäjä kuitenkin yrittää tallentaa sopimuksesta peräisin olevan laskun, hänen vastaanottaa liiketoimintaprosessin virheen, jos laskun **Laskun päivämäärä** -kenttä on tyhjä.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

### <a name="in-finance-and-operations"></a>Finance and Operationsissa

Laskun alkuperä on määritettävä integraatiota varten, jotta Finance and Operationsin Field Servicen sopimuslaskuista luodut vapaatekstilaskut voidaan erottaa. Kun laskun alkuperän tyyppi on **Sopimuksen laskun integrointi**, **Ulkoisen laskun numero** -kenttä näkyy **Myyntilasku**-ylätunnisteessa.

Sen lisäksi että **Ulkoisen laskun numero** näkyy ylätunnisteessa, sen tietojen avulla voidaan varmistaa, että Field Servicen sopimuslaskuista luodut laskut suodatetaan pois synkronoitaessa laskuja Finance and Operationsista Field Serviceeen.

1. Valitse **Myyntireskontra** \> **Asetukset** \> **Laskun alkuperän koodit**.
2. Luo uusi laskun alkuperä valitsemalla **Uusi**.
3. Anna **Laskun alkuperä** -kentässä laskun alkuperän nimi, kuten **FS**.
4. Kirjoita **Kuvaus**-kenttään kuvaus, kuten **Field Servicen sopimuslasku**.
5. Valitse **Alkuperän tyypin määritys** -valintaruutu.
6. Valitse **Laskun alkuperän tyyppi** -kentässä **Sopimuksen laskun integrointi**.
7. Valitse **Tallenna**.

### <a name="in-the-data-integration-project"></a>Tietojen integrointiprojektissa

Tehtävä: **Laskurivit**  

Varmista, että Finance and Operationsin kentän **Päätilin näyttöarvon** oletusarvo päivitetään vastaamaan haluttua arvoa.

Oletusmallin arvo on **401100**.

## <a name="template-mapping-in-data-integration"></a>Mallin yhdistäminen tietojen integroinnin yhteydessä

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integroinnin yhteydessä.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Sopimuslaskut (Field Servicestä Fin and Opsiin): Laskuotsikot

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Sopimuslaskut (Field Servicestä Fin and Opsiin): Laskurivit

[![Mallin yhdistäminen tietojen integroinnin yhteydessä](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)

