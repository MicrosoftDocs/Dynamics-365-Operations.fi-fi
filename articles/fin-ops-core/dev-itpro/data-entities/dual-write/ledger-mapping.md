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
ms.openlocfilehash: e41d600464d707d01a0e319dd3cd343b04aa26b7
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782377"
---
# <a name="integrated-ledger"></a>Integroitu kirjanpito

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Yrityssovelluksen kirjanpitotiedot määrittävät perusasetukset sille, miten yritys harjoittaa liiketoimintaa. Kirjanpitotiedot esimerkiksi kuvaavat, mitä tilikautta noudattaa sekä mitä valuuttoja ja tilejä se käyttää. Tässä ohjeaiheessa käsitellään näiden perustaloustietojen integrointia.

## <a name="templates"></a>Mallit

Kirjanpitotiedot sisältävät perustaloushallinnon taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
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
