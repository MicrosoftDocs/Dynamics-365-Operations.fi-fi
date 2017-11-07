---
title: Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin myyntitarjousten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 9117b5af3beff7290816586f63091b12e357339c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi. 

Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin (Sales) myyntitarjousten otsikot ja rivit synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations). 

## <a name="template-and-tasks"></a>Malli ja tehtävät

Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan myyntitarjousten otsikot ja rivit Salesista Finance and Operationsiin:

- **Mallin nimi:** Myyntitarjoukset (Salesista Fin and Opsiin)
- **Projektin tehtävien nimet:**

    - QuoteHeader
    - QuoteLine

Seuraavat synkronointitehtävät tarvitaan, ennen kuin myyntitilaukset otsikot ja rivit voidaan synkronoida:

- Tuotteet (Fin and Opsista Salesiin)
- Tilit (Salesista Fin and Opsiin) (jos käytössä)
- Yhteyshenkilöstä asiakkaisiin (Salesista Fin and Opsiin) (jos käytössä)

## <a name="entity-set"></a>Yksikköjoukko

| Myynti        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Tarjoukset       | Tarjous     | Myyntitarjouksen otsikot   |
| QuoteDetails | QuotationLine | CDS-myyntitarjousrivit |

## <a name="entity-flow"></a>Yksikön työnkulku

Myyntitarjoukset luodaan Salesissa ja synkronoidaan Finance and Operationsiin.

Salesin myyntitarjoukset synkronoidaan vain, jos seuraavat ehdot täyttyvät:

- Kaikkia myyntitarjousrivien tuotteita ylläpidetään ulkoisesti.
- Myyntitarjous on aktiivinen tai aktivoitu.

## <a name="prospect-to-cash-solution-for-sales"></a>Salesin ratkaisu prospektista käteiseksi

**Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kenttä on lisätty tarjousyksikköön seuraamaan johdonmukaisesti, koostuuko myyntitarjous kokonaan ulkoisesti ylläpidetyistä tuotteista. Jos myyntitarjouksessa on vain ulkoisesti ylläpidettyjä tuotteita, tuotteita ylläpidetään Finance and Operationsissa. Tämä auttaa varmistamaan, ettet yritä synkronoida myyntitarjousrivejä sellaisten tuotteiden kanssa, joita Finance and Operations ei tunne.

Kaikki tarjouksen tuotteet ja rivit päivitetään tarjouksen otsikon **Sisältää vain ulkoisesti ylläpidettyjä tuotteita** -tiedoilla. Nämä tiedot sijaitsevat tarjousriviyksikön **Tarjous sisältää vain ulkoisesti ylläpidettyjä tuotteita** -kentässä.

**Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä hallitaan Finance and Operationsissa, jossa niitä myös käsitellään.

Seuraavat kentät ovat Salesissa vain luku -muotoisia, koska arvoja ei synkronoida Finance and Operationsiin:

- **Myyntitarjouksen otsikon vain luku -kentät:** Alennusprosentti, Alennus, Rahdin summa
- **Myyntitarjousrivien vain luku -kentät:** Vero

## <a name="preconditions-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Järjestelmiin tulisi päivittää seuraavat asetukset ennen myyntitilausten synkronointia:

### <a name="setup-in-sales"></a>Asetukset Salesissa

- Siirry kohtaan **Asetukset** &gt; **Hallinto** &gt; **Järjestelmäasetukset** &gt; **Sales** ja varmista, että **Alennuksen laskutapa** -kentässä on valittu **Yksikköä kohden**. Tällä asetuksella voidaan varmistaa, että Salesin rivinimikkeen alennus vastaa Finance and Operationsin asetusta. Muussa tapauksessa alennus ei ole oikein Finance and Operationsissa, koska Finance and Operations lukee alennuksen yksikkökohtaisena alennuksena, vaikka se oli rivikohtainen alennus Salesissa.

### <a name="setup-in-finance-and-operations"></a>Asetukset Finance and Operationsissa

- Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit**. Valitse **Numerojärjestys**-välilehdessä myyntitarjousten numerojärjestys ja valitse sitten **Näytä tiedot**. Valitse sitten **Yleinen asetus** -kohdassa **Manuaalinen**-kentässä **Kyllä**.
- Valitse **Myyntireskontra** &gt; **Asetukset** &gt; **Myyntireskontran parametrit**. Valitse sitten **Lähetykset**-välilehden **Toimituspäivän tarkistus** -kentässä **Ei mitään**. Tämä asetuksen ansiosta synkronointi ei aiheuta myyntitarjousten epäonnistumista.

### <a name="setup-in-the-data-integration-project"></a>Asetukset tietojen integrointiprojektissa

#### <a name="quoteheader"></a>QuoteHeader

- **Pyydetty toimituspäivämäärä** -kenttä on pakollinen Finance and Operationsissa, ja synkronointi epäonnistuu, jos kenttä jätetään tyhjäksi. Voit estää tämän ongelman, kun kentän ollessa tyhjä oletuspäivämäärä otetaan kohdasta **Lähde &gt; CDS**. Päivämäärä on päivitettävä halutuksi arvoksi. Tällä hetkellä kuluvaa päivää ei voi ilmaista arvolla, kuten **Tänään**. Anna tietty päivämäärä. Mallin **Pyydetty toimituspäivämäärä** oletusarvo on **1/1/2020**.
- **Osoitteen maa- tai aluekoodi** -kenttä on pakollinen Finance and Operationsissa. Voit estää synkronointivirheet määrittämällä oletusarvon, jota käytetään, jos kenttä on jätetty tyhjäksi Salesissa. Oletusarvo on hyödyllinen myös siksi, ettei paikallisten osoitteiden arvoa tarvitse antaa manuaalisesti **Maa tai alue** -kentässä. Oletusmallin **DeliveryAddressCountryRegionISOCode** -arvoa ei ole.
- Päivitä **CDS-organisaation tunnus** -määritys kohdassa **Lähde &gt; CDS** siten, että se vastaa organisaatioyksikön **CDS-organisaatio**-arvoa:

    - **Organization_OrganizationId**-oletusmalliarvo on **ORG001**.
    - **Account_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.
    - **InvoiceAccount_OrganizationId**-oletusmalliarvo on **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Päivitä **CDS-organisaation tunnus** -määritys kohdassa **Lähde &gt; CDS** siten, että se vastaa organisaatioyksikön **CDS-organisaatio**-arvoa:

    - **Organization_OrganizationId**-oletusmalliarvo on **ORG001**.
    - **Product_Organization_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.
    - **Quotation_Organization_Organization_OrganizationId**-oletusmalliarvo on **ORG001**.

- **Pyydetty toimituspäivämäärä** -kenttä on pakollinen Finance and Operationsissa, ja synkronointi epäonnistuu, jos kenttä jätetään tyhjäksi. Voit estää tämän ongelman, kun kentän ollessa tyhjä oletuspäivämäärä otetaan kohdasta **Lähde &gt; CDS**. Päivämäärä on päivitettävä halutuksi arvoksi. Tällä hetkellä kuluvaa päivää ei voi ilmaista arvolla, kuten **Tänään**. Anna tietty päivämäärä. Mallin **Pyydetty toimituspäivämäärä** oletusarvo on **1/1/2020**.
- Voit lisätä seuraavat yhdistämismääritykset kohdasta **CDS &gt; Kohde** ja varmistaa näin, että tarjousrivit tuodaan Finance and Operationsiin, jos asiakkaalla tai tuotteella ei ole oletustietoja:

    - **SiteId** – Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan luoda Finance and Operationsissa. **SiteId**-oletusmalliarvoa ei ole.
    - **WarehouseId** – Varasto on pakollinen, jotta tarjoukset ja myyntitilausrivit voidaan käsitellä Finance and Operationsissa. **WarehouseId**-oletusmalliarvoa ei ole.

- Varmista, että Finance and Operationsin myynnin mittayksikön arvokartta on olemassa **CDS &gt; Kohde** -määritykselle, jota käytetään määritettäessä **Quantity_UOM** kohteeseen **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Mallin yhdistäminen tietojen integrointiohjelmassa

> [!NOTE]
> - **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu monimutkaisiin Finance and Operationsin määrityksiin. Tämä määritys ei tue tällä hetkellä integrointimääritystä. Nykyisessä versiossa **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä käsitellään Finance and Operationsissa.
> - **Maksuehdot**-, **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.

### <a name="quoteheader"></a>QuoteHeader

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Liittyvät aiheet

[Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin](products-template-mapping.md)

[Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin](accounts-template-mapping.md)

[Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin](contacts-template-mapping.md)



