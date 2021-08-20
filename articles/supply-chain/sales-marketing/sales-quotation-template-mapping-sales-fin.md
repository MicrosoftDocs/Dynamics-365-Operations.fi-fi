---
title: Myyntitarjousten otsikoiden ja rivien synkronointi suoraan Salesista Supply Chain Managementiin
description: Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntitarjousten otsikot ja rivit suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: a39b6b5fff88a02b71d81fd870e8c92ab055bc4d257e14c9b84cac0deac2c5c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771320"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Myyntitarjousten otsikoiden ja rivien synkronointi suoraan Salesista Supply Chain Managementiin

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä ohjeaiheessa käsitellään malleja ja niiden taustalla olevia tehtäviä, joita käytetään synkronoimaan myyntitarjousten otsikot ja rivit suoraan Dynamics 365 Salesista Dynamics 365 Supply Chain Managementiin.

> [!NOTE]
> Tutustu [Microsoft Dataverse for Appsin tietojen integrointiin](/powerapps/administrator/data-integrator), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.

## <a name="data-flow-in-prospect-to-cash"></a>Prospektista käteiseksi -ratkaisun tiedonkulku

Prospektista käteiseksi -ratkaisu käyttää tietojen integrointitoimintoa Supply Chain Managementin and Salesin esiintymien tietojen synkronoinnissa. Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Supply Chain Managementin ja Salesin välillä. Seuraava kuva näyttää, miten tiedot synkronoidaan Supply Chain Managementin ja Salesin välillä.

[![Prospektista käteiseksi -ratkaisun tiedonkulku.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavaa mallia ja sen taustalla olevia tehtäviä käytetään synkronoitaessa myyntitarjousten otsikot ja rivit suoraan Salesista Supply Chain Managementiin:

- **Mallin nimi tietojen integroinnissa:** Myyntitarjoukset (Salesista Supply Chain Managementiin) – suora
- **Tehtävien nimet tietojen integrointiprojektissa:**

    - QuoteHeader
    - QuoteLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:

- Tuotteet (Supply Chain Managementista Salesiin) - suora
- Tilit (Salesista Supply Chain Managementiin) - Suora (jos käytössä)
- Yhteyshenkilöistä asiakkaisiin (Salesista Supply Chain Managementiin) - Suora (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Myynti        | Toimitusketjun hallinta     |
|--------------|----------------------------|
| Tarjoukset       | Dataversen myyntitarjouksen otsikko |
| QuoteDetails | Dataversen myyntitarjousrivit  |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitarjoukset luodaan Salesissa ja synkronoidaan Supply Chain Managementiin.

Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:

- Kaikkia myyntitarjouksen tarjoustuotteita ylläpidetään ulkoisesti.
- Kun valitset **Aktivoi tarjous**, myyntitarjouksesta tulee aktiivinen.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty **Quote**-yksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista. Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Supply Chain Managementissa. Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Supply Chain Management ei tunne.

Kaikki myyntitarjouksen tarjoustuotteet päivitetään myyntitarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla. Nämä tiedot sijaitsevat **QuoteDetails**-yksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.

Alennus lisätään tarjoustuotteeseen ja se synkronoidaan Supply Chain Managementiin. Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Supply Chain Managementin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään Supply Chain Managementissa, jossa niitä myös käsitellään.

Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Supply Chain Managementiin:

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

- Varmista, että Supply Chain Managementin **SalesUnitSymbol**-kohdassa on vaadittu arvomääritys.
- Varmista, että Salesissa on määritetty pakolliset yksiköt.

    **oumid.name**-kohdan malliarvoksi, jolla on arvomääritys, on määritetty **SalesUnitSymbol**.

- Valinnainen: Kun lisäät seuraavat yhdistämismääritykset, voit varmistaa, että myyntitarjouksen rivit tuodaan Supply Chain Managementiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:

    - **SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Supply Chain Managementissa. **SiteId**-oletusmalliarvoa ei ole.
    - **WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Supply Chain Managementissa. **WarehouseId**-oletusmalliarvoa ei ole.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> - **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Supply Chain Managementin monimutkaisiin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Supply Chain Managementissa.
> - **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

### <a name="quoteheader"></a>QuoteHeader

![Mallin yhdistäminen tietojen integrointiohjelmassa.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Mallin yhdistäminen tietojen integrointiohjelmassa.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Prospektista käteiseksi](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]