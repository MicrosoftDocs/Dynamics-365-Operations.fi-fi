---
title: Myyntitarjousten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232203"
---
# <a name="troubleshoot-sales-quotations"></a>Myyntitarjousten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>En saa muutettua palvelunimikkeen myyntitarjouksen myyntimäärää.

### <a name="issue-description"></a>Ongelman kuvaus

Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat viestin "Päivittäminen ei ole sallittua Määrä-kentän osalta".

### <a name="issue-resolution"></a>Ongelman ratkaisu

Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä. Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä nimikettä ei ole. On vain palvelu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]