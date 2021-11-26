---
title: Konsernin sisäisen kaupan määrittäminen
description: Tässä aiheessa käsitellään konsernin sisäisen kaupan määrittämistä
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7288cc8f336b6b1f5174fe2bef38017e0c96e560
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/09/2021
ms.locfileid: "7777713"
---
# <a name="set-up-intercompany-trade"></a>Konsernin sisäisen kaupan määrittäminen

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementin käyttäminen konsernin sisäisessä kaupassa edellyttää, että asiakkaat ja toimittajat on määritettävä suorittamaan konsernin sisäinen kauppa. Lisäksi on määritettävä ostoreskontra, myyntireskontra, hankinta sekä myynti ja markkinointi.

## <a name="before-you-set-up-intercompany-trade"></a>Ennen konsernin sisäisen kaupan määrittämistä

Ennen konsernin sisäisen kaupan määrittämistä on päätettävä, mitkä asiakkaat ovat konsernin sisäisiä asiakkaita ja mitkä toimittajat ovat konsernin sisäisiä toimittajia. Kunkin Microsoft Dynamics 365 Supply Chain Management-yrityksen osalta on päätettävä, mitä kaupankäyntikäytäntöä käytetään konsernin sisäisessä kauppasuhteessa tietyn konsernin sisäisen asiakkaan tai toimittajan kanssa.

Organisaation ja käyttäjien kannattaa tutustua etenkin konsernin sisäisiin parametreihin.

- Määritysten vaikutuksista kannattaa keskustella niiden esimiesten kanssa, jotka vastaavat kussakin yrityksessä konsernin sisäisestä kaupasta.
- Kullekin yritykselle on määritettävä soveltuvat arvot.

## <a name="set-up-trading-relations"></a>Kauppasuhteiden määrittäminen

Asiakkaiden ja toimittajien konsernin sisäinen kauppa määritetään seuraavasti:

1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
1. Valitse asiakastili.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Määritä asiakastilin konsernin sisäiset asetusparametrit. Nämä parametrit sisältävät yrityksen, joka sisältää vastaavan toimittajan ja toimittajatilin. Parametrit sisältävät myös ostotilauskäytännöt, myyntitilauskäytännöt, arvon yhdistämismäärityksen sekä myynti- ja ostosopimusten käytännöt. Lisäksi voidaan määrittää, käytetäänkö perustietoarvoja asiakastililtä tai toisen yrityksen toimittajatililtä.
1. Toista vaiheet 1–4 yrityksen jäljellä olevien konsernin sisäisten asiakkaiden osalta.
1. Siirry kohtaan **Ostoreskontra \> Toimittajat \> Kaikki toimittajat**.
1. Valitse toimittajatili.
1. Valitse toimintoruudun **Yleiset**-välilehdessä **Konsernin sisäinen**.
1. Määritä toimittajatilin konsernin sisäiset asetusparametrit. Nämä parametrit sisältävät yrityksen, joka sisältää vastaavan asiakkaan ja asiakastilin. Parametrit sisältävät myös myyntitilauskäytännöt, ostotilauskäytännöt, arvon yhdistämismäärityksen sekä osto- ja myyntisopimusten käytännöt. Lisäksi voidaan määrittää, käytetäänkö perustietoarvoja toimittajatililtä tai toisen yrityksen asiakastililtä.
1. Toista vaiheet 6–9 yrityksen jäljellä olevien konsernin sisäisten toimittajien osalta.

## <a name="set-up-products"></a>Tuotteiden määrittäminen

Asiakkaiden ja toimittajien konsernin sisäinen kauppa määritetään seuraavasti:

1. Mene kohtaan **Tuotetietojen hallinta \> Tuotteet \> Kaikki tuotteet ja päätuotteet**.
1. Määritä niiden yrityksiin vapautettavat tuotteet, joissa halutaan käydä konsernin sisäistä kauppaa.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
