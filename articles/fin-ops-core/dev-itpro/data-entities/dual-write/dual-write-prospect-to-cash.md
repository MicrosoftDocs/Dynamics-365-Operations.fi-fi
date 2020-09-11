---
title: Prospektista käteiseksi -kaksoiskirjoitus
description: Tässä ohjeaiheessa on tietoja prospektista käteiseksi -kaksoiskirjoituksesta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: a2ca0ce277a062c8d525b6a3619eaf1b0114667b
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719261"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospektista käteiseksi -kaksoiskirjoitus

[!include [banner](../../includes/banner.md)]



Useimpien yritysten tärkeä tavoite on muuntaa prospektit asiakkaiksi ja ylläpitää sitten jatkuvaa liikesuhdetta kyseisiin asiakkaisiin. Microsoft Dynamics 365 -sovelluksissa prospektista käteiseksi -prosessi tapahtuu tarjousten tai tilaustenkäsittelytyönkulkujen kautta. Myyntitiedot täsmäytetään ja kirjataan. Prospektista käteiseksi -kaksoiskirjoituksen integrointi luo työnkulun. Se käyttää tarjousta ja tilausta, joka saadaan Dynamics 365 Salesista tai Dynamics 365 Supply Chain Managementista ja määrittää tarjouksen ja tilauksen käytettäväksi molemmissa sovelluksissa.

Sovellusliittymissä voit käyttää käsittelyn tiloja ja laskun tietoja reaaliajassa. Tämän vuoksi voit helpommin hallita toimintoja, kuten tuotteiden varastointia, varastonhallintaa ja täyttämistä Supply Chain Managementissa ilman tarjousten ja tilausten uudelleenluomista.

![Prospektista käteiseksi -kaksoiskirjoituksen tietovirta](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Ennen kuin voit synkronoida myyntitarjoukset, sinun on päivitettävä seuraavat asetukset.

### <a name="setup-in-sales"></a>Asetukset Salesissa

Siirry Salesissa kohtaan **Asetukset \> Hallinta \> Järjestelmäasetukset \> Sales** ja varmista, että käytetään seuraavia asetuksia:

- **Käytä järjestelmän hinnanlaskentaa** -järjestelmäasetuksen arvoksi on määritetty **Kyllä**.
- **Alennuksen laskutapa** -kentän arvoksi on määritetty **Rivinimike**.

### <a name="sites-and-warehouses"></a>Sivustot ja varastot

Supply Chain Managementissa **Sivusto**- ja **Varasto**-kentät ovat pakollisia tarjous- ja tilausriveille. Jos määrität sivuston ja varaston oletustilausasetuksissa, nämä kentät määritetään automaattisesti, kun lisäät tuotteen tarjous- tai tilausriville. 

### <a name="number-sequences-for-quotations-and-orders"></a>Tarjousten ja tilausten numerosarjat

Supply Chain Managementin ja Salesin numerosarjoja ei yhdistetä, jos tarjoukset ja tilaukset luodaan ja synkronoidaan Salesissa ja Supply Chain Managementissa. Jos Salesissa luotu myyntitilaus synkronoidaan Supply Chain Managementiin, sillä on sama myyntitilausnumero Supply Chain Managementissa. Jotta myyntitilauksen numeroa ei kopioida, molemmissa sovelluksissa on käytettävä eri numerosarjajärjestelmiä.

Ajatellaan, että Supply Chain Managementin numerosarja on **1, 2, 3, 4, 5, ...** ja Salesin numerosarja on **100, 99, 98, ...**. Jos luot Salesissa 100 myyntitilausta, lopulta luodaan tilausnumero, joka on jo olemassa Supply Chain Managementissa. Toisin sanoen kaksi numerosarjaa ovat lopulta päällekkäisiä, koska myyntitilaukset luodaan Supply Chain Managementissa ja Salesissa. Sen sijaan voit käyttää esimerkiksi Supply Chain Managementissa numerosarjaa **F1, F2, F3, ...** ja Salesissa numerosarjaa **C1, C2, C3, ...**. Nämä numerosarjat eivät koskaan tuota myyntitilausnumeroiden kaksoiskappaleita.

## <a name="sales-quotations"></a>Myyntitarjoukset

Myyntitarjoukset luodaan Salesissa tai Supply Chain Managementissa. Jos luot tarjouksen Salesissa, se synkronoidaan Supply Chain Managementiin reaaliajassa. Samoin, jos luot tarjouksen Supply Chain Managementissa, se synkronoidaan Salesiin reaaliajassa. Huomaa seuraavat seikat:

+ Voit lisätä tarjouksen tuotteeseen alennuksen. Tässä tapauksessa alennus synkronoidaan Supply Chain Managementiin. Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-kenttien hallinta perustuu Supply Chain Managementin määrityksiin. Tämä määritys ei tue integrointimääritystä. Sen sijaan **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-kenttiä ylläpidetään ja käsitellään Supply Chain Managementissa.
+ Myyntitarjouksen otsikon vain luku -kenttiä ovat **Alennusprosentti**, **Alennus** ja **Rahdin summa**.
+ **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-kentät eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

Jos käytät myös Field Service -ratkaisua, muista ottaa **Tarjousrivin pikakäynnistys** -parametri uudelleen käyttöön. Kun parametri otetaan uudelleen käyttöön, voit jatkaa tarjousrivien luomista pikaluontitoiminnon avulla.
1. Siirry Dynamics 365 Sales -sovellukseen.
2. Valitse yläreunan siirtymispalkista Asetukset-kuvake.
3. Valitse **Lisäasetukset**.
4. Valitse **Mukauta järjestelmä** -vaihtoehto.
5. Valitse **Tarjousrivi**-valikkovaihtoehto.
6. Siirry **Tietopalvelut**-osioon ja valitse **Salli pikaluonti** -valintaruutu.

## <a name="sales-orders"></a>Myyntitilaukset

Myyntitilaukset luodaan Salesissa tai Supply Chain Managementissa. Jos luot myyntitilauksen Salesissa, se synkronoidaan Supply Chain Managementiin reaaliajassa. Samoin jos luot myyntitilauksen Supply Chain Managementissa, se synkronoidaan Salesiin reaaliajassa. Huomaa seuraavat seikat:

+ Dynamics 365 Salesin kirjoitettavat tuotteet näkyvät tuoteluokkina Dynamics 365 Supply Chain Managementissa.
+ Alennuksen laskeminen ja pyöristäminen:

    - Salesin alennuksen laskentamalli on erilainen kuin Supply Chain Managementin alennuksen laskentamalli. Supply Chain Managementissa myyntirivin lopullinen alennussumma voi olla alennussummien ja alennusprosenttien yhdistelmän tulos. Jos tämä lopullinen alennussumma jaetaan rivin määrällä, tulos saatetaan pyöristää. Pyöristystä ei kuitenkaan tehdä, jos pyöristetty yksikkökohtainen alennussumma synkronoidaan Salesiin. Voit varmistaa, että Supply Chain Management -myyntirivin koko alennussumma synkronoidaan oikein Salesiin, kun koko summa synkronoidaan ilman, että sitä jaetaan rivimäärällä. Tämän vuoksi Salesin Alennuksen laskutapa -kohdan arvoksi on määritettävä **Rivinimike**.
    - Kun myyntitilausrivi synkronoidaan Salesista Supply Chain Managementiin, käytetään koko rivin alennussummaa. Koska Supply Chain Managementissa ei ole kenttää, johon rivin koko alennussumman voisi tallentaa, summa jaetaan määrällä ja tallennetaan **Rivialennus**-kenttään. Kaikki tässä divisioonassa tapahtuva pyöristys tallennetaan myyntirivin **Myyntikulut**-kenttään.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Esimerkki: Synkronointi Salesista Supply Chain Managementiin

Myyntitilaus on seuraava:

+ **Sales:** Määrä = 3, rivikohtainen alennus = 10,00 $
+ **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = –$0,01

Jos synkronoit Supply Chain Managementista Salesiin, saat seuraavan tuloksen:

+ **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = –$0,01
+ **Sales:** Määrä = 3, rivikohtainen alennus = (3 × 3,33 $) + 0,01 $ = 10,00 $

## <a name="dual-write-solution-for-sales"></a>Kaksoiskirjoitusratkaisu Salesia varten

**Tilaus**-yksikköön on lisätty uusia kenttiä, jotka näkyvät sivulla. Useimmat näistä kentistä näkyvät Salesin **Integrointi**-välilehdessä. Muutamia erityisiä kenttiä:

+ **Käsittelytila**-kenttä näyttää tilauksen käsittelyn tilan Supply Chain Managementissa. Tämä kenttä on lukittu, ja se näyttää vain Supply Chain Managementin tilauksen tilan. Käytettävissä ovat seuraavat arvot:

    + **Aktiivinen** – tila sen jälkeen, kun tilaus on aktivoitu Salesissa **Aktivoi**-painikkeen avulla.
    + **Vahvistettu**
    + **Toimitettu**
    + **Laskutettu**
    + **Osittain toimitettu**
    + **Osittain laskutettu**
    + **Keräilty**
    + **Peruutettu**

    Seuraavasta taulukosta ilmenee, miten käsittelyn tila yhdistetään **CRM:n tilakoodi** -arvoon.

    | Käsittelytila           | CRM:n tilakoodi    |
    |-----------------------------|--------------------|
    | Aktiiviset                      | Uusi/Odottava/Pidossa |
    | Vahvistettu/Kerätty            | Käsittelyssä        |
    | Osittain toimitettu         | Osittainen            |
    | Toimitettu                   | Päätetty           |
    | Laskutettu / Osittain laskutettu | Laskutettu           |
    | Peruutettu                    | Ei rahaa           |

+ **Luo lasku**- ja **Peruuta tilaus** -painikkeet piilotetaan Salesin **Myyntitilaus**-sivulla.
+ **Myyntitilauksen tila** -arvo pysyy **aktiivisena**, jotta muutokset Supply Chain Managementista siirtyvät Salesin myyntitilaukseen. Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[Tila\]** -arvoksi **Aktiivinen**.

## <a name="invoices"></a>Laskut

Myyntilaskut luodaan Supply Chain Managementissa ja synkronoidaan Salesiin. Huomaa seuraavat seikat:

+ **Laskun numero** -kenttä on lisätty **Lasku**-yksikköön. Se näkyy sivulla.
+ **Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Supply Chain Managementissa, josta ne synkronoidaan Salesiin. **Lasku**-sivua ei voi muokata, sillä laskut synkronoidaan Supply Chain Managementista.
+ **Myyntitilauksen tila** -arvo muuttuu automaattisesti **Laskutettu**-tilaksi, kun liittyvä lasku on synkronoitu Supply Chain Managementista Salesiin. Lisäksi laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu. Tämän vuoksi myyntitilauksen omistaja voi tarkastella laskua.
+ **Kuljetusehdot**-, **Toimitusehdot**- ja **Toimitustila**-kenttiä ei lisätä oletusarvoisiin yhdistämismäärityksiin. Näiden kenttien määrittämistä varten on määritettävä arvomääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä yksikkö synkronoidaan.

## <a name="templates"></a>Mallipohjat

Prospektista käteiseksi -toiminto sisältää perusentiteettikarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Finance and Operations -sovellukset | Dynamics 365:n mallipohjaiset sovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
| Myyntilaskun otsikot V2    | laskut                          |             |
| Myyntilaskun rivit V2      | invoicedetails                    |             |
| CDS-myyntitilauksien otsikot     | salesorders                       |             |
| CDS-myyntitilausrivit       | salesorderdetails                 |             |
| Myyntitilausten alkuperän koodit    | msdyn\_salesorderorigins          |             |
| CDS-myyntitarjouksen otsikko  | tarjoukset                            |             |
| CDS-myyntitarjousrivit   | quotedetails                      |             |

Tässä ovat prospektista käteiseksi -toiminnon liittyvät perusentiteettikartat.

+ [Asiakkaat V3 tileille](customer-mapping.md#customers-v3-to-accounts)
+ [CDS Contacts V2 yhteyshenkilöihin](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Asiakkaat V3 yhteyshenkilöihin](customer-mapping.md#customers-v3-to-contacts)
+ [msdyn_sharedproductdetails-yksikköön vapautetut tuotteet V2](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Kaikki tuotteet kohteeseen msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Hinnasto](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
