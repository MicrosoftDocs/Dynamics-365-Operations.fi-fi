---
title: Integroitu kirjanpito
description: Tässä ohjeaiheessa käsitellään kirjanpitotietojen integraatiota Finance and Operationsin ja muiden Dynamics 365 -sovellusten välillä Dataversen avulla.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 0deb4198acb59b90bf06e4050889d028df2223e3
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063644"
---
# <a name="integrated-ledger"></a>Integroitu kirjanpito

[!include [banner](../../includes/banner.md)]



Yrityssovelluksen kirjanpitotiedot määrittävät perusasetukset sille, miten yritys harjoittaa liiketoimintaa. Kirjanpitotiedot esimerkiksi kuvaavat, mitä tilikautta noudattaa sekä mitä valuuttoja ja tilejä se käyttää. Tässä ohjeaiheessa käsitellään näiden perustaloustietojen integrointia.

## <a name="templates"></a>Mallit

Kirjanpitotiedot sisältävät perustaloushallinnon taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Taloushallinnon ja toimintojen sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
---------------------------------|----------------------------------|------------
[CDS-vaihtokurssit](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Tilikartta](mapping-reference.md#121) | msdyn_chartofaccountses |
[Valuutat](mapping-reference.md#218) | transactioncurrencies |
[Vaihtokurssivaluuttapari](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Vaihtokurssin tyyppi](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Taloushallinnon dimensiomuoto](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Taloushallinnon dimensiot](mapping-reference.md#128) | msdyn_dimensionattributes |
[Kirjanpidon vuosikalenterin integraation yksikkö](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Kirjanpidon vuosikalenterin kausi](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Kirjanpidon kalenterivuoden integraation yksikkö](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Päätili](mapping-reference.md#152) | msdyn_mainaccounts |
[Päätililuokat](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
