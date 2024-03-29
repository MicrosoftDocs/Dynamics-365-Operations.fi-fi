---
title: Arvonlisäveromaksut ja pyöristyssäännöt
description: Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: kfend
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c24a9850543e9d08ee1726186f433c7cfd26608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865680"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>Arvonlisäveromaksut ja pyöristyssäännöt

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.

Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti. Tämä toiminto voidaan suorittaa suorittamalla arvonlisäveron tilitys- ja kirjausprosessi **Arvonlisävero**-sivulla. Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille. Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä **Arvonlisävero**-sivulla pyöristyssääntö. 

Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.

Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.

## <a name="examples"></a>Esimerkkejä

Kauden arvonlisävero näyttää hyvityssaldoksi -98 765,43. Yritys on perinyt arvonlisäveroja enemmän kuin maksanut. Yrityksellä on siten arvonlisäverovelkaa. 

Yritys haluaa käyttää pyöristysmenetelmää, joka pyöristää saldon lähimpään 1,00 euroon. Alv-kirjanpidosta vastaava käyttäjä tekee seuraavat toimet:

1. Valitse **Vero** > **Välilliset verot** > **Arvonlisävero** > **Alv-viranomaiset**.
2. Valitse **Yleinen**-pikavälilehdessä **Pyöristystapa**-kentästä **Normaali**.
3. Syötä **Pyöristys**-kenttään arvoksi 1,00.
4. Kun arvonlisävero täytyy maksaa veroviranomaisille, avaa **Verot** > **Ilmoitukset** > **arvonlisävero** > **Vahvista ja kirjaa arvonlisävero**. Voit nähdä, että arvonlisäveron maksutilillä oleva alv-velka **98 765,43** pyöristetään arvoon **98 765**.

Seuraavassa taulukossa on esitetty, miten summa 98 765,43 summa pyöristetään käyttämällä kutakin **Alv-viranomaiset**-sivulla **Pyöristystapa**-kentästä valittavissa olevaa pyöristysmenetelmää.

> [!NOTE]                                                                                  
> Jos pyöristysarvo on määritetty arvoon 0,00, toimi seuraavasti:
>
> - Pyöristyksessä pyöristyskäyttäytyminen on sama kuin **pyöristyksessä = 0,01**.
> - **Pyöristyslomakkeen vaihtoehdot**, **alaspäin**, **pyöristäminen** ja **oma etu**, käyttäytyvät samoin kuin **pyöristys = 1,00**.

| Pyöristystapavaihtoehto                | Pyöristysarvo = 0,01 | Pyöristysarvo = 0,10 | Pyöristysarvo = 1,00 | Pyöristysarvo = 100,00 | Pyöristysarvo = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Normaali                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Alaspäin                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Pyöristys                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Oma etu, maksettavien saldo | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Oma etu, saatavien saldo  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Normaali pyöristys ja pyöristyksen tarkkuus on 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
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
```

> [!NOTE]                                                                                  
> Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi. 

Lisätietoja on seuraavissa aiheissa:
- [Arvonlisäveron yleiskatsaus](indirect-taxes-overview.md)
- [Arvonlisäveromaksun luominen](tasks/create-sales-tax-payment.md)
- [Luo arvonlisäverotapahtumia asiakirjoihin](tasks/create-sales-tax-transactions-documents.md)
- [Näytä kirjatut arvonlisäverotapahtumat](tasks/view-posted-sales-tax-transactions.md)
- [pyöristysfunktio](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
