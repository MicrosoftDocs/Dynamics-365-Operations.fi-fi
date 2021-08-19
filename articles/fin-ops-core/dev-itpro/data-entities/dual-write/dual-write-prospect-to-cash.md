---
title: Prospektista käteiseksi -kaksoiskirjoitus
description: Tässä ohjeaiheessa on tietoja prospektista käteiseksi -kaksoiskirjoituksesta.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 03bfb5f97b332abb7f34e179d7b294ed2228ab474825a76271f42cc60971a645
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716091"
---
# <a name="prospect-to-cash-in-dual-write"></a>Prospektista käteiseksi -kaksoiskirjoitus

[!include [banner](../../includes/banner.md)]

Useimpien yritysten tärkeä tavoite on muuntaa prospektit asiakkaiksi ja ylläpitää sitten jatkuvaa liikesuhdetta kyseisiin asiakkaisiin. Microsoft Dynamics 365 -sovelluksissa prospektista käteiseksi -prosessi tapahtuu tarjousten tai tilaustenkäsittelytyönkulkujen kautta. Myyntitiedot täsmäytetään ja kirjataan. Prospektista käteiseksi -kaksoiskirjoituksen integrointi luo työnkulun. Se käyttää tarjousta ja tilausta, joka saadaan Dynamics 365 Salesista tai Dynamics 365 Supply Chain Managementista ja määrittää tarjouksen ja tilauksen käytettäväksi molemmissa sovelluksissa.

Sovellusliittymissä voit käyttää käsittelyn tiloja ja laskun tietoja reaaliajassa. Tämän vuoksi voit helpommin hallita toimintoja, kuten tuotteiden varastointia, varastonhallintaa ja täyttämistä Supply Chain Managementissa ilman tarjousten ja tilausten uudelleenluomista.

![Prospektista käteiseksi -kaksoiskirjoituksen tietovirta.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Lisätietoja asiakkaan ja yhteyshenkilön integroinnista on kohdassa [Integroidut asiakkaan päätiedot](customer-mapping.md). Lisätietoja tuotteen integroinnista on kohdassa [Yhtenäinen tuotekokemus](product-mapping.md).

> [!NOTE]
> Dynamics 365 Salesissa sekä prospekti että asiakas viittaa tietueeseen **Tili**-taulussa, jossa **RelationshipType**-sarake on joko **Prospekti** tai **Asiakas**. Jos liiketoimintalogiikka sisältää **Tili**-hyväksyntäprosessin, jossa **Tili**-tietue luodaan ja hyväksytään ensin prospektiksi ja sitten asiakkaaksi, kyseinen tietue synkronoituu Finance and Operations -sovellukseen vasta, kun se on asiakas (`RelationshipType=Customer`). Jos **Tili**-rivi halutaan synkronoida prospektina, prospektin tietojen integrointiin tarvitaan mukautettu yhdistämismääritys.

## <a name="prerequisites-and-mapping-setup"></a>Edellytykset ja yhdistämismääritykset

Ennen kuin voit synkronoida myyntitarjoukset, sinun on päivitettävä seuraavat asetukset.

### <a name="setup-in-sales"></a>Asetukset Salesissa

Siirry Salesissa kohtaan **Asetukset \> Hallinta \> Järjestelmäasetukset \> Sales** ja varmista, että käytetään seuraavia asetuksia:

- **Käytä järjestelmän hinnanlaskentajärjestelmää** -järjestelmäasetuksen arvoksi on määritetty **Kyllä**.
- **Alennuksen laskutapa** -sarakkeen arvoksi on määritetty **Rivinimike**.

### <a name="sites-and-warehouses"></a>Sivustot ja varastot

Supply Chain Managementissa **Sivusto**- ja **Varasto**-sarakkeet ovat pakollisia tarjous- ja tilausriveille. Jos määrität sivuston ja varaston oletustilausasetuksissa, nämä sarakkeet määritetään automaattisesti, kun lisäät tuotteen tarjous- tai tilausriville. 

### <a name="number-sequences-for-quotations-and-orders"></a>Tarjousten ja tilausten numerosarjat

Supply Chain Managementin ja Salesin numerosarjoja ei yhdistetä, jos tarjoukset ja tilaukset luodaan ja synkronoidaan Salesissa ja Supply Chain Managementissa. Jos Salesissa luotu myyntitilaus synkronoidaan Supply Chain Managementiin, sillä on sama myyntitilausnumero Supply Chain Managementissa. Jotta myyntitilauksen numeroa ei kopioida, molemmissa sovelluksissa on käytettävä eri numerosarjajärjestelmiä.

Ajatellaan, että Supply Chain Managementin numerosarja on **1, 2, 3, 4, 5, ...** ja Salesin numerosarja on **100, 99, 98, ...**. Jos luot Salesissa 100 myyntitilausta, lopulta luodaan tilausnumero, joka on jo olemassa Supply Chain Managementissa. Toisin sanoen kaksi numerosarjaa ovat lopulta päällekkäisiä, koska myyntitilaukset luodaan Supply Chain Managementissa ja Salesissa. Sen sijaan voit käyttää esimerkiksi Supply Chain Managementissa numerosarjaa **F1, F2, F3, ...** ja Salesissa numerosarjaa **C1, C2, C3, ...**. Nämä numerosarjat eivät koskaan tuota myyntitilausnumeroiden kaksoiskappaleita.

## <a name="sales-quotations"></a>Myyntitarjoukset

Myyntitarjoukset luodaan Salesissa tai Supply Chain Managementissa. Jos luot tarjouksen Salesissa, se synkronoidaan Supply Chain Managementiin reaaliajassa. Samoin, jos luot tarjouksen Supply Chain Managementissa, se synkronoidaan Salesiin reaaliajassa. Huomaa seuraavat seikat:

+ Voit lisätä tarjouksen tuotteeseen alennuksen. Tässä tapauksessa alennus synkronoidaan Supply Chain Managementiin. Otsikon **Alennus**-, **Veloitukset**- ja **Vero**-sarakkeiden hallinta perustuu Supply Chain Managementin määrityksiin. Tämä määritys ei tue integrointimääritystä. Sen sijaan **Hinta**-, **Alennus**-, **Veloitus**- ja **Vero**-sarakkeita ylläpidetään ja käsitellään Supply Chain Managementissa.
+ Myyntitarjouksen otsikon vain luku -sarakkeita ovat **Alennusprosentti**, **Alennus** ja **Rahdin summa**.
+ **Kuljetusehdot**-, **Toimitusehdot**-, **Toimitustapa**- ja **Toimitustila**-sarakkeet eivät sisälly oletusarvoisiin yhdistämismäärityksiin. Näiden sarakkeiden määrittämistä varten on määritettävä arvon yhdistämismääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä taulu synkronoidaan.

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
    - Kun myyntitilausrivi synkronoidaan Salesista Supply Chain Managementiin, käytetään koko rivin alennussummaa. Koska Supply Chain Managementissa ei ole saraketta, johon rivin koko alennussumman voisi tallentaa, summa jaetaan määrällä ja tallennetaan **Rivialennus**-sarakkeeseen. Kaikki tässä divisioonassa tapahtuva pyöristys tallennetaan myyntirivin **Myyntikulut**-sarakkeeseen.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Esimerkki: Synkronointi Salesista Supply Chain Managementiin

Myyntitilaus on seuraava:

+ **Sales:** Määrä = 3, rivikohtainen alennus = 10,00 $
+ **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = –$0,01

Jos synkronoit Supply Chain Managementista Salesiin, saat seuraavan tuloksen:

+ **Supply Chain Management:** Määrä = 3, rivin alennussumma = $3,33, myynnin kulut = –$0,01
+ **Sales:** Määrä = 3, rivikohtainen alennus = (3 × 3,33 $) + 0,01 $ = 10,00 $

## <a name="dual-write-solution-for-sales"></a>Kaksoiskirjoitusratkaisu Salesia varten

**Tilaus**-tauluun on lisätty uusia sarakkeita, jotka näkyvät sivulla. Useimmat näistä sarakkeista näkyvät Salesin **Integrointi**-välilehdessä. Lisätietoja tilasarakkeiden yhdistämismääriyksistä on kohdassa [Myyntitilausten tilasarakkeiden yhdistämismäärityksen määrittäminen](sales-status-map.md).

+ **Luo lasku**- ja **Peruuta tilaus** -painikkeet piilotetaan Salesin **Myyntitilaus**-sivulla.
+ **Myyntitilauksen tila** -arvo pysyy **aktiivisena**, jotta muutokset Supply Chain Managementista siirtyvät Salesin myyntitilaukseen. Voit ohjata tätä toimintaa määrittämällä **Tilakoodi \[Tila\]** -arvoksi **Aktiivinen**.

## <a name="invoices"></a>Laskut

Myyntilaskut luodaan Supply Chain Managementissa ja synkronoidaan Salesiin. Huomaa seuraavat seikat:

+ **Laskun numero** -sarake on lisätty **Lasku**-tauluun. Se näkyy sivulla.
+ **Myyntitilaus**-sivun **Luo lasku** -painike on piilotettu, koska laskut luodaan Supply Chain Managementissa, josta ne synkronoidaan Salesiin. **Lasku**-sivua ei voi muokata, sillä laskut synkronoidaan Supply Chain Managementista.
+ **Myyntitilauksen tila** -arvo muuttuu automaattisesti **Laskutettu**-tilaksi, kun liittyvä lasku on synkronoitu Supply Chain Managementista Salesiin. Lisäksi laskun omistajaksi määritetään sen myyntitilauksen omistaja, josta lasku on muodostettu. Tämän vuoksi myyntitilauksen omistaja voi tarkastella laskua.
+ **Kuljetusehdot**-, **Toimitusehdot**- ja **Toimitustila**-sarakkeita ei lisätä oletusarvoisiin yhdistämismäärityksiin. Näiden sarakkeiden määrittämistä varten on määritettävä arvon yhdistämismääritys, joka koskee vain niiden organisaatioiden tietoja, joiden välillä taulu synkronoidaan.

## <a name="templates"></a>Mallit

Prospektista käteiseksi -toiminto sisältää perustaulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
[Kaikki tuotteet](mapping-reference.md#138) | msdyn_globalproducts | |
[Asiakkaat V3](mapping-reference.md#101) | tilit | |
[Asiakkaat V3](mapping-reference.md#116) | yhteyshenkilöt | |
[Yhteyshenkilöt V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS-myyntitilauksien otsikot](mapping-reference.md#217) | salesorders | |
[CDS-myyntitilausrivit](mapping-reference.md#216) | salesorderdetails | |
[CDS-myyntitarjouksen otsikko](mapping-reference.md#215) | tarjoukset | |
[CDS-myyntitarjousrivit](mapping-reference.md#214) | quotedetails | |
[Vapautetut tuotteet V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Myyntilaskun otsikot V2](mapping-reference.md#118) | laskut | Finance and Operations -sovelluksen Myyntilaskun otsikot V2 -taulu sisältää myyntitilausten laskut ja vapaatekstilaskut. Dataversessa käytetään kaksoiskirjoituksen suodatinta, joka suodattaa pois vapaatekstilaskuasiakirjat. |
[Myyntilaskun rivit V2](mapping-reference.md#117) | invoicedetails | |
[Myyntitilausten alkuperän koodit](mapping-reference.md#186) | msdyn_salesorderorigins | |

Lisätietoja hinnastoista on kohdassa [Yhtenäinen tuotekokemus](product-mapping.md).

## <a name="limitations"></a>Rajoitukset

- Palautustilauksia ei tueta.
- Hyvityslaskuja ei tueta.
- Taloushallinnon dimensiot on määritettävä päätiedoille, kuten asiakkaalle ja toimittajalle. Kun asiakas lisätään tarjoukseen tai myyntitilaukseen, asiakastietueeseen liitetyt taloushallinnon dimensiot siirtyvät automaattisesti tilaukseen. Kaksoiskirjoitus ei sisällä tällä hetkellä päätietojen taloushallinnon dimensioiden tietoja.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
