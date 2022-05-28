---
title: Pankin tiliotteen tiedoston tuomisen vianmääritys
description: Tässä artikkelissa kerrotaan, miten korjata ongelmia, jotka johtuvat pienistä eroista tiliotetiedostossa.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 422b2df6c4de3a948b0e62bfb70f99b12e04a8f9
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711170"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Pankin tiliotteen tiedoston tuomisen vianmääritys

[!include [banner](../includes/banner.md)]

On tärkeää, että pankin tiliotetiedosto vastaa asetteluja, jotka ovat tuettuja Microsoft Dynamics 365 Financessa. Tiliotteiden tiukkojen standardien vuoksi suurin osa integraatioista toimii oikein. Kuitenkin joskus tiliotetiedostoa ei voi tuoda tai se sisältää virheellisiä tuloksia. Yleensä ongelmat johtuvat pienistä eroista tiliotetiedostossa. Tässä artikkelissa selitetään, miten nämä erot ja niistä johtuvat ongelmat korjataan.

## <a name="what-is-the-error"></a>Mikä virhe on kyseessä?

Kun tiliotetiedoston tuontia on yritetty, siirry Tietojen hallinnan työhistoriaan ja sen suoritustietoihin löytääksesi virheen. Virhe voi auttaa osoittamalla tiliotteeseen, saldoon tai tiliotteen riviin. Se ei kuitenkaan todennäköisesti anna riittävästi tietoa, jotta ongelman aiheuttavan kentän tai elementin voisi tunnistaa.

> [!NOTE]
> Tuodut tiliotteet voivat olla päällekkäisiä vain yhdelle aikapisteelle.  Jos esimerkiksi tiliote päättyy 1.1.2021 klo 00.00, seuraavan tiliotteen alkamispäivä voi olla 1.1.2021 klo 00:00.

## <a name="what-are-the-differences"></a>Mitä ovat erot?
Vertaa pankkitiedoston asettelumääritystä Financen tuontimääritykseen ja kiinnitä huomiota kenttien ja elementtien eroihin. Vertaa tiliotetiedostoa liittyvään Finance-näytetiedostoon. ISO20022-tiedostoissa on erot helppo nähdä.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Tuotujen tililaskelmien aikavyöhyke-erot
Tuontitiedoston päivämäärän ja ajan arvot voivat poiketa Finance and Operationsin päivämäärä- ja aika-arvoista. Voit estää tämän ristiriidan määrittämällä aikavyöhykeasetukset **Määritä tietolähteet** -sivulla. Lisätietoja aikavyöhyke asetusten määrittämisestä on kohdassa [Pankin täsmäytyksen lisätuontiprosessin määrittäminen](set-up-advanced-bank-reconciliation-import-process.md).

## <a name="transformations"></a>Muunnokset
Yleensä muutokset on tehtävä johonkin kolmesta muunnoksesta. Jokaisen muunnos on kirjoitettu tiettyyn standardiin.

| Resurssin nimi                                         | Tiedostonimi                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Muunnosten virheenkorjaus
### <a name="adjust-the-bai2-and-mt940-files"></a>Oikaise BAI2- ja MT940-tiedostot

BAI2- ja MT940-tiedostot ovat tekstiin perustuvia tiedostoja ja ne on oikaistava, jotta Extensible Stylesheet Language Transformation -kielen (XSLT) virheenkorjauksen voi ottaa käyttöön. Ohjelma tekee oikaisun, kun tiedosto tuodaan.

1.  Luo XML-tiedosto ja kopioi siihen seuraava tekstinkatkelma.

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopioi tiliotetiedoston sisältö ja liitä se XML-tiedostoon niin, että ne korvaavat **PASTESTATEMENTFILEHERE**-kohdan.

### <a name="debug-the-xslt"></a>XSLT-virheenkorjaus

Lisätietoja on kohdassa <https://msdn.microsoft.com/library/ms255605.aspx>.

1.  Käynnistä Microsoft Visual Studio.
2.  Luo konsolisovellus.
3.  Avaa haluamasi XSLT-muoto.
4.  Valitse XSLT-muotoa ja sen ominaisuussivua.
5.  Aseta syötteeksi tiliotetiedoston sijainti.
6.  Määritä tulosteelle sijainti ja tiedostonimi.
7.  Määritä tarvittavat katkaisukohdat.
8.  Valitse valikosta **XML** &gt; **Aloita XSLT-virheenkorjaus**.

### <a name="format-the-xslt-output"></a>Muotoile XSLT-tuloste

Kun muunnos ajetaan, se luo tiedoston, jonka voi avata Visual Studiossa. Voit muotoilla tiedoston nopeasti Ctrl+A, Ctrl+K ja Ctrl+D -näppäinkomennoilla.

### <a name="adjust-the-transformation"></a>Muunnoksen oikaiseminen

Oikaise muunnos saadaksesi haluamasi kentän tai elementin tiliotetiedostoon. Määritä sitten kyseinen kenttä tai elementti asiaankuuluvaan Finance-elementtiin.

### <a name="debitcredit-indicator"></a>Debet/kredit-ilmaisin

Toisinaan on mahdollista, että veloitukset on tuotu hyvityksinä ja hyvitykset veloituksina. Tämän ongelman ratkaisemiseksi on muutettava asiaankuuluvaa XSLT:tä. Jos tiliotteet ovat peräisin useasta pankista, varmista, että kaikissa käytetään samaa debet-/kredit-lähestymistapaa tai luo niille erilliset muunnokseet.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator -malli
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit -malli
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator -malli

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Esimerkkejä tiliotteiden muodoista ja teknisistä asetteluista
Seuraavassa taulukossa on esimerkkejä tuonnin lisäasetuksista pankkitilin täsmäytystietojen tuontitiedoston teknisistä asettelumäärityksistä sekä kolme esimerkkitiliotetiedostoa: Voit ladata esimerkkitiedostot ja tekniset asettelut täällä: [Tuontitiedoston esimerkit](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tekninen asettelumääritys                             | Esimerkkitiliotetiedosto          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
