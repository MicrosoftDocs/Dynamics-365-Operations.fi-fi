---
title: "Arvonlisäveromaksut ja pyöristyssäännöt"
description: "Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8de01b77fcbeb65321e60614b6a11d264460208f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>Arvonlisäveromaksut ja pyöristyssäännöt

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten ALV-viranomaisten pyöristyssäännön määrittäminen toimii, ja miten arvonlisäverosaldo pyöristetään arvonlisäverotyön arvonlisäveron selvityksen ja kirjauksen aikana.

Arvonlisäverot täytyy ilmoittaa ja maksaa säännöllisesti. Tämä voidaan tehdä suorittamalla arvonlisäveron tilitys- ja kirjausprosessi Arvonlisävero-sivulla. Kauden arvonlisävero tilitetään arvonlisäverotilejä vastaan, ja alv-saldo kirjataan arvonlisäveron maksutilille. Arvonlisäveron maksutilille kirjattu alv-saldo voidaan pyöristää veroviranomaisten ohjeiden mukaan määrittämällä Arvonlisävero-sivulla pyöristyssääntö. 

Pyöristysero kirjataan arvonlisäveron pyöristystilille, joka valitaan kirjanpidossa Automaattisten tapahtumien tilit -kentästä.

Seuraavassa esimerkissä on kuvattu arvonlisäveron pyöristyssäännön toimintaa.

### <a name="example"></a>Esimerkki:

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
| Oma etu, saatavien saldo  | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |

> [!NOTE]                                                                                  
> Jos valitset Oma etu, pyöristys tehdään aina yrityksen eduksi. 

Lisätietoja on seuraavissa aiheissa:
- [Arvonlisäveron yleiskatsaus](indirect-taxes-overview.md)
- [Arvonlisäveromaksun luominen](tasks/create-sales-tax-payment.md)
- [Myyntitapahtumien luominen asiakirjoihin](tasks/create-sales-tax-transactions-documents.md)
- [Näytä kirjatut arvonlisäverotapahtumat](tasks/view-posted-sales-tax-transactions.md)



