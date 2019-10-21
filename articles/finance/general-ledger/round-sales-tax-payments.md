---
title: Arvonlisäveromaksut ja pyöristyssäännöt
description: Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186322"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Arvonlisäveromaksut ja pyöristyssäännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.

Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti. Tämä voidaan tehdä suorittamalla arvonlisäveron tilitys- ja kirjausprosessi Arvonlisävero-sivulla. Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille. Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä Arvonlisävero-sivulla pyöristyssääntö. 

Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.

Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.

## <a name="examples"></a>Esimerkkejä

Kauden arvonlisävero näyttää hyvityssaldoksi -98 765,43. Yritys on perinyt arvonlisäveroja enemmän kuin maksanut. Yrityksellä on siten arvonlisäverovelkaa. 

Yritys haluaa käyttää pyöristysmenetelmää, joka pyöristää saldon lähimpään 1,00 euroon. Alv-kirjanpidosta vastaava käyttäjä tekee seuraavat toimet:

1.  Valitse Vero &gt; Välilliset verot &gt; Arvonlisävero &gt; Alv-viranomaiset.
2.  Valitse Yleinen-pikavälilehdessä Pyöristystapa-kentästä Normaali.
3.  Syötä Pyöristys-kenttään arvoksi 1,00.
4.  Kun arvonlisävero täytyy maksaa, avaa Tilitä ja kirjaa arvonlisävero -sivu. (Valitse Vero &gt; Ilmoitukset &gt; Arvonlisävero &gt; Tilitä ja kirjaa arvonlisävero.)
5.  Arvonlisäveron maksutilillä oleva alv-velka (98 765,43) pyöristetään arvoon 98 765.

Seuraavassa taulukossa on esitetty, miten summa 98 765,43 summa pyöristetään käyttämällä kutakin Alv-viranomaiset-sivulla Pyöristystapa-kentästä valittavissa olevaa pyöristysmenetelmää.

| Pyöristystapavaihtoehto                | Pyöristysarvo = 0,01 | Pyöristysarvo = 0,10 | Pyöristysarvo = 1,00 | Pyöristysarvo = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Normaali                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Alaspäin                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Pyöristys                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Oma etu, maksettavien saldo | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Oma etu, saatavien saldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Ei pyöristystä, koska pyöristys on 0,00

round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149

### <a name="normal-round-and-round-precision-is-001"></a>Normaali pyöristys ja pyöristyksen tarkkuus on 0,01

<table>
  <tr>
    <td>Pyöristys
    </td>
    <td>Laskentaprosessi
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi. 

Lisätietoja on seuraavissa aiheissa:
- [Arvonlisäveron yleiskatsaus](indirect-taxes-overview.md)
- [Arvonlisäveromaksun luominen](tasks/create-sales-tax-payment.md)
- [Myyntitapahtumien luominen asiakirjoihin](tasks/create-sales-tax-transactions-documents.md)
- [Näytä kirjatut arvonlisäverotapahtumat](tasks/view-posted-sales-tax-transactions.md)
- [pyöristysfunktio](https://msdn.microsoft.com/library/aa850656.aspx)


