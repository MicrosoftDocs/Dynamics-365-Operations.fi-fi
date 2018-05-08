---
title: Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Myyntitarjouksien otsikoiden ja rivien synkronointi suoraan Salesista Finance and Operationsiin

[!include [banner](../includes/banner.md)]

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan suoraan Microsoft Dynamics 365 for Finance and Operationsiin.

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

## <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkrontaessa myyntitarjousten otsikot ja rivit suoraan Salesista Finance and Operationsiin:

- **Mallin nimi tietojen integroinnissa:** Myyntitarjoukset (Salesista Fin and Opsiin) – suora
- **Tehtävien nimet tietojen integrointiprojektissa:**

    - QuoteHeader
    - QuoteLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:

- Tuotteet (Fin and Opsista Salesiin) - suora
- Tilit (Salesista Fin and Opsiin) - suora (jos käytössä)
- Yhteyshenkilöistä asiakkaisiin (Salesista Fin and Opsiin) - suora (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Myynti        | Finance and Operations     |
|--------------|----------------------------|
| Tarjoukset       | CDS-myyntitarjouksen otsikko |
| QuoteDetails | CDS-myyntitarjousrivit  |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitarjoukset luodaan Salesissa ja synkronoidaan Finance and Operationsiin.

Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:

- Kaikkia myyntitarjouksen tarjoustuotteita ylläpidetään ulkoisesti.
- Kun valitset **Aktivoi tarjous**, myyntitarjouksesta tulee aktiivinen.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Quote**-yksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista. Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa. Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.

Kaikki myyntitarjouksen tarjoustuotteet päivitetään myyntitarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla. Nämä tiedot sijaitsevat **QuoteDetails**-yksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.

Alennus lisätään tarjoustuotteeseen ja se synkronoidaan Finance and Operationsiin. Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Finance and Operationsin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään Finance and Operationsissa, jossa niitä myös käsitellään.

Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Finance and Operationsiin:

- Myyntitarjouksen otsikon vain luku -kentät: **Alennusprosentti**, **Alennus** ja **Rahdin summa**
- Tarjoustuotteiden vain luku -kentät: **Vero**

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Seuraavat asetukset tulee päivittää ennen myyntitarjousten synkronointia.

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Varmista, että sen käyttäjän ryhmän käyttöoikeudet on määritetty, jolle Salesissa asetettu yhteys on määritetty. Jos käytät esittelytietoja, käyttäjällä on usein järjestelmänvalvojan käyttöoikeudet, mutta ryhmällä ei. Jos ryhmällä ei ole järjestelmänvalvojan käyttöoikeuksia, kun suoritat projektin tietojen integrointiohjelmasta, saat virheilmoituksen, jossa kerrotaan ensisijaisen ryhmän puuttumisesta.

    Voit määrittää ryhmän käyttöoikeudet siirtymällä kohtaan **Asetukset** &gt; **Suojaus** &gt; **Ryhmät**. Valitse sitten haluamasi ryhmä. Valitse **Roolien hallinta** ja valitse sitten rooli, jolla on halutut käyttöoikeudet, kuten **järjestelmänvalvoja**.

- Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että käytössä ovat seuraavat asetukset:

    - **Käytä järjestelmän hinnanlaskentajärjestelmää** -asetuksen arvoksi on määritetty **Kyllä**.
    - **Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="quoteheader"></a>QuoteHeader

- Varmista, että **Shipto\_country**- ja **DeliveryAddressCountryRegionISOCode**-kohdan välinen yhdistämismääritys on tehty. Voit määrittää arvomäärityksessä oletusarvon, jota käytetään, jos kohta on jätetty tyhjäksi. Voit vain jättää vasemman puolen tyhjäksi ja määrittää oikean puolen arvoksi halutun maan tai alueen. Tällöin kansallisiin tilauksiin ei tarvitse kirjoittaa maata tai aluetta.

    Malliarvo on arvomääritys, jossa on yhdistetty useita maita tai alueita. Jos kohta jätetään tyhjäksi, arvo on **US**.

#### <a name="quoteline"></a>QuoteLine

- Varmista, että Finance and Operationsin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.
- Varmista, että Salesissa on määritetty pakolliset yksiköt.

    **oumid.name**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **SalesUnitSymbol**.

- Valinnainen: Kun lisäät seuraavat yhdistämismääritykset, voit varmistaa, että myyntitarjouksen rivit tuodaan Finance and Operationsiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:

    - **SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa. **SiteId**-oletusmalliarvoa ei ole.
    - **WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa. **WarehouseId**-oletusmalliarvoa ei ole.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> - **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Finance and Operationsissa.
> - **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

### <a name="quoteheader"></a>QuoteHeader

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)


