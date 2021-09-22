---
title: Pakettinimikettä ei tueta konsernin sisäisissä prosesseissa
description: Pakettinimikettä ei voi ostaa. Myyntitilaus ostaa vain pakettinimikkeen komponentit eikä itse pakettinimikettä.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 21adc7d071837b762157364f6f8ed370c69c7fd3
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476230"
---
# <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>Pakettinimikettä ei tueta konsernin sisäisissä prosesseissa

## <a name="symptoms"></a>Oireet

Pakettinimike ei ole käytettävissä ostotilauksessa, koska jos tarkastelet pakettinimikkeen myyntitilaus rivejä, määrä on *0* (nolla) ja tila on *Peruutettu*.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. myyntitilauksella ostetaan vain pakettinimikkeen osat. Sillä ei osteta itse pakettinimikettä. Jos sinun on ostettava paketti, harkitse, pitääkö se merkitä pakettinimikkeeksi, koska tämä toiminto on suunniteltu tuottokirjausskenaarioita varten. Lisätietoja pakettinimikkeistä: [Paketit](/dynamics365/finance/accounts-receivable/revenue-recognition-setup).
