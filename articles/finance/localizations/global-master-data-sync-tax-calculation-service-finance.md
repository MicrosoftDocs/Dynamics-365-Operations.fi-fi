---
title: Dynamics 365 Financen veronlaskentapalvelun arvonlisäveroasetusten synkronointi
description: Tässä artikkelissa kerrotaan, miten veroasetusten perustiedot synkronoidaan Verolaskentapalvelusta Microsoft Dynamics 365 Financeen.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283850"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Dynamics 365 Financen veronlaskentapalvelun arvonlisäveroasetusten synkronointi

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten veroasetusten perustiedot synkronoidaan Verolaskentapalvelusta Microsoft Dynamics 365 Financeen.

Kun olet suorittanut tarvittavat määritysvaiheet kohdassa [Aloita verolaskenta](global-get-started-with-tax-calculation-service.md), seuraavat veroasetusten asetukset synkronoidaan automaattisesti Verolaskentapalvelusta Financeen.

## <a name="sales-tax-code"></a>Arvonlisäverokoodi

| Verolaskentapalvelu           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Alv-koodi                          | Arvonlisäverokoodi                      |
| Kuvaus                       | Nimi                                |
| Käyttäjän syöte                        | Tilityskausi                   |
| Käyttäjän syöte                        | Kirjanpidon kirjausryhmä                |
| Käyttäjän syöte                        | Arvonlisäveron valuutta                  |
| Negatiivinen verokanta on määritetty | Salli negatiivinen alv-prosentti |

## <a name="tax-value"></a>Veron arvo

| Verolaskentapalvelu | Finance                   |
| ----------------------- | ------------------------- |
| Tapahtumapäivästä   | Päivämäärästä                 |
| Tapahtumapäivään     | Päivämäärään                   |
| Pienin summa          | Vähimmäisraja             |
| Enimmäissumma          | Enimmäisraja             |
| Veroprosentti                | Arvo                     |
| Vähennyskelvoton korko     | Vähennyskelvoton prosenttiosuus |

## <a name="tax-limits"></a>Verorajat

| Verolaskentapalvelu | Finance           |
| ----------------------- | ----------------- |
| Tapahtumapäivästä   | Päivämäärästä         |
| Tapahtumapäivään     | Päivämäärään           |
| Vähimmäisverosumma      | Pienin mahdollinen arvonlisävero |
| Enimmäisverosumma      | Suurin mahdollinen arvonlisävero |

## <a name="sales-tax-group"></a>Arvonlisäveroryhmä

| Verolaskentapalvelu                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Veroryhmä                                       | Arvonlisäveroryhmä                            |
| Tämän veroryhmän verokoodit                  | Arvonlisäveroryhmän arvonlisäverokoodit |
| Verokoodi on merkitty **on vapautettu**         | Veroton                                     |
| Verokoodi on merkitty **on vapautettu**         | Vapautuskoodi                                |
| Verokoodiksi on merkitty **On käänteinen veloitus** | Käänteinen veloitus                             |
| Verokoodi on merkitty **on käyttövero**        | Käyttövero                                    |

## <a name="item-sales-tax-group"></a>Nimikkeen arvonlisäveroryhmä

| Verolaskentapalvelu             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Nimikkeen veroryhmä                      | Nimikkeen arvonlisäveroryhmä                            |
| Tämän nimikeveroryhmän verokoodit | Nimikkeen arvonlisäveroryhmän arvonlisäverokoodit |

Kun synkronointi on valmis, jatka jäljellä olevien parametrien säilyttämistä Financessa kirjausta ja raportointia varten.

> [!NOTE]
> Veroasetusten synkronointia Financesta verolaskentapalveluun ei tueta. Luo ensin veroasetukset verolaskentapalveluun olemassa olevassa Finance-ympäristössä. Synkronoi sitten asetustiedot takaisin Finance-ympäristöön.
